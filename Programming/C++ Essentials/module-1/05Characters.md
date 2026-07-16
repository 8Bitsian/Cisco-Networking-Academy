# 5.0 Characters: Handling Textual Data in C++
## 5.1 Character Type
We can define a word as a string of characters (letters, numbers, punctuation marks, etc.). In the C++ langauge all strings consist of multiple characters and are treated as arrays. To store and manipulate singular characters, the C++ langauge provides a special type of data called a `char` which is an abbreviation of the word _character_.

EX. `char character;`

## 5.2 ASCII Code
Computers store characters as unqiue numbers. Many of these are invisible to humans, such as **white spaces**, while others control the input/output devices, such as **control characters**.

The universal and widely accepted standard implemented by (almost) all computers and operating system worldwide is the **American Standard Code for Information Interchange** or **ASCII**. The code provides space for 256 different characters, but we're only interested in the first 128. Note that the letters are arranged in the same order as the Latin alphabet. Nowadays, ASCII is being superseded (or rather extended) bby a new international standard named UNICODE, so now its a subset. UNICODE is able to represent virtually all characters used throughout the world.

| Char | Dec | Hex | Char | Dec | Hex | Char | Dec | Hex | Char | Dec | Hex |
|:----:|:---:|:---:|:----:|:---:|:---:|:----:|:---:|:---:|:----:|:---:|:---:|
|(NUL) |0    |0    |(space)|32  |20   |@     |64   |40   |`     |96   |60   |
|(SOH) |1    |1    |!     |33   |21   |A     |65   |41   |a     |97   |61   |
|(STX) |2    |2    |"     |34   |22   |B     |66   |42   |b     |98   |62   |
|(ETX) |3    |3    |#     |35   |23   |C     |67   |43   |c     |99   |63   |
|(EOT) |4    |4    |($)   |36   |24   |D     |68   |44   |d     |100  |64   |
|(ENQ) |5    |5    |%     |37   |25   |E     |69   |45   |e     |101  |65   |
|(ACK) |6    |6    |&     |38   |26   |F     |70   |46   |f     |102  |66   |
|(BEL) |7    |7    |'     |39   |27   |G     |71   |47   |g     |103  |67   |
|(BS)  |8    |8    |(     |40   |28   |H     |72   |48   |h     |104  |68   |
|(HT)  |9    |9    |)     |41   |29   |I     |73   |49   |I     |105  |69   |
|(LF)  |10   |0A   |*     |42   |2A   |J     |74   |4A   |J     |106  |6A   |
|(VT)  |11   |0B   |+     |43   |2B   |K     |75   |4B   |k     |107  |6B   |
|(FF)  |12   |0C   |,     |44   |2C   |L     |76   |4C   |l     |108  |6C   |
|(CR)  |13   |0D   |-     |45   |2D   |M     |77   |4D   |m     |109  |6D   |
|(SO)  |14   |0E   |.     |46   |2E   |N     |78   |4E   |n     |110  |6E   |
|(SI)  |15   |0F   |/     |47   |2F   |O     |79   |4F   |o     |111  |6F   |
|(DLE) |16   |10   |0     |48   |30   |P     |80   |50   |p     |112  |70   |
|(DC1) |17   |11   |1     |49   |31   |Q     |81   |51   |q     |113  |71   |
|(DC2) |18   |12   |2     |50   |32   |R     |82   |52   |r     |114  |72   |
|(DC3) |19   |13   |3     |51   |33   |S     |83   |53   |s     |115  |73   |
|(DC4) |20   |14   |4     |52   |34   |T     |84   |54   |t     |116  |74   |
|(NAK) |21   |15   |5     |53   |35   |U     |85   |55   |u     |117  |75   |
|(SYN) |22   |16   |6     |54   |36   |V     |86   |56   |v     |118  |76   |
|(ETB) |23   |17   |7     |55   |37   |W     |87   |57   |w     |119  |77   |
|(CAN) |24   |18   |8     |56   |38   |X     |88   |58   |x     |120  |78   |
|(EM)  |25   |19   |9     |57   |39   |Y     |89   |59   |y     |121  |79   |
|(SUB) |26   |1A   |:     |58   |3A   |Z     |90   |5A   |z     |122  |7A   |
|(ESC) |27   |1B   |;     |59   |3B   |[     |91   |5B   |{     |123  |7B   |
|(FS)  |28   |1C   |<     |60   |3C   |\     |92   |5C   ||     |124  |7C   |
|(GS)  |29   |1D   |=     |61   |3D   |]     |93   |5D   |}     |125  |7D   |
|(RS)  |30   |1E   |>     |62   |3E   |^     |94   |5E   |~     |126  |7E   |
|(US)  |31   |1F   |?     |63   |3F   |_     |95   |5F   |      |127  |7F   |

## 5.3 Character Type Values
We can use the `char` type in two ways in the C++ langauge:
1. We can specify the character itself with single quotes or apostrophes `''`
2. We can assigned non-negative integer values that correpsonds to the code of the desired character

EX. `character = 'A';` and `character = 65;` both assign captial A to the variable `character`.

The second solution is not recommended. however, since there are other computers that use codes other than ASCII. For example, many IBM mainframes use code called **Extended Binary Coded Decimal Interchange Code** or **EBCDIC**.

## 5.4 Literal
A **literal** is a symbol which uniquely identifies its value, or to put it plainly, the literal means itself.

Look at the following examples:
- `A` is a literal as when you look at it you can immediately guess its value; You can even know that it's a literal of the `char` type
- `100` is a literal of the `int` type
- `100.0` is a literal of the `float` type
- `i + 100` is a combination of a variable and a literal joined with the `+` operator; This structure is called an **expression**.

## 5.5 Escape Characters
The **escape character** `\` is a special convention by the C++ langauge that allows us to escape from the normal meaning of a character that follows the backslash - i.e., we can escape from the usual role of the character.

The C++ langauge allows us to escape other circumstaces too. We can start with literals denoting whitespace:
- `\n` denotes a transition to a new line and is sometimes called an **Line Feed** (**LF**), as printers react to this character by pulling out the paper by one line of text
- `\r` denotes the return to the beginning of the line and is sometimes called a **Carriage Return** (**CR**) - "carrriage" being the synonym of a "print head" in the typewriter era
- `\a` (as in **alarm**) references when teletypes were often used to communicate with computers; sending this character to a teletype turns on its ringer; hence, the character is officially called **BEL** (as in **bell**). IF you try to send this character to the console, you'll hear a short beep
- `\0` denotes the a character that doens't represent any character and is called **nul** from the latin word **nullus**

## 5.6 `char` Values are `int` Values
Paragraph
