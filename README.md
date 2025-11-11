<!---
{
  "id": "0508295d-de49-4a67-8113-efebffc62d96",
  "teaches": "Using the Windows Terminal",
  "depends_on": [],
  "author": "Stephan Bökelmann",
  "first_used": "2025-03-30",
  "keywords": ["CMD", "Windows", "basics"]
}
--->

# Using the Windows Terminal

## 1) Introduction
Today most people are used to work with _graphical user interfaces_ (GUIs) on their computers.
Using the terminal is a fundamental task, that can make a developers life easier. 
While GUIs provide opportunities in terms of explorability of programs, finding new functions and playing around - terminal interfaces can help understanding the exact calls that are being made to a machine.
In addition, workflows in a terminal are usually easier to reproduce, since the only input you need can be written down explicitly.
Rather than trying to explain to someone where exactly a button is located on the screen, which also may vary from version to version and resolution to resolution, a simple line of text is enough to run a specific command. 

---

The terminal is actually called a terminal-emulator, since its purpose is to mimic the older terminal stations.
One of these terminal stations is the [Teletype 33](https://en.wikipedia.org/wiki/Teletype_Model_33).
Being one of the first devices to empoly the _ASCII_ standard encoding, published in 1963, and coming at a relatively low price, $1,000 (in 1963 USD), it quickly turned into the standard input/output for the upcoming minicomputer.

<details>
  <summary>Teletype</summary>

  Want to learn more about the Teletype? Check out [this TTY exercise.](www.github.com/STEMgraph/missing)

</details>

---

Imagine a computer to be more of a general purpose calculator in the beginning of computing. 
Over a terminal, two numbers are punched in, the `Enter`-key is pressed, the computer maps the two inputs onto an output and sends the series of pulses of the result back to the terminal. 


### 1.1) Further Readings and Other Sources
- [Command Line Commands – CLI Tutorial](https://www.freecodecamp.org/news/command-line-commands-cli-tutorial)
- Moeller. [The Windows Command Line Beginner's Guide - Second Edition](https://www.amazon.de/-/en/Windows-Command-Line-Beginners-Guide/dp/1091574022)
- Video: [Windows Command Line Tutorial - 1 - Introduction to the Command Prompt](https://www.youtube.com/watch?v=MBBWVgE0ewk)

## 2) Tasks
1. **Open your Terminal**: Press `Win + r` on your keyboard. This opens the `Run` dialog. Type `cmd` and press the `Return`-key. A black window opens. This is the Windows _Command Line Interface_ (CLI), which grants you text based control over your operating systems' functions
2. **Defining a Variable**: Type `set num=5` into the black window and press `Return` or `Enter`. The computer will accept your command, store the connection between `num` and the value `5` in RAM. When it is done doing so it will tell you it's ready for the next command by _prompting_ you with a few characters at the beginning of the next line.
3. **Print a Variables' Content**: Type `echo %num%` into the CLI. This command will make the operating system search for the stored content of the variable `num` and print it to the terminal.
4. **Pay Attention**: Type `echo num` into the CLI. Now the terminal will only print the character-sequence `num`. Make sure, to use the `%...%` notation when accessing a variable with the `echo` command.
5. **Calculate a Sum**: Use the `set` command again, but now to calculate an output: `set /a num + 3`. The computer answers with the result of the calculation. 
6. **Try out other Calculations**: The `/a` indicates, that the user wants the computer to behave _arithmetically_. You can use this for `*`, `-`, `/` (and `%`) as well.
7. **Setting a Result Variable**: Run `set /a res = num + 5`, and `set /a res2 = num + res`. This way, you can store results in variables.
8. **Test a Condition**: Your computer can also check conditions. Type `if %res%==10 echo Great!`. 
9. **Repeat an Operation**: Run `for /l %i in (5,1,10) do echo %i`. Vary the three numbers within the parenthesis and figure out what their purpose is.
10. **Persistence**: Close the CMD and run task 1 again. Execute the command `echo %num%`. 
11. **Puzzle**: Initialize a variable called `Gauss` with a value of `0`. Write one line, that uses `for /l`, `set /a` and `Gauss = Gauss + ` to calculate the sum of all integer numbers from `1` to `100` with a single line of CMD.

## 3) Questions
1. What advantages does using the terminal offer compared to graphical user interfaces?
2. How can terminal commands improve reproducibility in software development?
3. Why can it be important to understand basic terminal operations, even when working mostly in GUI environments?
4. In what ways does using a terminal strengthen your understanding of how an operating system works?
5. Why might automation be easier with terminal tools than with graphical interfaces?
6. How can learning the terminal help you troubleshoot problems more effectively on your computer?

## 4) Advice
Don’t be intimidated by the black screen—every expert once started with a simple `echo Hello`. The command line is a powerful tool that rewards curiosity and experimentation. Get used to reading error messages, exploring built-in help (`command /?`), and breaking things safely. As you grow more comfortable, you'll find the terminal not only speeds up your work but deepens your understanding of how computers really operate. One command at a time, you’re becoming fluent in the native language of machines.

> “Controlling complexity is the essence of computer programming.”  
> — *Brian W. Kernighan*

<details>
  <summary>Linux</summary>

  Checkout the [Linux BASH](https://github.com/STEMgraph/8d3e51c2-4811-4275-976c-04e3b3215998) exercise as well to see the differences and similarities!

</details>
