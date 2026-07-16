# 6.0 Making Simple Decisions: Introduction to Flow Control in C++

## 6.1 One does not asks who errs
A programmer writes a program and the program asks questions. A computer executes the program and proivdes the answers. The program must be able to react according to the answers it receives. Computers only know two kinds of answers: yes, this is true or no, this is false. To ask questions, the C++ language uses a set of very special operators.

## 6.2 How to ask questions

## 6.2.1 Is x equal to y?
To ask whether to values are equal you use the **equal operator** `==`.

Don't forget this distinction:
- `=` is the assignment operator
- `==` is the question "are these values equal?"

It is a binary operator with a left-side binding. It need two arguments and checks if they're equal.

Due to the low priority of the equal operator, use parentheses.

EX. `counter == (2 * counter);`

## 6.2.2 Is x not equal to y?
To ask whether to values are not equal you use the **not equal operator** `!=`.

It is a binary operator with a left-side binding. It need two arguments and checks if they're not equal.

EX. `counter != 5;`

## 6.2.3 Is x greater than (or equal to) y?
To ask whether to values are greater than you use the **greater than operator** `>`. The answer `true` confirms the statement; The answer `false` denies it.

EX. `counter > 0;`

To ask whether to values are greater than or equal to each other you use the **greater than or equal operator** `>=`.

It is a binary operator with a left-side binding. It need two arguments and checks if they're greater than or equal. This operator's priority is greater than the ones indicated by `==` and `!=`.

EX. `counter >= 1;`

## 6.2.4 Is x less than or equal to y?
To ask whether to values are less than you use the **less than operator** `<`.

EX. `counter < 5;`

To ask whether to values are less than or equal to each other you use the **less than or equal operator** `<=`.

It is a binary operator with a left-side binding. It need two arguments and checks if they're greater than or equal. This operator's priority is greater than the ones indicated by `==` and `!=`.

EX. `counter <= 4;`

## 6.3 How to use the answers we got?
There are two ways we can use the answers we get from our questions:
1. We can store the answers in variables for later use. If the answer is `true`, the computer will assign `1` (which is arguably different from zero). If the answer is `false`, the computer will asign `0`.
2. We can use the answer to make a decision using special mechniasm which allows us to do something if a condition is met.

To make these decisions, the C++ offers a special instruction, which due to its nature and application, is called a **conditional instruction** (**statement**). There are several varients of the conditional instruction, the simplest of which is the `if` statement: `if (condition_true_or_false) execute_if_true;`

The conditional statement consists of the following elements in this order:
- `if` keyword
- an expression (a question or an answer) whose value will be interpreted soley in terms of `true` (when it's value is a non-zero) and `false` (when equal to zero)
- an instruction

How does the statement work?
- If the `condition_true_or_false` expression enclosed inside the parentheses represents the truth (i.e., it's value is a non-zero), the statement behind this condition `execute_if_true` will execute
- If the `condition_true_or_false` expression enclosed inside the parentheses represents a falsehood (i.e., it's value is zero), the statement behind this condition is omitted and the next executable instruction will be the one that lies after the conditional statement

There may only be one statement after the `if` statement. When we have to conditonally execute more than one instruction we need to use braces `{}` which creates a structure called a **compound statement** or **block**. The block is treated as a single instruction by the compiler. Thsi is how to circumvent the `if` statement limitation.

## 6.4 Update the Priority Table
Now we can update our priority table.

