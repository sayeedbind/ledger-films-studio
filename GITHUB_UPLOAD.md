# Uploading to GitHub

Repo target: **https://github.com/sayeedbind/ledger-films-studio**

This machine has no `git` or `gh` installed, so use the GitHub website method below (no terminal needed), or install Git first for the terminal method.

---

## Option A — GitHub website (no terminal, recommended here)

1. Create the repo: go to https://github.com/new
   - **Owner:** `sayeedbind`
   - **Repository name:** `ledger-films-studio`
   - **Visibility:** Public (required — the agent reads PLAYBOOK.md from a public raw URL without login)
   - Do **not** add a README, .gitignore or licence (this folder already has them).
   - Click **Create repository**.

2. On the new empty repo page, click **Add file → Upload files**.

3. Open `C:\Users\SAYEED\Desktop\YouTube\ledger-films-studio`, select **everything inside it** — the files **and** the `docs`, `examples`, `skills` folders — and drag them into the upload box. GitHub preserves the folder structure.

   - The `.gitignore` file starts with a dot and may be hidden in Explorer. In File Explorer: **View → Show → Hidden items** to see it before dragging.

4. Commit message: `v1.0.0: LedgerFilms Studio — LONG 16:9 + SHORT 9:16 business documentary workflow`
5. Click **Commit changes**.
6. Open the repo and check the file tree matches the list below.
7. **Verify the raw URL the prompt loads actually works:**
   https://raw.githubusercontent.com/sayeedbind/ledger-films-studio/main/PLAYBOOK.md
   If it renders the playbook, you're done.
8. Optional: **Releases → Draft a new release → Choose a tag →** `v1.0.0` → **Create new tag** → **Publish release**.

---

## Option B — terminal (install Git first)

Install Git for Windows from https://git-scm.com/download/win, reopen PowerShell, then run these one at a time from `C:\Users\SAYEED\Desktop\YouTube\ledger-films-studio`:

```bash
git init
```

```bash
git add -A
```

```bash
git commit -m "v1.0.0: LedgerFilms Studio — LONG 16:9 + SHORT 9:16 business documentary workflow"
```

```bash
git branch -M main
```

```bash
git remote add origin https://github.com/sayeedbind/ledger-films-studio.git
```

```bash
git push -u origin main
```

If the repo already has content and the push is rejected, pull first:

```bash
git pull --rebase origin main
git push -u origin main
```

---

## File tree to verify

```
ledger-films-studio/
├── README.md                  ← start here (includes the paste-ready prompt)
├── SYSTEM_PROMPT.md           ← the short copy-paste prompt
├── PLAYBOOK.md                ← the full instructions the AI reads from GitHub
├── AGENTS.md                  ← "run nothing, browser only" (Codex)
├── CLAUDE.md                  ← "run nothing, browser only" (Claude Code)
├── CHANGELOG.md
├── GITHUB_UPLOAD.md           ← this file
├── .gitignore
├── docs/
│   ├── chatgpt-setup.md
│   ├── troubleshooting.md
│   └── community-entry.md     ← paste into the DualUp community page
├── examples/
│   ├── long-form-example.md
│   └── short-example.md
└── skills/
    └── ledger-films-studio/
        ├── SKILL.md
        └── references/
            ├── videoexpress-ui-map.md
            ├── fast-pacing-and-trim.md
            ├── cinematography.md
            ├── motion-graphics.md
            └── scripting-multishot.md
```

## If you rename the repo

`SYSTEM_PROMPT.md`, `README.md` and `SKILL.md` contain the literal string `sayeedbind/ledger-films-studio` in three URLs. If you pick a different repo name, find-and-replace that string in those three files before uploading.
