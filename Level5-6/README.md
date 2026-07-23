# Bandit Level 5-6

## How to login to the level
Connect to this level by using:

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```

## Objective
The password is in a file in the directory `inhere` that has the following properties
- human-readable
- 1033 bytes in size
- not executable

## Background Research
Before attempting this level I researched more about the `find` command and discovered that you can add arguments to it like you can with `ls -a`. I discovered that there are 
arguments that are useful for this level:
- `-readable` which shows me only files i have permission to read
- `size 1033c` which shows me only files with a size of 1033 bytes (c)
- `! -executable` The `!` means `"NOT"` so its saying to show only files that are not executable

I also discovered that there are multiple size prefixes, some of them being:
- `c` - Bytes
- `k` - KiB (1024 bytes)
- `M` - Mib (1024^2^ bytes)
- `G` - GiB (1024^3^ bytes)

## My Approach
OverTheWire provided me with the information:
- The password is in a file wich has the properties; human-readable, 1033 bytes in size and not executable
- The file is stored in a directory called `inhere`

Firstly, I listed the contents of the current directory and saw the `inhere` directory and `cd`'d into it.
I then used the command
```bash
find ./* -readable -size 1033c ! -executable
```
I used this command because the arguements ive included make it so that only files that fit the criteria are shown and found

## Command Breakdown
```bash
find ./* -readable -size 1033c ! -executable
```
- `find` - finds files that fit the criteria
- `./*` - All items in directory
- `-readable` - Only returns files that the current user has permission to read
- `-size 1033c` - Only returns files that are exactly **1033 bytes** in size (`c` stands for bytes)
- `! - executable` - Excludes executable files (`!` means **NOT**)

## Screenshot of my work
<img width="909" height="445" alt="image" src="https://github.com/user-attachments/assets/b352ac48-616d-49d3-b92b-be38d7ece34f" />


## Challenges I faced
- The challenge wasn't finding the file—it was learning how to use the `find` command effectively.
- I initially didn't know that `find` supported filters such as `-size`, `-readable`, and `! -executable`. 
  After reading the documentation and experimenting with the command, I realised I could combine multiple conditions to narrow the search down to a single file.

## What I Learned
- The `find` command can search for files based on multiple properties at once.
- Search conditions can be combined to create very specific queries.
- Prefixing a condition with `!` negates it.
- The `c` suffix specifies that the file size should be measured in bytes.

## Key Takeaways
- Powerful command-line tools become even more useful when you combine multiple search conditions.
- Learning command options can eliminate the need to manually inspect files.
- The `find` command is one of Linux's most powerful file-searching tools.

## How to login to next level
Once you've retrieved the password, connect to the next level using:

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```
Then enter the password:
```text
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
```

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

⬅️ [Previous: Level 4-5](../Level4-5/README.md)

➡️ [Next: Level 6-7](../Level6-7/README.md)
