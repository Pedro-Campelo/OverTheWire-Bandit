# Bandit Level 0

## Objective
Find the file called 'readme' in the home directory and read it's contents for the password. Then log into the next level using that password and continue the game.

## Background Research
Before attempting this level, I had never searched for or accessed a file through the terminal so i researched how to do so. And discovered the commands:
```bash
ls - Lists the contents of a directory
cat - Displays file content, combines multiple files, and create new text files directly from the terminal
```

## My Approach
OverTheWire provided me with the information:
- The password is in a file called 'readme'
- The 'readme' file is located in the home directory

So what I did was I used the 'ls' command to list all the contents of the directory I'm in. I saw the 'readme' file OverTheWire mentioned and ran the command:

```bash
cat readme
```

This command printed out the password which i used to successfully login into the next level

## Command Breakdown
```bash
bandit0@bandit:~$ ls
```
Lists content inside of the main directory

```bash
bandit0@bandit:~$ cat readme
```
Print out the content of the file 

## Screenshot of my work
<img width="673" height="206" alt="image" src="https://github.com/user-attachments/assets/58844a62-fb90-40be-9fce-281f2a4a61b4" />

## Challenges I faced


## What I Learned


## Key Takeaways


## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)
⬅️ [Previous: Level 0](../Level-0/README.md)
➡️ [Next: Level 1-2](../Level1-2/README.md)
