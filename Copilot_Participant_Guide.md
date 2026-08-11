# M365 Copilot — Finance Session
## Participant Hands-On Guide | FY 2026-27
**Bajaj Finance Limited | Powered by Technizer Edge**

---

> 👋 **Welcome!**
> This guide walks you through 5 live exercises using M365 Copilot Chat.
> Your trainer will demonstrate each one first — then it's your turn to try.
> All you need is access to **M365 Copilot Chat** and the shared Excel file.

---

## 📁 Your Data File

**File name:** `BFL_Finance_Copilot_Data.xlsx`

| Sheet Tab | What's Inside |
|---|---|
| `Financial Statements` | Quarterly P&L — revenue, expenses, profit, ratios |
| `Budget Analysis` | 12 departments — budget vs actuals, variance |
| `Expense Analysis` | 14 expense categories — 6-month trend |
| `Financial Reporting` | 15 KPIs — monthly actuals vs targets |
| `Financial Forecasting` | 3-scenario forecast — Base, Bull, Bear |

> 📎 **How to attach the file in Copilot Chat:**
> Type `/` in the chat box → select the Excel file → it attaches automatically

---

## ⚡ The Meta Prompt — Your Starting Point

> Before every exercise, paste this Meta Prompt first.
> Copilot will generate a ready-to-use Working Prompt for you.
> Then attach the file and run that Working Prompt.

```
Act as a Microsoft 365 Copilot prompt expert specialising in finance analysis.

I am a [YOUR ROLE] at Bajaj Finance Limited.
I need to [WHAT YOU WANT TO DO].
My audience is [WHO WILL READ THIS].
The data I have is [BRIEF DESCRIPTION OF YOUR EXCEL SHEET].

Write me a detailed, structured Copilot prompt I can use in M365 Copilot Chat.
The prompt should specify: role, task, context, data format, output format, and tone.
```

> ✏️ **Fill in the brackets before pasting.** Each exercise below gives you the exact words to use.

---

## 🔄 How Every Exercise Works

```
Step 1 → Paste the Meta Prompt (fill in your role, goal, data)
Step 2 → Read the Working Prompt Copilot generates
Step 3 → Attach the Excel file using /
Step 4 → Paste the Working Prompt → see the output
Step 5 → Try your own variation!
```

---

---

# Exercise 1 — Financial Statement Summarisation
**Sheet to use:** `Financial Statements`
**Your role:** Finance Controller
**Time:** ~10 minutes

---

### Step 1 — Paste this Meta Prompt

```
Act as a Microsoft 365 Copilot prompt expert specialising in finance analysis.

I am a Finance Controller at Bajaj Finance Limited.
I need to summarise our quarterly P&L into a concise executive brief for the CFO.
My audience is the CFO and the Management Committee.
The data I have is an Excel file with a consolidated P&L showing revenue, expenses,
EBITDA, PAT, PAT Margin, NIM, ROA, and Cost-to-Income Ratio across Q1 to Q4 of FY 2026-27.

Write me a detailed, structured Copilot prompt I can use to complete this task.
The prompt should specify: role, task, context, data format, output format, and professional tone.
```

### Step 2 — Read what Copilot generated
Take 30 seconds to read the Working Prompt. Does it mention:
- [ ] A specific role (Finance Controller / Analyst)?
- [ ] The output format (summary, table, bullet points)?
- [ ] The audience (CFO, Management Committee)?

### Step 3 — Attach the file and run
Attach `BFL_Finance_Copilot_Data.xlsx` → paste the generated Working Prompt → hit send.

### Step 4 — What to look for in the output
- Revenue trend across Q1–Q4
- PAT and PAT Margin movement
- Key ratio interpretation (NIM, ROA, Cost-to-Income)
- Management insights

### 💡 Try This Yourself
After the demo, modify the Meta Prompt and ask Copilot to:
> *"Focus only on Q3 and Q4 — identify why PAT margin improved"*

---

---

# Exercise 2 — Budget Analysis
**Sheet to use:** `Budget Analysis`
**Your role:** Finance Business Partner
**Time:** ~10 minutes

---

### Step 1 — Paste this Meta Prompt

```
Act as a Microsoft 365 Copilot prompt expert specialising in finance analysis.

I am a Finance Business Partner at Bajaj Finance Limited.
I need to review H1 budget vs actuals across all departments and identify which departments
are over-spending, under-spending, and what action to take.
My audience is the CFO and departmental cost centre heads.
The data I have is an Excel file with 12 departments showing annual budget, Q1 and Q2
budget vs actuals, YTD variance in ₹ Crores, and a status flag for each department.

Write me a detailed, structured Copilot prompt I can use to complete this task.
The prompt should specify: role, task, context, data format, output format, and professional tone.
```

### Step 2 — Read what Copilot generated
Check if the prompt asks for:
- [ ] Department-wise classification (over / on-track / under)?
- [ ] ₹ variance figures?
- [ ] A recommended action per department?

### Step 3 — Attach the file and run
Attach `BFL_Finance_Copilot_Data.xlsx` → paste the generated Working Prompt → hit send.

### Step 4 — What to look for in the output
- Which departments are over budget (🔴)
- Which are on track (🟢)
- Recommended action per department
- H2 risk flag

### 💡 Try This Yourself
> *"Which single department poses the highest risk of full-year budget overrun? Give me 3 reasons."*

---

---

# Exercise 3 — Expense Analysis
**Sheet to use:** `Expense Analysis`
**Your role:** Finance Controller
**Time:** ~10 minutes

---

### Step 1 — Paste this Meta Prompt

```
Act as a Microsoft 365 Copilot prompt expert specialising in finance analysis.

I am a Finance Controller at Bajaj Finance Limited.
I need to analyse 6 months of expense data to identify spending patterns,
unusual month-on-month increases, and cost optimisation opportunities.
My audience is the CFO and COO.
The data I have is an Excel file with 14 expense categories (Fixed and Variable)
showing monthly spend from April to September 2026, with MoM change % and % of total spend.

Write me a detailed, structured Copilot prompt I can use to complete this task.
The prompt should specify: role, task, context, data format, output format, and professional tone.
```

### Step 2 — Read what Copilot generated
Check if the prompt asks for:
- [ ] Fixed vs Variable split analysis?
- [ ] MoM spike identification?
- [ ] Cost optimisation recommendations?

### Step 3 — Attach the file and run
Attach `BFL_Finance_Copilot_Data.xlsx` → paste the generated Working Prompt → hit send.

### Step 4 — What to look for in the output
- Top 5 expense categories by spend
- Categories with consistent MoM growth
- Months with unusual spikes
- 3 cost optimisation suggestions

### 💡 Try This Yourself
> *"Which 3 Variable expenses grew the fastest in H1? What could we do to control them in H2?"*

---

---

# Exercise 4 — Financial Reporting
**Sheet to use:** `Financial Reporting`
**Your role:** Finance Lead
**Time:** ~10 minutes

---

### Step 1 — Paste this Meta Prompt

```
Act as a Microsoft 365 Copilot prompt expert specialising in finance analysis.

I am a Finance Lead at Bajaj Finance Limited responsible for the monthly reporting pack.
I need to prepare an H1 performance summary covering 15 KPIs — tracking actuals vs targets
and highlighting what is on-track, at-risk, and exceeding plan.
My audience is the Board of Directors and CFO.
The data I have is an Excel file with 15 KPIs tracked monthly from April to September 2026,
with H1 actuals, H1 targets, and a variance column.

Write me a detailed, structured Copilot prompt I can use to complete this task.
The prompt should specify: role, task, context, data format, output format, and professional tone.
```

### Step 2 — Read what Copilot generated
Check if the prompt asks for:
- [ ] KPI classification (on-track / at-risk / trailing)?
- [ ] Board-level headline numbers?
- [ ] An executive narrative paragraph?

### Step 3 — Attach the file and run
Attach `BFL_Finance_Copilot_Data.xlsx` → paste the generated Working Prompt → hit send.

### Step 4 — What to look for in the output
- Green / Amber / Red KPI classification
- 3 Board headline numbers
- Improving trends across H1
- H2 watch items

### 💡 Try This Yourself
> *"Write a 3-sentence CFO commentary on NPA trends and Collection Efficiency for the Board pack."*

---

---

# Exercise 5 — Financial Forecasting Support
**Sheet to use:** `Financial Forecasting`
**Your role:** FP&A Manager
**Time:** ~10 minutes

---

### Step 1 — Paste this Meta Prompt

```
Act as a Microsoft 365 Copilot prompt expert specialising in financial planning and analysis.

I am an FP&A Manager at Bajaj Finance Limited.
I need to review our FY 2026-27 financial forecast across three scenarios — Base, Bull, and Bear —
and prepare a structured planning brief for the CFO and Strategy team.
My audience is the CFO, FP&A Head, and Strategic Planning Committee.
The data I have is an Excel file with forecast assumptions and a projected P&L for FY 2026-27
showing PAT, NII, EBITDA, EPS, and AUM across all three scenarios with FY25-26 actuals as baseline.

Write me a detailed, structured Copilot prompt I can use to complete this task.
The prompt should specify: role, task, context, data format, output format, and professional tone.
```

### Step 2 — Read what Copilot generated
Check if the prompt asks for:
- [ ] Side-by-side scenario comparison?
- [ ] Sensitivity / key assumption analysis?
- [ ] CFO decision points?

### Step 3 — Attach the file and run
Attach `BFL_Finance_Copilot_Data.xlsx` → paste the generated Working Prompt → hit send.

### Step 4 — What to look for in the output
- Base vs Bull vs Bear comparison table
- Key assumptions driving each scenario
- Bear Case risk and PAT impact
- 3 CFO decision points for H2

### 💡 Try This Yourself
> *"What is the PAT difference between Base Case and Bear Case? What is the single biggest assumption driving that gap?"*

---

---

## 🃏 Prompt Writing Quick Reference

Use this card when writing your own prompts after the session.

| Element | Question to Ask Yourself | Example |
|---|---|---|
| **Role** | Who should Copilot act as? | "You are a Finance Controller at BFL..." |
| **Task** | What exactly do I want? | "Analyse the Q3 PAT decline..." |
| **Context** | What background does Copilot need? | "Q2 PAT was 8.4%, Q3 dropped to 7.9%..." |
| **Format** | How should the output look? | "Produce a 5-point brief with ₹ figures..." |
| **Tone** | Who is the audience? | "CFO-level, precise, no jargon..." |

---

## 📝 Notes

Use this space during the session:

**Exercise 1 — What surprised me:**

&nbsp;

**Exercise 2 — What I'd use this for at work:**

&nbsp;

**Exercise 3 — Prompt I want to try:**

&nbsp;

**Exercise 4 — Questions for the trainer:**

&nbsp;

**Exercise 5 — My biggest takeaway:**

&nbsp;

---

*Bajaj Finance Limited | M365 Copilot Finance Training | FY 2026-27*
*Delivered by Technizer Edge*
