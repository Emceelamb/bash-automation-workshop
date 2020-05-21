# Automating Mindfully

>  Mindfulness is the basic human ability to be fully present, aware of where we are and what we’re doing, and not overly reactive or overwhelmed by what’s going on around us.

In the hyper-computerized world we are spending more and more time in front of the computer and have less time to reflect on our technologically mediated actions. Many disconnectionists and Luddites propose spending more time away from the screen in a digital detox. As technologists we can decrease our screentime increasing our productivity by automating our computing tasks. In doing so we reduce our mental workload in order to be more present aware of our tasks at hand.

Through learning skills in automating tasks we will learn more about how computers operate at a low level, while becoming more comfortable working in a textual interface.  By developing scripts to automate repetitive tasks you'll learn to think more algorithmically about computing  and free yourself to be more present and less hindered by act of computing.
> Automation is the technology by which a process or procedure is performed with minimal human assistance. - Wikipedia

*Knowledge of CLI is not required but it would be helpful when creating tasks*

*This tutorial focuses on the Bash scripting language but the concepts can be applied to any scripting language.*

[Presentation slides](https://docs.google.com/presentation/d/1CA3az15TlhXbYIWF7MYpe-86yN7IhVPKrrSmYkAq8O0/edit?usp=sharing "Google Slides")

[Workshop feedback form](https://forms.gle/ah98V5dmRq6JVsGk7 "Google form")

## Technical Learning Outcomes
- Consider mindfulness and its relation to computing
- Discuss use cases for automation
- Learn how to break down tasks into sequential steps
- Learn Bash Scripting fundamentals
- Create an executable Bash script
- Learn the difference between the Terminal, Command Line, Shell 

## Workshop Schedule
- Breathing Exercise
- Introduction
- Discussion on mindfulness, technology, and automation
- Presentation
- Guided scripting exercises
- Make your own welcome screen
- Wrap up

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

The Shell or Shell interpreter is the program that takes command line instructions in the terminal and sends it to the terminal. Bash or Bourne Again SHell is a Unix shell and command language for the GNU project. It is one of the most popular default shells, but there are other shell variants out there you may be interested in such as: Zsh, DASH, PowerShell, etc.

[Read more about the differences](https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)

### Your First Bash Script
1. In your terminal navigate to your home directory: `cd ~`
2. Create a folder for your scripts titled `bin`: `mkdir bin`
3. Navigate to the newly created folder: `cd bin`
4. Create a file and name it 'hello-world': `touch hello-world`
5. Open the newly created file in a text editor
6. On the First line enter the shebang line: `#!/usr/bin/env bash`
7. On the following line type in: `echo Hello World`
8. Close and save the file
9. Mark the script file as executable: `sudo chmod +x hello-world`
10. Execute the script with: `./hello-world`

The script script should look like:
```bash
# hello-world

#!/usr/bin/env bash

echo Hello World
```

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
#!/usr/bin/env bash 
#Shebang tells shell interpreter what environment to use

# This is a comment

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
- [In depth Bash scripting tutorial](https://ryanstutorials.net/bash-scripting-tutorial/bash-loops.php#introduction)
