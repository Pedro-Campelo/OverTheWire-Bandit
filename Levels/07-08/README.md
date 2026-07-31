# Bandit Level 7-8

## How to login to the level
Connect to this level by using:

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3
```

## Objective
Find the password which is stored in the `data.txt` file next to the word `millionth`

## Background Research
I searched up how to find a specific word in a `.txt` file in linux and discovered the `grep` command.
This command is used to search for specific words, phrases or patterns inside text files.

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
<img width="652" height="66" alt="image" src="https://github.com/user-attachments/assets/96ca3e27-c26a-4b5f-84c5-91e5ab6b3d37" />

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
ssh bandit8@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
VR1ljMayciFxbnUokuQmJFw6QC9VKtub
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 6-7](../06-07/README.md)

➡️ [Next: Level 8-9](../08-09/README.md)
