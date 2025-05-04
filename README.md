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

_**Password : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If**_

This password is to be used to log into the next level **bandit1** on the machine.

## Level 1

In this level I have to find the password in a file named "-" in the home directory. Interacting with the dashed filename presents some obstacles because the dash "-" is generally used by commands to specify options and arguments. 

To open and read the content of the dashed file I need to specify the option "<" or "./" before the filename. 

```cat < -``` 
```cat ./-```

<img src = "https://github.com/user-attachments/assets/3d38f8fa-cc19-49ce-b1bd-32c68c4f9e02" width = "300">

_**Password : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx**_

## Level 2

This level requires me to find the password in a file called "spaces in this filename" in the home directory. The spaces in the filename can be interpreted as separtor for arguments and hence is generally avoided or substituted with an alternative character like "_"

The entire filename can be wrapped in quotes or backslash key can be used before the spaces. 

```cat "spaces in this filename"``` 
```cat spaces\ in\ this\ filename```

<img src = "https://github.com/user-attachments/assets/b828c880-ba83-43f1-a2d3-21165731e050" widht = "100">

_**Password : MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx**_

## Level 3 

The password in this level is stored in the "inhere" directory. The file is hidden and is not shown when the basic "ls" command is used. 

The hidden files and directories can be revealed using the "-a" option with the ls command. 

<img src = "https://github.com/user-attachments/assets/34fa015e-230f-4df0-812d-de349475d90b" width = "300">

_**Password :2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ**_

## Level 4

The password in this level is stored in the only human-readable file in the inhere directory. The directory has multiple files and all of them needs to be checked if the contents are in human readable format. 

The "file" command with the "-i" argument is used to identify the file MIME type. MIME is a standard that indicates the format of a file. 

<img src = "https://github.com/user-attachments/assets/603498ec-4287-4ea4-9193-a5d28bcfb4de" width = "500">

_**Password :4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw**_


## Level 5 

The password in this level is stored in a file in the "inhere" directory and has the following properties. 
- human-readable
- 1033 bytes in size
- not executable

The properties of the file can be verified with the find command and the arguments "size","-executable"

<img src = "https://github.com/user-attachments/assets/8b47c1a7-e573-40b0-b9e7-2031e313f7a6" width = "500">

_**Password :HWasnPhtq9AVKe0dmk45nxy20cvUa6EG**_

## Level 6

The password in this level is stored on the machine and has the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

This is an advanced version of the previous task. I need to find by user, group and size. 

<img src = "" width = "">

_**Password : **_

## Level

<img src = "" width = "">

_**Password : **_

## Level

<img src = "" width = "">

_**Password : **_

## Level


## Level


## Level


## Level


## Level












