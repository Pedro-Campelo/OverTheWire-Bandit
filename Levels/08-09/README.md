# Bandit Level 8-9

## How to login to the level
Connect to this level by using:

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
VR1ljMayciFxbnUokuQmJFw6QC9VKtub
```

## Objective
Find the password which is stored in the file data.txt and is the only line of text that occurs only once

## Background Research
I searched up how to sort a text 

## My Approach
OverTheWire provided me with the information:
- The password is stored in the `data.txt` file next to the word `millionth`

Using this information I ran the command:
```bash
grep "millionth" data.txt
```
The command searched `data.txt` for the word `millionth` and printed the line containing it. 
The password appeared immediately after the word, allowing me to log into the next level.

## Command Breakdown

```bash
grep "millionth" data.txt
```

`grep` - Command used to search for specific words, phrases, or patterns inside text files
`millionth` - The word I'm looking for
`data.txt` - The file the word is in

## Screenshot of my work
<img width="745" height="55" alt="image" src="https://github.com/user-attachments/assets/96ed6f90-05e6-43b5-9aba-b4e1b0173e2f" />

## Challenges I faced
- The challenge was fairly straightforward after I discovered what the grep command is and how to use it

## What I Learned
- The `grep` command can search files for specific words, phrases, or patterns inside text files.

## Key Takeaways
- Learning the right command can save a huge amount of time.
- `grep` is an essential Linux tool for searching text.

## How to login to next level
Once you've retrieved the password, connect to the next level using:

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 7-8](../07-08/README.md)

➡️ [Next: Level 9-10](../09-10/README.md)
