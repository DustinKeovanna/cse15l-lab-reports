# Lab Report #1
I'll showcase three filesystem commands we learned in our first lab for this report. The three commands are **cd**, **ls**, **cat** and I'll also show examples of using each command with no arguments, a path to a directory as an argument, and a path to a file as an argument.

## The cd Command
(given no argument)
```
[user@sahara ~]$ cd
[user@sahara ~]$ pwd
/home

```
(given directory path as argument)
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ pwd
/home/lecture1

```
(given a file path as an argument)
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ cd en-us.txt
bash: cd: en-us.txt: Not a directory

```
