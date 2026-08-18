# BlackArch Arsenal

A single-file, no-bloat technical reference for **BlackArch Linux** — installation, post-install hardening, the 2800+ tool arsenal, real-world offensive workflows, OPSEC, and hands-on drills. Written for people who already know their way around Linux; this is not a beginner tutorial.

**Live site:** https://zi3lak.github.io/blackarch-arsenal/

This is the professional/advanced companion to [arch-linux-guide](https://github.com/zi3lak/arch-linux-guide) (the beginner-friendly, Polish-language Arch Linux guide). Where that project teaches Arch from zero, this one assumes Arch fluency and goes straight into offensive security tooling.

## What's inside

| Section | Content |
|---|---|
| `00_Overview` | Philosophy, BlackArch vs Kali, system requirements, install method matrix |
| `01_Install` | Netinstall ISO, strap-on-existing-Arch, Slim ISO — step by step |
| `02_Post-Install` | DNS, mirrors, sudo user, AUR helper, tool category install, WM setup |
| `03_Arsenal` | Searchable, filterable database of BlackArch tools by category |
| `04_Workflows` | End-to-end playbooks: external pentest, wireless, AD/red team, forensics |
| `05_OPSEC` | Network isolation, VPN/Tor routing, disk encryption, sandboxing |
| `06_Advanced` | Pacman troubleshooting, kernel hardening, Btrfs snapshots, custom ISO builds |
| `07_Drills` | Hands-on hacker challenges for isolated lab environments, with hints and reference solutions |
| `08_Intel` | **Live, auto-updated** tool radar + hacker trivia and field tricks |

## Why this exists

Static guides go stale the moment a new tool lands in the BlackArch repo. This one doesn't — see [AUTOMATION.md](AUTOMATION.md) for how a scheduled AI agent keeps the `08_Intel` feed current, every day, without a human touching the repo.

## Legal / ethical notice

Every technique, workflow, and drill in this repo is written for **authorized security testing only**: your own lab, systems you own, or engagements you're explicitly contracted for. Section `07_Drills` explicitly scopes every exercise to isolated lab targets (Metasploitable2, DVWA, OWASP Juice Shop, retired HTB/THM boxes, homemade AD labs). Using this material against systems without written authorization is illegal in most jurisdictions.

## Structure

```
index.html       # the entire guide — single file, no build step, no dependencies
CHANGELOG.md      # human-readable log of every content update
AUTOMATION.md     # how the daily auto-update agent works
LICENSE
```

No CSS framework, no JS framework, no bundler. Open `index.html` in a browser and it works. That's the point.

## Contributing

Found a stale command, a broken workflow, or a tool that deserves a mention? Open an issue or PR. Manual contributions are always welcome alongside the automated daily updates.

## License

MIT — see [LICENSE](LICENSE).
