# 🚀 DevOps Journey

Learning in public: **DevOps / Cloud Engineer**.

I'm documenting every study day here: what I learned, what broke, and how I fixed it.

## 🎯 Goal

Become a DevOps / Cloud Engineer with strong skills in Linux, AWS, Docker, Kubernetes, Terraform, CI/CD, monitoring, and deploying AI applications.

## 🗺️ Roadmap

| Phase | Months | Focus |
|-------|--------|-------|
| 1. Foundations | 1–3 | Linux, networking, Git, Bash, Python, AWS basics |
| 2. Core DevOps | 4–6 | Docker, CI/CD (GitHub Actions), Terraform, Kubernetes basics, AWS SAA |
| 3. Depth + AI | 7–12 | EKS, Helm, Prometheus/Grafana, ArgoCD, deploying AI apps on Kubernetes |

## ✅ Skills Tracker

- [x] Linux environment setup (WSL2, Ubuntu 24.04)
- [ ] Linux fundamentals
- [ ] Networking basics
- [ ] Git and GitHub
- [ ] Bash scripting
- [ ] Python for automation
- [ ] AWS fundamentals
- [ ] Docker
- [ ] CI/CD with GitHub Actions
- [ ] Terraform
- [ ] Kubernetes
- [ ] Monitoring (Prometheus, Grafana)
- [ ] GitOps (ArgoCD)
- [ ] Deploying AI applications

## 📅 Daily Log

### Day 1 — 14 Nov 2026 · Linux basics

**What I did**
- Explored WSL2 and found existing distros with `wsl -l -v`
- Checked the OS version with `cat /etc/os-release` (Ubuntu 24.04 LTS)
- Practised navigation and file commands: `pwd`, `ls`, `ls -la`, `ls -lh`, `cd`, `mkdir`, `touch`, `echo`, `cat`, `cp`, `mv`, `rm`
- Used `man ls` to find options and learned to search inside the manual with `/`

**What I learned**
- `>` overwrites a file, `>>` appends to it
- Hidden files start with a dot, and `ls -a` shows them
- Relative paths (`day1/about-me.txt`) vs absolute paths (`/home/sam/day1/about-me.txt`)
- Spaces in filenames cause problems, so use hyphens instead
- `mv` renames or moves (one file), `cp` copies (two files)
- Tab completion prevents typos

**Problems I hit and how I fixed them**
- `syntax error near unexpected token 'newline'`: I used `>` without a filename. Fixed by adding the destination file.
- Accidentally created a file named `My name is Sam` by running `echo > "My name is Sam"`. Learned that whatever follows `>` becomes the filename, then removed it with quotes.
- `cd..: command not found`: a space is needed between a command and its argument.
- `Pattern not found` in `man`: search only goes forward. Pressed `g` to jump to the top and searched again.

**Key takeaway:** read the error message carefully. It usually tells you exactly what's wrong.

---

*Next: Day 2 — Linux file system structure*
