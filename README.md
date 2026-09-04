# Sumayya Maqdoom — Data Science Portfolio

A single-page portfolio site (`index.html`) with a matching one-page resume (`resume.pdf`).

## Deploy to Vercel (takes about 2 minutes)

**Option A — no coding, drag and drop:**
1. Go to https://vercel.com and sign in (GitHub, Google, or email).
2. Click **Add New → Project**, then look for **"Deploy without Git"** / drag-and-drop upload on the same screen.
3. Drag this whole folder (`index.html` + `resume.pdf`) into the upload area.
4. Click **Deploy**. Vercel gives you a live URL in under a minute.

**Option B — via GitHub (recommended if you'll keep updating it):**
1. Create a new repo on GitHub, e.g. `portfolio`.
2. Add these two files (`index.html`, `resume.pdf`) to the repo root and push:
   ```
   git init
   git add index.html resume.pdf
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```
3. Go to https://vercel.com/new, import that GitHub repo.
4. Framework preset: **Other** (it's a static site, no build step needed).
5. Click **Deploy**.

Either way, the "Download resume" and "Resume (PDF)" buttons on the site link to `resume.pdf` sitting next to `index.html` — keep both files in the same folder/repo root, or they'll break.

## Editing content later

Everything is in `index.html` — one file, plain HTML/CSS/JS, no build tools or dependencies. Open it in any text editor:
- Project entries are under `<!-- PROJECTS -->`
- Experience/timeline under `<!-- EXPERIENCE -->`
- Skills matrix under `<!-- SKILLS -->`

To regenerate the resume PDF after editing content, edit `make_resume.py` and run:
```
pip install reportlab
python3 make_resume.py
```

## Using your custom domain / linking from LinkedIn

Once deployed, Vercel gives you a URL like `your-project.vercel.app`. You can add this to your LinkedIn "Featured" section and to your resume's portfolio link (update the link in `resume.pdf` by re-running `make_resume.py` with the new URL if it changes).
