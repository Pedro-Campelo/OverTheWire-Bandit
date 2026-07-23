# Bandit Level 1-2

## How to login to the level
Connect to this level by using:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
```

## Objective
Find the file called `-` in the home directory and read it's contents for the password. Then log into the next level using that password and continue the game.

## Background Research
I didn't do any background research before starting this level because I learnt how to read text files in the level before

## My Approach
OverTheWire provided me with the information:
- The password is in a file called `-`
- The `-` file is located in the home directory

Firstly, I used the `ls` command to list all the contents of the directory Im in. I saw the `-` file OverTheWire mentioned and ran the command:

```bash
cat -
```

When I ran this command nothing happened so I pressed `CTRL + C` to stop the proccess and went to find out what went wrong.
I discovered that went you enter 
```bash
cat -
```
`cat` interprets `-` as standard input (stdin), not as a filename, so instead of opening a file called `-`
it waits for you to type something. So instead of writing: 
```bash
cat -
```
I wrote
```bash
cat ./-
```
Prefixing the filename with `./` explicitly tells `cat` to look for a file named `-` in the current working directory rather 
than interpreting `-` as standard input.

## Command Breakdown
```bash
cat ./-
```
- `cat` - Reads the file
- `.` - Means current directory
- `/` - Seperator
- `-` - The file name

## Screenshot of my work
<img width="552" height="176" alt="image" src="https://github.com/user-attachments/assets/d28077e6-8235-40d9-a1ca-c3a766f7e29e" />

## Challenges I faced
This level was fairly straightforward after realising I have to use the files path instead of writing just its name.

## What I Learned
- When I use `-` after a command it is treated as an option not as a filename

## Key Takeaways
- Not every filename can be accessed by simply typing its name.
- `./` tells Linux to treat `-` as a filename in the current directory.
- Understanding *why* a command fails is just as important as knowing the correct solution.

## How to login to next level
Once you've retrieved the password, connect to the next level using:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 0-1](../Level0-1/README.md)

➡️ [Next: Level 2-1](../Level2-1/README.md)
