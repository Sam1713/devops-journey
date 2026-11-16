# Day 2 — 17 Nov 2026 · The Linux file system

## What I did
- Explored the root of the file system with `ls /`
- Navigated into `/var/log` and identified common system logs
- Checked `/bin` with `ls -l` and discovered it's a link
- Tested file creation in `/tmp` vs `/etc`
- Scored 6/6 on the Day 2 quiz

## What I learned
- Linux follows a standard layout (FHS), so every server keeps the same kinds of files in the same places
- `/etc` = configuration, `/var/log` = logs, `/home` = user folders, `/tmp` = temporary files, `/usr/bin` = commands
- Relative paths (`var`) start from my current folder; absolute paths (`/var`) start from root and work anywhere
- Key logs: `auth.log` (logins, sudo, SSH attempts), `syslog` (general system messages), `dpkg.log` (package installs and updates)
- **Log rotation:** logrotate renames the current log to `.1`, shifts older ones up, compresses them as `.gz`, and deletes the oldest. This stops logs from filling the disk.
- `/bin` is a link to `/usr/bin`, where commands really live (Ubuntu merged them; that's why `ls /` shows `*.usr-is-merged` folders)
- `/etc` is protected so only root can change system configuration

## Problems I hit and how I fixed them
- `cat: /var/log: Is a directory`: `cat` reads files, not folders. Used `ls` instead.
- `cd var` failed from my home folder: `var` is a relative path. Fixed by using `/var` or running it from `/`.
- `cat /var log` gave two errors: the space split it into two arguments.
- `touch: cannot touch '/etc/test.txt': Permission denied`: `/etc` is protected system configuration. `/tmp` worked.
- Typed `/user/bin` instead of `/usr/bin`. One character matters.

## Key takeaway
If the same error appears twice, stop and read it carefully instead of retrying variations.
