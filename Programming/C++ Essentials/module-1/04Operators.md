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
Paragraph

### 4.3 Priorities
Paragraph

### 4.4 Bindings
Paragraph

### 4.5 Priority Table
Paragraph

## 4.6 Parentheses
Paragraph

## 4.7 Increment & Decrement Operators
Paragraph

## 4.8 Pre- and post-operators and their priorities
Paragraph

## 4.9 Shortcut Operators
Paragraph
