# Git & GitHub Setup Workflow Reference

## Initial Repository Creation (for walexy account)

### Prerequisites
- `gh` CLI installed and authenticated: `gh auth status`
- Access to GitHub at https://github.com/walexy

### Commands Used

**1. Check git status:**
```bash
git --version && git config --list | grep remote
```

**2. Initialize/reinit repository:**
```bash
git init
```

**3. Create new repo on GitHub:**
```bash
gh repo create backcountry-bean-counters --public --source=. --remote=origin
```
Options:
- `--public`: Make repo public (use `--private` for private)
- `--source=.`: Include local files
- `--remote=origin`: Set remote URL automatically

**4. Commit and push:**
```bash
git add . && git commit -m "Initial commit with .gitignore"
git push -u origin main
```

## Git Remote Management

### Add existing repo as remote:
```bash
git remote add origin https://github.com/walexy/YOUR-REPO-NAME.git
git branch -M main
git push -u origin main
```

### Check remotes:
```bash
git remote -v
git status
```

## Repository URL Pattern
For `walexy` account:
```
https://github.com/walexy/YOUR-REPO-NAME.git
```

## Useful gh CLI Commands

```bash
# List your repos
gh repo list walexy

# View specific repo
gh repo view walexy/backcountry-bean-counters --web

# Create new private repo
gh repo create my-project --private --source=. --push

# Fork a repository
gh repo fork owner/repo --name="My Project"
```

## Notes for Future Sessions
- Always check `gh auth status` to verify authentication
- `.gitignore` should be committed early
- Push initial commit with meaningful message
- Use `--source=.` to push existing local files when creating new repo

---
Created: $(date)
Account: walexy@github.com