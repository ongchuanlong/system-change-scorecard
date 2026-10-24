# System Change Scorecard

Run this when a change to how your system works ships, before you call it done. A change here means a new rule, a script, a scheduled job, an automation, an AI agent's instructions or permissions, or a change to how your notes and files are organised. Ordinary work inside the system (writing a document, answering an email) doesn't need it.

## The 7 checks

Score each one ✅ (passes), ⚠ (passes with a gap you've named) or ❌ (fails).

| # | Check | Passes when | How to check it |
|---|---|---|---|
| 1 | **Single home** (must pass) | Every fact the change relies on lives in one place, and everything else points there instead of keeping its own copy | Search for the value or phrase across your files. One live home, the rest pointing to it |
| 2 | **Truth-checked** (must pass) | Every new or changed value was checked against the real source (the live spreadsheet, the website, the account), not against another note that repeats it | Write down which source you opened and what it said. No new outside fact counts as a pass; say so |
| 3 | **Watched** (must pass) | Something will notice if the change stops working or goes out of date: a weekly check, an alert, a test, a list that gets reviewed | Name the watcher. "Nothing watches it" is a fail |
| 4 | **Propagated** (must pass) | Everything that depends on the change was updated in the same sitting: indexes, dashboards, instructions, copies that must match | List each one you touched. One left undone is a fail, or a ⚠ if it's a real question for someone else to decide |
| 5 | **Reversible** | There's a known, clean way to undo it | Name the undo: version history, a backup, a switch that turns it off |
| 6 | **Filed** | The decision and its reason are written where they belong, not left in a chat or in your head | Name the file and section |
| 7 | **Safe** (must pass) | The change gives nothing that runs on its own (a scheduled job, a script, an AI agent working unattended) a new power, such as sending, sharing, deleting, running commands, reaching the internet or scheduling, or a new source of outside text, such as emails or web pages. If it does, a hard block stops misuse: a permission it doesn't have, a rule the system enforces, a tool that isn't there. "The instructions tell it not to" doesn't count | Name the new power or outside text and the block that holds it. No new power and no outside text is a pass; say so |

Check 7 is there because an assistant that reads outside text can be steered by it. An email or a web page can carry instructions written for the AI, not for you, so anything unattended should be unable to do harm, not just told not to.

## The gate

Checks 1 to 4 and 7 must pass. A ❌ on any of them makes the verdict **Not done**, whatever the other rows say, and the change gets fixed before it's called finished.

| Verdict | When |
|---|---|
| **Ship** | All 7 ✅ |
| **Ship with follow-up** | One or more ⚠ and no ❌ on a must-pass check. Name the follow-up and who owns it |
| **Not done** | Any ❌ on checks 1 to 4 or 7 |

## The log

Keep one dated entry per change, newest first, in a file of its own. A line is enough:

```
- YYYY-MM-DD: <the change in one line>. 1 ✅ ... · 2 ✅ ... · 3 ⚠ ... · 4 ✅ ... · 5 ✅ ... · 6 ✅ ... · 7 ✅ ... **Verdict.** Follow-up: <what, who>.
```

Over time the log shows which checks you keep missing, which is where your system is weakest. A worked example is in [examples/example-entry.md](examples/example-entry.md).
