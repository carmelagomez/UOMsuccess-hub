# UOM Re-enrolment Hub

The playbook for re-enrolment calls and emails to continuing University of Melbourne (UOM) online students.

The hub has six sections:

- **Engagement Strategy**: the week-by-week touchpoints for each Online Term, lined up with the 2026 UOM Online Academic Calendar
- **Scripts & Templates**: emails, the call script, voicemail and the referral handover
- **Her Week**: how the advisor balances MBS and UOM work in off-peak, peak and final-push periods
- **Our Lane**: what we handle, and what goes to the UOM student success advisers
- **Tracker & Reporting**: the tracker columns and funnel measures
- **Launch Checklist**: everything to set up before the first call round

## Important: this site is public

Anyone with the link can see this page. **Never add student names, IDs, emails or phone numbers here.** Student details stay in the tracker spreadsheet on SharePoint or in the CRM.

## How to make changes

**Option 1: ask Claude.** Start a chat, say "update my UOM hub in carmelagomez/uomsuccess-hub", and describe the change, for example "move call round 2 to Wednesday" or "add a template for students taking a break". Claude edits the page and publishes it.

**Option 2: edit it yourself on GitHub.**
1. Open `index.html` in this repository and click the pencil icon (Edit this file).
2. Press Ctrl+F and search for the text you want to change.
3. Change only the words between the quote marks or tags. Leave the surrounding code alone.
4. Click **Commit changes**. The live site updates within a minute or two.

## Where things live in `index.html`

| To change | Search for |
|---|---|
| Online Term start dates | `const OTS=` |
| Engagement strategy steps and actions | `const S=[` |
| Email and call templates | `const T=[` |
| The advisor's week and typical day | `const W={` |
| Launch checklist items | `const C=[` |
| Our Lane, Tracker and intro text | the section's heading text, e.g. `We refer to the UOM SSAs` |

## Updating the academic calendar

The dates all come from the Online Term start dates in `const OTS=`. When the 2027 calendar is released, add the 2027 terms there. The application deadline, enrolment deadline, census date and every touchpoint date are worked out from those start dates.
