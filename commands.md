# basic linux commands tutorial
In this section, you will learn:
What is this commands? Why do you do it? How do you do it?


![curl -s 'https://raw.githubusercontent.com/jlevy/the-art-of-command-line/master/README.md' | egrep -o '`\w+`' | tr -d '`' | cowsay -W50](cowsay.png)

Fluency on the command line is a skill often neglected or considered arcane, but it improves your flexibility and productivity as an engineer in both obvious and subtle ways. This is a selection of notes and tips on using the command-line that we've found useful when working on Linux. Some tips are elementary, and some are fairly specific, sophisticated, or obscure. This page is not long, but if you can use and recall all the items here, you know a lot.


* [cd](#cd)
* [mkdir](#mkdir)
* [cp](#cp)
* [pwd](#pwd)
* [mv](#mv)
* [rm](#rm)
* [history](#history)
* [Home directory and ~(#Home directory and ~)](#Home directory and ~)
* file paths in linux
* Using the tab key to complete file paths(#Using the tab key to complete file paths)
* Using up and down arrow for history(#Using up and down arrow for history)

## pwd
The pwd tool prints the name of the present/current working directory (PWD - Present Working Directory). Following is its syntax:
![Image of pwd](/images/pwd.png)
You can see currently where we are. 
*(base)* is a python virtual environment, you don't have to know it for now.
*dujiaxin* is my user name.
*dujiaxin-ThinkPad-T450* is my computer's name, and yes it's long. The *@* connects username with host name, so it looks like 'username@hostname'
What prints here is also my home directory.

## Home directory and ~
A home directory, also called a login directory, is the directory on Unix-like operating systems that serves as the repository for a user's personal files, directories and programs. It is also the directory that a user is first in after logging into the system.
A home directory is created automatically for every ordinary user in the directory called /home. A standard subdirectory of the root directory, /home has the sole purpose of containing users' home directories. The root directory, which is designated by a forward slash ( / ), is the directory that contains all other directories and their subdirectories as well as all files on the system. For more definition, check [this link](#http://www.linfo.org/home_directory.html)

## cd
*cd* stands for *"change directory"*, it can bring you to anywhere you want in your computer that you can access.
![Image of cd](/images/cd.png)

- Go to your home directory with `cd`. Access files relative to your home directory with the `~` prefix (e.g. `~/.bashrc`). In `sh` scripts refer to the home directory as `$HOME`.

- To go back to the previous working directory: `cd -`.

## mkdir
mkdir make a directory
![Image of pwd](/images/mkdir.png)

## cp
copy
![Image of cp](/images/cp.png)

## mv
move something
![Image of mv](/images/mv.png)

## rm
remove
![Image of rm](/images/rm.png)

## Using the tab key to complete file paths
In Bash, use **Tab** to complete arguments or list all available commands and **ctrl-r** to search through command history (after pressing, type to search, press **ctrl-r** repeatedly to cycle through more matches, press **Enter** to execute the found command, or hit the right arrow to put the result in the current line to allow editing).

## history
To see recent commands, use `history`. Follow with `!n` (where `n` is the command number) to execute again. There are also many abbreviations you can use, the most useful probably being `!$` for last argument and `!!` for last command (see "HISTORY EXPANSION" in the man page). However, these are often easily replaced with **ctrl-r** and **alt-.**.