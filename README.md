# IBA 250 — Born-Global AI Venture Toolkit

Password-gated GitHub Pages site for IBA 250 students. Live at:
https://marlethm.github.io/iba250-toolkit/

This is a **soft gate** (client-side password check), not real security. Fine for course
materials that aren't sensitive, but don't treat it as private.

## What's in this repo

- `index.html` — the whole site (single file: HTML, CSS, and JavaScript together).
- `step-a-brainstorming-prompt.md` — the Step A prompt, offered as a real download on the site.
- `.nojekyll` — tells GitHub Pages to serve the site as-is (required; do not delete).

## Publishing changes (after you edit index.html or add a file)

From this folder, in Terminal:

```
git add .
git commit -m "describe your change here"
git push
```

GitHub Pages rebuilds automatically 1-2 minutes after you push. Refresh the live URL
(hard refresh — Cmd+Shift+R on Mac — if you don't see the change).

## Changing the class password

1. Pick a new password.
2. In Terminal, run (replace `NEW-PASSWORD` with your real password, keep the quotes):
   ```
   python3 -c "import hashlib; print(hashlib.sha256('NEW-PASSWORD'.encode()).hexdigest())"
   ```
3. Copy the long string it prints out.
4. Open `index.html`, find this line near the bottom (search for `PASSWORD_HASH`):
   ```js
   const PASSWORD_HASH = "...";
   ```
5. Replace the text between the quotes with the string you copied.
6. Save the file, then push (see "Publishing changes" above).

The current password (as of August 2026) is `IBA250Fall2026`.

## Adding content to a "Coming soon" section (Step B, Step C, Stage 2, Stage 3, Worked Example)

Each section is one `<section class="view" id="view-...">...</section>` block inside
`index.html`. Find the one you want (e.g. `id="view-step-b"`), and replace its contents
following the same pattern as the Step A section right above it: a short intro, a card
with any fields students need to fill in, a card with the prompt itself (add a Download
button the same way Step A does, pointing at a new `.md` file you add to this folder),
and an "After you run it" checklist. Remove the `<span class="badge-soon">Coming soon</span>`
line once real content is in place.

## Verifying it still works before you push

Open `index.html` directly in your browser (double-click it) and check:

- The password screen appears and blocks the rest of the page.
- A wrong password shows an error and does not unlock it.
- The correct password unlocks the page, and reloading the page keeps it unlocked
  (until you close the browser tab).
- The left-hand menu switches between sections.
- The Step A "Download" button and "Copy" button both work.
