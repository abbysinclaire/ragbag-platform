# RAGBAG Platform - Quick Setup Guide

## Step-by-Step Setup (10 minutes)

### 1️⃣ Get the Files on GitHub

**Option A: Upload directly to GitHub**
1. Go to GitHub.com and create a new repository
2. Name it `ragbag-platform` (or whatever you like)
3. Click "uploading an existing file"
4. Drag and drop all the files from this folder
5. Commit the files

**Option B: Use Git (if you have it installed)**
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR-USERNAME/ragbag-platform.git
git push -u origin main
```

### 2️⃣ Enable GitHub Pages

1. In your GitHub repo, click **Settings**
2. Scroll down to **Pages** (in the left sidebar)
3. Under "Source", select **main** branch
4. Click **Save**
5. Wait 1-2 minutes, then refresh the page
6. You'll see: "Your site is live at https://YOUR-USERNAME.github.io/ragbag-platform/"

### 3️⃣ Configure Your Site

Edit `_config.yml`:
```yaml
title: RAGBAG Research Platform
description: Your group description
baseurl: "/ragbag-platform"  # Change to your repo name
```

Push the change:
```bash
git add _config.yml
git commit -m "Configure site"
git push
```

### 4️⃣ Enable Discussions (for Chat/Brainstorm)

1. In your repo, click **Settings**
2. Scroll to "Features" section
3. Check ✅ **Discussions**
4. Go to the Discussions tab and set up categories:
   - 💡 Ideas
   - ❓ Q&A  
   - 🎨 Show & Tell

Then update the links in `brainstorm.md` to point to your actual repo.

### 5️⃣ Add Your First Member

1. Copy `_members/alice-chen.md` 
2. Rename it to `_members/your-name.md`
3. Edit it with your info:

```markdown
---
name: Your Name
bio: What you're interested in
email: your@email.com
tags: [your, interests, here]
---

## My Seasonal Project: Project Name

What you're working on...
```

4. Push to GitHub:
```bash
git add .
git commit -m "Added my member page"
git push
```

5. Wait 1-2 minutes and check your site!

### 6️⃣ Add Your First Research Entry

Create `_research/2026-02-05-my-first-entry.md`:

```markdown
---
title: "My Research Topic"
date: 2026-02-05
author: Your Name
tags: [research, learning]
---

## What I Learned

Your research notes here...
```

Push it up and it'll appear in your research archive!

## Daily Workflow

1. **Document as you go**: Edit your member page to track progress
2. **Add research**: Create new files in `_research/` when you learn something
3. **Discuss**: Use GitHub Discussions for brainstorming
4. **Commit & push**: Your changes go live in 1-2 minutes

```bash
git add .
git commit -m "Updated my project progress"
git push
```

## Pro Tips

✨ **Edit on GitHub**: You can edit files directly on GitHub.com - click the pencil icon
📱 **Mobile**: Use the GitHub mobile app to update on the go
🔗 **Link things**: Reference other members or research entries with links
🏷️ **Tag consistently**: Agree on tags as a group to keep organized
📸 **Add images**: Put images in `assets/images/` and reference them in markdown

## Need Help?

- **Jekyll docs**: https://jekyllrb.com/docs/
- **Markdown guide**: https://www.markdownguide.org/
- **GitHub Pages**: https://docs.github.com/en/pages

## What You Get

✅ Personal documentation pages for each member
✅ Research archive organized by date and tags
✅ Chat/brainstorm via GitHub Discussions
✅ Free hosting forever
✅ Version control and collaboration built-in
✅ Learn Git, web development, and markdown as you go

Happy researching! 🚀
