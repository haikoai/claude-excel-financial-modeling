# I connected Claude to Excel and it builds my financial models now

I drop in an old workbook, describe the deal, and it comes back with a model I can actually hand to a partner: three linked statements that balance, a DCF, sensitivity tables, board-ready waterfall charts, and a cash flow with the runway on one line. Blue inputs, black formulas, my exact format.

This repo is the setup so you can do the same.

---

## What it builds

- **DCF** — revenue to unlevered free cash flow, line by line, with both terminal-value methods (perpetuity growth and EBITDA multiple) reconciled in the same workbook.
- **WACC** — cost of debt, cost of equity, beta comps (relevered from public names), and a sensitivity grid you can audit.
- **Sensitivity tables** — two-variable data tables so the model shows the lever that actually moves value, not just a point estimate.
- **Real-estate cash flow** — a monthly strip: rental income, vacancy, bad debt, effective income, expenses, NOI, debt service, levered cash flow, DSCR.
- **Equity waterfall** — GP/LP contributions, preferred return, hurdle promotes, and the return path as a chart, ending in LP IRR and equity multiple.

## The formatting rules it follows

These are the conventions that make a model reviewable, and the reason a partner trusts the output:

- **Blue** = hardcoded inputs.
- **Black** = formulas.
- **Italic** = percentages and rates.
- **(Parentheses)** = negatives.
- Every driver lives in one cell and flows everywhere. No number is typed twice.

## How to use it

1. Open your existing workbook (or a blank one) alongside Claude.
2. Paste the master prompt below.
3. Describe the deal in plain English: the company or property, the years, the key assumptions you already know.
4. Claude returns the structure, the formulas, and the formatting. You keep your real numbers.
5. Ask it to add the sensitivity table or the waterfall chart last, once the base model ties out.

## The master prompt

You are my financial modeling analyst. Build a clean, auditable model in the conventions below. Ask me for any driver you need before you assume it.

Rules: hardcoded inputs are blue, formulas are black, percentages are italic, negatives in parentheses. Every driver lives in exactly one cell and is referenced everywhere else. Label every row. Show your terminal value two ways and reconcile them. When the base case ties out, add a two-variable sensitivity table on the drivers I name, then a waterfall chart of the return path. Do not type any number twice.

Start by asking me what we are modeling and which drivers I already know.

---

Built by **haiko**. The full walkthrough, the sample workbooks, and the rest of the "automating your job with AI" guides are at **haikoai.com**.
