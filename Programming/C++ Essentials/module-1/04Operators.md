# 4.0 Operators: Essential Tools for C++
## 4.0.1 Floating-point Numbers
Another data type that's designed to represent and store the numbers that have non-empty decimal fractions are considered **floating numbers**. You can omit zero when it's the only digit in front of or after the decimal point. The decimal point is essential to recognize floating-point numbers in C++. `4` is an `int`, and `4.0` is a `float`.

When you want to use any numbers that are very big or small, you can use scientific notation. The speed of light can be written as `300000000 m/s`. The shorthand for this would be `3E8 m/s` which is the same as `3 * 10^8`. The letter _E_ (or the lowercase letter _e_ - it comes from the word exponent) is a concise version of the phrase "times ten to the power of".

Note:
- The exponent (the value after the `E`) has to be an integer
- The base (the value in front of the `E`) may or may not be an integer

What happens when we convert integer values into floats and vice versa? We can always transform from `int` to `float`, but it can lead to a loss of accuracy. The transformation affects the internal (machine) representation of those values as computers use different methods for storing floats and ints in their memory. The same can be said for the vice versa, with it sometimes being the case that converting a `float` into an `int` is not always feasible. Integer variables (like floats) have a limited capacity. They cannot contain abritraily large or small numbers. In some systems it may be the maximum permissible `int` value, while in others an error occurs., and in others still the value assigned can be completely random. This is what is called an **implementation dependent issue**.

## 4.0.2 Operators
Paragraph

## 4.0.3 Multiplication
Paragraph

## 4.0.4 Division
Paragraph

## 4.0.5 Division by Zero
Paragraph

## 4.0.6 Addition
Paragraph

## 4.0.7 Subtraction
Paragraph

## 4.0.8 Unary Minus
Paragraph

## 4.0.9 Unary Plus
Paragraph

## 4.0.10 Remainder
Paragraph

## 4.0.11 Priorities
Paragraph

## 4.0.12 Remainder
Paragraph

## 4.0.13 Priorities
Paragraph

## 4.0.14 Bindings
Paragraph

## 4.0.15 Priority Table
Paragraph

## 4.0.16 Parentheses
Paragraph

## 4.0.17 Increment & Decrement Operators
Paragraph

## 4.0.18 Pre- and post-operators and their priorities
Paragraph

## 4.0.19 Shortcut Operators
Paragraph

```txt
#include <iostream>
using namespace std;

int main(void) {
  cout << "Hello, world!" << endl;
  return 0;
}
```

`snippet`
