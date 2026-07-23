# Bandit Level 0-1

## Objective
Find the file called 'readme' in the home directory and read it's contents for the password. Then log into the next level using that password and continue the game.

## Background Research
Before attempting this level, I had never searched for or accessed a file through the terminal so i researched how to do so. And discovered the commands:
```bash
ls
cat
```

- `ls` lists the contents of the current directory.
- `cat` displays the contents of a file in the terminal.

## My Approach
OverTheWire provided me with the information:
- The password is in a file called 'readme'
- The 'readme' file is located in the home directory

Firstly, I used the 'ls' command to list all the contents of the directory Im in. I saw the 'readme' file OverTheWire mentioned and ran the command:

```bash
cat readme
```

This command printed out the password which i used to successfully login into the next level

## Command Breakdown
```bash
bandit0@bandit:~$ ls
```
Lists all files and directories in the current working directory.

```bash
bandit0@bandit:~$ cat readme
```
Displays the contents of the `readme` file in the terminal.

## Screenshot of my work
<img width="673" height="206" alt="image" src="https://github.com/user-attachments/assets/58844a62-fb90-40be-9fce-281f2a4a61b4" />

## Challenges I faced
This level was fairly straightforward after learning the 'ls' and'cat' commands.
The main challenge was understanding which commands should be used for this level

## What I Learned
- How to list files in the current directory using `ls`.
- How to display the contents of a text file using `cat`.

## Key Takeaways
- Learned how to view files from the terminal.
- Used `ls` to inspect directory contents.
- Used `cat` to read a text file.
- Successfully retrieved the password for the next level.

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 0](../Level0/README.md)

➡️ [Next: Level 1-2](../Level1-2/README.md)
