# Introduction

This chapter will go over math operators.

# An Example

A math operator is a symbol that performs a mathematical operation. Here is an example of an operator being used:

```lua
print(2 + 5)
```

Running this will print out `7`. This is an example of the addition operator in action.

Operators can also be used on variables.

```lua
local myNumber = 10
print(myNumber + 15)
```

This prints out `25`. In the first line, `myNumber` is initialized with a value of 10. In the second line, the sum of `myNumber` and `15` is printed.

Another example of an operator being used:

```lua
local aCoolNumber = 10
aCoolNumber = aCoolNumber - 3
print(aCoolNumber)
```

This prints out `7`. The first line initializes `aCoolNumber` with a value of 10. The second line changes the value of `aCoolNumber` to its current value minus `3`, which would be `7`.

# List of Math Operators

| Operator | Description | Example
| --- | ----------- | ----------- |
| + | Adds two operands | 10 + 5 |
| - | Subtracts two operands | 8 - 3 |
| * | Multiplies two operands | 3 * 10 |
| / | Divides two operands | 8 / 2 |
| ^ | Raises the first operand to the power of the second operand | 2^3 |
| % | Takes the first operand, divides it by the second operand, and returns the remainder | 10 % 3 |
| - | Negates the current operand | -6 |

>⚠️ Be wary about dividing numbers by zero. This will return `inf` (also known as infinity), which can cause unexpected problems in your code.

# Conclusion
 
Congratulations on learning the basic math operators! While coding, you will be using them quite a lot.

# Quiz

Do not run these code snippets.

#1. What does this print out?

```lua
print(10/5)
```

<details>
  <summary>Solution</summary>
  2
</details>

#2. What does this print out?

```lua
local myVariable = 2 + 5
print(myVariable)
```

<details>
  <summary>Solution</summary>
  7
</details>

#3. What does this print out?

```lua
local myCurrentValue = 10
myCurrentValue = myCurrentValue ^ 2
print(myCurrentValue)
```

<details>
  <summary>Solution</summary>
  100
</details>

#4. What does this print out?

```lua
local variable1 = 10
local variable2 = variable1 + 5
print(variable2)
```

<details>
  <summary>Solution</summary>
  15
</details>

#5. What does this print out?

```lua
local variable1 = 10
local variable2 = variable1 - 2
local variable3 = variable2 * 2
print(variable3)
```

<details>
  <summary>Solution</summary>
  16
</details>

#6. What does this print out?

```lua
local myVariable = 2
print(myvariable / 2)
```

<details>
  <summary>Solution</summary>
  The code errors as it tries to perform an arithmetic on a nil value as there is no variable named `myvariable`
</details>

#7. What does this print out?

```lua
print((8 + 2)/2)
```

<details>
  <summary>Solution</summary>
  5
</details>

