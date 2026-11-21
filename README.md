# Ethan Kilmer

Self-taught, early in my career. I build Linux systems tooling and safety checks for AI coding agents, and I write down what went wrong with them. Founder of TWU LLC: https://twu.software

## Featured projects

| Project | What it is | Tests (own tests, fresh clone) |
| --- | --- | --- |
| [twu-public](https://github.com/Ethan-da-Tech-Wizard/twu-public) | 924 sanitized, open-source systems tools: Linux administration, systemd governors, diagnostic harnesses, and local AI agent workflows. | 924 files, independent security audit PASS (0 leaks), 2026-11-21 |
| [release-kit](https://github.com/Ethan-da-Tech-Wizard/release-kit) | Scrub private values out of a folder, verify with an independent gate, and run tests in an isolated runner. Python standard library only. | 236 pass, Python 3.9 on macOS, 2026-11-21 |
| [agent-guardrails](https://github.com/Ethan-da-Tech-Wizard/agent-guardrails) | A stop latch, write guards and a secret-scan suite for running AI coding agents safely. Python standard library only. | 13 / 57 / 125 pass (stop_latch / write_guards / secret_scan_suite), Python 3.9 on macOS, 2026-11-21 |
| [mbp14-linux-power](https://github.com/Ethan-da-Tech-Wizard/mbp14-linux-power) | Linux CPU energy performance profiles, RAPL energy accounting, and thermal stability governors for MacBook Pro 14. | 27 files, verified on hardware, 2026-11-21 |

"Pass" means the repository's own tests, written with AI agents under my direction. It is not an independent audit. A passing test run applies only to the cases and the machine tested.

## Older repositories

Each count is the repo's own test suite, re-run on 2026-11-21 from a fresh clone (Python 3.9.6 or Node 24, macOS, no installs, scratch HOME and TMPDIR). It shows those tests ran on one machine. It is not an audit.

| Repo | What it is | Tests I re-ran |
| --- | --- | --- |
| [ashr](https://github.com/Ethan-da-Tech-Wizard/ashr) | Phone-in-the-loop approval supervisor for coding agents (Node, no npm dependencies) | 219 run, 218 pass, 1 skipped |
| [relayscrub](https://github.com/Ethan-da-Tech-Wizard/relayscrub) | Offline scrubber for secrets and personal data in agent traffic (Python, stdlib) | 122 pass |
| [git-secret-shield](https://github.com/Ethan-da-Tech-Wizard/git-secret-shield) | Secret detection by patterns plus entropy, with a git hook. Experimental; it can miss secrets | 31 pass |
| [EHXTREAM_CALC](https://github.com/Ethan-da-Tech-Wizard/EHXTREAM_CALC) | Embeddable scientific and graphing calculator (JavaScript) | 64 engine tests pass; the browser test (Playwright, optional) passes 21 of 21 after a build-script fix I made |
| [linux-privilege-audit-engine](https://github.com/Ethan-da-Tech-Wizard/linux-privilege-audit-engine) | Looks for unsafe privileged-execution paths in systemd, udev, cron, sudoers and launchd. Findings are leads, not proof | 51 run, 50 pass, 1 skipped on Python 3.9 (below its declared minimum). An earlier run of mine saw 1 failure in a test that depends on directory group ownership |
| [policy-command-guard](https://github.com/Ethan-da-Tech-Wizard/policy-command-guard) | Allow/deny policy for agent shell commands, tested against attack lists. Not a sandbox | 15 pass |

## Incidents and recoveries

Large projects fail in many small ways. What I care about is noticing quickly, finding the cause, fixing it, and adding a check so it does not come back. Two examples from my own work:

- **A green gate was not enough.** My release gate reported PASS on a staged release; a separate AI review session (not a person outside the project) then found 23 issues the gate could not see, because it only finds what it was told to look for. All 23 were fixed, each with a regression test, and later independent reviews re-checked them (eight review rounds in total, each finding real bugs the previous round missed). The rule I added: a green gate is never the last step. That is why [release-kit](https://github.com/Ethan-da-Tech-Wizard/release-kit) says "a PASS means nothing known was found, not that the tree is safe".
- **My own numbers were wrong.** I recomputed every derived figure in my career documents with a script and found 14 that were wrong as written. I retired each one in writing and rebuilt the documents on a ledger where every claim is marked verified, self-reported, dropped or held.

## How I work

AI coding agents wrote most of the code in all of these, under my direction and verification. I decide what gets built, set the acceptance rules, re-run the checks myself, and decide what I am willing to claim. When a check turns out to miss something, I fix it and record it. Most of my repositories are prototypes.

## By the numbers

Measured 2026-11-21 on one Mac with a counting script I wrote. AI-assisted; these are counts, not pass rates, and they measure volume, not quality. My workspace changes daily, so treat them as a dated snapshot.

- Over 700,000 lines of Python (712,433 physical lines in 1,982 files, not deduplicated, conflict copies excluded) in the top-level `scripts/` folder of my private workspace. Private and not published, so you cannot inspect it. Reproduce: `python3 -I volume_count.py --from-recs snapshot_walk.json` (my script and saved snapshot, kept privately).
- 18,788 test functions in 1,469 test files across that workspace, found by static counting (definitions, not passes). Deduplicated, same script, same private scope.

## Contact

ethan@twu.software | https://twu.software
