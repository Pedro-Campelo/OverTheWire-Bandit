# Bandit Level 6-7

## How to login to the level
Connect to this level by using:

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
```

## Objective
Find the password which is stored somewhere on the server with all the following properties:
- owned by user `bandit7`
- owned by group `bandit6`
- `33 bytes` in size

## Background Research
I didn't do any background research since I felt like I knew enough already about the find command

## My Approach
OverTheWire provided me with the information:
- The password is somewhere on the server with the properties; owned by user `bandit7`, owned by group `bandit6` and `33` bytes in size

Firstly, I used the variables given to me and ran the command:
```bash
find / -user bandit7 -group bandit6 -size 33c
```
I used this command because the arguments Ive included make it so that only files that fit the criteria are shown and found.
I then scrolled through all the files until I found a file which I have access to. I found a file called `bandit7.password`.
It was in `/var/lib/dpkg/info/` so I ran the command:
```bash
cat /var/lib/dpkg/info/bandit7.password
```
Which gave me the password for me to continue the challenge

## Command Breakdown


## Screenshot of my work
<img width="1129" height="259" alt="image" src="https://github.com/user-attachments/assets/69ea6996-681b-40a2-8ce9-6c9fa5d73e0f" />

---

<img width="749" height="59" alt="image" src="https://github.com/user-attachments/assets/f0a0d1c4-8154-4310-a645-57d8be2ef8f3" />


## Challenges I faced
- The challenge was fairly straight forward after I identified the right conditions for the find command

## What I Learned
- The `find` command can search the entire filesystem.
- Files can be filtered by owner, group and size.
- Permission denied messages are normal when searching directories you don't have access to.

## Key Takeaways
- Combining multiple search conditions can quickly locate a specific file.
- Permission errors don't necessarily mean the command has failed.
- Linux file ownership is an important part of system security.

## How to login to next level
Once you've retrieved the password, connect to the next level using:

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 5-6](../04-05/README.md)

➡️ [Next: Level 7-8](../06-07/README.md)
