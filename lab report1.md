# Lab Report #1
I'll showcase three filesystem commands we learned in our first lab for this report. The three commands are **cd**, **ls**, **cat** and I'll also show examples of using each command with no arguments, a path to a directory as an argument, and a path to a file as an argument.

## The cd Command
(given no argument)
```
[user@sahara ~]$ cd
[user@sahara ~]$ pwd
/home

```
By giving no input for the cd command, it moves us back the the main directory, which is /home. No error occurs when given no input for using the cd command.

(given directory path as argument)
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ pwd
/home/lecture1

```
This shows lecture1 being an input for the command, and the 2nd line shows we're in the lecture1 directory. This means the working directory we're currently in is lecture1. No error occurs when given a working directory input for using the cd command.

(given a file path as an argument)
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ cd en-us.txt
bash: cd: en-us.txt: Not a directory

```
We tried to use the command on the file, "en-us.txt" but were given an error because cd only lets us switch between working directories. You can't do this with files. I switched to the messages directory because it was a directory that had files to test the command with.

## The ls Command
(given no argument)
```
[user@sahara ~]$ ls
lecture1  messages

```
By giving no input for the ls command, it shows us the folders in the current directory we're in. In "home", we have two folders which are lecture1 and messages. The current directory was home, and no error occurred.

(given directory path as argument)
```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  lecture1  messages  README

```
This shows lecture1 being an input for the ls command. The markdown shows how within the lecture1 folder, there exist five files in the folder. No error occurs and the current directory was /lecture1. 

(given a file path as an argument)
```
[user@sahara ~/lecture1/messages]$ ls af.txt
af.txt

```
using the ls command on the file doesn't produce an error, but it doesn't provide much important info since the only thing within a file is the file itself. The working directory I'm in is messages.

## The cat command

(given no argument)
```
[user@sahara ~/lecture1]$ cat

```
I'm in the lecture1 working directory, and there was no output. No error occurred because the command is still waiting for me input a file to print its contents.

(given directory path as argument)
```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory

```
An error occurred because you can't print stuff if it's a directory. Folders aren't files. My current directory was lecture1.

(given a file path as an argument)
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cat Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}
// a

```
We switched to the lecture1 working directory because it had the Hello.java file. using cat on a file simply prints its contents. No Error occured.

