# RAGBAG Research Platform

A collaborative platform for independent research groups, built with Jekyll and hosted on GitHub Pages.

## Features

✨ **Individual Member Pages** - Each member has their own space to document seasonal exploration projects
📚 **Research Archive** - Organized by date and tags for easy searching
💬 **Brainstorming Space** - Integrated with GitHub Discussions for collaborative thinking
🏷️ **Tag System** - Organize content by topics and themes
📱 **Responsive Design** - Works on all devices

## Quick Start

### 1. Create Your GitHub Repository

1. Create a new repository on GitHub (name it something like `ragbag-platform`)
2. Clone this repository to your computer, or push these files to your new repo

```bash
git clone https://github.com/YOUR-USERNAME/ragbag-platform.git
cd ragbag-platform
```

### 2. Configure Your Site

Edit `_config.yml`:
- Change `baseurl` to your repo name (e.g., `/ragbag-platform`)
- Update `title` and `description`

### 3. Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select `main` branch
4. Click **Save**

Your site will be live at: `https://YOUR-USERNAME.github.io/ragbag-platform/`

### 4. Enable GitHub Discussions (for Brainstorming)

1. Go to your repo **Settings**
2. Scroll to "Features"
3. Check ✅ **Discussions**
4. Update the links in `brainstorm.md` to point to your repo

## How to Use

### Adding a New Member

Create a new file in `_members/` folder:

```markdown
---
name: Your Name
bio: Short bio about your interests
email: your.email@example.com
tags: [interest1, interest2, interest3]
---

## Seasonal Project: Your Project Title

Document your exploration project here!

### Week 1
What you're working on...

### Goals
- [ ] Goal 1
- [ ] Goal 2
```

File naming: `firstname-lastname.md` (e.g., `alice-chen.md`)

### Adding Research Input

Create a new file in `_research/` folder:

```markdown
---
title: "Your Research Title"
date: 2026-02-05
author: Your Name
tags: [tag1, tag2, tag3]
links:
  - title: "Resource Name"
    url: "https://example.com"
---

## Your Research Content

Write your research notes, findings, and thoughts here!
```

File naming: `YYYY-MM-DD-title.md` (e.g., `2026-02-05-complex-systems.md`)

### Updating Your Site

1. Make changes to your markdown files
2. Commit and push to GitHub:

```bash
git add .
git commit -m "Added new research entry"
git push
```

3. GitHub Pages will automatically rebuild your site in 1-2 minutes

## Local Development (Optional)

To preview your site locally before pushing:

1. Install Ruby and Jekyll:
   - [Jekyll Installation Guide](https://jekyllrb.com/docs/installation/)

2. Install dependencies:
```bash
bundle install
```

3. Run local server:
```bash
bundle exec jekyll serve
```

4. View at `http://localhost:4000`

## Project Structure

```
ragbag-platform/
├── _config.yml           # Site configuration
├── _layouts/             # Page templates
│   ├── default.html      # Base layout
│   ├── member.html       # Member page layout
│   └── research.html     # Research entry layout
├── _members/             # Member documentation
│   ├── alice-chen.md
│   └── jordan-martinez.md
├── _research/            # Research entries
│   └── 2026-02-03-complex-systems.md
├── assets/
│   └── css/
│       └── style.css     # Styling
├── index.md              # Homepage
├── members.md            # Members index
├── research.md           # Research archive
└── brainstorm.md         # Brainstorm page
```

## Customization

### Change Colors

Edit `assets/css/style.css` and modify the gradient colors:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Add New Pages

Create a new `.md` file in the root directory with:
```markdown
---
layout: default
title: Your Page Title
---

Your content here...
```

### Modify Navigation

Edit `_layouts/default.html` and update the `<nav>` section.

## Tips

- **Write in Markdown**: Use headers (`##`), lists (`-`), and links (`[text](url)`)
- **Use Tags Consistently**: Keep a list of agreed-upon tags to maintain organization
- **Update Regularly**: Document as you go rather than batch updating
- **Cross-reference**: Link between member pages and research entries
- **Use Discussions**: GitHub Discussions is great for async brainstorming

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## License

This template is open source and free to use for your research group!

---

Built with 💜 by RAGBAG - Learning from scratch, together
