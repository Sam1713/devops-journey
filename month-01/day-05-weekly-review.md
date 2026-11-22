# Day 5 — 22 Nov 2026 · Week 1 review

## What I did
- Recall check on Week 1 topics, focusing on gaps from my mock interview (scores: framework 6.5/10, disk vs memory 8.5/10, host key 5/10 → full answer with guidance, hashed vs encrypted 8/10)
- Rewrote my interview introduction (about 70–90 seconds when spoken)
- Completed OverTheWire Bandit level 3 → 4 with no hints
- Scored 6/6 on the weekly review quiz

## What I learned
- **Troubleshooting framework:** confirm the problem → check the service → read logs (application, then system) → check resources (disk, memory, CPU) → find recent changes → communicate with the team
- **Disk vs RAM:** disk is permanent, slower storage for files; RAM is fast, temporary memory for running programs. A full disk means apps and databases can't write, so they crash or reject requests, and customers see errors or an outage.
- **Host key changed:** it could be harmless (server rebuilt) or a man-in-the-middle attack. Don't connect until the team confirms why; if nobody can explain it, escalate as a security incident.
- **Hashed vs encrypted:** encryption can be reversed with a key; hashing can't be reversed at all. Websites store password hashes and compare them at login, so stolen databases don't reveal real passwords.
- **Hidden files:** names starting with `.` are hidden from `ls`. Always use `ls -la` in an unfamiliar folder; attackers sometimes hide files this way.
- **First character of `ls -l`:** `-` means a regular file (use `cat`), `d` means a directory (use `cd` or `ls`)

## Problems I hit and how I fixed them
- Answered only the first recall question and skipped the rest: my biggest habit to fix. Reread the question before answering.
- Guessed filenames with `cat` before listing the folder. Fix: run `ls -la` first.
- `cd` on a file → `Not a directory`. The `-` at the start of the `ls -l` line showed it was a file, so `cat` was the right tool.
- Saved a password with the wrong label. Verified with `cat`, spotted it, and fixed the line with `sed`.


## Key takeaway
Answer every question completely, ending with the action and the impact, and always check for hidden files with `ls -la`.
