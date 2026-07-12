# Deploy Your Portfolio to GitHub Pages

Step-by-step. Should take about **5 minutes** end-to-end.

**Your target URL:** `https://vikkiecrush.github.io`

---

## Step 1 — Create the special repository on GitHub

GitHub Pages user sites use a magic naming convention: the repo must be named **exactly** `<your-username>.github.io`.

1. Go to [https://github.com/new](https://github.com/new)
2. **Repository name:** `vikkiecrush.github.io` *(must match exactly — case sensitive)*
3. **Description:** `Personal portfolio site — Victory Ikpe, Senior Data Scientist`
4. **Public** (required for free GitHub Pages)
5. **Do NOT initialize with README, .gitignore, or license** — we already have those locally
6. Click **Create repository**

## Step 2 — Push this local project to that repo

Open Terminal, then run these commands one-by-one:

```bash
cd "/Users/v0i0084/portfolio-vikkiecrush"

# initialize git in this folder
git init
git branch -M main

# stage and commit everything
git add .
git commit -m "Initial portfolio: bio, value prop, artifacts 1-2 live"

# connect to your GitHub repo
git remote add origin https://github.com/vikkiecrush/vikkiecrush.github.io.git

# push
git push -u origin main
```

If prompted for credentials, use your GitHub username and a **personal access token** (not your password — GitHub requires tokens for CLI operations). Create one at: [https://github.com/settings/tokens/new](https://github.com/settings/tokens/new) with `repo` scope.

## Step 3 — Enable GitHub Pages

1. On GitHub, go to your new repo: `https://github.com/vikkiecrush/vikkiecrush.github.io`
2. Click **Settings** (top nav of the repo)
3. In the left sidebar, click **Pages**
4. Under **Source**, select **Deploy from a branch**
5. Under **Branch**, choose **main** and **/ (root)**, then click **Save**
6. Wait 1-2 minutes. GitHub will show a green banner: *"Your site is live at https://vikkiecrush.github.io"*

## Step 4 — Verify

Open [https://vikkiecrush.github.io](https://vikkiecrush.github.io) in your browser.

Check:
- Hero loads with your name and title
- Nav links smooth-scroll to each section
- Both artifact cards click through to full detail pages
- Live-bot link on the Nil Pick Detective page opens ChatGPT
- Canva link on the AI/ML Evolution page opens the timeline
- LinkedIn and GitHub buttons in the footer work

---

## Making updates later

Whenever you want to update the site (add an artifact, edit your bio, fix a typo):

```bash
cd "/Users/v0i0084/portfolio-vikkiecrush"

# make your edits, then:
git add .
git commit -m "Add Artifact 3: <name>"
git push
```

GitHub Pages redeploys automatically within ~30 seconds.

---

## Troubleshooting

**"Site not found" after enabling Pages?**
Wait 5 minutes. First deploys sometimes take longer. Refresh with cache clear (Cmd+Shift+R).

**Repo name has a typo?**
The repo *must* be exactly `vikkiecrush.github.io` (lowercase). Rename via Settings > General > Rename.

**Want a custom domain later (e.g. `victoryikpe.com`)?**
Add a `CNAME` file with just the domain string in it, and configure DNS with your registrar. GitHub docs: [Custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

**Want to add a profile photo?**
Drop your image into `assets/images/profile.jpg`. Then in `index.html`, find the placeholder `VI` initials block in the hero and replace with:
```html
<img src="assets/images/profile.jpg" alt="Victory Ikpe" class="w-full h-full object-cover rounded-full" />
```
Commit, push, done.
