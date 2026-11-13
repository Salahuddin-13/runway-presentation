# RUNWAY — Official Slide-by-Slide Presentation Script
**INNOVASIA 2K26 · National Level Hackathon (Vasavi College of Engineering, Hyderabad)**  
**Problem Statement:** PS-04 (FinTech)  
**Team:** Innovexa  
**Project Repository:** [https://github.com/SHOCKER5919Q/runway-innovasia-2k26](https://github.com/SHOCKER5919Q/runway-innovasia-2k26)  

---

## 📋 Executive Presentation Overview

| Parameter | Specification |
| :--- | :--- |
| **Deck Format** | 17 Ultra-Clean High-Density Dark Mode FinTech Slides |
| **Presentation Target Time** | **8 to 10 Minutes** (~160–190 words/minute) |
| **Core Architecture** | **Three-State Isolation**: Actual (Cyan) × Predicted (Lime) × Simulated (Amber) |
| **Mathematical Engine** | 13-Week Cash Forecast, 4,000 Monte Carlo Paths, Single-Factor Gaussian Copula |
| **Statistical Integrity** | Split-Conformal Prediction (61% → 84% coverage), Honest Model Gate ($t = 1.29$) |
| **Regulatory Engine** | MSMED Act 2006 §15 Statutory Due Dates + Income-Tax Act §43B(h) Disallowance |
| **Technical Proof** | 285+ Automated Tests (210 Backend · 75 Frontend), ~5,000 Accounting Checks, Dual-DB Verified (SQLite & PostgreSQL) |

---

## ⏱️ Recommended Pitch Timing Map

- **Slides 01–03 (The Hook & Architecture):** 0:00 – 1:45 *(The Problem, 3-State Principle)*
- **Slides 04–07 (Real-World Liquidity & Risk):** 1:45 – 3:45 *(Nominal vs. Available Cash, 13-Week Horizon, Debtor Drift)*
- **Slides 08–10 (Signature Demo & Optimizer):** 3:45 – 5:45 *(The ₹15L Order 51-Day Funding Gap & Counterfactual Fixes)*
- **Slides 11–13 (AI Architecture & Quant Foundations):** 5:45 – 7:30 *(Deterministic Tools, Anti-Hallucination Gate, Quant Math)*
- **Slides 14–17 (Architecture, Proof & Trust):** 7:30 – 9:30 *(FastAPI/Next.js Pipeline, 285 Tests, DPDP Alignment, Closing)*

---

## Slide 01: RUNWAY
**Section:** Opening · **Slide:** 1 of 17

**🖥️ What Is On Screen:**  
*Deep dark canvas with lime ambient glow. Hero title 'RUNWAY · The financial intelligence layer for Indian MSMEs' with Team Innovexa branding.*

### 🎙️ Spoken Script (Verbatim Voice)

> "RUNWAY is a financial intelligence layer built for Indian MSMEs: micro, small and medium enterprises. Team Innovexa from Vasavi College of Engineering, Hyderabad, built it for INNOVASIA 2K26, under problem statement PS-04 in the FinTech track."
> 
> "The idea fits in three short lines on the slide. See the business as it really is. Understand where it is likely to go. Then test a decision before you make it, while it's still cheap to change your mind."
> 
> "The name says it too. A runway is how far you can go before you run out. For a small business owner, that distance is measured in cash."
> 
### 💡 Key Takeaway for Evaluators & Judges
**RUNWAY helps MSME owners see, forecast and test their financial decisions before they commit.**

### 🔍 Technical & Domain Glossary
- **MSME**: Micro, Small and Medium Enterprises. India's backbone of small manufacturers, traders and service businesses.
- **Runway**: In finance, how long a business can keep operating with the cash it has.

---

## Slide 02: Where it went vs. where it's going
**Section:** The problem · **Slide:** 2 of 17

**🖥️ What Is On Screen:**  
*Comparison headline: 'Most software shows where the money went. RUNWAY shows where it’s going.' Three practical questions displayed as interactive cards.*

### 🎙️ Spoken Script (Verbatim Voice)

> "Almost every accounting tool an MSME uses today, whether that's Tally, Vyapar or a spreadsheet, looks backwards. It's very good at telling you where the money went last month."
> 
> "The questions an owner actually loses sleep over look forward. Will I be able to pay salaries in six weeks? If my biggest customer pays late again, what happens? Should I take this big order?"
> 
> "That's the gap RUNWAY fills. It doesn't replace the books. It sits on top of them and turns history into a forward view."
> 
### 💡 Key Takeaway for Evaluators & Judges
**Existing tools record the past. RUNWAY is built to look ahead.**

---

## Slide 03: Three states, never mixed
**Section:** The core idea · **Slide:** 3 of 17

**🖥️ What Is On Screen:**  
*The Three States visual pillars: ACTUAL (Cyan, Reconciled Truth) + PREDICTED (Lime, 13-Week Copula Model) + SIMULATED (Amber, Common Random Numbers Sandbox).*

### 🎙️ Spoken Script (Verbatim Voice)

> "This is the single most important design decision in the whole project. Every number in RUNWAY belongs to exactly one of three states."
> 
> "ACTUAL is what is really happening: a reconciled ledger built from bank statements, invoices, GST registers and settlement files. Every figure traces back to a source row. It's shown in cyan as a solid line."
> 
> "PREDICTED is what is likely to happen: a probabilistic forecast, drawn in lime as a band rather than a line, because the future is a range, not a point."
> 
> "SIMULATED is what could happen if you make a particular decision. It's drawn in amber with a dashed line."
> 
> "These three are kept apart in the database, in the API and on screen. The point is simple and important: an estimate can never be mistaken for a bank balance."
> 
### 💡 Key Takeaway for Evaluators & Judges
**Reality, expectation and what-if are always kept visually and technically separate.**

### 🔍 Technical & Domain Glossary
- **Reconciled ledger**: A single record of transactions where bank entries are matched against invoices and other source documents.

---

## Slide 04: Cash you can use
**Section:** Cash, honestly · **Slide:** 4 of 17

**🖥️ What Is On Screen:**  
*Cash dichotomy graphic: Nominal Bank Balance ₹14,07,195 vs. Real Available Cash ₹4,77,221. Explaining the ₹5L lien-marked FD and ₹4.3L committed tax/payroll.*

### 🎙️ Spoken Script (Verbatim Voice)

> "Most dashboards show your bank balance and call it cash. That's misleading."
> 
> "Part of that balance may be restricted. A fixed deposit marked as a lien against a loan can't pay payroll. Part of it may already be committed: GST you've set aside, salaries due on Friday."
> 
> "So RUNWAY works out available liquidity: cash, minus restricted money, minus committed money. That's the number the home screen opens with."
> 
> "Two strict rules apply. First, overdraft headroom is shown separately, because it's credit, not cash. Second, an unpaid invoice never counts as cash, however confident you are that the customer will pay."
> 
### 💡 Key Takeaway for Evaluators & Judges
**Available cash = cash − restricted − committed. Credit and unpaid invoices are never counted as cash.**

### 🔍 Technical & Domain Glossary
- **Lien-marked**: Money pledged as security for a loan. It sits in your account but you can't spend it.
- **Liquidity**: How much money is genuinely available to meet obligations right now.

---

## Slide 05: The next 13 weeks
**Section:** Predicted · **Slide:** 5 of 17

**🖥️ What Is On Screen:**  
*Interactive 13-week cash chart: P50 median curve, P10–P90 shaded uncertainty band, and red dashed safety buffer threshold.*

### 🎙️ Spoken Script (Verbatim Voice)

> "RUNWAY projects cash over the next 13 weeks, which is one quarter. That's the horizon an owner can actually act within."
> 
> "Many forecasting tools take past balances and fit a curve. RUNWAY builds the forecast invoice by invoice instead. Over the next quarter most of the cash movement is already known: invoices you've raised, bills you owe, GST dates, payroll, rent and EMIs. Statistics are only used for the genuinely unknown part, the sales that haven't been invoiced yet."
> 
> "That projection is then simulated thousands of times using Monte Carlo. The result isn't one line but a band. P50 is the middle outcome. The P10 to P90 band covers the range where reality should land about 80% of the time. The dashed red line is the safety buffer, the minimum cash the owner wants to keep."
> 
> "There's also a subtle but important point: late payments are correlated. When the market tightens, everyone pays late together. RUNWAY models that with a shared market factor, so it doesn't underestimate the bad scenarios."
> 
### 💡 Key Takeaway for Evaluators & Judges
**A 13-week cash forecast built from real invoices, simulated thousands of times, with honest uncertainty bands.**

### 🔍 Technical & Domain Glossary
- **Monte Carlo**: Running a model thousands of times with random variation to see the full range of possible outcomes.
- **P10 / P50 / P90**: Percentiles. P50 is the middle outcome; 10% of outcomes fall below P10 and 10% above P90.

---

## Slide 06: One customer, 29% of revenue
**Section:** Customers · **Slide:** 6 of 17

**🖥️ What Is On Screen:**  
*Donut chart showing ABC Distributors accounting for 29% of total revenue, with settled payment delay drifting from 8 days to +22.4 days late.*

### 🎙️ Spoken Script (Verbatim Voice)

> "In the demo business, Sri Lakshmi Industrial Supplies, one customer stands out: ABC Distributors."
> 
> "They account for 29% of revenue and pay, on average, 22 days after the agreed terms."
> 
> "How that 22-day figure is calculated matters. It comes from 200 settled invoices only. Open invoices are deliberately left out, because an invoice that hasn't been paid yet tells you nothing about how fast someone pays. Including it would quietly bias the number."
> 
> "This is the kind of fact owners often sense but rarely see put into numbers. RUNWAY measures it."
> 
### 💡 Key Takeaway for Evaluators & Judges
**RUNWAY measures customer concentration and payment behaviour from settled invoices only.**

---

## Slide 07: The dots, already connected
**Section:** Risk centre · **Slide:** 7 of 17

**🖥️ What Is On Screen:**  
*Risk matrix linking customer concentration, ₹3.8L overdue receivables, and ₹4.1L impending GST liability into a connected warning alert.*

### 🎙️ Spoken Script (Verbatim Voice)

> "A list of facts isn't enough. What matters is how they combine. The Risk Centre connects them automatically."
> 
> "First, a buyer concentration alert: one customer carries too much of the business. Second, a receivables ageing alert: money owed is slipping further past its due dates."
> 
> "Third, the most serious one: a stress test. If the whole market slowed its payments by 30 days, this business would not survive the quarter, even after drawing its full overdraft."
> 
> "The owner didn't have to ask for any of this. The engine raised it on its own."
> 
### 💡 Key Takeaway for Evaluators & Judges
**RUNWAY combines individual signals into clear, early warnings, including stress tests.**

### 🔍 Technical & Domain Glossary
- **Stress test**: Simulating a severe but plausible shock to see whether the business can survive it.
- **Receivables ageing**: Grouping unpaid customer invoices by how overdue they are.

---

## Slide 08: The funding gap
**Section:** Scenario lab · **Slide:** 8 of 17

**🖥️ What Is On Screen:**  
*Signature timeline: ₹15L order at 18% gross margin. Day 0 accepted → Day 37 ₹12.3L materials paid → Day 88 ₹15L collected. Highlighting the 51-day funding gap.*

### 🎙️ Spoken Script (Verbatim Voice)

> "Now the signature moment. The owner is offered a new order: ₹15 lakh, at 18% margin, on 60-day payment terms."
> 
> "Most people would ask: how much profit will I make? RUNWAY asks a better question: can I survive the time it takes to get paid?"
> 
> "Here's the timeline. Around day 37, ₹12.3 lakh of raw materials has to be paid for. The customer's money arrives around day 88. That leaves a gap of about 51 days where the business has to carry the cost out of its own pocket."
> 
> "This is how profitable businesses go bust: not from losses, but from timing."
> 
### 💡 Key Takeaway for Evaluators & Judges
**A profitable order can still be dangerous. RUNWAY shows the funding gap, not just the profit.**

### 🔍 Technical & Domain Glossary
- **Funding gap**: The period between paying your costs and receiving payment from the customer.

---

## Slide 09: Same order, different financing
**Section:** Scenario lab · **Slide:** 9 of 17

**🖥️ What Is On Screen:**  
*Comparative multi-column analysis: As-Is vs. 30% Advance vs. Invoice Discounting vs. Credit Line. Shows minimum cash jumping from ₹2.10L to ₹6.24L under 30% advance.*

### 🎙️ Spoken Script (Verbatim Voice)

> "So what does that order do to the business?"
> 
> "Today, the lowest point cash is expected to reach over the quarter is ₹11.07 lakh, with a 17% chance of falling below the safety buffer."
> 
> "Accept the order as-is, and minimum cash drops to just ₹1.79 lakh. The chance of breaching the buffer jumps to 55%, worse than a coin flip."
> 
> "Now change just one thing: ask for a 30% advance. Re-run it. Minimum cash recovers to ₹6.24 lakh and the breach probability falls to 35%."
> 
> "Same order, same margin. The only difference is how it's financed. That's what testing a decision before you make it looks like."
> 
> "One technical detail makes this comparison trustworthy. The baseline and the scenario use exactly the same random draws, a technique called common random numbers. So the difference you see comes from the decision, not from simulation noise."
> 
### 💡 Key Takeaway for Evaluators & Judges
**Changing only the financing (a 30% advance) turns a risky order into a manageable one.**

### 🔍 Technical & Domain Glossary
- **Breach probability**: The chance that cash falls below the owner's chosen safety buffer at some point in the quarter.
- **Common random numbers**: Using identical random inputs for two simulations so their difference reflects only the change being tested.

---

## Slide 10: It ranks. You decide.
**Section:** Optimise · **Slide:** 10 of 17

**🖥️ What Is On Screen:**  
*Mathematical ranking card showing the utility function: utility = liquidity + profit − downside − cost, ranking alternatives against declared risk appetite.*

### 🎙️ Spoken Script (Verbatim Voice)

> "Beyond testing one idea at a time, RUNWAY can compare several options side by side: accept as-is, accept with an advance, discount the receivables, or take a loan."
> 
> "It ranks them on one risk-adjusted score. The score rewards liquidity and profit and penalises extra downside risk and financing cost. The weights come from the owner's own declared appetite for risk."
> 
> "Options that break a policy the owner has set are marked infeasible, and the screen names the exact policy they break. In the demo, two of the four options are ruled out this way."
> 
> "Importantly, the engine ranks; it never decides. Every term of the score is shown, so the owner can see why one option came out ahead."
> 
### 💡 Key Takeaway for Evaluators & Judges
**A transparent, risk-adjusted ranking of options. The final decision always stays with the owner.**

---

## Slide 11: An AI that can't invent a number
**Section:** AI copilot · **Slide:** 11 of 17

**🖥️ What Is On Screen:**  
*Four-stage security pipeline diagram: Deterministic Intent Router (22 Typed Tools) → <untrusted_data> Isolation Fencing → Numeric Verification Gate → Audited Output.*

### 🎙️ Spoken Script (Verbatim Voice)

> "RUNWAY includes an AI copilot. The owner can simply ask, in plain English, 'Should I accept a ₹15 lakh order on 60-day terms?'"
> 
> "The big risk with AI in finance is that it makes up numbers that sound confident. RUNWAY is built so that can't happen."
> 
> "Step one: the question is matched to one of 22 deterministic tools, the same calculations the rest of the app uses, before any language model gets involved. Step two: those tools return structured data. Step three: the language model only writes the explanation, using that data. Step four: every rupee figure in the reply is checked against the tool output. If even one number doesn't match, the entire reply is thrown away."
> 
> "The answer comes back labelled SIMULATED, with the evidence attached."
> 
### 💡 Key Takeaway for Evaluators & Judges
**The AI only explains numbers the system has computed. Any unverified figure gets the reply discarded.**

### 🔍 Technical & Domain Glossary
- **Deterministic tool**: A calculation that always produces the same output for the same input, with no guesswork.

---

## Slide 12: It refuses to invent accuracy
**Section:** Honesty · **Slide:** 12 of 17

**🖥️ What Is On Screen:**  
*Statistical calibration cards: Split-conformal coverage expanding from 61% to 84% (target 80%), and paired t-test card (t = 1.29) proving simpler median baseline ships.*

### 🎙️ Spoken Script (Verbatim Voice)

> "A lot of AI products only show their best results. RUNWAY measures itself and publishes what it finds, including when it isn't good enough."
> 
> "Left card: uncertainty bands. Raw prediction bands that were meant to contain the real outcome 80% of the time only did so 61% of the time. A calibration step called conformal prediction fixes that, lifting coverage to 84% against the 80% target."
> 
> "Right card: model choice. The team built a gradient-boosted machine-learning model to predict payment delays. It beat a simple per-customer median by 3.2%. But a proper statistical test gave t = 1.29, which means the improvement can't be told apart from noise. So RUNWAY ships the simpler model, and says so on screen."
> 
> "The line at the bottom sums it up: a product that only reports wins is not reporting."
> 
### 💡 Key Takeaway for Evaluators & Judges
**Accuracy is measured and published, and a simpler model wins when the complex one isn't truly better.**

### 🔍 Technical & Domain Glossary
- **Conformal calibration**: A statistical method that adjusts prediction ranges so they contain the true value as often as claimed.
- **t-statistic**: A measure of whether a difference is real. Roughly, values below 1.96 mean 'could just be chance'.

---

## Slide 13: Borrowed from quant finance
**Section:** Under the hood · **Slide:** 13 of 17

**🖥️ What Is On Screen:**  
*Eight-tile quantitative foundations grid: Single-factor copula, Common random numbers, Liquidity VaR/CVaR, Conformal calibration, HHI concentration, Robust z-score, MSMED §15 / 43B(h), and Integer paise.*

### 🎙️ Spoken Script (Verbatim Voice)

> "Under the clean interface sit techniques normally used on trading desks and in banks, adapted for a small business's cash."
> 
> "A single-factor copula models the fact that customers tend to pay late together. Common random numbers keep scenario comparisons fair. Liquidity VaR and CVaR, adapted from market risk, describe how bad a bad quarter looks and how bad it gets when it goes wrong. They're clearly labelled as operational measures, not regulatory ones."
> 
> "Conformal calibration makes the bands honest. The Herfindahl-Hirschman Index measures concentration and turns it into a plain sentence: 'your book is carried by the equivalent of 4.9 equal customers'. Robust z-scores find unusual transactions using the median, which outliers can't drag around."
> 
> "It also encodes Indian law. Under MSMED Section 15 and Income-tax Section 43B(h), payments to micro and small suppliers must be made within 15 or 45 days, and the forecast respects that."
> 
> "Finally, every amount is stored as a whole number of paise, never as a floating-point number, so not a single paisa is lost to rounding. About 5,000 automated checks confirm the books balance exactly."
> 
### 💡 Key Takeaway for Evaluators & Judges
**Serious, tested quantitative methods, explained in language an owner can act on.**

### 🔍 Technical & Domain Glossary
- **VaR / CVaR**: Value at Risk: a bad-case loss. Conditional VaR: the average loss when things go beyond that bad case.
- **HHI**: A concentration score. 1 ÷ HHI gives the 'effective number' of equally sized customers.
- **43B(h)**: An Income-tax rule: payments owed to micro and small enterprises must be made on time to be tax-deductible.

---

## Slide 14: From raw files to decisions
**Section:** Architecture · **Slide:** 14 of 17

**🖥️ What Is On Screen:**  
*End-to-end pipeline flow: 7 Ingestion Adapters → Exact-Money Unified Ledger → 3 States → Risk Engine → FastAPI (62 endpoints) / Copilot (22 tools) → Next.js 16 (21 screens).*

### 🎙️ Spoken Script (Verbatim Voice)

> "Here's how data flows through the system, left to right."
> 
> "It starts with the files a business already has: bank CSVs, Tally XML, GST registers, payment-gateway settlements or manual entries. These are parsed, fingerprinted and de-duplicated, then turned into a unified ledger where each transaction is normalised, matched to a counterparty, classified and linked to its invoice."
> 
> "From that ledger come the three states: actual, predicted and simulated. On top of them sit the risk, health and recommendation engines."
> 
> "Everything is exposed through a REST API with 62 endpoints and through the AI copilot with its 22 tools. Both feed a web app with 21 screens."
> 
> "The stack is FastAPI and SQLAlchemy in Python on the backend, and Next.js with React on the frontend. It runs on SQLite by default, so setup is a single command, and it's verified on PostgreSQL too."
> 
### 💡 Key Takeaway for Evaluators & Judges
**A clean pipeline: raw files → unified ledger → three states → risk → API and copilot → app.**

---

## Slide 15: Built, tested, verified
**Section:** Proof · **Slide:** 15 of 17

**🖥️ What Is On Screen:**  
*Six large benchmark metrics: 62 API endpoints, 21 screens, 285+ automated tests (210 backend · 75 frontend), ~5,000 accounting checks, 28 tables, 2 verified DBs (SQLite & PostgreSQL).*

### 🎙️ Spoken Script (Verbatim Voice)

> "This is working software, not a concept."
> 
> "There are 62 API endpoints and 21 screens. There are 306 automated tests: 211 on the backend and 95 on the frontend. About 5,000 accounting checks confirm that opening balance plus credits minus debits equals closing balance, exactly, every time. The data model has 28 tables."
> 
> "The same test suite passes on both SQLite and PostgreSQL. Making that work exposed three hidden bugs that SQLite silently tolerated, and the team added a schema audit so that kind of bug can't come back."
> 
### 💡 Key Takeaway for Evaluators & Judges
**A real, tested product, verified across two databases with thousands of accounting checks.**

---

## Slide 16: What it will never do
**Section:** Trust · **Slide:** 16 of 17

**🖥️ What Is On Screen:**  
*Four clear ethical boundaries: What RUNWAY will NEVER do — Move your money, Apply for credit, Change a contract, Fake a connection.*

### 🎙️ Spoken Script (Verbatim Voice)

> "Trust in a financial product also comes from clear limits."
> 
> "RUNWAY never acts on the owner's behalf. It won't move money, won't apply for credit and won't change a contract. It advises; the owner acts."
> 
> "It's also honest about integrations. It doesn't claim live connections to Account Aggregator, GST or TReDS that it doesn't have. For each connector, the Integrations screen states exactly what would be needed, including the regulatory requirements."
> 
> "When borrowing is suggested, it only comes after the free options, like asking for an advance, and its cost is always shown next to the cost of the shortfall it would cover."
> 
### 💡 Key Takeaway for Evaluators & Judges
**RUNWAY advises but never acts, and never overstates what it's connected to.**

### 🔍 Technical & Domain Glossary
- **Account Aggregator**: India's RBI-regulated framework for sharing financial data with a user's consent.
- **TReDS**: Trade Receivables Discounting System: a platform where MSMEs can sell their invoices for early payment.

---

## Slide 17: Transactions to better decisions
**Section:** Closing · **Slide:** 17 of 17

**🖥️ What Is On Screen:**  
*Grand finale trajectory: Transactions → Understanding → Foresight → Better Decisions. 'without ever pretending to know more than it does.' Team Innovexa.*

### 🎙️ Spoken Script (Verbatim Voice)

> "To bring it together: RUNWAY takes raw transactions and turns them into understanding. It turns understanding into foresight, and foresight into better decisions."
> 
> "It does all of that without ever pretending to know more than it does. Every estimate is labelled, every forecast carries its uncertainty, and every number the AI speaks has been checked."
> 
> "That's RUNWAY, from Team Innovexa. Thank you."
> 
### 💡 Key Takeaway for Evaluators & Judges
**Transactions → understanding → foresight → better decisions, honestly.**

---

