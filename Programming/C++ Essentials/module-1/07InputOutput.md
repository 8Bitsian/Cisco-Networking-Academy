# 7.0 Connecting with the Real World: Input and Output in C++
## 7.1 Input and Output
Sending data in the direction from human (user) to the computer program is called **input**. The stream of data in the opposite direction, i.e., from the computer to the human, is called **output** which is handled by the `cout` stream which is capable of writing the data of virtually any datat type on a computer screen. The **insertion operator** `<<` inserts a string of characters into the character device (e.g., a console). 

## 7.2 Output
`cout` is one of the streams associated with the screen (or more formally **console**) and is operable via header file name. If you want to print a variable to the screen, the only thing you have to do is send it to the cout stream through the `<<` operator, which indicates the desired direction of data transfer.

Both the `<<` operator and the `cout` stream are responsible for two actions:
1. Converting the internal (machine) representation of the variable value into a form readable by humans
2. Transferring the converted form to the output device e.g. console

Streams are great for both input and output as they can easily output several values of different types and mix them with text, and input many values at once.

## 7.3 Input
Paragraph
