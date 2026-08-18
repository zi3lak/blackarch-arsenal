# Automation

This repo runs a **daily scheduled Claude Code agent** that keeps the "Live Tool Radar" feed (section `08_Intel` in `index.html`) current, and updates `CHANGELOG.md` in step.

## What it does, every run

1. **Checks upstream** for anything published in roughly the last 24–48h:
   - BlackArch package additions / repo changes (`blackarch/blackarch` on GitHub — commit log and new PKGBUILDs)
   - `blackarch.org` news / changelog
2. **Writes 1–3 plain-English entries** for the most notable new or updated tools: what the tool is, which BlackArch category it lives in, and the exact one-liner to install it (`pacman -S <pkg>` or `blackman -i <pkg>`).
3. **Appends** each entry inside the `<!-- INTEL_FEED_START -->` / `<!-- INTEL_FEED_END -->` markers in `index.html`, newest entry first, using the existing `.ba-box` markup — **no CSS is ever touched**.
4. **Logs the same update** as a dated `[auto]`-tagged bullet in `CHANGELOG.md`.
5. **Commits and pushes directly to `main`** with a descriptive commit message (e.g. `[auto] Intel: add <tool> to Live Tool Radar`).
6. If there's genuinely nothing new upstream that day, it **skips the commit** — no noise commits just to prove it ran.

GitHub Pages serves straight from `main`, so every push goes live automatically — no build step, no manual deploy.

## Guardrails

- The agent only ever edits content **between the intel-feed markers** and appends to `CHANGELOG.md`. It does not touch `<style>`, the JS logic, section 00–07 content, or the tool database, to keep the hand-authored reference material stable and reviewable by humans.
- Every automated commit is a normal git commit on `main` — fully visible in `git log`, revertible like any other commit.
- If upstream sources are unreachable or ambiguous, the agent does nothing rather than guess.

## Cadence

Runs once daily. See the scheduled agent's configuration for the exact time — manage it with the `/schedule` command in Claude Code (list / edit / pause / delete the routine named for this repo).

## Running it manually

You don't need to wait for the schedule. Ask Claude Code (in this repo) to "check for new BlackArch tools and update the Intel feed" and it will do the same steps on demand.

## Pausing / stopping

Use `/schedule` to list active routines and delete or pause the one targeting `blackarch-arsenal`. Deleting the schedule does not affect the repo's history — it only stops future automated runs.
