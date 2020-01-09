# Automating Mindfulness

>  Mindfulness is the basic human ability to be fully present, aware of where we are and what we’re doing, and not overly reactive or overwhelmed by what’s going on around us.

In the hyper-computerized  world we are spending more and more time in front of the computer with less time to reflect on our actions. Many disconnectionists and luddites propose spending more time away from the screen in a digital detoxification. As technologists we can achieve this (while increasing our productivity) by automating our computing tasks and unburden ourselves with our mental workload in order to be more present aware at our tasks at hand.

To automate our computing environment we will learn more about how computers operate at a lower level while gaining comfortability with a textual interface. If you find yourself frequently performing repetitive tasks you can take the time to write an automation script. In the process you'll learn to think more algorithmically about the tasks and free yourself to be more present while computing.

> Automation is the technology by which a process or procedure is performed with minimal human assistance. - Wikipedia

*This tutorial focuses on the Bash scripting language but the concepts can be applied to any scripting language.*

## Technical Learning Outcomes
- Consider mindfulness as a relates to computing
- Discuss use cases for automation
- Learn the difference between the Terminal, Command Line, Shell
- Learn Bash Scripting fundamental
- Create an executable Bash script

### A note to participants
This workshop will utilize Bash, one of the most prevalent shell interpreters in the world. If you are using a Unix-like computer it probably has Bash - it comes as the default shell interpreter for MacOS and most distributions of Linux. If you have a Windows OS that's OKAY! Ubuntu Terminal can be installed as a [Windows 10 App](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab) without the need to dual boot.

## What is the difference between Terminal, Command Line and Shell?

The terminal our case refers to programs called terminal emulators. These terminal emulators include: 
- Terminal.app (MacOS pre-installed terminal emulator)
- Xterm
- iTerm
- GNU Term
- SSH (Connection to another machine through terminal)
- Built-in to IDE's 

The command line refers to the textual interface. There are many  command line interface (CLI) programs that can be operated through a terminal only. These programs are typically less resource intensive than their GUI counterparts.

The Shell or Shell interpretor is the program that takes command line instructions in the terminal and sends it to the terminal. Bash or Bourne Again SHell isa Unix shell and command language for the GNU project. It is one of the most popular default shells, but there are other shell variants out there you may be interested in such as: Zsh, DASH, PowerShell, etc.

[Read more about the differences](https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)

### Configuration
- Aliases are exist for the session. You can make them permanent by adding them to you .bashrc or .bash\_aliases file
- you can add a bin folder so you can run the scripts globally

## Useful cli tools

| Useful Command Line tool  | What it does                                                       |
| ------------------------- | -------------                                                      |
| `pwd`                     | prints current path                                                |
| `cd`                      | change directory                                                   |
| `ls`                      | list directory contents                                            |
| `touch`                   | makes a file                                                       |
| `cat`                     | prints a file                                                      |
| `less`                    | shows file in a scrollable way                                     |
| `history`                 | prints bash command history                                        |
| `cp`                      | copy                                                               |
| `mv`                      | moves and/or renames a file                                        |
| `rm`                      | removes a file; the  -r flag removes a directory and its  contents |
| `help`                    | prints out help \* depends on if programmer created a help         |
| `man`                     | prints out manual for program                                      |
| `alias`                   | creates a variable of commands                                     |
| `&`                       | runs program in background                                         |
| `chmod`                   | modifies file access rights                                        |
| `exit`                    | exits bash                                                         |

## Bash Quick Tips
```bash
#!/usr/bin/env bash #Shebang tells environment to use

# Variables
NAME="MARK"
echo $NAME 
echo "$NAME"
echo "Hi ${NAME}!"

# MARK
# Mark
# Hi MARK!

# Shell execution
echo "I'm in $(pwd)"
# I'm in <current-directory>

# Conditional
string="String is declared."
if [[ -z "$string" ]]; then
  echo "String is empty"
elif [[ -n "$string" ]]; then
  echo "String is not empty"
fi
# String is not empty

# Loops
for i in {1..5}; do
    echo "Welcome $i"
done

# Welcome 1
# Welcome 2
# Welcome 3
# Welcome 4
# Welcome 5

```

### References
- [Bash Scripting Cheat Sheet](https://devhints.io/bash)
- [Terminal, Console, Shell Differences](https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)
- [How to Create and Use Bash Scripts by Tania Rascia](https://www.taniarascia.com/how-to-create-and-use-bash-scripts/)
