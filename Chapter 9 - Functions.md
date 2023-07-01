# Introduction to Functions

If you haven't already, make sure your `main.lua` file is empty.

Let’s say you want to write something that prints out a series of numbers from 10 to 1. Ideally, you would write something like this.

```lua
for i = 10, 0, -1 do
	print(i)
end
```

If you run this code, it will print the numbers 10 to 0. Everything works!

Let’s say that you want to reuse the exact code for somewhere else though. Your first instinct may be to copy and paste the code. You'll end up with something like this:

```lua
for i = 10, 0, -1 do
	print(i)
end

for i = 10, 0, -1 do
	print(i)
end
```

However, copy/pasting your code introduces a new problem. What if we want to change the loop and have it print out the numbers 15 to 0 instead? You would have to tweak both loops. This is especially problematic when you copy/paste the same loop more than twice, which can make maintaining your code more difficult. Even worse, maintaining becomes a lot more difficult once the code becomes more complex rather than a simple for loop.

Fortunately, Lua offers a way to effectively reuse code. They come in the form of functions!

A **function** is a block of code that you can reuse at any time. 

>ℹ️ If you’ve taken pre-algebra or anything further in math, you might have learned about functions in math. In coding, the concept of functions is the exact same!

Here’s an example of a function being defined.

```lua
local function printCountdown()
end
```

There’s a whole lot to take in! There are five parts that you should take note of.

`local`, just like with variables, signifies that the scope of the function is local. Variable and function scopes will be covered in the next chapter.
`function` signifies that you are declaring a function.
`printCountdown` is the name of the function, akin to variable names. Just like variable names, you will need to follow the [variable naming rules](https://github.com/4grabs/Isaac-Modding-Tutorial/blob/main/Chapter%205%20-%20Variables.md)
`()` is what holds the function parameters. Function parameters will be covered in a later section.
`end` indicates the end of the function, just like loops and if statements. Everything between the parentheses and end is what is known as the function body.

Essentially, the code creates a variable named `printCountdown()` but the data type of the variable is a function.

Using the loop from earlier, we can change it to a function, like this.

```lua
local function printSequence()
  for i = 10, 0, -1 do
    print(i)
  end
end
```

Once you add that, delete everything from your code except for the function and run it!

You will quickly notice that nothing is being printed out once it's ran. That is because you are not calling the function.
 
In order to call the function, simply type in the function name followed by a pair of parentheses. Your code should look like this now.

```lua
local function printSequence()
  for i = 10, 0, -1 do
    print(i)
  end
end

printSequence()
```

If you run the code now, the numbers 10 through 0 will now be printed to the console!

You can call a function as many times as you want. They’re extremely important as it allows you to reuse code rather than copy/pasting it.

✨ As stated earlier, functions are essentially variables but with a special data type. You can even create a function with a similar syntax to how you would normally declare a variable like this:
>
>```lua
>local myFunction = function()
>end
>
>myFunction()
>```
>
>However, most people do not write their functions that way, therefore you should stick with the other method of writing them.


>⚠️ Be sure to not call the function before declaring it. Not doing so will cause an error. For example:
>
>```lua
>printSequence()
>
>local function printSequence()
>  for i = 10, 0, -1 do
>    print(i)
>  end
>end
>```
>
> As a result, you will get an error which says "attempt to call a nil value (global 'printSequence'). That is because on line 1, `printSequence` is nil since a function hasn't been defined yet, and you are trying to call it as if it's a function, which is not valid.

# Function Arguments & Parameters

Let’s say you want to write a function that takes a specific value that you pass, such as passing two numbers and having them add the numbers together. Fortunately, this is where function arguments and parameters come in.

Function **arguments** are values that you pass to the function. Function **parameters** are variables that holds the value you passed.

Here’s an example of it in action!

```lua
local function addTwoNumbers(x, y)
	print(x + y)
end

addTwoNumbers(10, 15)
```

Running this code will print out the number 25. You may be confused as to what is going on, so let’s take a look at one thing at a time.

```lua
addTwoNumbers(10, 15)
```

These are the arguments that are being passed to the function. We are passing 10 as the first argument and 15 as the second argument.

```lua
local function addTwoNumbers(x, y)
```

`x` and `y` are the parameters of the function. Just like arguments, they must be separated with commas! As stated earlier, they are just variables which hold the value of the arguments that were passed. Since `x` is the first parameter, its value when the function was called in the example above was 10 since the first argument passed was 10. The same goes for `y`, its value was 15 as the value of the argument was 15.

If you have been paying attention, you might’ve noticed that you were already introduced to the concept of parameters and functions to some extent! Throughout the guidebook, we’ve been using the `print` function and we were able to pass anything inside of it, ranging from strings all the way to booleans.

# The Return Statement

Let’s say you have a function which adds two numbers and you want to get the result of the function and store it as a variable.

This is very much possible with Lua thanks to the `return` statement.

`return` causes the function to stop running and have it return a value instead. Here’s an example in action.

```lua
local function addTwoNumbers(x, y)
	return x + y
end


local sum = addTwoNumbers(3, 5)
print(sum)
```

Running this code will print 8. This is because we’re assigning whatever is being returned from the addTwoNumbers function to the `sum` variable, which in this case is 8.

You can return any data type from a function too! Here’s a more detailed example.

```lua
local priceOfApples = 10

local function canAffordApple(money)
	if money >= priceOfApples then
		return true
	else
		return false
	end
end

local canAfford = canAffordApple(3)
print(canAfford)
```

This code checks to see if the `money` argument is greater than or equal to the value of the `priceOfApples` variable, which is 10, and a boolean is returned. 

In the example, since `3` is being passed as the argument, the function will return `false` and the result is printed. If you were to change the argument to anything greater than or equal to the value of `priceOfApples`, the function will instead return true.
		
# Quiz

Do not run the code that you see in the quiz. 

#1. What does this print out?

```lua
local function printAPhrase()
  print("A phrase")
end

printAPhrase()
```

<details>
  <summary>Solution</summary>
  "A phrase"
</details>

#1. What does this print out?

```lua
local function printANumber()
  print(5)
end
```

<details>
  <summary>Solution</summary>
  Nothing, as the function is not being called.
</details>

#3. What does this piece of code print out?

```lua
local function multiplyTwoNumbers(num1, num2)
  print(num1 * num2)
end

multiplyTwoNumbers(5, 10)
```

<details>
  <summary>Solution</summary>
  50
</details>

#4. What does this piece of code print out?

```lua
local function subtractTwoNumbers(a, b)
  return b - a
end

local difference = subtractTwoNumbers(30, 10)

print(difference)
```

<details>
  <summary>Solution</summary>
  20
</details>

#5. Does this error? If so, why?

```lua
local function subtractTwoNumbers(a, b)
  return b - a
end

local difference = subtractTwoNumbers(30)

print(difference)
```

<details>
  <summary>Solution</summary>
  Yes. Since a second argument is being passed, the value of `b` inside of the function is `nil`, which errors since you can't perform arithmitic operations on values that aren't numbers.
</details>

#6. Write a function named `printSequence` which prints out a series of numbers. It should take three arguments. The first argument is the starting number. The second argument is the final number of the sequence. The third number is the sequence incrementation.

<details>
  <summary>Hint</summary>
  The function is just a for loop.
</details>

<details>
  <summary>Solution</summary>
  
  ```lua
  local function printSequence(startingNumber, finalNumber, incrementation)
    for i = startingNumber, finalNumber, incrementation do
      print(i)
    end
  end
  ```

</details>


