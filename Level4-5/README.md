# Bandit Level 4-5

## How to login to the level
Connect to this level by using:

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
```

## Objective
Find the only human-readable file in the `inhere` directory, Read it's contents and use that to enter the next level

## Background Research
None I used knowledge from previous levels to complete this level

## My Approach
OverTheWire provided me with the information:
- The password is in the only human-readable file
- The file is stored in a directory called `inhere`

Firstly, I used the `ls` command to list all the contents of the directory Im in. I saw the `inhere` directory OverTheWire mentioned and entered that directory using the command:
```bash
cd inhere
```
Then I ran the command `ls` and was shown 10 files. I opened each file one at a time using the command:
```bash
cat ./filename
```
until I could read the output. I was unhappy with this approach and researched quicker more efficient ways to complete this level and discovered the command
```bash
file ./*
```
This command lists all files in the directory along with that files file type.
I then discovered that `"human readable"` files are usually wrote in:
- `ASCII text`
- `Unicode text`
- `UTF-8 text`

so I used this new knowledge and discovered that `-file07`'s file type is `ASCII text` meaning it is human-readable. So I ran the command
```bash
cat ./file07
```
to get the password

## Command Breakdown
```bash
file ./*
```
- `file` - Inspects files
- `./` - In current directory
- `*` - Means every file in this directory

## Screenshot of my work
###First Approach:
<img width="1173" height="493" alt="image" src="https://github.com/user-attachments/assets/71ed9666-53d1-438a-918a-c2c528fa53af" />


###Second Approach:
<img width="1158" height="518" alt="image" src="https://github.com/user-attachments/assets/acf4d0ed-ebf2-4e61-b24b-b4ecdd3d6862" />

## Challenges I faced


## What I Learned


## Key Takeaways


## How to login to next level
Once you've retrieved the password, connect to the next level using:

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 3-4](../Level3-4/README.md)

➡️ [Next: Level 5-6](../Level5-6/README.md)
