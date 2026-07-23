# Bandit Level 2-3

## How to login to the level
Connect to this level by using:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```

## Objective
Find the file called `--spaces in this filename--` in the home directory and read it's contents for the password. Then log into the next level using that password and continue the game.

## Background Research
I didn't do any background research before starting this level because I learnt how to read text files in the level before

## My Approach
OverTheWire provided me with the information:
- The password is in a file called `--spaces in this filename--`
- The `--spaces in this filename--` file is located in the home directory

Firstly, I used the `ls` command to list all the contents of the directory Im in. I saw the `--spaces in this filename--` file OverTheWire mentioned and because the filename contained spaces 
I encased the filename in quotation marks and therefore ran the command:

```bash
cat ./"--spaces in this filename--"
```
`./` isn't required in this level because the filename doesn't start with `-`, but I used it anyway because it explicitly tells the command to look in the home directory
Which successfully gave me the password for this level.

## Command Breakdown
```bash
cat ./"--spaces in this filename--"
```
- `cat` - Reads the file
- `.` - Means current directory
- `/` - Seperator
- `""` - Specifies that everything in the quotation marks is one filename
- `--spaces in this filename--` - The file name

## Screenshot of my work
<img width="444" height="78" alt="image" src="https://github.com/user-attachments/assets/a20b02b1-1718-4d3e-b414-9005e6a450f4" />

## Challenges I faced
This level didn't present any major challenges because I already understood how to use `cat` from the previous levels
The only new concept was learning how quotation marks allow filenames containing spaces to be treated as a single argument

## What I Learned
- Quotation marks allow filenames containing spaces to be treated as a single argument
- Linux splits command-line arguments on spaces unless they are quoted
- Using quotation marks prevents the shell from interpreting each word as a separate filename

## Key Takeaways
- Filenames containing spaces must be quoted.
- Understanding how the shell parses commands helps avoid common mistakes.

## How to login to next level
Once you've retrieved the password, connect to the next level using:

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 1-2](../Level1-2/README.md)

➡️ [Next: Level 3-4](../Level3-4/README.md)
