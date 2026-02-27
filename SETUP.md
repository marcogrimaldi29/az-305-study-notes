# 🛠️ Setup Guide — GitHub Upload, Pages & Website Integration

This guide walks you through:

1. [Uploading to GitHub](#1-upload-to-github)
2. [Enabling GitHub Pages](#2-enable-github-pages)
3. [Personalising Your Site](#3-personalise-your-site)
4. [Linking from marcogrimaldi29.com](#4-link-from-marcogrimaldi29com)
5. [Testing Locally (optional)](#5-testing-locally-optional)
6. [Keeping Notes Up to Date](#6-keeping-notes-up-to-date)

---

## 1. Upload to GitHub

### Option A — Using GitHub.com (no local tools needed)

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository** (the `+` button, top right)
3. Fill in:
   - **Repository name:** `az-305-study-notes`
   - **Description:** `AZ-305 Microsoft Azure Solutions Architect Expert — Study Notes`
   - **Visibility:** Public *(required for free GitHub Pages)*
   - ✅ Check **"Add a README file"** → No (we already have one)
4. Click **Create repository**
5. In the new empty repo, click **Add file → Upload files**
6. Drag and drop **all files and folders** from this project (including `.github/` folder, `_includes/`, `_config.yml`, `Gemfile`, all `.md` files)
7. Scroll down, write a commit message like `Initial commit: AZ-305 study notes`
8. Click **Commit changes**

> ⚠️ Make sure `.github/workflows/pages.yml` is uploaded — it's a hidden folder on macOS/Linux.
> On macOS: press **Cmd+Shift+.** in Finder to show hidden files before uploading.

### Option B — Using Git CLI (recommended)

```bash
# 1. Initialise the repo locally
cd az-305-study-notes
git init
git add .
git commit -m "Initial commit: AZ-305 study notes"

# 2. Create the repo on GitHub and push
# Replace YOUR_GITHUB_USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/az-305-study-notes.git
git branch -M main
git push -u origin main
```

### Option C — Using GitHub CLI

```bash
# Install GitHub CLI: https://cli.github.com/
cd az-305-study-notes
git init && git add . && git commit -m "Initial commit"
gh repo create az-305-study-notes --public --source=. --push
```

---

## 2. Enable GitHub Pages

### Step 1 — Update `_config.yml` with your username

Open `_config.yml` and replace the two placeholder lines near the top:

```yaml
# Before:
url:     ""
baseurl: ""

# After (replace YOUR_GITHUB_USERNAME with your real GitHub username):
url:     "https://YOUR_GITHUB_USERNAME.github.io"
baseurl: "/az-305-study-notes"
```

Also update the `gh_edit_repository` line:
```yaml
gh_edit_repository: "https://github.com/YOUR_GITHUB_USERNAME/az-305-study-notes"
```

Commit and push this change.

### Step 2 — Update `index.md` and `README.md`

In both files, replace `YOUR_GITHUB_USERNAME` with your real GitHub username.

### Step 3 — Enable Pages in GitHub Settings

1. Go to your repo on GitHub: `github.com/YOUR_GITHUB_USERNAME/az-305-study-notes`
2. Click **Settings** (top tab)
3. In the left sidebar, click **Pages**
4. Under **Source**, select **GitHub Actions** *(not "Deploy from a branch")*
5. Click **Save**

### Step 4 — Trigger the first deployment

The GitHub Actions workflow runs automatically on every push to `main`.
To trigger it manually:

1. Go to your repo → **Actions** tab
2. Click **"Deploy to GitHub Pages"** in the left sidebar
3. Click **"Run workflow"** → **"Run workflow"**

### Step 5 — View your live site

After ~2 minutes, your site will be live at:

```
https://YOUR_GITHUB_USERNAME.github.io/az-305-study-notes/
```

You can confirm the URL in **Settings → Pages** where it will show a green "Your site is live" banner.

---

## 3. Personalise Your Site

### Update author name and personal URL

In `_config.yml`, these lines control the footer and sidebar links:

```yaml
author:           "Marco Grimaldi"        # ← your name
personal_site_url:  "https://marcogrimaldi29.com"  # ← your site
personal_site_label: "marcogrimaldi29.com"
```

### Change colour scheme

```yaml
# In _config.yml:
color_scheme: dark    # dark | light
```

### Add a logo

1. Place a PNG file at `assets/images/logo.png` (recommended: 200×50px)
2. Uncomment in `_config.yml`:
   ```yaml
   logo: "/assets/images/logo.png"
   ```

### Add a custom domain (optional)

If you want to host at a subdomain like `az305.marcogrimaldi29.com`:

1. In your DNS provider, add a **CNAME** record:
   ```
   Name:  az305
   Value: YOUR_GITHUB_USERNAME.github.io
   ```
2. In GitHub Settings → Pages → Custom domain, enter: `az305.marcogrimaldi29.com`
3. Check ✅ **Enforce HTTPS**
4. In `_config.yml`:
   ```yaml
   url:     "https://az305.marcogrimaldi29.com"
   baseurl: ""    # empty when using custom domain
   ```

---

## 4. Link from marcogrimaldi29.com

Once your GitHub Pages site is live, here are three ways to reference it from your blog:

### Option A — Direct text link (simplest)

Add to any post or page on your blog:

```html
<a href="https://YOUR_GITHUB_USERNAME.github.io/az-305-study-notes/" target="_blank">
  📘 AZ-305 Study Notes — Azure Solutions Architect Exam Prep
</a>
```

### Option B — Styled card (recommended for blog sidebar or post)

```html
<div style="border: 2px solid #1a73e8; border-radius: 12px; padding: 1.2rem;
            background: #f8f9fa; max-width: 420px; font-family: sans-serif;">
  <h3 style="margin-top: 0; color: #1a73e8;">
    📘 AZ-305 Azure Study Notes
  </h3>
  <p style="color: #444; font-size: 0.95rem;">
    Complete exam prep notes for the <strong>Microsoft Azure Solutions Architect Expert</strong>
    certification — decision diagrams, SLA tables, SKU comparisons, and exam caveats.
  </p>
  <p style="margin-bottom: 0;">
    <a href="https://YOUR_GITHUB_USERNAME.github.io/az-305-study-notes/"
       target="_blank"
       style="background: #1a73e8; color: white; padding: 0.5rem 1rem;
              border-radius: 6px; text-decoration: none; font-weight: bold;">
      Open Study Notes →
    </a>
    &nbsp;
    <a href="https://github.com/YOUR_GITHUB_USERNAME/az-305-study-notes"
       target="_blank" style="color: #555; font-size: 0.85rem;">
      View on GitHub ↗
    </a>
  </p>
</div>
```

### Option C — Markdown link (for Jekyll / WordPress / Ghost blogs)

```markdown
## 📘 AZ-305 Azure Solutions Architect Study Notes

I've published my complete AZ-305 exam prep notes as an open-source website.
The notes cover all four exam domains with Mermaid diagrams, SLA tables, SKU
comparisons, and exam caveats.

👉 **[View AZ-305 Study Notes](https://YOUR_GITHUB_USERNAME.github.io/az-305-study-notes/)**

Topics covered:
- Domain 1 (25–30%): Identity, Governance & Monitoring
- Domain 2 (25–30%): Data Storage Solutions
- Domain 3 (15–20%): Business Continuity
- Domain 4 (30–35%): Infrastructure Solutions (compute, networking, migrations)
- Azure Well-Architected Framework & Cloud Adoption Framework
- Quick Reference Cheatsheet with SLA tables and exam traps
```

### Update the back-link in this repo

In `_config.yml`, the footer already links back to `marcogrimaldi29.com`.
The `index.md` landing page also has an "About the Author" section linking there.
No additional changes needed — the cross-linking is built in.

---

## 5. Testing Locally (optional)

If you want to preview the site before pushing to GitHub:

### Prerequisites

- Ruby 3.1+ — [ruby-lang.org](https://www.ruby-lang.org/en/downloads/)
- Bundler: `gem install bundler`

### Run locally

```bash
cd az-305-study-notes

# Install dependencies (first time only)
bundle install

# Start local server
bundle exec jekyll serve --livereload

# Open in browser
open http://localhost:4000/az-305-study-notes/
```

> 💡 `--livereload` automatically refreshes the browser when you save a file — very handy for editing.

---

## 6. Keeping Notes Up to Date

### Add a new section to an existing page

Just edit the `.md` file and push — the site rebuilds automatically via GitHub Actions.

### Add a new page

1. Create a new `.md` file, e.g., `07-practice-questions.md`
2. Add front matter at the top:
   ```yaml
   ---
   layout: default
   title: "07 — Practice Questions"
   nav_order: 9
   description: "AZ-305 practice questions and answer explanations."
   permalink: /07-practice-questions/
   mermaid: true
   ---
   ```
3. Write your content below the front matter
4. Push — it appears in the sidebar automatically

### Check deployment status

Go to your repo → **Actions** tab → click the latest **"Deploy to GitHub Pages"** run.
Green ✅ = live. Red ❌ = check the error log (usually a YAML syntax issue in `_config.yml`).

---

## 🔗 Quick Reference URLs

After setup, replace `YOUR_GITHUB_USERNAME` everywhere with your actual GitHub username:

| Resource | URL |
|----------|-----|
| GitHub Repo | `https://github.com/YOUR_GITHUB_USERNAME/az-305-study-notes` |
| Live Pages Site | `https://YOUR_GITHUB_USERNAME.github.io/az-305-study-notes/` |
| Pages Settings | `https://github.com/YOUR_GITHUB_USERNAME/az-305-study-notes/settings/pages` |
| Actions Log | `https://github.com/YOUR_GITHUB_USERNAME/az-305-study-notes/actions` |
| Personal Blog | `https://marcogrimaldi29.com` |

---

*Questions or issues? Open a GitHub Issue on the repo.*
