# B2B Weekly Review Report

Interactive HTML slide deck for the B2B weekly business review.
**Live link:** https://anunaya-07.github.io/weekly-review-b2b/weekly-review-b2b.html

---

## What to do every week

### Step 1 — Update the Excel data file

Open `data for weekly review analysis.xlsx` and update the following sheets with the new week's data:

| Sheet | What to update |
|---|---|
| `Trades data` | Add all new HTM trades for the week |
| `Entity data (Distributor)` | Add any newly onboarded distributors |
| `Client Onboarding dates` | Add any newly onboarded clients |

Save and close the file before proceeding.

---

### Step 2 — Regenerate the report data

Open **Claude Code** (or ask the team member who manages this) and run the extraction script to re-read the Excel and update the report's data.

The script reads from `data for weekly review analysis.xlsx` and updates the `const D = {...}` block inside `weekly-review-b2b.html` with fresh numbers for:
- Weekly trades, GTV, unique distributors & clients
- KPI badges (this week vs last week vs 8-week average)
- Top 5 issuers and distributors
- Category-wise GTV breakdown
- Onboarding pipeline numbers

---

### Step 3 — Push to GitHub

Once the HTML file is updated, open **Terminal** and run these 3 commands:

```bash
cd "/Users/anunaya.choudhary/Windsurf Projects/Weekly Review Report"
git add "weekly-review-b2b.html"
git commit -m "Update: week of <DATE>"
git push
```

Replace `<DATE>` with the week, e.g. `May 4–10`.

The live link updates automatically within ~1 minute of the push.

---

## Files in this folder

| File | Purpose |
|---|---|
| `weekly-review-b2b.html` | The report — this is the only file that gets pushed to GitHub |
| `data for weekly review analysis.xlsx` | Source data — **do not push this to GitHub** (contains distributor/client names) |

---

## Making manual edits to the HTML

If you need to change text, colours, or slide layout directly in `weekly-review-b2b.html`:

1. Open the file in any text editor (VS Code recommended)
2. Make your changes
3. Follow **Step 3** above to push

---

## Slide structure

| Slide | Title |
|---|---|
| Cover | B2B Weekly Review |
| Slide 01 | Trades & GTV |
| Slide 02 | Onboarding Pipeline |
| Slide 03 | Distributor & Client Activity |
| Slide 04 | GTV by Issuer |
| Slide 05 | Average Order Size |
| Slide 06 | Top Distributors |
| Slide 07 | GTV by Category |
| FD Cover | Fixed Deposits |
| FD Slide 01 | Onboarded Distributors |
| FD Slide 02 | Onboarded Investors |
| FD Slide 03 | Orders vs FD Booked |

---

## Need help?

Contact the report owner or open a conversation in Claude Code with the message:
> "I have updated the trade data, can you update the analysis accordingly"
