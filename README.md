# Medic 1 Patient Follow-Up Site

## Structure
- `index.html` : landing page (submit or view)
- `request/` : follow-up request form
- `results/` : table of completed follow-ups
- `pdfs/` : one PDF per completed follow-up, named by follow-up number (`26-001.pdf`)
- `followups.json` : the table's data

## Posting a completed follow-up
1. Copy the PDF into `pdfs/` named exactly as the follow-up number, e.g. `pdfs/26-001.pdf`
2. Add one entry to `followups.json`:

```
[
 {"n":"26-001","c":"Cardiac arrest","p":"33M"}
]
```

`n` = follow-up number (must match the PDF filename), `c` = complaint, `p` = age/sex. Newest sorts to the top automatically.

3. Commit and push:

```
git add -A && git commit -m "Post follow-up 26-001" && git push
```

## Reminder
This repository is public. Only publication-ready case summaries go in `pdfs/`. Git history preserves anything ever pushed.
