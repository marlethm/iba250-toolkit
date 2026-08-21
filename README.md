# IBA 250 — Born-Global AI Venture Toolkit (GitHub Pages)

A single-page site (`index.html`) gated by a shared password. No student
accounts needed — just the URL and the password you give out in class.

**Important:** this is a soft gate, not real security. The password check
runs in the visitor's browser, so anyone who opens the browser's dev tools
could find the password hash and, with effort, work out or brute-force the
password. Use this only for materials that aren't sensitive if seen by an
outsider — which is what's here. Don't put anything confidential (grades,
personal student data, unpublished exams) on this page.

## 1. Publish it

```bash
# from this folder
git init
git add index.html .nojekyll README.md
git commit -m "IBA 250 toolkit: Step A"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Repo can be **public** — the password gate is the only barrier, and a
public repo means GitHub Pages works on the free plan with no extra setup.

Then: **Settings → Pages → Build and deployment → Source: Deploy from a
branch → Branch: `main` / `/(root)` → Save.** GitHub gives you a URL like
`https://<your-username>.github.io/<repo-name>/` within a minute or two.

## 2. Set your real password

The file ships with a demo password (`changeme2026`) — replace it before
you share the link.

Generate a SHA-256 hash of your chosen password:

```bash
python3 -c "import hashlib; print(hashlib.sha256('YOUR-NEW-PASSWORD'.encode()).hexdigest())"
```

Copy the 64-character result, open `index.html`, find this line near the
bottom (inside the `<script>` tag):

```js
const PASSWORD_HASH = "d4d6209550be592f2663cec93e6ed62a953b8fda4eb15b87d5bc6aad1de578ac";
```

Replace the hash with your new one, commit, and push:

```bash
git add index.html
git commit -m "Set class password"
git push
```

Pick something you can say out loud in class or post on the LMS — it
doesn't need to be a "strong" password in the security sense, since this
isn't protecting anything sensitive.

## 3. Add content for later steps

Each stage already has a placeholder section and nav entry (Step B, Step C,
Stage 2, Stage 3, Worked Example), each marked "Coming soon." To fill one
in:

1. Open `index.html` and find the matching `<section class="view" id="view-step-b">` block (swap `step-b` for the one you're editing).
2. Replace the `<span class="badge-soon">Coming soon</span>` and placeholder paragraph with real content — you can copy the structure used in the Step A section (the `.card` blocks, the `<pre id="...">` prompt block, the "before/after" cards).
3. If you add a new `<pre>` prompt block, give it a unique `id` and either reuse the existing copy button's JS by duplicating the button + a small script snippet, or ask Claude to wire it up.
4. Commit and push — GitHub Pages redeploys automatically, usually within a minute.

## 4. Testing changes before you push

Password checking uses the browser's built-in crypto, which requires a
"secure context." Double-clicking `index.html` to open it as a `file://`
page will **not** work for the password gate. Test locally with:

```bash
python3 -m http.server 8000
# then open http://localhost:8000 in a browser
```

Or just push and test on the live `github.io` URL.

## Files

- `index.html` — the whole site (single file, no build step)
- `.nojekyll` — tells GitHub Pages not to run Jekyll processing on this repo
- `README.md` — this file (not part of the published site)
