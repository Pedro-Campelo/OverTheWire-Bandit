# Bandit Level 3-4

## How to login to the level
Connect to this level by using:

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
```

## Objective
Enter the directory called `inhere`, then read the hidden file for the password. Then log into the next level using that password and continue the game.

## Background Research
I researched how to enter a directory and how to list hidden content in a directory.
To enter a directory you have to use:
```bash
cd directory-name
```
And to list all files and folders in a directory including hidden ones you have to use:
```bash
ls -a
```

## My Approach
OverTheWire provided me with the information:
- The password is in a hidden file
- The hidden file is stored in a directory called `inhere`

Firstly, I used the `ls` command to list all the contents of the directory Im in. I saw the `inhere` directory OverTheWire mentioned and entered that directory using the command:
```bash
cd inhere
```
Then I ran the command `ls` but the hidden file wasn't listed since `ls` by default doesn't show hidden files
```bash
ls -a
```
Which listed 2 directorys and one file called `...Hiding-From-You`
I then identified that the file that contains the password must be the file called `...Hiding-From-You` so I ran the command:
```bash
cat ...Hiding-From-You
```

## Command Breakdown
```bash
cd inhere
```
- `cd` - Change Directory
- `inhere` - The name of the directory I want to change into

```bash
ls -a
```
- `ls` - List all content in directory
- `-a` - Tells `ls` to also list hidden items

```bash
cat ...Hiding-From-You
```
- `cat` - Reads the file
- `...Hiding-From-You` - The file name

## Screenshot of my work
<img width="417" height="147" alt="image" src="https://github.com/user-attachments/assets/c8baa9e3-726d-4e0c-8c08-4f677fad8a83" />

## Challenges I faced
This level didn't present any major challenges after I learnt how to change directory and list hidden files

## What I Learned
- `-a` when paired with `ls` lists all files including hidden ones
- `cd` changes your directory

## Key Takeaways
- Files can sometimes be hidden
- Always consider using `ls -a` if you can't find the file you're looking for

## How to login to next level
Once you've retrieved the password, connect to the next level using:

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 2-3](../Level2-3/README.md)

➡️ [Next: Level 4-5](../Level4-5/README.md)
