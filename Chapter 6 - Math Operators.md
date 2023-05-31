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

| Operator | Description | Example | Result
| --- | ----------- | ----------- | --- |
| + | The addition operator adds two operands | 10 + 5 | 15 |
| - | The subtraction operator sbtracts two operands | 8 - 3 | 5 |
| * | The multiplication operator multiplies two operands | 3 * 10 | 30 |
| / | The division operator divides two operands | 8 / 2 | 4 |
| // | The floored division operator divides two operands and rounds down the quotient | 10 // 3 | 3 |
| ^ | The exponent operator raises the first operand to the power of the second operand | 2^3 | 8 |
| % | The modulo operator takes the first operand, divides it by the second operand, and returns the remainder | 10 % 3 | 1 |
| - | The unary minus operator inverts the sign of the operand. This uses the same symbol as the subtraction operator. | -(3-5) | 2 |

>⚠️ Be wary about dividing numbers by zero. This will return `inf` (also known as infinity), which can cause unexpected problems in your code.

# Operator Precedence

When performing math operations, you aren't limited to only one operation. For example:

```lua
local finalAnswer = 5 - 1 + 3
print(finalAnswer)
```

This prints out `7` as a result as the code first subtracts `5 - 1` and then adds `3` to the difference. 

However, it's important to note that the final value is not being calculated from the left-most operator to the right-most operator. For example:

```lua
local finalAnswer = 2 + 5 * 10
print(finalAnswer)
```

You might assume that the final answer would be 70. However, you'll instead get `52`. This is because there is a specific order in which math operations are being performed.

**Operator Precedence** (or **order of operations**) is the order in which math operators are performed to calculate the final result.

If you have taken any math classes, you may be familiar with the term **PEMDAS**. Operator Precedence works the same way!

When an equation is being evaluated, the following operations are being evaluated in order:

1. Unary - First, everything with a unary operator is evaluated. This is not to be confused with subtraction.
2. Paranthesis - Next, everything in parenthesis is evaluated. Everything evaluated inside of parenthesis also follows the operator precedence.
3. Exponents - Next, every term with an exponent operator is evaluated.
4. Multiplication - Next, every operand tied to the multiplication operator is evaluated.
5. Division - Next, every operand tied to the division operator is evaluated.
6. Addition - Next, every operand tied to the addition operator is evaluated.
7. Subtraction - Finally, every operand tied to the subtraction operator is evaluated.

Here is an example of this in action.

```lua
local myAnswer = (10 * 2) / 5 + 1
print(myAnswer)
```

This prints out `5`. This is because the following operations are being performed in order:

1. Everything in the parentheses are being evaluated first. In this case, `10 * 2` is being evaluated. The final product is `20`. The equation can now be simplified to `20 / 5 + 1`
2. Since a division operator is present, `20 / 5` is performed next, with the final product being `4`. The equation can now be simplified to `4 + 1`.
3. Finally, the remaining operands are added together, which produces the final answer of `5`.


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

