# Bandit Level 0

## Objective
Connect to the Bandit game server using SSH and successfully log in as the 'bandit0' user.

## Background Research
Before attempting this level, I had never used or heard of SSH before. So rather than copying the command directly, I researched 'what SSH is, how it works, and how to use it'
I found out that SSH (Secure Shell) is a cryptographic network protocol that allows users to securely connect to remote computers over an unsecured network. It encrypts all 
communication between the client and the server, protecting passwords and transmitted data from being intercepted. and to use this tool you have to run the command

```bash
ssh username@remote_host_ip -p port number
```

## My Approach
OverTheWire provided me with this information:
- Username: bandit0
- Host: bandit.labs.overthewire.org
- Port: 2220
- Password: bandit0

Using this information, I substituted the values into the command and ended up running the command

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
When I connected for the first time my computer reported that the authenticity of the host couldn't yet be verified. This happens because my computer has not yet connected to this server before, so I verified the server's identity by
typing 'yes'. After doing that I entered the password and successfully logged into the server as bandit0

## Command Breakdown
'ssh' - Starts an SSH connection

'bandit0' - Username used to authenticate

'@' - Separates the username from the host

'bandit.labs.overthewire.org' - Remote server hostname

'-p' - Specifies a custom port

'2220' - Port used by the bandit server

## Screenshot of my work
<img width="858" height="569" alt="image" src="https://github.com/user-attachments/assets/874d4fff-b47c-43be-86f1-2be8381a0e78" />

## Challenges I faced
- Since this was my first time using SSH, I wasn't familiar with the syntax.
- I also didn't understand why i was displayed a security warning before connecting.

## What I Learned
- What is SSH and why its used
- How to use SSH to securely connect to a remote server
- What a port is and its purpose in network communication

## Key Takeaways
- Successfully connected to a remote Linux server.
- Learned the basics of SSH.
- Understood why SSH verifies unknown hosts.
- Gained confidence using the Linux terminal.

## Navigation

🏠 [Repository Home](https://github.com/Pedro-Campelo/OverTheWire-Bandit)

➡️ [Next: Level 1](../Level0-1/README.md)
