# Day 1 — 14 Nov 2026 · Linux basics

## What I did
- Explored WSL2 and found existing distros with `wsl -l -v`
- Checked the OS version with `cat /etc/os-release` (Ubuntu 24.04 LTS)
- Practised navigation and file commands: `pwd`, `ls`, `ls -la`, `ls -lh`, `cd`, `mkdir`, `touch`, `echo`, `cat`, `cp`, `mv`, `rm`
- Used `man ls` to find options and learned to search inside the manual with `/`
- Scored 4/5 on the Day 1 quiz (missed `mv` vs `cp`, then practised it)

## What I learned
- `>` overwrites a file, `>>` appends to it
- Hidden files start with a dot, and `ls -a` shows them
- Relative paths (`day1/about-me.txt`) vs absolute paths (`/home/sam/day1/about-me.txt`)
- Spaces in filenames cause problems, so use hyphens instead
- `mv` renames or moves (one file), `cp` copies (two files)
- `cp` and `mv` silently overwrite existing files; `-i` asks before overwriting
- `ls -lh` shows sizes in human-readable form (4.0K instead of 4096)
- Tab completion prevents typos; double Tab lists all matches

## Problems I hit and how I fixed them
- `syntax error near unexpected token 'newline'`: I used `>` without a filename. Fixed by adding the destination file.
- Accidentally created a file named `My name is Sam` by running `echo > "My name is Sam"`. Learned that whatever follows `>` becomes the filename, then removed it with quotes.
- `cd..: command not found`: a space is needed between a command and its argument.
- `cp test.txt notes.txt` wiped the content of `notes.txt`: `cp` overwrites without asking. Use `cp -i` for safety.
- `Pattern not found` in `man`: search only goes forward. Pressed `g` to jump to the top and searched again.

## Key takeaway
Read the error message carefully. It usually tells you exactly what's wrong.
