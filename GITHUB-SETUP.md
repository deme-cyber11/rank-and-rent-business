# 🚀 Connect to GitHub - Quick Guide

Your local git repository is ready! Follow these steps to push to GitHub.

## ✅ What's Already Done

- ✅ Git initialized
- ✅ .gitignore configured (protects sensitive data)
- ✅ Initial commit created (all files staged)
- ✅ Ready to push to GitHub

---

## 📋 Next Steps

### Step 1: Create GitHub Repository

**Option A: Via GitHub Website** (Recommended)

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** icon (top right) → **New repository**
3. Fill in:
   ```
   Repository name: rank-and-rent-business
   Description: Complete rank & rent business system with SEO/GEO skills
   Visibility: ⚪ Private (recommended - protects your business strategies)
   ```
4. **Important**: ❌ Do NOT check "Initialize with README" (you already have files)
5. Click **Create repository**

**Option B: Via GitHub CLI** (if you have `gh` installed)

```bash
gh repo create rank-and-rent-business --private --source=. --remote=origin
```

---

### Step 2: Connect Your Local Repository to GitHub

After creating the repo, GitHub shows commands. Copy and run them:

```bash
# Navigate to your project
cd "/Users/costa.demetral/Rank & Rent Project"

# Add GitHub as remote (replace YOUR-USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR-USERNAME/rank-and-rent-business.git

# Verify remote was added
git remote -v

# Push to GitHub
git push -u origin main
```

**Example** (replace `yourusername`):
```bash
git remote add origin https://github.com/yourusername/rank-and-rent-business.git
git push -u origin main
```

---

### Step 3: Verify Upload

1. Refresh your GitHub repository page
2. You should see all your files:
   - README.md
   - GETTING-STARTED.md
   - .claude/
   - skills/
   - workflows/
   - etc.

---

## 🔄 Daily Workflow (After Initial Setup)

### When You Make Changes:

```bash
# 1. Check what changed
git status

# 2. Stage your changes
git add .

# 3. Commit with descriptive message
git commit -m "Add new plumbing content template"

# 4. Push to GitHub
git push
```

### Quick Commit Script

Save this as `quick-commit.sh` in your project:

```bash
#!/bin/bash
git add .
git commit -m "${1:-Update project files}"
git push
echo "✅ Pushed to GitHub!"
```

Make it executable:
```bash
chmod +x quick-commit.sh
```

Use it:
```bash
./quick-commit.sh "Added Miami plumber property"
```

---

## 🌐 Optional: Auto-Deploy to Web Hosting

After pushing to GitHub, you can auto-deploy your rank & rent sites:

### Option 1: Netlify (Recommended)

1. Go to [netlify.com](https://netlify.com)
2. Sign up with GitHub
3. "Add new site" → "Import an existing project"
4. Select your repo → Deploy
5. **Result**: Every `git push` auto-deploys in ~30 seconds!

### Option 2: Cloudflare Pages

1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. "Create a project" → Connect GitHub
3. Select repo → Deploy

### Option 3: GitHub Pages

1. In your GitHub repo: Settings → Pages
2. Source: "Deploy from branch"
3. Branch: `main` → Save
4. Site live at: `https://yourusername.github.io/rank-and-rent-business`

**See**: [workflows/build/github-auto-deploy-setup.md](workflows/build/github-auto-deploy-setup.md) for detailed instructions.

---

## 🔒 Security Notes

### Your `.gitignore` Protects:

- ✅ Client information (`sites/*/client-info.json`)
- ✅ API keys and credentials
- ✅ Sensitive ranking data
- ✅ System files (.DS_Store, etc.)
- ✅ Large zip files

### Before Committing Sensitive Data:

If you accidentally add sensitive data:

```bash
# Remove from staging (before commit)
git reset HEAD path/to/sensitive/file

# After commit (remove from history)
git rm --cached path/to/sensitive/file
git commit -m "Remove sensitive data"
git push
```

---

## 📊 Useful Git Commands

```bash
# View commit history
git log --oneline

# See what changed
git diff

# Create new branch
git checkout -b feature-new-niche

# Switch branches
git checkout main

# Merge branch
git merge feature-new-niche

# Pull latest changes (if collaborating)
git pull

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Discard all local changes
git reset --hard HEAD
```

---

## 🐛 Troubleshooting

### "Permission denied (publickey)"

You need to set up SSH keys or use HTTPS:

**Quick fix - Use HTTPS**:
```bash
git remote set-url origin https://github.com/YOUR-USERNAME/rank-and-rent-business.git
```

**Better - Set up SSH** (one-time):
```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
# Press Enter to accept defaults
cat ~/.ssh/id_ed25519.pub
# Copy output and add to GitHub: Settings → SSH Keys → New SSH key
```

### "Failed to push"

```bash
# Pull first, then push
git pull origin main --rebase
git push
```

### "Large files warning"

GitHub has 100MB file limit. Check:
```bash
find . -type f -size +50M
```

Remove large files:
```bash
git rm --cached path/to/large/file
echo "path/to/large/file" >> .gitignore
git commit -m "Remove large file"
```

---

## 📁 Repository Structure on GitHub

After pushing, your GitHub repo will show:

```
rank-and-rent-business/
├── 📄 README.md (project overview)
├── 📄 GETTING-STARTED.md (first property guide)
├── 📄 ARCHITECTURE.md (system architecture)
├── 📄 SYSTEM-OVERVIEW.md (visual overview)
├── 📄 PROJECT-TRACKER.md (portfolio tracker)
├── 📄 QUICK-REFERENCE.md (command reference)
├── 📄 GITHUB-SETUP.md (this file)
├── 📁 .claude/ (skills configuration)
├── 📁 workflows/ (process templates)
├── 📁 content-templates/ (reusable content)
├── 📁 sites/ (your properties)
├── 📁 data/ (research & tracking)
├── 📁 reports/ (performance reports)
└── 📁 skills/ (complete skills library)
```

---

## ✅ Checklist

Before pushing:
- [ ] Created GitHub repository
- [ ] Copied remote URL from GitHub
- [ ] Ran `git remote add origin [URL]`
- [ ] Ran `git push -u origin main`
- [ ] Verified files appear on GitHub
- [ ] Repository is set to Private (recommended)

After first push:
- [ ] Add repository description on GitHub
- [ ] Add topics/tags: `rank-and-rent`, `seo`, `local-business`
- [ ] (Optional) Set up auto-deploy with Netlify/Cloudflare
- [ ] (Optional) Invite collaborators if working with team

---

## 🎯 Current Status

```bash
# Check your status anytime:
cd "/Users/costa.demetral/Rank & Rent Project"
git status
git log --oneline -5  # Last 5 commits
git remote -v          # Show GitHub connection
```

---

## 🚀 You're Ready!

Your project is git-ready. Just:
1. Create GitHub repo
2. Run the remote add command
3. Push!

**Questions?** Run `git status` or `git --help`

---

**Created**: 2026-01-18
**Status**: ✅ Ready to push to GitHub
