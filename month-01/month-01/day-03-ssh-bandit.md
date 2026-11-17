# Day 3 — 18 Nov 2026 · SSH and OverTheWire Bandit

## What I did
- Recall check on Day 2: config in `/etc`, logs in `/var/log`, relative vs absolute paths
- Explored `/mnt/c` (the Windows C: drive mounted inside WSL) and unfamiliar folders in `/`
- Learned why SSH exists and how an SSH command is built
- Logged into a remote server over SSH for the first time
- Completed OverTheWire Bandit levels 0 → 2
- Scored 5/5 on the Day 3 quiz

## What I learned
- **SSH (Secure Shell)** lets engineers work on remote servers through an encrypted connection. It replaced Telnet, which sent passwords as plain text.
- SSH command structure: `ssh user@server -p port`. The port is like a door number; SSH normally uses 22.
- The prompt `user@machine:folder$` shows who I am and which machine I'm on. Always check it before running commands on remote servers.
- `exit` closes the SSH session and returns me to my own machine.
- Failed SSH logins are recorded in `/var/log/auth.log` on the server.
- `/home` contains a home folder for every user on a system.
- WSL mounts the Windows C: drive at `/mnt/c`; some Windows files are locked while Windows is using them.
- `sbin` holds system administration commands like `reboot` and `shutdown`.
- A capitalised folder like `Docker` in `/` usually means software added it; standard Linux folders are lowercase.
- Words starting with `-` are treated as options by commands. A lone `-` often means "read from the keyboard" (standard input). To refer to a file with an unusual name like this, write it as a path starting with `./`.

## Problems I hit and how I fixed them
- `cat` on a dash-named file just waited for input: the dash was read as an option, not a filename. Fixed by referring to it as a path. Pressed Ctrl + C to cancel the waiting command.
- Ran commands as the wrong user (`bandit0` instead of `bandit1`): didn't read my prompt. Now I check the prompt before every command.
- `Permission denied, please try again.` on SSH login: mixed up the username and the password.
- Wandered into `/home` while trying to fix the problem: `cd ~` always takes me back to my home folder.

## Key takeaway
Always read the prompt. On real servers, running a command as the wrong user or on the wrong machine causes incidents.
