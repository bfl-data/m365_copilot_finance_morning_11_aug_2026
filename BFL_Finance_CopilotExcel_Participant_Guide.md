# Copilot in Excel — Participant Exercise Guide
### Formulas & Pivot Tables for the Finance Team
**Bajaj Finance Limited | M365 Copilot Training**
**File:** `BFL_Finance_Copilot_Demo.xlsx`

---

## Before You Begin

- Use **Copilot agent** to open the agent in the Copilot panel
- Add `BFL_Finance_Copilot_Demo.xlsx` from OneDrive
- Keep the Copilot panel open throughout all exercises
- The file has **25 rows of Finance Operations data** — one sheet, no formula columns yet
- Columns N–Q are intentionally blank — you will fill these using Copilot

### Dataset Overview

Each row is a **finance operations request** — an invoice, vendor payment, reconciliation, journal entry, or expense claim raised by a business unit and worked to closure by a Finance owner, against a committed SLA.

| Column | Field | Description |
|--------|-------|-------------|
| A | Request ID | Unique finance request reference (FIN-001 to FIN-025) |
| B | Business Unit | Unit that raised the finance request |
| C | BU Code | Short business-unit identifier |
| D | Region | West / Central |
| E | Finance Request Type | Invoice Processing, Vendor Payment, GL Reconciliation, Journal Entry, Expense Claim |
| F | Finance Owner | Finance analyst handling the request |
| G | Received Date | When the request was received |
| H | Cleared Date | When it was cleared/posted (blank if still open) |
| I | Actual TAT (Days) | Actual turnaround in days |
| J | SLA (Days) | Committed turnaround for that request type |
| K | Amount Band | ≤ ₹1L, ₹1–5L, ₹5–25L, ₹25L–1Cr, > ₹1Cr |
| L | Priority | Normal, High, Urgent |
| M | Status | Completed, In Progress, Escalated |
| **N–Q** | *(blank)* | **You will add these using Copilot** |

---

## Exercise 1 — Add a Formula Column: Escalation Flag

### Your Turn
Type into the Copilot panel:

```
In column N, add a formula that flags each finance request as "Escalate"
or "OK" based on its Priority and Status:
- "Escalate" if Priority is "Urgent" OR Status is "Escalated"
- "OK" for all other cases
Label the column "Escalation Flag". Apply to all 25 rows.
```

### What Copilot Will Produce
```excel
=IF(OR(L3="Urgent",M3="Escalated"),"Escalate","OK")
```
Copilot will name the column, write the formula, and fill it down to N27.

> **Discussion Point:** Which request types and amount bands attract Urgent or Escalated status? Are the high-value items (> ₹1Cr) getting the fast-track attention they need?

---

## Exercise 2 — Add a Formula Column: SLA Breach

### Your Turn
Type into the Copilot panel:

```
In column O, add a formula that checks whether each finance request
breached its SLA. Compare the Actual TAT in column I against the SLA in
column J. If Actual TAT is greater than the SLA, return "Breach".
Otherwise return "On Time". If Actual TAT is blank (request still open),
return "In Progress".
Label the column "SLA Breach". Apply to all 25 rows.
```

### What Copilot Will Produce
```excel
=IF(I3="","In Progress",IF(I3>J3,"Breach","On Time"))
```

> **Discussion Point:** Invoice Processing shows the most SLA breaches by a wide margin. What upstream factors — missing PO references, approval bottlenecks, incomplete vendor master data — tend to drive that pattern?

---

## Exercise 3 — Add a Formula Column: Ageing Days

### Your Turn
Type into the Copilot panel:

```
In column P, calculate the number of days each finance request has been
open. If the request is already cleared (column H has a date), return 0.
If it is still open, return the number of days since it was received
(column G) up to today.
Label the column "Ageing Days". Apply to all 25 rows.
```

### What Copilot Will Produce
```excel
=IF(H3<>"",0,TODAY()-DATEVALUE(G3))
```
Cleared requests show 0. Open requests show how many days they have been ageing.

> **Discussion Point:** Which open requests are ageing the most? Are the stale items concentrated in a particular owner, business unit, or request type — and do any of them carry a reconciliation break that could affect the month-end close?

---

## Exercise 4 — Add a Formula Column: TAT Category

### Your Turn
Type into the Copilot panel:

```
In column Q, classify each cleared finance request into a TAT
performance category based on how the Actual TAT (column I) compares to
the SLA (column J):
- "Fast" if TAT is 50% or less of the SLA
- "Within SLA" if TAT is within the SLA
- "Moderate Breach" if TAT exceeds SLA by up to 50%
- "Critical Breach" if TAT exceeds SLA by more than 50%
- "In Progress" if TAT is blank
Label the column "TAT Category". Apply to all 25 rows.
```

### What Copilot Will Produce
```excel
=IF(I3="","In Progress",IF(I3<=J3*0.5,"Fast",IF(I3<=J3,"Within SLA",IF(I3<=J3*1.5,"Moderate Breach","Critical Breach"))))
```

---

## Exercise 5 — Ask Copilot to Explain a Formula

### Your Turn
Copy the formula from cell **Q3** and paste it into the Copilot panel:

```
Explain this formula to me in simple terms. What does each part do?
```

### What Copilot Will Explain
> *"This formula first checks if the Actual TAT in I3 is blank — if so, the request is still In Progress. Then it checks if TAT is at most half the SLA, which means the owner cleared it very Fast. Next it checks if TAT is within the full SLA — that's Within SLA. If TAT went over the SLA but not by more than 50%, it's a Moderate Breach. Anything beyond 150% of the SLA is a Critical Breach. Each IF only runs when the previous condition wasn't true."*

---

## Exercise 6 — Create a Pivot Table: Requests by Type and Status

### Your Turn
Type into the Copilot panel:

```
Create a pivot table that shows the count of finance requests for each
Request Type, broken down by Status (Completed, In Progress, Escalated).
I want to see which request types have the most unresolved or escalated
cases.
```

### What Copilot Will Produce
A new sheet with a Pivot Table:
- **Rows:** Finance Request Type (Invoice Processing, Vendor Payment, GL Reconciliation, Journal Entry, Expense Claim)
- **Columns:** Status (Completed, In Progress, Escalated)
- **Values:** Count of Request ID

> **Discussion Point:** GL Reconciliation carries a high escalated-plus-open ratio relative to its volume (only 1 of 4 cleared). What does that signal about how reconciliation breaks are being investigated and closed ahead of the month-end?

---

## Exercise 7 — Create a Pivot Table: Average TAT by Finance Owner

### Your Turn
Type into the Copilot panel:

```
Now create a pivot table showing the average Actual TAT in days for each
Finance Owner, broken down by Request Type. I want to identify which
owners or request types are taking the longest to clear.
```

### What Copilot Will Produce
- **Rows:** Finance Owner (Pooja Nair, Rahul Sharma, Anita Desai, Vikram Joshi, Ravi Kumar)
- **Columns:** Finance Request Type
- **Values:** Average of Actual TAT (Days)

> **Discussion Point:** Anita Desai carries the highest overall average TAT (9.5 days), driven by a single > ₹1Cr Invoice Processing request that ran to 16 days. Is that a capacity issue, a high-value-approval issue, or a data-quality issue — and which request type consistently breaches SLA across multiple owners?

---

## Exercise 8 — Bonus: Ask Copilot for Insights

### Your Turn
Type into the Copilot panel:

```
Look at the data in this sheet. Which business units have the most SLA
breaches? Summarise the key finance-operations risk areas for the team
in 3 bullet points.
```

### What to Expect
Copilot will scan the data and generate a natural-language summary — no formula needed. This shows how Copilot moves from *calculation* to *analysis* to *insight* within the same Excel session.

---

## Reference: What Your Pivots Should Show

Once you've built the pivots in Exercises 6–7, sanity-check them against these figures:

- **25 finance requests total** — 18 Completed, 5 In Progress, 2 Escalated
- **Invoice Processing** is the highest-volume type (7) and the largest source of SLA breaches (6 of 10 total breaches)
- **GL Reconciliation** shows the weakest closure profile — only 1 of 4 cleared, the rest open or escalated
- **10 SLA breaches** in total: 8 in West, 2 in Central

*(Trainers: the full pre-built pivot answer key is available separately, so the participant file stays clean for the exercises.)*

---

*Bajaj Finance Limited | AI Academy — Finance Operations | Microsoft Copilot Training Programme*
