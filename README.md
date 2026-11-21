# Ethan Kilmer

Self-taught, early in my career. I build Linux systems tooling and safety checks for AI coding agents, and I write down what went wrong with them. Founder of TWU LLC: https://twu.software

**AI assistance.** My code is written with AI coding agents under my direction. I choose what to build, write the specs and acceptance tests, review the output and re-run the checks myself. The numbers below measure volume, not quality.

## Featured projects

| Project | What it is | Tests (own tests, fresh clone) |
| --- | --- | --- |
| [release-kit](https://github.com/Ethan-da-Tech-Wizard/release-kit) | Scrub private values out of a folder, verify with an independent gate, and run tests in an isolated runner. Python standard library only. | 236 pass, Python 3.9 on macOS, 2026-11-21 |
| [agent-guardrails](https://github.com/Ethan-da-Tech-Wizard/agent-guardrails) | A stop latch, write guards and a secret-scan suite for running AI coding agents safely. Python standard library only. | 13 / 57 / 125 pass (stop_latch / write_guards / secret_scan_suite), Python 3.9 on macOS, 2026-11-21 |
| [linux-privilege-audit-engine](https://github.com/Ethan-da-Tech-Wizard/linux-privilege-audit-engine) | Looks for unsafe privileged-execution paths (systemd, udev, cron, sudoers, launchd). Findings are prompts for investigation, not proof. | 51 run, 50 pass, 1 skipped, Python 3.9 on macOS, 2026-11-21 |
| [git-secret-shield](https://github.com/Ethan-da-Tech-Wizard/git-secret-shield) | Secret detection with patterns plus entropy, and a git hook. Experimental; it can miss secrets. | 31 pass, Python 3.9 on macOS, 2026-11-21 |

"Pass" means the repository's own tests, written with AI agents under my direction. It is not an independent audit. A passing test run applies only to the cases and the machine tested.

## Incidents and recoveries

Large projects fail in many small ways. What I care about is noticing quickly, finding the cause, fixing it, and adding a check so it does not come back. Two examples from my own work:

- **A green gate was not enough.** My release gate reported PASS on a staged release; a separate AI review session (not a person outside the project) then found 23 issues the gate could not see, because it only finds what it was told to look for. The fix list is tracked and not all of it is applied yet. The rule I added: a green gate is never the last step. That is why [release-kit](https://github.com/Ethan-da-Tech-Wizard/release-kit) says "a PASS means nothing known was found, not that the tree is safe".
- **My own numbers were wrong.** I recomputed every derived figure in my career documents with a script and found 14 that were wrong as written. I retired each one in writing and rebuilt the documents on a ledger where every claim is marked verified, self-reported, dropped or held.

## By the numbers

Measured 2026-11-21 on one Mac with a counting script I wrote. AI-assisted; these are counts, not pass rates, and they measure volume, not quality. My workspace changes daily, so treat them as a dated snapshot.

- Over 700,000 lines of Python (712,433 physical lines in 1,982 files, not deduplicated, conflict copies excluded) in the top-level `scripts/` folder of my private workspace. Private and not published, so you cannot inspect it. Reproduce: `python3 -I volume_count.py --from-recs snapshot_walk.json` (my script and saved snapshot, kept privately).
- 18,788 test functions in 1,469 test files across that workspace, found by static counting (definitions, not passes). Deduplicated, same script, same private scope.

## Contact

ethan@twu.software | https://twu.software
