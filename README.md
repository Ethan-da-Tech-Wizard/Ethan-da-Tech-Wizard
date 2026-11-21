# Ethan Kilmer

I build small Linux and AI-agent safety tools, and I write down what went wrong with them. Self-taught, early in my career.

## Featured: [TWU_Open_Release](https://github.com/Ethan-da-Tech-Wizard/TWU_Open_Release)

Six guardrail tools for people who run AI coding agents against one workspace: a local workflow engine, a staged job queue with checked receipts, network and persistence baselines, secret and personal-data scanners with git hooks, a stop latch, and write guards that stop two writers silently overwriting one file. Python standard library only.

- 480 tests across the six components (103, 107, 63, 138, 20, 49), run on macOS by me, with CI on Ubuntu and macOS. The latest run on `main` is green.
- The part I am proudest of is the recovery record: each story says what broke, how I found it, the fix, and the test that now guards it. That includes overwrites between my own agent sessions that still happened.
- They are not a security boundary. They catch accidents from cooperating processes, not a hostile one. The tests are my own and no outside party has reviewed the code. Known limits are in the repo.

## Older repositories

Each count is the repo's own test suite, re-run on 2026-11-21 from a fresh clone (Python 3.9.6 or Node 24, macOS, no installs, scratch HOME and TMPDIR). It shows those tests ran on one machine. It is not an audit.

| Repo | What it is | Tests I re-ran |
| --- | --- | --- |
| [ashr](https://github.com/Ethan-da-Tech-Wizard/ashr) | Phone-in-the-loop approval supervisor for coding agents (Node, no npm dependencies) | 219 run, 218 pass, 1 skipped |
| [relayscrub](https://github.com/Ethan-da-Tech-Wizard/relayscrub) | Offline scrubber for secrets and personal data in agent traffic (Python, stdlib) | 122 pass |
| [git-secret-shield](https://github.com/Ethan-da-Tech-Wizard/git-secret-shield) | Secret detection by patterns plus entropy, with a git hook. Experimental; it can miss secrets | 31 pass |
| [EHXTREAM_CALC](https://github.com/Ethan-da-Tech-Wizard/EHXTREAM_CALC) | Embeddable scientific and graphing calculator (JavaScript) | 64 engine tests pass (the browser test needs a browser and was not run) |
| [linux-privilege-audit-engine](https://github.com/Ethan-da-Tech-Wizard/linux-privilege-audit-engine) | Looks for unsafe privileged-execution paths in systemd, udev, cron, sudoers and launchd. Findings are leads, not proof | 51 run, 50 pass, 1 skipped on Python 3.9 (below its declared minimum). An earlier run of mine saw 1 failure in a test that depends on directory group ownership |
| [policy-command-guard](https://github.com/Ethan-da-Tech-Wizard/policy-command-guard) | Allow/deny policy for agent shell commands, tested against attack lists. Not a sandbox | 15 pass |

## How I work

AI coding agents wrote most of the code in all of these, under my direction and verification. I decide what gets built, set the acceptance rules, re-run the checks myself, and decide what I am willing to claim. When a check turns out to miss something, I fix it and record it. Most of my repositories are prototypes.

## Size of the private workspace

Measured on 2026-11-21 with a counting script I wrote. These figures describe my private, unpublished workspace, so you cannot inspect them, and they measure volume, not quality: about 930,000 lines of Python in about 2,850 files, and 14,930 test definitions (found by static count; definitions, not passes). The workspace changes daily, so this is a dated snapshot.
