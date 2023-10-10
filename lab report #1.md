# Lab Report #1
I'll showcase three filesystem commands we learned in our first lab for this report. The three commands are **cd**, **ls**, **cat** and I'll also show examples of using each command with no arguments, a path to a directory as an argument, and a path to a file as an argument.

## The cd Command
(given no argument)
```
[user@sahara ~]$ cd
[user@sahara ~]$ pwd
/home

```
By giving no input for the cd command, it moves us back the the main directory, which is /home.

(given directory path as argument)
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ pwd
/home/lecture1

```
This shows lecture1 being an input for the command, and the 2nd line shows we're in the lecture1 directory.

(given a file path as an argument)
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ cd en-us.txt
bash: cd: en-us.txt: Not a directory

```
We tried to use the command on the file, "en-us.txt" but were given an error because cd only lets us switch terminals. You can't do this with files.
