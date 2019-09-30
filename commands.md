# basic linux commands tutorial
In this section, you will learn:
What is this commands? Why do you do it? How do you do it?

* cd
* mkdir
* cp
* pwd(#pwd)
* mv
* rm
* history
* Home directory and ~(#Home directory and ~)
* file paths in linux
* Using the tab key to complete file paths(#Using the tab key to complete file paths)
* Using up and down arrow for history(#Using up and down arrow for history)

## pwd
The pwd tool prints the name of the present/current working directory (PWD - Present Working Directory). Following is its syntax:
![Image of pwd](/image/pwd.png)

## Home directory and ~
A home directory, also called a login directory, is the directory on Unix-like operating systems that serves as the repository for a user's personal files, directories and programs. It is also the directory that a user is first in after logging into the system.
A home directory is created automatically for every ordinary user in the directory called /home. A standard subdirectory of the root directory, /home has the sole purpose of containing users' home directories. The root directory, which is designated by a forward slash ( / ), is the directory that contains all other directories and their subdirectories as well as all files on the system.

The name of a user's home directory is by default identical to that of the user. Thus, for example, a user with a user name of mary would typically have a home directory named mary. It would have an absolute pathname of /home/mary. An absolute pathname is the location of a directory or file relative to the root directory, and it always starts with the root directory (i.e., with a forward slash).

The only user that will by default have its home directory in a different location is the root (i.e., administrative) user, whose home directory is /root. /root is another standard subdirectory of the root directory, and it should not be confused with the root directory (although it sometimes is by new users). For security purposes, even system administrators should have ordinary accounts with home directories in /home into which they routinely log in, and they should use the root account only when absolutely necessary.

There are several easy ways for a user to return to its home directory regardless of its current directory (i.e., the directory in which it is currently working in). The simplest of these is to use the cd (i.e., change directory) command without any options or arguments (i.e., input files), i.e., by merely typing the following and then pressing the ENTER key:

cd

The tilde (the wavy horizontal line character) is used to represent users' home directories on Unix-like operating systems, including users' home directories that are used to store web pages on Unix-like web servers. Thus, a user could also return to its home directory by using the tilde as an argument to cd, i.e.,

cd ~

The absolute pathname of a user's home directory is stored in that user's $HOME environmental variable. Environmental variables are a class of variables that tell the shell (i.e., the program that provides the text-only user interface for entering commands) how to behave as a user works at the command line (i.e., all-text mode). Thus a third way for a user to return to its home directory is to use $HOME as an argument to cd, i.e.,

cd $HOME

##Using the tab key to complete file paths
In Bash, use **Tab** to complete arguments or list all available commands and **ctrl-r** to search through command history (after pressing, type to search, press **ctrl-r** repeatedly to cycle through more matches, press **Enter** to execute the found command, or hit the right arrow to put the result in the current line to allow editing).