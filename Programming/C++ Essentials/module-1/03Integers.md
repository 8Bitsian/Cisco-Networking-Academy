# 3.0 The Basics of Integers and Variables
## 3.1 Numbers and how computers see them
Computers use the binary system to store numbers and perform operations on them.

There are two types of numbers handled by modern computers:
1. **Integers**, which are real numbers devoid of fractional parts
2. **Floating-point** (**floats**) numbers are real numbers that contain a fractional part

Both these kinds of numbers differ in how that are stored in computer memory and in the range of acceptable values. Additionally, the characteristic of a number which determines its kind, range and application is called a **data type**. An integer type is represented by the keyword `int` and the floating-point type is represented by the keyword `float`.

There are two additional conventions, the first of which allows us to use the numbers in octal representation. If an integer number is preceded by the 0 digit, it will be treated as an octal value. This means that the number must contain digits taken from the 0 to 7 range only.
- Ex. `0123` is an octal number with a decimal value equal to _83_.

The second allows us to use hexadecimal numbers. If an integer number is preceded by 0x or 0X, it will be treated as an hexadecimal value.
- Ex. `0x123` is a hexadecimal number with a decimal value equal to _291_.

## 3.2 A variable is variable
The C++ language allows special containers called variables. Every variable has a name, type, and value.

When naming vairables, you must adhere to the following syntax:
- The name of the variable must be composed of uppercase (A-Z), lowercase (a-z), digits (0-9) and characters (_-)
- The name of the variable must begin with a character or letter
- The name of variables are case sensitive, so upper- and lowercase letters are treated differently

The same naming restrcitions apply to all entity names used in C++.

The **type** is an attribute that uniquely defines which values can be stored inside the variable. You can only enter a value that is compatible with the variable's type.

You can make a variable through a **variable declaration** which is a syntactic structure that binds a name by the programmer with a specific type offered by the C++ langauge. The **declaration syntax** is simple: Use the name of the desired type, then the variable name (or variable names separated by commas if there are more than one), and then end the statement with a semicolon.

Ex. `int varible_1, variable_2;`

You can give a value to the newly declared variable via the **assignment operator**.

Ex. `int varible_3 = 1 + 2,;`

## 3.3 Understanding keywords
**Reserved keywords** are a list of words that are predefined and cannot be used as names for other entities such as variables nor functions. Fortunatley, because th C++ compiler is case-sensitive, you can modify any of these words by changing the case of any letter, thus creating a new word, which is not reserved.

| Keywords | | | | | |
|:---:|:---:|:---:|:---:|:---:|:---:|
| and | asm | auto | bitand | bitor | bool |
| break | char | const | continue | default | delete |
| do | else | export | float | goto | int |
| namespace | not | private | public | register | sizeof |
| switch | throw | try | typeid | union | unsigned |
| virtual | void | volatile | wchar_t | xor | xor_eq |

## 3.4 Comments on comments
Comments are a way for developers to add a few words addressed not the compiler, but to other humans to explain to readers how the code functions. Each comment is lexically equivalent to one space. Whenver the compiler encounters a comment in your program, the comment is completely transparent to it - form its point of view its only one space (regardless of how long the actual comment is).

The C++ langauge supports two ways of inserting comments:
1. `// line comments` discard everything from where the pair of slash signs is found up to the end of the line
2. `/* block comments */` can span for multiple line from where the slash and asterisk are to the asterisk and slash is/

Developers often put notes at the beginning of the source informing when they write the program stating who amended it and why.

The note may appear as follows:

```txt
/* ************************************
Program_name version #.#
Author: John Doe
Date: DD-MM-YYYY
Contact: JDoe@website.com

Changelog:
DD-MM-YYYY: Title: Description
************************************ */
```
