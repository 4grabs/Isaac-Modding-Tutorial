# An Introduction to Loops

Let's say you want to print out `"Hello World!" three times. Your first instinct might be to write this:

```lua
print("Hello World!")
print("Hello World!")
print("Hello World!")
```

But what if you need to print it out ten times? Or a hundred? Or even as much as possible? CVopying/pasting the line won't be the right solution as not only does that tremendously bloat your codebase and make it much harder to read, but if you need to change what is printed, you will have a very hard time going through all of these lines and updating them.

This is where loops come in!

A **loop** is a series of lines executed for a certain amount of time. Lua offers four different loop types, each with their use cases. In this chapter, however, we will only go over three of these loops since the fourth one revolves around a topic that has not been covered yet.

# The While Loop

A **while loop** is a loop that will continuously execute its' set of lines until a certain condition is evaluated to `true`. Here's an example:

```lua
local myNumber = 50

while myNumber > 25 do
  print("It's greater than 25")
  myNumber = myNumber - 1
end
```

If you run this piece of code, it will print out `"It's greater than 25"` 25 times. The structuring is somewhat similar to how conditional statements look. Here's a look at each part of the while loop:

* `while` - The start of the loop.
* `myNumber > 25` - The condition being evaluated. If it evaluates to `true`, the code inside of the loop runs. Otherwise, the loop stops.
* `do` - The end of the condition check. The block of code after it will now only run if the condition evaluates to true.
* `end` - The the end of the loop

>⚠️ Make sure while loops can stop running at some point! If it can not stop running, it will become what is known as an **infinite loop** and will crash the game. For example:
>
>```lua
>local myNumber = 50
>
>while myNumber > 25 do
>  print("It's greater than 25")
>end
>```
>
> Since the `myNumber = myNumber - 1` line was removed, it's no longer possible for `myNumber` to become less than or equal to `25`, making it an infinite loop. An infinite loop can happen with all four loop types although they are most common with while loops.

>ℹ️ If you've coded before, you may be thinking that you could add something to yield (or "pause") the loop, allowing infinite loops to not crash. However, the Isaac modding API does not offer this.

# The Repeat Loop

A **repeat loop** works similarly to the while loop. It executes a set of lines before evaluating its condition. Here's an example:

```lua
local myNumber = 5

repeat
  print("The loop is running")
  myNumber = myNumber - 1
until myNumber <= 0
```

This prints out `"The loop is running"` 6 times. Here's a look at each part of the loop:

* `repeat` - The start of the loop. The block of code after this will run.
* `until` - The end of the loop and the start of the condition check.
* `myNumber <= 0` - The loop's condition. If it evaluates to `true`, the block of code ran again. Otherwise, the loop stops running.

# The For Loop

A **for loop** is a loop that runs a certain amount of times. Here's an example:

```lua
for i = 1, 10 do
  print(i)
end
```

Running this will print out the numbers 1 through 10. Compared to other loops, there's quite a lot to it! Here's a look at each part of the loop:

* `for` - The start of the loop.
* `i = 1` - The loop's variable. the variable is being initialized with a value of `1`.
* `, 10` - The loop's goal. Each time the loop runs, `i` is incremented by 1. Once `i` is greater than `10`, the loop stops running.

>ℹ️ In an earlier chapter, you may remember that it was stated to almost always include `local` when initializing a variable. However, the for loop's variable is local as it can only be used within the loop. Including the `local` keyword will cause a syntax error. Variable scopes will be covered in a later chapter.

By default, the loop's variable increments itself by `1` in each iteration of the loop. You can change how much is being incremented by specifying a third number. Here's an example:

```lua
for i = 0, 10, 2 do
  print(i)
end
```

This prints out `0`, `2`, `4`, `6`, `8`, and `10`. The third number specified in the loop's first line, `2`, indicates that each time the loop is run, `i` will increment itself by `2`.

You can also have loops count down backward like this:

```lua
for i = 10, 0, -5 do
  print(i)
end
```

This prints out `10`, `5`, and `0`.

>✨ In for loops, it is common for programmers to name their variable `i`. However, if the code inside your loop ends up being large, it's a good idea to give it a descriptive name.

# Break

There might be cases where you want a loop to stop running early if a certain condition is met. This is where the break statement comes in.

**break** is a special statement that stops the loop from running. Here's a look at it in action:

```lua
for i = 100, 0, -5 do
   if i <= 50 then
      break
   end
   
   print(i)
end
```
 
When running this, you'll notice that the code stops printing at `55`. This is because at the start of each iteration of the loop, the conditional checks to see if `i` is less than or equal to 50. If the conditional evaluates to true, the `break` statement stops the loop from executing.

# Nested Loops

Just like conditional statements, you can nest loops. Here's an example of a for loop being nested:

```lua
for i = 1, 10 do
  for j = 1, 10 do
    print(j)
  end
end
```

This prints out the numbers 1 - 10 a total of 10 times. This is because in each iteration of the outer loop, a new loop is ran ten times.

>✨ Try not to nest too many loops as it will make your code hard to read. If you need to nest your loops, it's a good idea to give their variables descriptive names. You can also simplify them by using functions, which will be covered in the next chapter.

# Quiz

Try to figure out the answers to these questions without running the code.

#1. How many times will this loop run?

```lua
local myNumber = 10

while myNumber >= 5 do
    myNumber = myNumber - 1
end
```

<details>
  <summary>Solution</summary>
  6 times.
</details>

#2. How many times will this loop run?

```lua
local myNumber = 15

while myNumber < 5 do
    print("It's running")
end
```

<details>
  <summary>Solution</summary>
  0 times. Since `myNumber` is initialized with a value greater than 5, the loop's condition evaluates to `false` and won't run at all.
</details>

#3. What is wrong with this loop?

```lua
local myNumber = 100 

while myNumber > 50 do
    myNumber = myNumber + 1
end
```

<details>
  <summary>Solution</summary>
  It's an infinite loop since `myNumber` can never be less than or equal to than `50`, causing the program to crash.
</details>

#4. What does this loop print out?

```lua
for i = 0, 20, 5 do
    print(i)
end
```

<details>
  <summary>Solution</summary>
  0, 5, 10, 15, 20
</details>

#5. What does this loop print out?

```lua
for i = 0, 10, 2 do
    print(i)

    if i == 6 then
        break
    end
end
```

<details>
  <summary>Solution</summary>
  0, 2, 4, 6
</details>

#6. What does this loop print out?

```lua
for i = 3, 10, 3 do
    print(i)
end
```

<details>
  <summary>Solution</summary>
  3, 6, 9
</details>

#7. Write a loop that prints out the numbers `0` through `100` with the loop's variable incrementing by 10.

<details>
  <summary>Solution</summary>
  
  ```lua
for i = 0, 100, 10 do
    print(i)
end
  ```
  
</details>
