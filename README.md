# System Change Scorecard

Seven checks I run before calling a change to my system done.

I run my work (a small business, university and a content channel) on a set of notes, rules and automations that an AI assistant works inside every day. Changing that system is easy. Knowing a change is actually finished is harder. More than once a change looked done, but nothing was checking it, and it went out of date without anyone noticing. So I wrote this scorecard and graded every change against it.

## What it checks

| # | Check | The question |
|---|---|---|
| 1 | Single home | Does each fact live in one place only? |
| 2 | Truth-checked | Was it checked against the real source, not a note about it? |
| 3 | Watched | Will something notice if it breaks or goes stale? |
| 4 | Propagated | Was everything that depends on it updated too? |
| 5 | Reversible | Is there a clean way to undo it? |
| 6 | Filed | Is the decision written down where it belongs? |
| 7 | Safe | Does anything that runs on its own gain a new power, and if so, what stops it being misused? |

Checks 1 to 4 and 7 must pass. A miss on any of them means the change isn't done, however good the rest looks.

The full scorecard, with how to check each row and how to grade a change, is in [SCORECARD.md](SCORECARD.md). A worked example with made-up details is in [examples/example-entry.md](examples/example-entry.md).

## Who it's for

Anyone who keeps a system of their own: notes, automations, scripts, or an AI assistant with access to their files and accounts. Nothing here needs a particular tool. It's a checklist, so copy it into whatever you use.

## How I use it

When a change ships (a new rule, a scheduled job, a new permission), it gets one dated line in a log with a mark for each check and a verdict. Over time the log shows which checks I keep missing, which tells me where my system is weakest. My AI assistant grades each change it builds with me and reports the verdict before the change is called done.

If this was useful, a star helps other people find it.

## Licence

MIT. Use it, change it, share it. See [LICENSE](LICENSE).

Made by [Ong Chuan Long](https://ongchuanlong.pages.dev).
