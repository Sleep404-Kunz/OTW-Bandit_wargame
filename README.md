# OTW-Bandit_wargame
Over The Wire CTF (Bandit)

Description: Bandit wargame for benginners offerd by OverTheWire. This machine is meant to teach new beginners about the commands and how to use the commands. This machine has 35 levels (0-34)

<img src = "https://github.com/user-attachments/assets/7ecc2def-4b9d-42f0-8656-ad3bfc802a01" width = "400">


## Level 0
Use of SSH to remotely connect to the Bandit machine.

```ssh bandit0@bandit.labs.overthewire.org -p 2220```
```ls```
```cat readme```

The machine uses port 2220 which has to be specified with the _-p_ option as show above. 

<img src = "https://github.com/user-attachments/assets/ecd51139-c2ce-416c-8e9f-87c984643887" width = "250">

After logging into the machine, I have to obtain the password for the next level in the file called **readme**.

```ls```
```cat readme```

<img src = "https://github.com/user-attachments/assets/74fb23ae-e587-4f7a-8703-e5918078ff17" width = "400">

This password is to be used to log into the next level **bandit1** on the machine.

## Level 1

In this level I have to find the password in a file named "-" in the home directory. Interacting with the dashed filename presents some obstacles because the dash "-" is generally used by commands to specify options and arguments. 

To open and read the content of the dashed file I need to specify the option "<" or "./" before the filename. 

```cat < -``` 
```cat ./-```

<img src = "https://github.com/user-attachments/assets/43bfdc24-c401-4eb3-9d25-3493b4d21148" width = "300">

## Level 2

This level requires me to find the password in a file called "spaces in this filename" in the home directory. The spaces in the filename can be interpreted as separtor for arguments and hence is generally avoided or substituted with an alternative character like "_"

The entire filename can be wrapped in quotes or backslash key can be used before the spaces. 

```cat "spaces in this filename"``` 
```cat spaces\ in\ this\ filename```

<img src = "https://github.com/user-attachments/assets/955b5f69-3a70-48dc-bf73-0a5ccdd9b253" widht = "50">

## Level 3 

The password in this level is stored in the "inhere" directory. The file is hidden and is not shown when the basic "ls" command is used. 

The hidden files and directories can be revealed using the "-a" option with the ls command. 

<img src = "https://github.com/user-attachments/assets/6e9f1410-36dc-415d-9e15-7b596bffcca2" width = "300">

## Level 4

The password in this level is stored in the only human-readable file in the inhere directory. The directory has multiple files and all of them needs to be checked if the contents are in human readable format. 

The "file" command with the "-i" argument is used to identify the file MIME type. MIME is a standard that indicates the format of a file. 

<img src = "https://github.com/user-attachments/assets/4b9c4837-fe4a-428d-bd1e-7a5642a13540" width = "500">

## Level 5 

The password in this level is stored in a file in the "inhere" directory and has the following properties. 
- human-readable
- 1033 bytes in size
- not executable

The properties of the file can be verified with the find command and the arguments "size","-executable"

<img src = "https://github.com/user-attachments/assets/de08ad43-e94b-4ec3-8345-b236b73ef753" width = "500">

## Level 6

The password in this level is stored on the machine and has the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

This is an advanced version of the previous task. I need to find by user, group and size. I can use the find command with the "user", "group", and "size" arguments. I will start the find command recursively from the root directory "/".

```find / -user bandit7 -group bandit6 -size 33c```

The command above shows multiple files that have permission restrictions. To filter out the results with permission restrictions, the errors can be redirected from the output on the terminal to "/dev/null" folder. "2>/dev/null" needs to be appended to the command as follows.

```find / -user bandit7 -group bandit6 -size 33c 2>/dev/null ```

<img src = "https://github.com/user-attachments/assets/e403b566-db55-4bd2-8960-1610bb5fe1e4" width = "500">

## Level 7

Password for this level is stored in the file data.txt next to the word "millionth". 

I can pipe the output from the cat command into the grep command to output the line that has the word "millionth"

```cat data.txt | grep millionth```

<img src = "https://github.com/user-attachments/assets/58eb4988-f660-47a0-936f-e5f1ab14a5f2" width = "500">

## Level 8

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once. 

The file contains multiple passwords occuring more than once and the correct password occuring only once. I can use the "sort" command to group together the duplicate passwords. I can then pipe the output to the "uniq -u" to print only the unique lines without duplicates. 

```sort data.txt | uniq -u```

<img src = "https://github.com/user-attachments/assets/7539f591-52ae-47bb-86b9-39a785da758d" width = "500">

_**Password : 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM**_

## Level 9 (In progress :construction:)

The password for in this level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

<img src = "" width = "">

_**Password  : **_

## Level

<img src = "" width = "">

_**Password  : **_

## Level

<img src = "" width = "">

_**Password  : **_

## Level

<img src = "" width = "">

_**Password  : **_

## Level

<img src = "" width = "">

_**Password  : **_











