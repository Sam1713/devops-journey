# Day 4 — 21 Nov 2026 · SSH host keys and tricky filenames

## What I did
- Recalled earlier topics: `>` vs `>>`, the different log files and what they record, what `/usr/bin` means, and the `cat -` trap every beginner falls into
- Answered why SSH asks for confirmation on the first connection
- Explored the `.ssh` folder and the `known_hosts` file
- Got back my lost Bandit level 2 password and completed level 2 → 3
- Scored 5/5 on the quiz

## What I learned
- The first time I connect, SSH asks me to confirm I trust the server. It saves the server's host key (its identity) so it can detect impersonation later.
- `known_hosts` stores the servers I've connected to: the server name (hashed) plus its host key.
- The names are **hashed**, not encrypted, for protection from hackers. A hash can't be reversed, but SSH can still check if a server matches.
- Each server can have several key types (`ed25519`, `rsa`, `ecdsa`); `ed25519` is the modern one.
- The `.ssh` folder is locked to only me because private keys will live there.
- Filenames with spaces need quotes (" "), so Linux reads them as one name.
- Filenames starting with `-` are read as options. Writing `./` in front makes Linux treat it as a filename. `--` also means "end of options."
- `sed -i` edits a file directly with no undo; `sed -i.bak` keeps a backup.

## Problems I hit and how I fixed them
- `cd my folder` → `too many arguments`: the space split the name in two. Quotes fix it.
- Lost my level 2 password because I never saved it. Logged in again and recovered it, and now I label every password I save.
- Needed several attempts to read a Bandit file whose name had spaces and dashes. Each error gave a clue, and I solved it by combining quotes and `./`.
- Ran `sed -i` on a line that was already correct. Lesson: verify first, change only if needed.

## Key takeaway
Each error message is a clue. Reading errors carefully and combining what I already know solved a problem I'd never seen before.
