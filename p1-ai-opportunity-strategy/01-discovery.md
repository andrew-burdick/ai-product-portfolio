# P1 Discovery: Kestrel Business Bank

> Kestrel Business Bank is fictional. All personas and figures are synthetic hypotheses, not research findings. In a real engagement, these would be validated through 8–10 customer and banker interviews.

## Problem statement
Relationship bankers serving SME customers struggle to recommend the right mix of products during customer conversations, because of Kestrel's broad product range, scattered product information and infrequent training. As a result, customers are passed between bankers and their needs are missed, while Kestrel holds fewer products per customer than it should. We believe this because (assumed signals, to validate) about 1 in 4 SME enquiries is handed to another banker, SME customers hold an average of 1.8 products, and a banker survey shows low confidence outside their core products. We'll know we've solved it when products per SME customer rise from 1.8 to 2.1 and handoffs per enquiry fall by 30% within 12 months, without any rise in complaints about unsuitable products.

*All figures are synthetic assumptions.*

## Strategic fit
This primarily supports priority 1, growing the SME customer base by 10%. Bankers who can confidently present Kestrel's full range turn more first conversations into lasting relationships, so new SME customers are won and kept rather than lost after a handoff.

## Personas (synthetic)

### 1. Sam Okafor: new sole trader

**Role:** Mobile mechanic, Penrith NSW. ABN registered three weeks ago.
**Snapshot:** Sam is skilled at the trade but new to running a business, and wants banking sorted so he can get on the tools.

**Jobs to be done**
- Keep business money separate from personal money
- Get paid on the spot, often at a customer's driveway
- Set money aside for tax and GST (from $75k turnover)
- Look legitimate to customers and suppliers

**Top 3 pain points**
1. Opening an account takes days and asks for paperwork he doesn't have handy *(slow onboarding)*
2. He can't tell which account or fee plan suits him, so he calls the bank *(contact-centre volume)*
3. He doesn't know what he doesn't know about tax, BAS and insurance
   - *Proxy indicators Kestrel could observe:*
     - The share of new sole traders' contact-centre and chat enquiries about GST, BAS or tax in their first 90 days
     - The share of new sole traders with no tax set-aside account or regular transfers by their first BAS due date
     - Low balances, overdraft use or dishonoured payments around ATO due dates, identified through ATO BPAY and direct debit activity
   - *Survey measure:* At 90 days, ask "I feel confident about how much to set aside for tax and GST," scored from 1 (strongly disagree) to 5 (strongly agree).
   - *Scope note:* Kestrel should give general information only, such as explainers, reminders and set-aside tools, and refer Sam to the ATO, business.gov.au, a registered tax or BAS agent, or an insurance broker. If Kestrel gives personal tax advice, it risks breaching the *Tax Agent Services Act 2009*, which is overseen by the Tax Practitioners Board. If it gives personal insurance advice, it risks providing financial product advice without the right AFSL authorisation, which ASIC regulates. Either way, Sam could be harmed and Kestrel would carry the liability. Any AI assistant must stay inside the same boundary.

**Current workarounds:** Uses his personal account for everything, a third-party card reader, a notes-app spreadsheet, and asks questions in tradie Facebook groups.

**What good looks like:** An account opened the same day he registers his ABN, a plain-English fee comparison, and automatic nudges to set aside tax.

**Where AI could help:** A guided onboarding assistant that pre-fills details from the ABN lookup and answers fee questions in plain English.
**AI risk:** Sam may treat an AI answer on tax or GST as advice, and act on it if it's wrong.

**Assumptions to validate**
- Sole traders open a business account at start-up, not months later
- A registration-platform partnership would actually reach people like Sam
- Sam would trust an AI assistant for fee and product questions

---

### 2. Karen Mitchell: growing SME owner

**Role:** Co-owner of a commercial cleaning company in Brisbane with 35 staff and about $6m turnover.
**Snapshot:** Karen is winning bigger contracts and needs a bank that keeps pace without her chasing it.

**Jobs to be done**
- Cover fortnightly payroll through lumpy client payment cycles
- Fund growth: vans, equipment, and upfront costs on new contracts
- Get quick, correct answers from one contact

**Top 3 pain points**
1. Questions outside lending get handed off to other bankers, and she has to repeat herself *(banker confidence and handoffs)*
2. Credit decisions are slow when a contract needs a fast yes
3. She has little forward view of cash flow

**Current workarounds:** Her bookkeeper builds cash flow spreadsheets from Xero. She keeps equipment finance with a second bank and emails her banker's mobile directly.

**What good looks like:** One banker who knows her business and answers across products, a 13-week cash flow view, and credit decisions within days.

**Where AI could help:** A cash flow forecast built from her transaction data, and banker prompts that surface relevant products before she asks.
**AI risk:** She may feel her data is being used to sell to her rather than to help her, and she may distrust credit outcomes she can't see explained.

**Assumptions to validate**
- Handoffs, not pricing, drive her dissatisfaction
- She'd consolidate banking with Kestrel if service improved
- She values a relationship banker more than digital self-serve

---

### 3. Daniel Park: Kestrel relationship banker

**Role:** Relationship banker at the Parramatta business banking centre. Eight years at Kestrel, with a portfolio of about 120 SMEs.
**Snapshot:** Daniel is strong on lending, stretched on everything else, and spends too much time on admin.

**Jobs to be done**
- Grow portfolio revenue and hit cross-sell targets
- Answer customer questions right the first time
- Prepare credit submissions efficiently
- Stay compliant with AML/CTF obligations and credit policy

**Top 3 pain points**
1. He isn't confident on merchant, FX and deposit products, so he hands customers off *(banker confidence, cross-sell, handoffs)*
2. Credit paperwork and CRM notes eat into time with customers
3. He can't get portfolio insights without joining the analytics team's queue *(limited Power BI capability)*

**Current workarounds:** Keeps a personal product cheat sheet, calls specialists, waits weeks for analytics requests, and relies on memory before meetings.

**What good looks like:** Arrives at every meeting prepped with a customer summary and the next best conversation to have, answers confidently across the full range, and has a self-serve portfolio view.

**Where AI could help:** An internal assistant grounded in product and policy documents, building on the productivity pilot. It could also prepare meeting briefs and answer plain-English portfolio queries.
**AI risk:** Wrong pricing or policy passed on to a customer creates conduct risk. Daniel may also worry the tool will be used to monitor or replace him.

**Assumptions to validate**
- Low product confidence is the root cause of handoffs, rather than incentives or target design
- Bankers will adopt and trust an AI tool
- Product and policy documents are accurate enough to ground the AI

## Riskiest assumptions and how I would validate them
| Assumption | Why it matters | How I would validate it |
| --- | --- | --- |
| Low product confidence, not incentives or target design, causes handoffs | If incentives drive handoffs, a knowledge tool won't fix the problem | Interview 8–10 bankers; compare handoff rates between bankers with and without recent product training |
| Product and policy documents are accurate and current enough to ground an AI assistant | An assistant grounded in wrong documents gives confidently wrong answers | Audit a sample of 50 product and policy documents for accuracy, currency and conflicts |
| Bankers will adopt and trust an AI tool | Without adoption there is no benefit, however good the tool | Four-week pilot with 10 bankers: weekly active use, a trust survey, and qualitative feedback |

## How we would measure success
- **Outcome:** products per SME customer, from 1.8 to 2.1 within 12 months
- **Proxy:** handoffs per enquiry down 30%
- **Survey:** banker confidence across the full product range (1–5 scale), measured quarterly
- **Guardrail:** no rise in complaints about unsuitable products

## Out of scope
- Tax, BAS or insurance advice (general information and referrals only)
- Automated credit decisions; any AI support for credit stays advisory, with a human decision-maker
