 
# Introduction

This chapter goes over conditional statements, relational operators, and logical operators.

# Boolean Data Type

A boolean is a data type that can only hold two values: `true` and `false`. Just like other data types, you can also assign booleans to variables like this:

```lua
local myBoolean = true
local myOtherBoolean = false
```

As you continue reading this chapter, you will start to see cases where booleans shine!

>⚠️ Booleans are case-sensitive! Make sure that `true` and `false` are always typed in all lowercase.

# Relational Operators

A **relational operator** is an operator that compares two operands with each other, and returns a boolean value based on the result.

Here is the list of all of the conditional operators Lua has to offer:

| Operator | Description | Example | Result
| --- | ----------- | ---------------- | ------- |
| == | Checks to see if two operands are equal to each other | 5 == 5 | true |
| ~= | Checks to see if two operands are not equal to each other | 8 ~= 8 | false |
| > | Checks to see if the value of the left operand is greater than the value of the right operand | 8 > 5 | true |
| < | Checks to see if the value of the left operand is less than the value of the right operand | 5 < 3 | false |
| >= | Checks to see if the value of the left operand is greater than or equal to the value of the right operand   | 5 >= 5 | true |
| <= | Checks to see if the value of the left operand is less than or equal to the value of the right operand | 15 <= 8 | false |

>⚠️ Be careful not to confuse `=` with `==`! `=` is only used to assign a value to an object such as variables, while `==` is used to check if two values are equal to each other.

Let's take a look at conditional operators in action.

**Example #1**

```lua
local myValue = 90
print(myValue > 100)
```

If you run this code, this will print `false`. This is because `myValue` was initialized with a value of `90` and we're printing out the expression `myValue > 100`, which returns false as the current value of the variable is not greater than `100`.

**Example #2**

```lua
local aCoolValue = 40 >= 35
print(aCoolValue)
```

If you run this code, this will print `true`. This is because we're setting the value of `aCoolValue` to true since 40 is greater than or equal to 35. Then, we are printing out its value.

**Example #3**

With relational operators, we aren't restricted to only comparing numbers.

```lua
local myString = "a cool string"
local myOtherString = "not a cool string"
print(myString == myOtherString)
```

This prints `false` as the value of `myString` is not equal to `myOtherString`

# Comparing Two Different Types

When comparing two operands with each other, both operands don't have to be the same data type if you're using the `==` operator or the `~=` operator. For example:

```lua
print(5 == "a string")
```

This will print `false` as the number `5` is not equal to the string `"a string"`.

However, you can not compare two different data types using any other relational operator. If you were to run this:

```lua
print(5 <= "5")
```

The code will error with a message telling you that you tried to compare a number with a string.

# Introduction to conditional statements

While you're coding, there are times when you want something specific to happen only if a certain condition is met. For example, what if we only want the player to be able to use a specific item if they have enough help? This is where **conditional statements** come into play.

Let's take a look at the following piece of code:

```lua
local aTestValue = 2

if aTestValue == 2 then
  print("The value is two!")
end
```

You should already know what the first line does. All it does is initialize a variable named `aTestValue` with a value of `2`.

The third line is the conditional statement itself. There are three separate parts to take note of:
* `if` is the start of the conditional statement.
* `aTestValue == 2` is the **condition** that's being evaluated, which is checking to see if the value of `aTestValue` is equal to `2`.
* `then` is the end of the conditional check. The block of code after it will now only run if the conditional evaluates to `true`.
* `end` is the end of the conditional statement as a whole. 

That is the general gist of a conditional statement. It will run a block of code only if it evaluates to `true`. If you tried to run the following:

```lua
local aTestValue = 2

if aTestValue ~= 2 then
  print("The value is two!")
end
```

Nothing will print out now as the condition now evaluates to false, causing the code block to not run.

# Else If Statement

An **elseif** statement is part of a conditional statement that will only run if the previous condition evaluates to false. Let's take a look at an example:r

```lua
local myValue = 10

if myValue == 8 then
  print("It is equal to 8")
elseif myValue == 10 then
  print("It is equal to 10")
end
```

If you run this, "It is equal to 10" is printed out. Let's dissect this.

* The first line of code just initializes `myValue` with a value of `10`
* The third line of code checks to see if `myValue` is equal to 8.
* The fourth line of code will only run if `myValue` is equal to 8.`
* The fifth line of code is a new conditional check. This check will only be evaluated if the previous condition, `myValue == 8`, returns false. Since it returned false, it is evaluated.
* The sixth line of code only runs if the `elseif` statement evaluates to true.
* The seventh line is the end of the entire conditional statement.

If you were to change `myValue` to 8, then "It is equal to 8" is printed instead. If the value is not `10` and not `8`, then nothing is printed at all since both conditionals return false.

You can have as many `elseif` statements as you want in your conditional. Here is an example with three conditions being evaluated:

```lua
local myFavoriteFruit = "apple"

if myFavoriteFruit == "grapes" then
  print("You like grapes!")
elseif myFavoriteFruit == "blueberries" then
  print("You like blueberries")
elseif myFavoriteFruit == "apple" then
  print("You like apples")
end
```

This code prints out "You like apples" as a result.

# Else Statement

An **else** statement is part of a conditional statement that runs only if all previous conditionals return false. Here is an example:

```lua
local myCash = 10
local requiredMoney = 15

if myCash >= requiredMoney then
  print("You have enough money")
else
  print("You do not have enough money")
end
```

In this piece of code, we are checking to see if the value of `myCash` is greater than or equal to `requiredMoney`. Since it evaluates to `false` and there are no more expressions to evaluate, the code block between the `else` and `end` will execute.

You can also chain else-ifs along with an `else`.

```lua
local myFavoriteFruit = "grapefruit"

if myFavoriteFruit == "grapes" then
  print("You like grapes!")
elseif myFavoriteFruit == "blue berries" then
  print("You like blueberries")
elseif myFavoriteFruit == "apple" then
  print("You like apples")
else
  print("You have a bad taste in fruit")
end
```

This prints out "You have a bad taste in fruit" as all of the conditions evaluate as `false`.

# Logical Operators

A **logical operator** allows you to evaluate multiple conditions at once as well as manipulate the current condition being checked. Here is a list of logical operators Lua has:

| Operator | Description | Example | Result
| --- | ----------- | ---------------- | ------- |
| or | Returns true if at least one of the operands returns true | 5 == 10 or 3 >= 1 | true |
| and | Returns true only if both operands return true | 3 == 3 and 10 > 15 | false |
| not | Reverses the current condition. If the current condition is `true` and you use `not`, then it becomes false and vice versa | not false | true |

Here are examples of logical operators in action.

**Example #1**

```lua
local number1 = 5
local number2 = 8
local numberToCheck = 8

if number1 == numberToCheck or number2 == numberToCheck then
  print("One of the numbers returns true!")
end
```

This prints out "One of the numbers returns true!". Although `number1` is not equal to `numberToCheck`, `number2` is equal to `numberToCheck` which makes the condition evaluate to `true`.

**Example #2**

```lua
local myFruit1 = "apple"
local myFruit2 = "grapes"

if myFruit1 == "apple" and myFruit2 == "strawberry" then
  print("You have what I need")
else
  print("You don't have what I need")
end
```

This prints out "You don't have what I need". This is because while the first operand of `myFruit1 == "apple"` evaluates to true, `myFruit2 == "strawberry"` evaluates to `false`, which makes the condition `false` since the `and` operator is being used.

# Quiz

#1. What does this print out?

```lua
local myVariable = 8
print(myVariable <= 10)
```

<details>
  <summary>Solution</summary>
  true
</details>

#2. What does this print out?

```lua
local number1 = 8
local number2 = 9
local bannedNumber = 10
print(number1 ~= bannedNumber and number2 ~= bannedNumber)
```

<details>
  <summary>Solution</summary>
  true
</details>

#3. What does this print out?

```lua
local myMoney = 8
local requiredMoney = 5

if myMoney > requiredMoney then
  myMoney = myMoney - requiredMoney
end

print(myMoney)
```

<details>
  <summary>Solution</summary>
  3
</details>

#4. What does this print out?

```lua
local favoriteFruit = "banana"

if favoriteFruit == "apple" then
  print("You like apples!")
elseif favoriteFruit == "banana" then
  print("You have an okay taste in fruit")
else
  print("Your taste in fruit sucks!")
end
```

<details>
  <summary>Solution</summary>
  "You have an okay taste in fruit"
</details>
