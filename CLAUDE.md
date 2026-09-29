# UOM Re-enrolment Hub

A single static page (`index.html`) served by GitHub Pages. It is the playbook for KeyPath's re-enrolment calls and emails to continuing University of Melbourne (UOM) online students. Owner: Carmela (SSA manager). One advisor, who is also a full MBS SSA, does the UOM work.

## Rules

- The site is public. Never commit student names, IDs, emails or phone numbers. Student data lives in the SharePoint tracker.
- Scope is re-enrolment only. Wellbeing, academic, extension and course-advice issues are referred to the UOM student success advisers. Keep that line clear in any new content.
- Keep it one self-contained file with no build step. Google Fonts is the only external resource.
- Write in plain Australian English ("enrol", "enrolment").

## How the page works

- `const OTS=` holds the Online Term start dates from the UOM Online Academic Calendar. Every date on the Engagement Strategy tab is derived from them: application deadline = start − 7 days (pre-teaching Monday), enrolment deadline = start, census = start + 11 days, results for the previous term = start + 1 day.
- The strategy (`const S=[`) runs on the weeks of the term before the one being planned: SMS #1 (automated, week 3), call round 1 (week 5), call round 2 and mid-point email (week 6), assessment week (no cold calls), pre-teaching period (SMS #2, final calls), week 1 (deadline), week 3 (win-back after census).
- Templates `const T=[`, the advisor's week `const W={`, and the launch checklist `const C=[` are plain data arrays.
- The in-page editing (Edit page button) only works inside a Claude artifact. On GitHub Pages `window.claude` is absent, so the button stays hidden and checklist ticks save to the viewer's browser only. Changes here are made by editing `index.html`.
