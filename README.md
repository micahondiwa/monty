# C - Stacks, Queues - LIFO, FIFO

- A project done during my Full-Stack Software Engineering studies at [ALX Africa](https://www.alxafrica.com/software-engineering-2022/), a course offered by [Holberton School](https://www.holbertonschool.com/).

## Technologies
- Files written in ```vi```, ```vim```, and ```emacs``` editors. 
- C files compiled using ```gcc 9.4.0```.
- C files wriiten according to the betty coding style. Checked using [betty-style.pl](https://github.com/holbertonschool/Betty/blob/master/betty-style.pl) and [betty-doc.pl](https://github.com/holbertonschool/Betty/blob/master/betty-doc.pl).
- Files tested on ```Ubuntu 20.04``` LTS using ```gcc```.
- Outpus are  printed on ```stdout```
- Error messages printed on ```stderr```

## The Monty language
- Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

### Monty byte code files
- Files containing Monty byte codes usually have the ```.m ``` extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument.
- Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account.

### The monty program
- **Usage:** ```monty file```
  - where file is the path to the file containing Monty byte code
- If the user does not give any file or more than one argument to your program, print the error message ```USAGE: monty file```, followed by a new line, and exit with the status ```EXIT_FAILURE```
- If, for any reason, it’s not possible to open the file, print the error message ```Error: Can't open file <file>```, followed by a new line, and exit with the status ```EXIT_FAILURE```.
  - where ```<file>``` is the name of the file.
- If the file contains an invalid instruction, print the error message ```L<line_number>: unknown instruction <opcode>```, followed by a new line, and exit with the status ```EXIT_FAILURE```
  - where is the line number where the instruction appears.
  - Line numbers always start at 1
- The monty program runs the bytecodes line by line and stop if either:
  - it executed properly every line of the file
  - it finds an error in the file
  - an error occured
 - If you can’t malloc anymore, the program prints the error message ```Error: malloc failed```, followed by a new line, and exit with status ```EXIT_FAILURE```.
#### Compilation
```
$ gcc -Wall -Werror -Wextra -pedantic *.c -o monty
$
```
#### Run
```
$ ./monty monty_file.m
5
7
1
2
```
#### Interpreter Synopsis
```
$ ./monty [montyfilename]
$
```
#### Opcodes


