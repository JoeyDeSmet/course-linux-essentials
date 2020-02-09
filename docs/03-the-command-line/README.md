---
description: Learn basics of the command line
title: 03 - The Command Line
---

# Chapter 03 - The Command Line

<!-- TODO - Needs a nice intro -->

## The CLI

<!-- TODO: Refactor -->

As most people use an OS with a graphical user interface (GUI) for their day-to-day computer needs, the use of the CLI is a necessity for most Linux server users.

* A CLI (Command Line Interface) provides
  * more precise control
  * greater speed
  * and the ability to easily automate tasks through scripting
* Although Linux does have many GUI environments, you will be able to control Linux much more effectively by using the CLI.

## The Terminal

In the olden days, when computers were room-sized multi-user computer systems owned by companies and universities, the machines are placed inside secured rooms that were inaccessible by normal users. These normal users could however **interact with the system remotely using a terminal**, which used to be a printer for output, called a TeleTYpewriter (TTY), and a punch card system for input.

![Punch Cards - Source: http://www.computinghistory.org.uk/big/3415/ICL-Hand-Key-Punch-Card-Machine](./img/punchcard.jpg)

Later the terminal evolved to a display and keyboard which could be used to interact with the computer.

![A Display and Keyboard Terminal - Source: https://imgur.com/gallery/sTb5g/comment/715038647](./img/terminal.jpg)

These days the terminal is nothing but a software application that emulates the old physical terminals. That's why the actual correct name of this application is **terminal emulator**, but most people will talk about the terminal.

This terminal application, provides an interface that allows interaction with the user. It can read commands from the user and it can output text to the screen. The terminal application is however a very basic program that can provide the CLI but does not actually do anything more. The application that actually executes the commands from the user is called the **shell**.

So in short, the terminal emulator is an application accepts what the user types and passes to a shell. THe output from the shell is then redirected back to the terminal and displayed to the user.

Some free and commonly-used terminal emulators are:

* Putty for Windows
* Terminal and iTerm 2 for Mac OS X
* Terminal, KDE Konsole, XTerm and Terminator for Linux

## The Shell

The shell is an application that **interprets** the commands coming from the user (this can be from the terminal or from a shell script) and translates them into instructions that can be executed by the operating system.

If output is produced by the command, then this output is redirected back to the terminal and displayed for the user. If problems with the command are encountered, then an error message is displayed instead.

For example, when you type `ls` into a terminal, you are asking the shell to run the `ls` program and to print out a list of files in the current directory to your terminal.

A shell also acts as a scripting environment making it easier for the user to automate tasks using shell scripts. Below is a simple example of a bash script that output the message "Hello World from Bash" to the terminal.

```bash
#!/usr/bin/env bash

echo "Hello World from Bash"
```

### Different shells

There are quitte a lot of different shells available. Each shell has its own feature set and intricacies, regarding how commands are interpreted, but they all feature input and output redirection, variables, and condition-testing, among other things.

Each shell basically does the same job, but each understands different command syntax and provides different built-in functions.

#### The sh shell

Most shells derive their features from the original Unix shell program **sh** - **The Bourne Shell**. It was written by **Stephen Richard "Steve" Bourne** at AT&T Bell Labs in 1977 and since then it has been shipped with most earlier Unix systems.

![Steven Bourne](./img/steven_bourne.jpg)

Sh set the bar for many popular future shells with features like redirection, scripting abilities, and robust language constructs.

::: tip .sh extension
The Bourne Shell requires users to use the `.sh` extension for their scripts. However, often linux users will do the same for scripts for other shells. This is a bad habit as most scripts these days are not `sh`-compatible scripts.
:::

#### The Bash shell

On most Linux systems (standard Linux distribution such as Ubuntu or Arch) a program called **bash** (an open source shell which stands for **Bourne Again SHell**, an enhanced version of the original `sh`) acts as the default shell program.

This open source Linux shell is well-known in the community for its robust feature set and usability. Most Linux users thus run Bash at one point or another in their life.

![Bourne Again Shell shell](./img/bash.png)

Some excellent features of bash are

* unlimited command history
* aliases
* Unicode support
* auto-completion support for command names, paths, wildcards
* allows colored directory listings alongside text highlighting

#### The Korn shell

The **Korn Shell** (ksh) is probable one of the most popular open source shells for Linux at this time. It was developed by **David Korn** at Bell Labs. It combines the interactivity of the C shell and productivity of the Bash shell. The Korn Shell has always been popular because of its ahead-of-time features which include advance job control, command aliasing, floating-point arithmetic alongside many others.

Some import features:

* it allows users to terminate current jobs using `CTRL + Z` and put them either in the foreground or background using the commands `fg` and `bg`.
* it allows the shell code to be put directly in memory which allows increasing programming ability and efficient performances.
* Advanced command-line editing, adopted from popular editors such as vi and Emacs.
* Korn shell scripts are often faster than Bourne shell scripts and offer advanced I/O features alongside notable security mechanisms.

#### Zsh shell

The **Z shell** (Zsh) is an innovative, modern-day Linux shell that can be used as an interactive login shell and as a command interpreter for shell scripting. Zsh is an extended Bourne shell with many improvements, including features from other popular shells. Zsh is known for its performance, which improves upon many open source shells for Linux. Try Zsh if you’re Linux guru looking for advanced Linux shells.

![Zsh shell](./img/zsh.png)

Some key features of zsh are:

* very intelligent auto-completion functionality
* history sharing mechanism over different terminal windows running at the same time
* over 400 plugins and 200 plus themes from its popular, community-driven framework oh-my-zsh
* spelling correction

#### The Fish Shell

Fish is a smart and user-friendly command line shell for Linux, macOS, Windows and the rest of the family. It aims to be a modern-day replacement of the early open source shells for Linux. Fish offers a rich set of powerful features which makes it easier to discover, remember, and use exciting Linux commands on your machine. If you’re looking for a smart command-line shell for your Linux desktop, Fish is certainly worth a try.

Some cool features of Fish:

* Autosuggestions
* Sane Scripting
* Man Page Completions
* Glorious VGA Color
* Web Based configuration
* Works Out Of The Box

## Some Good Videos

<iframe width="560" height="315" src="https://www.youtube.com/embed/hMSByvFHOro" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>