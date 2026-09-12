# Changelog

All notable changes to this project are documented here. Format loosely follows [Keep a Changelog](https://keepachangelog.com/).

Entries tagged `[auto]` were written and committed by the scheduled daily agent described in [AUTOMATION.md](AUTOMATION.md). Entries without a tag were made manually.

## [Unreleased]

Nothing yet — the daily agent will append here.

## 2026-09-12

### Added
- [auto] Tool Radar: added aide — new package, the Advanced Intrusion Detection Environment file-integrity checker for detecting host tampering.
- [auto] Tool Radar: added gitminer — rebased onto maintained Gitminer3 upstream, fixing a GitHub secret-scanning tool that had been building from a dead v2 fork.

## 2026-09-11

### Added
- [auto] Tool Radar: added rickshell — new modular Python C2 framework for generating, encoding, catching, and interacting with reverse shells.
- [auto] Tool Radar: added vulture — new modular RF/SDR analysis platform combining signal processing with AI/ML pipelines.

## 2026-09-08

### Added
- [auto] Tool Radar: added xsser — upgraded to 1.9 with fixed dependency declarations, restoring clean installs of the XSS detection/exploitation framework.

## 2026-09-07

### Added
- [auto] Tool Radar: added wayparam — Wayback CDX param-mining tool bumped to 0.4.0, useful for building fuzz target lists from archived URLs.
- [auto] Tool Radar: added darkdump — dark-web OSINT search tool's PKGBUILD fixed for Python 3.14 venv-build breakage.

## 2026-08-24

### Added
- [auto] Tool Radar: added armitage — PKGBUILD fixed after being broken since 2022 (dead upstream source); now builds from Kali's GitLab mirror with OpenJDK 11 pinned.

## 2026-08-18

### Added
- Initial release: full single-file BlackArch Linux technical reference (`index.html`).
- Sections 00–06: overview, install (netinstall/strap/slim ISO), post-install, searchable tool arsenal, offensive workflows (external network, wireless, AD/red team, forensics), OPSEC, and advanced/troubleshooting.
- Section 07 `Drills`: six hands-on hacker challenges (recon, web enum, SQLi, hash cracking, AD lateral movement, binary reversing) scoped to isolated lab targets, each with a collapsible hint and reference solution, plus a weekly CTF-ladder cadence.
- Section 08 `Intel`: live auto-updated Tool Radar feed and a hacker trivia/field-tricks box.
- `AUTOMATION.md` documenting the daily scheduled agent that keeps the Intel feed current.
- Expanded the tool database with additional recon/webapp/OSINT entries (subfinder, httpx, arp-scan, whatweb, wpscan, mitmproxy, proxychains-ng, searchsploit, pixiewps, evil-winrm).
