# basic linux commands tutorial
In this section, you will learn:
What is this commands? Why do you do it? How do you do it?

Fluency on the command line is a skill often neglected or considered arcane, but it improves your flexibility and productivity as an engineer in both obvious and subtle ways. This is a selection of notes and tips on using the command-line that we've found useful when working on Linux. Some tips are elementary, and some are fairly specific, sophisticated, or obscure. This page is not long, but if you can use and recall all the items here, you know a lot.

* [pwd](#pwd)
* [Home directory and ~(#Home directory and ~)](#Home directory and ~)
* [ls](#ls)
* [cd](#cd)
* [mkdir](#mkdir)
* [cp](#cp)
* [mv](#mv)
* [rm](#rm)
* [history](#history)
* [Using the tab key to complete file paths](#Using the tab key to complete file paths)
* [Using up and down arrow for history](#Using up and down arrow for history)

## pwd
The pwd tool prints the name of the present/current working directory (PWD - Present Working Directory). Following is its syntax:

![Image of pwd](/images/pwd.png)

You can see currently where we are. 

**(base)** is a python virtual environment, you don't have to know it for now.

**dujiaxin** is my user name.

**dujiaxin-ThinkPad-T450** is my computer's name, and yes it's long. The *@* connects username with host name, so it looks like 'username@hostname'

What prints here is also my home directory.

## Home directory and ~
A home directory, also called a login directory, is the directory on Unix-like operating systems that serves as the repository for a user's personal files, directories and programs. It is also the directory that a user is first in after logging into the system.

A home directory is created automatically for every ordinary user in the directory called /home. A standard subdirectory of the root directory, /home has the sole purpose of containing users' home directories. The root directory, which is designated by a forward slash ( / ), is the directory that contains all other directories and their subdirectories as well as all files on the system. For more definition, check [this link](#http://www.linfo.org/home_directory.html)

## ls

`ls`shows what is inside current directory. You can learn what every column in `ls -l` means.

![Image of ls](/images/ls.png)

## cd
`cd` stands for *"change directory"*, it can bring you to anywhere you want in your computer that you can access.

![Image of cd](/images/cd.png)

- Go to your home directory with `cd`. Access files relative to your home directory with the `~` prefix (e.g. `~/.bashrc`). In `sh` scripts refer to the home directory as `$HOME`.

- To go back to the previous working directory: `cd -`.

- To go out of current directory: `cd ..`.

![Image of 2dot](/images/2dot.png)

## mkdir

`mkdir` make a directory. *here I make a directory called images*

![Image of mkdir](/images/mkdir.png)

## cp

`cp` is copy. *I copied all files from home/Pictures to images directory*

![Image of cp](/images/cp.png)

- `*` is file glob expansion with (and perhaps `?` and `[`...`]`) and quoting and the difference between double `"` and single `'` quotes. (See more on variable expansion below.)

## mv

move something. It's like **ctrl-x** with **ctrl-p**
`mv origin destination`

## rm

remove document 

![Image of rm](/images/rm.png)

## Using the tab key to complete file paths
In Bash, use **Tab** to complete arguments or list all available commands and **ctrl-r** to search through command history (after pressing, type to search, press **ctrl-r** repeatedly to cycle through more matches, press **Enter** to execute the found command, or hit the right arrow to put the result in the current line to allow editing).

## history
To see recent commands, use `history`. Follow with `!n` (where `n` is the command number) to execute again. There are also many abbreviations you can use, the most useful probably being `!$` for last argument and `!!` for last command (see "HISTORY EXPANSION" in the man page). However, these are often easily replaced with **ctrl-r** and **alt-.**.

![Image of history](/images/history.png)

![Image of history2](/images/history2.png)

## other useful tips

- use `touch` to create a empty file

![Image of touch](/images/touch.png)

- If you are halfway through typing a command but change your mind, hit **alt-#** to add a `#` at the beginning and enter it as a comment (or use **ctrl-a**, **#**, **enter**). You can then return to it later via command history.

- Learn basic Bash. Actually, type `man bash` and at least skim the whole thing; it's pretty easy to follow and not that long. Alternate shells can be nice, but Bash is powerful and always available (learning *only* zsh, fish, etc., while tempting on your own laptop, restricts you in many situations, such as using existing servers).

- Finding documentation:
  - Know how to read official documentation with `man` (for the inquisitive, `man man` lists the section numbers, e.g. 1 is "regular" commands, 5 is files/conventions, and 8 are for administration). Find man pages with `apropos`.
  - Know that some commands are not executables, but Bash builtins, and that you can get help on them with `help` and `help -d`. You can find out whether a command is an executable, shell builtin or an alias by using `type command`.
  - `curl cheat.sh/command` will give a brief "cheat sheet" with common examples of how to use a shell command.

- Learn about redirection of output and input using `>` and `<` and pipes using `|`. Know `>` overwrites the output file and `>>` appends. Learn about stdout and stderr.