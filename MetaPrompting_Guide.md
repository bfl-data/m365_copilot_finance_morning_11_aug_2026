# Meta-Prompting Guide — Finance
**Microsoft Copilot Training | Bajaj Finance Limited**

---

## What Is Meta-Prompting?

Instead of writing a prompt yourself, you ask Copilot to write the prompt for you — by telling it your role, your task, and what you need.

You are essentially saying:

> *"You are a prompt expert. You know how to talk to AI. Write me a prompt I can use for my actual work."*

The output becomes your **reference prompt** — something you refine and reuse across different Finance workflows and reporting situations.

---

## The Core Meta-Prompt Formula

```
Act as a Microsoft Copilot prompt expert.
I am a [YOUR ROLE] at [COMPANY/CONTEXT].
I need to [WHAT YOU WANT TO DO].
My audience is [WHO WILL READ THE OUTPUT].
Write me a detailed, structured Copilot prompt I can use to complete this task.
The prompt should specify: role, task, context, output format, and tone.
```

---

## Meta-Prompts for Finance — Bajaj Finance

Use these as your starting point. Copy, paste, and run in Copilot. Use the output as your working prompt for your exercises.

---

### 1. Financial Statement Summarisation

```
Act as a Microsoft Copilot prompt expert.
I am a Finance Controller at Bajaj Finance Limited, an NBFC. I receive quarterly P&L data —
revenue lines, expense lines, EBITDA, PAT, PAT Margin, NIM, ROA, and Cost-to-Income Ratio —
from our financial reporting system. I need to produce a concise executive summary of the
financial statements: a quarterly performance narrative, a key ratios interpretation, and
3 management insights for the CFO.

My audience includes the CFO and the Management Committee — senior leaders who need
precise financial insight, not raw data.

Write me a detailed, structured Copilot prompt I can use to produce this financial summary.
The prompt should specify: my role, the task, what input I will provide, the exact output
format for each section, and the appropriate analytical yet concise tone.
```

---

### 2. Budget Analysis and Variance Reporting

```
Act as a Microsoft Copilot prompt expert.
I am a Finance Business Partner at Bajaj Finance Limited. I collect budget vs actuals data
across departments each quarter — covering annual budget, quarterly budget, quarterly actuals,
YTD variance in ₹ Crores, and a RAG status flag per department. I need to convert this into
a structured Budget Variance Report — classifying departments as over-budget, on-track, or
under-budget, and recommending corrective actions.

My audience is the CFO and cost centre heads who will use this for budget review meetings.

Write me a Copilot prompt I can use to produce this budget variance report. The prompt should
tell Copilot exactly what to flag, how to classify each department, and what tone to use
(analytical, action-oriented, finance-ready).
```

---

### 3. Expense Analysis and Cost Optimisation

```
Act as a Microsoft Copilot prompt expert.
I am a Finance Controller at Bajaj Finance Limited. I track monthly expense data across 14
categories — split into Fixed and Variable — covering 6 months of spend with MoM change %
and % of total spend per category. I need to identify spending patterns, flag unusual
month-on-month increases, and surface cost optimisation opportunities for the CFO and COO.

My audience is the CFO and COO — non-finance-detail, outcome-focused leaders who need
clear findings and specific recommendations.

Write me a structured Copilot prompt that will produce an expense analysis from this monthly
data. The prompt should specify format (Fixed vs Variable split + top spends + spike flags +
recommendations), tone (precise, CFO-appropriate), and what signals to surface (MoM spikes,
consistently growing categories, renegotiation candidates).
```

---

### 4. Monthly and Quarterly Financial Reporting

```
Act as a Microsoft Copilot prompt expert.
I am a Finance Lead at Bajaj Finance Limited responsible for the monthly financial reporting
pack. I track 15 KPIs monthly — including AUM, NIM, NPA ratios, PAT Margin, Cost-to-Income,
Collection Efficiency, and New Customer Acquisitions — comparing actuals vs targets with a
variance column. I need to produce a Board-ready H1 performance summary that classifies each
KPI by status, surfaces headline numbers, and includes an executive narrative.

My audience is the Board of Directors and CFO who will use this for governance review.

Write me a Copilot prompt that will produce this financial reporting summary from KPI data.
The prompt should specify format (KPI classification table + 3 headline numbers + executive
narrative paragraph), tone (Board-level, precise, authoritative), and what to prioritise
(NPA trends, PAT performance, AUM growth).
```

---

### 5. Financial Forecasting and Scenario Planning

```
Act as a Microsoft Copilot prompt expert.
I am an FP&A Manager at Bajaj Finance Limited. After completing our annual forecasting cycle,
I have three scenario projections — Base Case, Bull Case, and Bear Case — covering PAT, NII,
EBITDA, EPS, AUM, and key assumptions driving each scenario. I need to produce a structured
Forecast Planning Brief for the CFO and Strategic Planning Committee — comparing scenarios,
identifying the most sensitive assumptions, and recommending CFO decision points for H2.

My audience is the CFO, FP&A Head, and Strategy team who will use this to finalise the
annual operating plan.

Write me a Copilot prompt that will produce this forecast brief from scenario data. The prompt
should specify format (scenario comparison table + assumption sensitivity + CFO decision points
+ strategic narrative), tone (analytical, strategic, planning-focused), and what patterns to
surface (PAT gap between scenarios, key assumption levers, H2 risk triggers).
```

---

## Still Confused? Run This.

If the prompt Copilot wrote doesn't feel right — too generic, wrong format, wrong tone — don't rewrite it yourself. Use this follow-up prompt instead:

```
The prompt you wrote is a good start, but I need you to adjust it.
Here is what I want to change:

- [Describe what felt off — e.g., "the format doesn't match what my CFO expects"]
- [Describe what's missing — e.g., "it doesn't tell Copilot to flag over-budget departments"]
- [Describe the tone issue — e.g., "it sounds too detailed for a Board-level document"]

Please rewrite the prompt with these corrections.
Keep the same structure (Role / Task / Context / Format / Tone) but fix the parts I've described.
```

---

## What to Do With the Output

Once Copilot gives you a well-structured prompt:

1. **Read it** — does it reflect your actual Finance role and reporting context?
2. **Replace the placeholders** — swap generic text with your real financial data or department details.
3. **Run it** — use it on the exercise dataset provided during training.
4. **Save it** — this is your reusable reference prompt for that Finance task type.

---

*Bajaj Finance Limited | AI Academy — Finance | Microsoft Copilot Training Programme*
