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
We tried to use the command on the file, "en-us.txt" but were given an error because cd only lets us switch terminals. You can't do this with files. I switched the messages directory because it was a directory to have files to test the command with.

## The ls Command
(given no argument)
```
[user@sahara ~]$ ls
lecture1  messages

```
By giving no input for the ls command, it shows us the folders in the current directory we're in. In "home", we have two folders which are lecture1 and messages.

(given directory path as argument)
```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  lecture1  messages  README

```
This shows lecture1 being an input for the ls command. The markdown shows how within the lecture1 folder, there exist five files in the folder. 

(given a file path as an argument)
```
[user@sahara ~/lecture1/messages]$ ls af.txt
af.txt

```
using the ls command on the file doesn't produce an error, but it doesn't provide much important info since the only thing within a file is the file itself.

## The cat command

(given no argument)
```
[user@sahara ~/lecture1]$ cat

```
I'm currently in the lecture1 directory, but it wouldn't matter anyways because there's nothing for the command to print.

(given directory path as argument)
```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory

```
You can't print stuff if it's a directory, since folders aren't files.

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
We switched to the lecture1 directory because it had the Hello.java file. using cat on a file simply prints its contents.

