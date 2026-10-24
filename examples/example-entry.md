# A worked example

The details here are made up. The change: a weekly job that reads a spreadsheet of unpaid invoices and prepares a reminder email for each one that is more than 14 days overdue.

## The entry

**2026-10-24, weekly invoice reminders.** A scheduled job runs every Monday at 9 am, reads the Invoices sheet and drafts one reminder per overdue invoice in my email account.

| # | Check | Mark | Note |
|---|---|---|---|
| 1 | Single home | ✅ | Due dates and amounts live only in the Invoices sheet; the job reads them each run and keeps no copy |
| 2 | Truth-checked | ✅ | Ran it once against the real sheet; it found the same 3 overdue invoices I counted by hand |
| 3 | Watched | ⚠ | Nothing tells me if the job stops running. Follow-up: add it to the weekly check of scheduled jobs (me, this week) |
| 4 | Propagated | ✅ | The list of scheduled jobs and the note on how invoicing works both mention it |
| 5 | Reversible | ✅ | Switch the schedule off; the job changes nothing in the sheet |
| 6 | Filed | ✅ | The reason (reminders were going out late or not at all) is in the invoicing note |
| 7 | Safe | ✅ | The job reads outside text (client names typed into the sheet) and gains a new power (email). Its email permission covers creating drafts only, so it can't send; every reminder waits for me to read and send it |

Verdict: **Ship with follow-up.** Add the job to the weekly check.

## Why check 7 passes here

The job's instructions say "only draft, never send", but that isn't what makes it safe. A client name in the sheet could be written to read like an instruction, and a model following it could try to send something. What makes it safe is that the account permission it holds can't send. If the job had been given full email access and told not to send, check 7 would fail and the verdict would be **Not done**.
