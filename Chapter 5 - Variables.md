# Introduction

This chapter goes over the basics of variables.

# Variables

**Variables** are named objects which store data. The data stored can be all types of data and can be accessed in your code. 

If you took pre-algebra, you may already be familiar with the concept of variables (i.e: `f(x) = x + 5`). In terms of coding, variables serve the same purpose although you can change their value at any time.

# Declaring a variable

In Lua, declaring a variable is very straightforward. In `main.lua`, paste the following code:

```lua
local myVariable = 5
print(myVariable)
```

Afterward, save the file and reload your mod. You will notice that the number `5` is printed out in the console.

Let’s take a step back and analyze the anatomy of this code.

The first line initializes the variable. There are four different parts of this line to note:
- `local` signifies that the variable is **local**. In a later chapter, we will go in-depth on what a local variable does exactly as well as what happens when you remove it. However, you should almost always specify the variable as local.
- `myVariable` is the variable **identifier**, the name of the variable.
- `=` is the **assignment operator**. This tells the program that a value is going to be assigned to the variable. The assignment operator is used when a value is being assigned to something.
- `5` is the **value** that is assigned to the variable.

The second line of code prints out the value of the variable. Since it was initialized with a value of `5`, running the code will print out the number `5`.

You can also change the value of a variable. For example:

```lua
local myVariable  = 90
myVariable = 30
print(myVariable)
```

Running this code will cause the number `30` to be printed out. This is because the first line initializes the variable with a value of `90`, then the second line changes the value of the variable to `30`, and then the third line prints out the current value.

# Data Types

A **data type** (or **type** for short) specifies the type of value that is being stored. Lua offers a small handful of data types you should be wary of. In this chapter, we will be going over three of them:

# Number

A **number** is, as the name implies, a number. In the earlier example with variables you can see the type of value being assigned to the variable is a number.

There are plenty of ways to write a number. You can write one as a decimal:

```lua
local myNumber = 51.2
local anotherNumber = 9.301
local anAwesomeNumber = 0.031
```

And you can also have a number be negative

```lua
local myNegativeNumber = -32
local anotherNegativeNumber = -7.3
local coolNegativeNumber = -0.6
```

# String

A **string** is a set of characters. If you recall in the previous chapter, we ran the following snippet of code:

```lua
print("Hello World!")
```

The `"Hello World!"` is an example of a string.

In Lua, there are three different ways to create a string:

```lua
local myString = "This is a string using double quotation marks!"
local anotherString = 'An amazing string using single quotation marks'
local finalString = [[Another string with double brackets]]
```

The third method of creating a string using the `[[]]` characters has a unique trait where it can span multiple lines. Take the following code for example:

```lua
local aLongString = "a very
long
long
string
"
```

Running this will cause an error because using strings with quotation marks can only be in a single line of code. However, you can have strings take up multiple lines of code using double brackets like this:

```lua
local aLongString = [[
a super
long
long
string
]]
```

>✨ Unless your strings need to span multiple lines of code, it is recommended to use double quotation marks for your strings as that is commonly used.

# nil

**nil** indicates that there is no value. For example,

```lua
local myVariable = nil
print(myVariable)
```

This will print out `nil` since we're initializing a variable with no value.

You can also do

```lua
local myVariable
print(myVariable)
```

Which also initializes myVariable with no value.

# Variable Naming Rules

As you can already tell, you can give a variable a unique name. However, there are some rules you need to follow when naming your variable, otherwise, you will run into errors.

## Rule 1 - Nubmers cant be First Characters

Variable names can not have numbers as its first character.

❌ **Incorrect**

```lua
local 5CoolNumbers = 42069
local 8 = 8
```

✔️ **Correct**

```lua
local aNumberWhichContains5 = 5
local stringWith5Characters = "abcdef"
```

## Rule 2 - No Special Characters

Variable names can not include special characters, such as `%`, `^`, etc.

❌ **Incorrect**

```lua
local my$Savings = 55.3
local two*two = 4
```

Variable names also can not include spaces. However, you can use underscores to emulate spaces.

❌ **Incorrect*

```lua
local a cool string = "wow a cool string"
local two plus two = 4
```

✔️ **Correct**

```lua
local a_cool_string = "wow a cool string"
local two_plus_two = 4
```

## Rule 3 - No Reserved Keywords

Lua has a set of keywords that are reserved for Lua, meaning they can not be used as names. The following keywords are

* `and`
* `end`
* `in`
* `repeat`
* `break`
* `false`
* `local`
* `return`
* `do`
* `for`
* `nil`
* `then`
* `else`
* `function`
* `not`
* `true`
* `elseif`
* `if`
* `or`
* `until`
* `while`

❌ **Incorrect*

```lua
local repeat = 5
local function = 8
```
## Rule 4 - Variables are Case Sensitive

Variable names are case-sensitive. For example:

```lua
local myVariable = 5
print(myvariable)
```

This will print `nil`. That is because the variable initialized is `myVariable`, yet we're printing `myvariable`. Since there was no variable declared with the name of `myvariable`, it prints out nil.

## Rule 5 - Variable Names Matter!

When giving a name to your variable, it should make logical sense. 

Let's say we have a variable that is used to assign health to an enemy. 

```lua
local eh = 900
```

`eh` is not clear and to the reader, it does not indicate it's used to specify how much health an enemy has.

```lua
local enemyHealth = 900
```

The name of this variable is a lot more clear and tells the reader that it's used to assign health to an enemy.

By giving variables good names, you will have an easier time remembering your code as well as allowing other people to read & work with your code without giving them headaches.

# Multiple Variables in One Line

In Lua, you can declare multiple variables in a single line. For example:

```lua
local a, b, c = 10, 5, 3
print(a)
print(b)
print(c)
```

This initializes three local variables, `a`, `b` and `c`, and gives them a value of `10`, `5`, and `3` respectively.

>✨ It is a good idea to avoid multiple variables in a single line as it may make your code harder to read.

# Conclusion

That was quite a lot! However, you should have hopefully learned one of the most important things in not just Lua, but coding as a whole.

# Quiz

This one's going to be quite long!

#1. Write a piece of code which does the following:
   * Initializes a variable named `foo` with a value of 5
   * Prints out the value of the variable

<details>
  <summary>Solution</summary>
  
  ```lua
  local foo = 5
  print(foo)
  ```
  
</details>

#2. What does this piece of code print out?

```lua
local myVariable = "foo"
print(myVariable)
```

<details>
  <summary>Solution</summary>
  foo
</details>

#3. What does this piece of code print out?

```lua
local myVariable = "baz"
myVariable = 100
print(myVariable)
```

<details>
  <summary>Solution</summary>
  100
</details>

#4. Which variable name is unacceptable?:

   * aCoolVariableName100
   * an amazing variable
   * one_variable

<details>
  <summary>Solution</summary>
  an amazing Variable
</details>

#5. So far, this chapter went over three data types (`string`, `nil`, and `number`). What data type would make the most sense when we want to assign a name to the player?

<details>
  <summary>Solution</summary>
  string
</details>

#6. What does this piece of code print out?

```lua
print(myVariable)
local myVariable = 100
```

<details>
  <summary>Solution</summary>
  `nil`. That is because we're printing out a variable that has not been initialized yet, which is `nil`. The variable is initialized after the code tries printing.
</details>

