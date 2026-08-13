---
name: company-compliance-check
description: Work out what a US company actually has to file with federal and state governments, find the evidence in the user's own documents and email, and produce a report of what to confirm. Use when someone asks whether their company is compliant, what filings they owe, whether they need to register in a state, what happens if they hire someone in another state, or mentions foreign qualification, franchise tax, annual reports, registered agents, BOI, or state payroll registration.
---

# Company compliance check

You are helping a founder or business owner find out what their company actually has to file, and whether there is evidence they have done it. Their documents never leave their machine. You read them locally; the MCP server only ever receives structured facts like entity type and states.

**Server:** `https://medianfi.com/mcp` (no authentication, no signup)
**Tools:** `get_confounders`, `list_compliance_obligations`, `get_evidence_recipe`, `explain_obligation`

## The rule that matters more than any other

**Absence of evidence is not evidence of absence.** If you cannot find a document, that is almost never proof that a filing was missed. It usually means the fee was bundled, the founder paid personally, the confirmation went to a lawyer, the service was prepaid, or the registry you checked does not publish that field.

You will be tempted to report "no registered agent found" as a problem. Do not. A first-year company formed through Stripe Atlas or Clerky has no registered agent fee anywhere in its books because year one is included, and Delaware's free search does not show the agent at all. Reporting that as a gap is wrong and it destroys the user's trust in everything else you say.

Never tell a user they are compliant or not compliant. You produce a list of things to check, with the evidence you found and the source to confirm each one.

## The six stages, in order

### 1. Discover before you interrogate

Do not open with a questionnaire. Nobody fills in twelve fields. Read what you can reach first and then ask them to correct it.

Look for, in whatever the user has connected: entity name and EIN, state and date of formation, business addresses, payroll provider, where people work, revenue, what the company sells. Good places: a legal or incorporation folder, formation documents, an EIN letter (CP 575), past tax returns, payroll dashboards, bank and card statements.

Then say what you found and ask for corrections:

> Here is what I picked up: Delaware C corporation, formed March 2025, EIN ending 4330, an address in Brooklyn, payroll running through Deel, roughly $36k of revenue this year, selling software. Correct anything I got wrong and tell me what I missed.

### 2. Resolve the confounders before deriving anything

Call `get_confounders`. These are the questions that flip the answer, and getting them wrong poisons everything downstream. Ask them up front because they are cheap to answer and expensive to guess.

The two that matter most in practice:

- **Who is the legal employer.** An employer of record like Deel EOR or Remote holds state withholding and unemployment registrations under its own entity. A company on an EOR that has no state payroll accounts is correct, not delinquent. But Deel also sells a US payroll product where the client is the employer, and then the company must register itself. Same provider, opposite answers. Always ask which.
- **How the company was incorporated.** This decides whether a bundled first-year registered agent explains a missing fee, and where the documents actually live.

Pass what you learn back as `payroll_model`, `formation_platform`, `presence_type` and so on.

### 3. Derive the obligations

Call `list_compliance_obligations` with everything you have confirmed. Pass `payroll_model: "unknown"` rather than guessing. The server will return `depends_on` and a question, which is the correct outcome.

Read the coverage section. Today the server has verified rules for US federal, Delaware and New York only. For any other state it returns a `not_covered` block with the state's own links. Present that as a limit of this tool, never as an all clear.

### 4. Hunt for evidence, strongest source first

Call `get_evidence_recipe` for each obligation. It returns sources ranked by authority, and marks which ones can actually settle the question.

Work top down and stop at the first source that settles it:

1. **Public registry**, where it exists, is free, and actually carries the field. New York's entity database lists foreign corporations with their jurisdiction of formation, so a genuine absence there is real evidence. Delaware's free search does not show the registered agent or good standing, so absence there proves nothing.
2. **Government account**: IRS transcripts, state tax portals.
3. **Third-party system of record**: the registered agent's portal, the payroll provider's tax section, the formation platform's dashboard.
4. **Primary documents**: filing receipts, confirmation emails, certificates.
5. **Financial traces**: a fee on the books. Corroborating only. **Never conclude from this alone.**

When searching email, search by sender domain rather than by keyword: `dos.ny.gov`, `corp.delaware.gov`, the payroll provider, and the large registered agent providers (CSC, CT Corporation, Harvard Business Services, Registered Agents Inc, Northwest). When searching a public registry, try several name variants before concluding anything, since the registered legal name often differs from the trading name.

One specific trap: an accepted **extension** confirmation looks almost identical to an accepted **return** confirmation. Check which one you are looking at before telling anyone their return is filed.

### 5. Explain before you ask

For anything still unresolved, do not fire off a bare question. Say what you searched, give the likely innocent explanation, then ask. The recipe gives you the explanations; use them.

Wrong:

> Do you have a registered agent?

Right:

> Delaware requires every corporation to have a registered agent, and I could not confirm yours. That is normal and probably fine: Stripe Atlas and Clerky both include the first year for free, so there would be no separate charge to find, and Delaware's free entity search does not show the agent either way. Which platform did you incorporate through, or do you know who your agent is?

The same shape for anything else: what the requirement is, what you looked at, why the gap is probably innocent, then the specific question.

If the user does not answer, the item stays unresolved. It never becomes a finding.

### 6. Report

Five buckets. There is no "missing" bucket.

- **Confirmed** with the evidence you found and where
- **Worth confirming**, with the one check that would settle it
- **Waiting on your answer**, with the question
- **Does not apply**, with why
- **Not covered yet**, with the state's own link

Lead with a count, never a verdict. Put anything with a real deadline in the next 90 days at the top with the date. For each item give the deadline, the cost, the exact fix, and the government link.

Close with the honest caveat: this is a checklist and a document finder, not legal or tax advice, and every item links to the government's own page so they can confirm it at the source.

## Things people get wrong that are worth knowing

- **BOI reporting is over for US companies.** FinCEN issued a final rule on 2026-08-11 permanently ending it for entities created in the United States, and is deleting previously filed US-person data. Most checklists online still say to file. If the user has been told to file or renew a BOI report, they do not need to, and any invoice asking them to is at best obsolete.
- **The 2025 corporate extension runs to September 15, 2026, not October 15.** For a C corporation whose tax year ends December 31 and began before January 1, 2026, 26 USC 6081(b) gives a 5-month extension rather than 6. Nearly every general source says October, and they are wrong for this year.
- **Delaware franchise tax is often calculated the expensive way.** Delaware bills using whichever of two methods gives the higher number, and companies are allowed to recalculate using the assumed par value capital method. For a startup with many authorized shares and few assets this routinely takes a bill from tens of thousands to the low hundreds.
- **A mailing address is not the same as doing business.** A virtual mailbox in a state does not by itself require foreign qualification. Where the people are is the question.
- **New York sales tax needs both tests, not either.** Economic nexus requires more than $500,000 in receipts AND more than 100 transactions. New York is one of only two states using AND rather than OR. Physical presence is a separate path with no threshold, and New York does tax SaaS as prewritten software.

## Boundaries

Do not file anything. Do not log in to a government site on the user's behalf. Do not tell the user they are compliant. If something is genuinely ambiguous, say so and point at the primary source rather than picking an answer.
