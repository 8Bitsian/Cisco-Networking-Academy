# 4.0 Operators: Essential Tools for C++
## 4.1 Floating-point Numbers
Another data type that's designed to represent and store the numbers that have non-empty decimal fractions are considered **floating numbers**. You can omit zero when it's the only digit in front of or after the decimal point. The decimal point is essential to recognize floating-point numbers in C++. `4` is an `int`, and `4.0` is a `float`.

When you want to use any numbers that are very big or small, you can use scientific notation. The speed of light can be written as `300000000 m/s`. The shorthand for this would be `3E8 m/s` which is the same as `3 * 10^8`. The letter _E_ (or the lowercase letter _e_ - it comes from the word exponent) is a concise version of the phrase "times ten to the power of".

Note:
- The exponent (the value after the `E`) has to be an integer
- The base (the value in front of the `E`) may or may not be an integer

What happens when we convert integer values into floats and vice versa? We can always transform from `int` to `float`, but it can lead to a loss of accuracy. The transformation affects the internal (machine) representation of those values as computers use different methods for storing floats and ints in their memory. The same can be said for the vice versa, with it sometimes being the case that converting a `float` into an `int` is not always feasible. Integer variables (like floats) have a limited capacity. They cannot contain abritraily large or small numbers. In some systems it may be the maximum permissible `int` value, while in others an error occurs., and in others still the value assigned can be completely random. This is what is called an **implementation dependent issue**.

## 4.2 Operators
An **operator** is a symbol of the programming language, which is able to operate on the values. For example, the **assignment operator** is `=` and it can assign values to variables.

### 4.2.1 Multiplication
An asterisk `*` is a **multiplication operator** and it can multiply variables.

### 4.2.2 Division
A slash `/` is a **divisional operator** and it can divide variables. The value in front of the slash is the **dividend** and the value behind is the **devisor**.

Division by zero is strictly forbidden - you'll liekly get a compilation error, runtime error, or some message at runtime.

In the following example, the compiler won't say anything but will return a special featrued value named `inf` (as in **infinitive**). This kind of illegal operation is considered an **exception**.

``` txt
float x, y;
x = 0.0;
y = 1.0 / x;
```

### 4.2.3 Addition
A plus sign `+` is an **addition operator** and it can add variables.

### 4.2.4 Subtraction
A minus sign `-` is a **subtraction operator** and it can subtract variables.

### 4.2.5 Unary Operators
There is an important distinction between **unary** and **binary** operators.

#### 4.2.5.1 Unary Minus
In subtracting application, the subtractor operator `-` expects two arguments: The left (a minuend in arithemetic temrs) and the right (a subtrahend). For this reason, the subtraction operator is considered one of the binary operators, just like addition, multiplication, and division operators. We can also use the minus operator as a unary operator, as it expects only one argument - the subtrahend - to make the value negative.

#### 4.2.5.1 Unary Plus
The same dual nature is expressed by the addition operator `+`, which can also be used as a unary operator whose role is to preseve the sign - to make the value positive.

### 4.2.6 Remainder
A percent sign `%` is the **remainder operator**, which has no equivalent among traditional arithmetic operators. It is a bianry operator which performs the **modulo operation** where both arguments cannot be floats. You also cannot computer the remainder with the right argument equal to zero because division by zero provokes undefined behavior.

### 4.3 Priorities
In programming you'll find more than one operator in an expression and which some precede one another. The phenomenon that causes some operators to act before others is known as the heirarerchy of priorities. The C++ langauge precisely defines the priorities of all operators and assumes that operators of larger (higher) priority perform their operations before the operators with lower priority.

### 4.4 Bindings
The **binding** of the operator determines the order of computations performed by some operators with equal priority, put side by side in an expression. Most operators in the C++ langauge have the **left-sided binding** which means that the calculation is conducted left to right.

### 4.5 Priority Table
We've currently gone through operators in order from highest to lowest priority. Both operators (`*` and `%`) have the same prioority, so the result is determined by the binding direction.

| Operators | Sign |
|:---:|:---:|
|++ -- + -| Unary |
|* / % | x |
| + - | Binary |
| = | x |

## 4.6 Parentheses
Just like with arithmetic rules, subexpression in **parentheses** `()` are calculated first, which can change the natural order of calculation. You can use as many parentheses are you need and we often use them for the readability of an expresion, even if they don't change the order of operations.

## 4.7 Increment & Decrement Operators
Some operators are frequently used to increment a variable by one. You can either add the 1 like this: `counter = x + 1;`, or you can use the **increment operator** `++` like this: `counter++;` Similarly you can also decrease the value of the chosen variable by one using the **decrement operator** `--` like this: `counter--;`.

## 4.8 Pre- and post-operators and their priorities
Increment and decrement operators behavior justify the precense of the prescence of the prefix pre- (before) and post- (after) in the operators' names: _pre-_ because the varioable is modified first and then its value is used; and _post-_ because the varible's value is used and then modified.

## 4.9 Shortcut Operators
If `op` is a **two-argument operator** (a very important condition) and the operator is used in the followwing context: `variable = variable op expression;`, then the expression can be simiplified as follows: `variable op = expression;`
