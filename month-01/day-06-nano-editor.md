# Day 6 — 23 Nov 2026 · nano text editor

## What I did
- Recalled earlier topics: `sed -i` usage and risk, two ways to read a file starting with `-`, and the troubleshooting steps when an application breaks
- Learned nano: why it's used, its advantages, and its shortcuts
- Created and edited a config file (`app.conf`) and cleaned up my password file format
- Scored 5/5 on the quiz

## What I learned
- nano is used on Linux servers because servers have no GUI
- It's the best way to add or edit a file while seeing what's inside, unlike `sed` or `echo`
- `^` means Ctrl: save with Ctrl + O (then Enter), search with Ctrl + W, exit with Ctrl + X
- A `*` next to the filename means there are unsaved changes
- If I exit without saving, nano asks whether to save; pressing N discards the changes
- `log_level=debug` gives very detailed logs that grow fast; teams switch back to `info` after troubleshooting
- Consistent formats (like `key=value`) matter in config files

## Problems I hit and how I fixed them
- Couldn't find how to save: pressed Ctrl + W (that's search, "Where Is"). Read the bottom bar and found Ctrl + O ("Write Out").
- The first letter of each line looked missing: my terminal window was cutting off the left edge. Verified the file was fine with `cat`.

## Key takeaway
Rushing isn't better. It's better to take time and understand the issue than to finish the session quickly. (Like reading nano's bottom bar before pressing keys.)
