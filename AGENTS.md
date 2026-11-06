# AGENTS.md

This repository is a **prompt package**. It contains no software.

## What to do
1. Open `PLAYBOOK.md` (the full instructions) and follow it exactly, starting at **Section 1 (Intake)**.
2. Do all production work in the VideoExpress web app (https://app.videoexpress.ai/) with your **browser tool**.
3. Optional reading: `examples/` (finished scene maps to imitate) and `skills/ledger-films-studio/references/` (UI click map, pacing and trim, cinematography, motion graphics, multishot template).

## What NOT to do
- Do not run any commands, scripts, tests, installs, linters, Python, Node or shell.
- Do not build, validate, scan or package anything. There is no CLI.
- Do not run a capability audit, readiness check, model verification or approval gate.
- Do not ask the user for anything except the intake, a sign-in, or a Terms/credits screen they must click themselves.

## Why
Sandboxed agents tried to launch local processes for older versions and the sandbox refused them with a "process security error", which also took down the browser runtime. This package is browser-only on purpose. The only tool you need is the browser.
