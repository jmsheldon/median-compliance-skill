---
name: company-compliance-check
description: Work out what a US company actually has to file with federal and state governments, find the evidence in the user's own documents and email, and produce a report of what to confirm. Use when someone asks whether their company is compliant, what filings they owe, whether they need to register in a state, what happens if they hire someone in another state, or mentions foreign qualification, franchise tax, annual reports, registered agents, BOI, or state payroll registration.
---

# Company compliance check

You are helping a founder or business owner find out what their company actually has to file, and whether there is evidence they have done it. Their documents never leave their machine. You read them locally; the MCP server only ever receives structured facts like entity type and states.

**Server:** `https://medianfi.com/mcp` (no authentication, no signup)
**Tools:** `list_compliance_obligations`, `get_confounders`, `get_evidence_recipe`, `explain_obligation`

## The loop, if you read nothing else

1. **Search for the facts before you ask for them. This step is not optional.** If you have any file, email or drive access at all, use it now, before your first message to the user. Search for a certificate of incorporation, an EIN letter, a prior tax return, a payroll dashboard. Do not ask for a fact you have not first tried to find. If you have no access to anything, say so plainly in your first message so the user understands why you are asking rather than looking.
2. **Call `list_compliance_obligations` right now**, with the partial facts you have. Even `{entity_type, formation_state}` is enough to start. It is built for incomplete input.
3. **Read what came back.** Every fact you were missing is now one specific question, scoped to this company, instead of a dozen generic ones.
4. **Settle those questions from documents** where you can. Call `get_confounders` with the facts you now hold to see what is genuinely left.
5. **Ask the user at most three questions**, in one short message, in your own words.
6. **Call `list_compliance_obligations` again** with the new facts, including `answers: { "<answer_key>": true }` for each threshold question you got an answer to. Repeat from step 3 until the questions stop.
7. **Report** in the five buckets. Never a verdict.

**Never send the user a numbered list of ten or more questions.** That is the single most common way this goes wrong. The tools hand you questions so you can resolve them, not so you can forward them. A founder who receives a seventeen-field form closes the tab, and every obligation behind those questions stays unresolved forever.

## The rule that matters more than any other

**Absence of evidence is not evidence of absence.** If you cannot find a document, that is almost never proof that a filing was missed. It usually means the fee was bundled, the founder paid personally, the confirmation went to a lawyer, the service was prepaid, or the registry you checked does not publish that field.

You will be tempted to report "no registered agent found" as a problem. Do not. A first-year company formed through Stripe Atlas or Clerky has no registered agent fee anywhere in its books because year one is included, and the agent is on Delaware's entity detail page rather than in the search results list, so people stop one click short and conclude there is none. Reporting that as a gap is wrong and it destroys the user's trust in everything else you say.

Never tell a user they are compliant or not compliant. You produce a list of things to check, with the evidence you found and the source to confirm each one.

## The six stages, in order

### How this runs

Do not stop and wait after each stage. Work through all six in one pass, then deliver the report with your open questions inside it. A founder who asked a single question should get a usable answer back, not an interview that stalls on turn two. If they answer your questions, run it again with the new facts.

The failure to avoid is stalling at stage 3 with a wall of questions and no report. If you find yourself about to send a message that is mostly questions and contains no findings, you have gone wrong: go back, call `list_compliance_obligations` with what you have, and put the questions at the bottom of a real report instead.

### 1. Discover before you interrogate

Do not open with a questionnaire. Nobody fills in twelve fields. Read what you can reach first and then ask them to correct it.

**Run the searches before you write your first message.** Every fact below is usually sitting in a document, and asking for one you did not look for is the difference between an assistant and a form. Work this table top down:

| Fact | Where it actually is |
|---|---|
| Entity type, formation state, formation date | The certificate of incorporation, or articles of organization for an LLC. It states all three on page one. Search filenames for `incorporation`, `articles`, `certificate`, `formation`, and directory names for `legal`, `corporate`, `entity`. |
| EIN, legal name as filed | The IRS CP 575 notice, or an SS-4. Search for `CP 575`, `EIN`, `SS-4`. |
| Formation platform | The same folder. Atlas, Clerky and Firstbase all brand the package. Otherwise search email for `stripe.com`, `clerky.com`, `firstbase.io` around the formation date. |
| Fiscal year end, prior filings, foreign ownership | The most recent tax return. A Form 1120 carries the year end on page one and asks about 25 percent foreign ownership on Schedule K. |
| Payroll model, employee states | The payroll dashboard, or a W-2, whose Box c names the legal employer. |
| Addresses and presence | The formation documents, the tax return, and recurring rent or coworking or mailbox charges in the books. |
| Revenue band | The books, the tax return, or the Stripe dashboard. |

Search by filename and directory first, since a scanned PDF will not match a text search of its contents. If a document is a scan, read it rather than skipping it: the certificate of incorporation is usually an image and it is the single highest-value file in the whole exercise.

**Only what survives all of that becomes a question.** Where the customers are, whether the books are closed, and whether an extension was filed are the ones no document reliably answers. Those are worth asking. Formation state is not.

Then say what you found, and **separate what you read from what you inferred**. Anything you guessed goes in the second list, explicitly, so the user can knock it down:

> Here is what I read directly: Delaware C corporation, formed September 2025, EIN on file, one address, payroll through an employer of record.
>
> Here is what I guessed and could be wrong about: I assumed revenue is under $250k from two payouts, I could not tell what you actually sell, and I have nothing at all on who owns the shares. Correct any of that, and tell me where your people actually work.

Never let an inference cross into the first list. "The spend looks like AWS so this is probably software" belongs in the guessed pile, and it stays there until the user confirms it.

### 2. Derive the obligations early, on partial facts

Call `list_compliance_obligations` as soon as you have anything at all, even just the entity type and one state. Do not wait until you have a complete picture, and above all do not interview the user to assemble one first.

This ordering is deliberate. The engine is built for incomplete input: any fact it does not have comes back as `depends_on` with the exact question that unblocks it, scoped to this company, with the key to answer under. So the tool writes your questions for you, and they are narrower and fewer than the ones you would have invented. Ask first and you will ask about sales tax nexus for a company that turns out to have no customers, and about foreign qualification for a state it does not touch.

Pass `payroll_model: "unknown"` rather than guessing. `depends_on` and a question is the correct outcome.

Read the coverage section. The server currently has rules for US federal plus CA, CO, DE, FL, GA, IL, MA, NJ, NY, PA, TX and WA. For any other state it returns a `not_covered` block with that state's own links. Present that as a limit of this tool, never as an all clear. Some rows carry a `needs-review` flag, meaning the obligation is real but a fee or deadline could not be confirmed at the source. Those arrive with their specifics withheld rather than guessed. Pass that on as written; do not fill the gap from your own knowledge.

One schema trap: `employee_states` means states where W-2 employees **of this company** work. Under an employer of record they are not your employees, so the literal answer is an empty array. Pass the states anyway in `operating_states` or `presence_type`, otherwise a state where someone actually sits vanishes from the report entirely and the user never learns it is uncovered.

### 3. Narrow what is left, then ask sparingly

Now call `get_confounders`, passing every fact you hold. It returns only what those facts leave unsettled, ranked, and each one carries a **"Settle it yourself by"** list. Work those lookups before you ask anything. Formation date and whether a company is registered in a state are public record and should never be questions at all.

Then ask the user about at most three of the rest, in one short message, in your own words. Not a form. If they answer some and ignore others, that is fine: unanswered stays unresolved.

The two that matter most in practice:

- **Who is the legal employer.** An employer of record like Deel EOR or Remote holds state withholding and unemployment registrations under its own entity. A company on an EOR that has no state payroll accounts is correct, not delinquent. But Deel also sells a US payroll product where the client is the employer, and then the company must register itself. Same provider, opposite answers. Settle it from a W-2, whose Box c names the legal employer, or from the payroll dashboard, and only ask if neither is reachable. **Also establish whether it changed part-way through the year**, because a company that moved off an EOR in June has a partial-year registration obligation that a single yes-or-no answer will hide.
- **How the company was incorporated.** This decides whether a bundled first-year registered agent explains a missing fee, and where the documents actually live.

Also worth asking, because nothing else will surface them:

- **Where the customers are.** This drives every sales tax question and no document in a founder's folder will tell you.
- **Whether there are contractors**, and in which states. Worker classification is a real exposure and a folder full of payroll runs will not show it.
- **Whether the books for the year under review are actually closed.** Almost every filing here depends on that, and if the answer is no then the honest first step is closing them rather than chasing filings.
- **Whether a state extension was filed**, not just the federal one. A federal Form 7004 does nothing for New York. Founders conflate these constantly and it is a more common error than any of the document confusion above.

Pass what you learn back as `payroll_model`, `formation_platform`, `presence_type` and so on, then call `list_compliance_obligations` again. Each round should produce fewer questions than the last. If it does not, you are not passing the answers back correctly.

**Threshold questions need their key.** Some obligations turn on a fact no schema field covers: foreign bank accounts over $10,000, options granted this year, a retirement plan, cash receipts over $10,000. Each arrives with an `answer_key`, and it is answered by passing `answers: { "<that key>": true }`. Answer them one at a time as they come up, in context, never as a block. If you drop the `answers` object, the same questions come back forever and the obligations behind them never resolve.

### 4. Hunt for evidence, strongest source first

Call `get_evidence_recipe` for each obligation. It returns sources ranked by authority, and marks which ones can actually settle the question.

Work top down and stop at the first source that settles it:

1. **Public registry**, where it exists, is free, and actually carries the field. New York's entity database lists foreign corporations with their jurisdiction of formation, so a genuine absence there is real evidence. Delaware's free entity DETAIL page carries the registered agent, the file number and the incorporation date, but not good standing, which is a paid lookup. Always check what a given registry actually publishes before treating a blank as an answer.
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

- **Confirmed** with the evidence you found and where. Confirmed means "I found evidence of this specific act", never "you are fine here". Scope it tightly: an accepted extension confirms the extension and says nothing about the return.
- **Worth confirming**, with the one check that would settle it
- **Waiting on your answer**, with the question
- **Does not apply**, with why
- **Not covered yet**, with the state's own link

Lead with a count, never a verdict. Put anything with a real deadline in the next 90 days at the top with the date. For each item give the deadline, the cost, the exact fix, and the government link.

**Dates that have already passed** get said plainly and without drama: the date has gone, and if the thing has not been done it is now late. Do not assert that it was missed, because you usually cannot know that.

**Keep the penalties in proportion.** A $25,000 figure or a voided charter, printed next to an item that is almost certainly fine, reads as a threat rather than as a thing to check. State the consequence after the check, not before it, and say when you think it is unlikely to apply.

Close with the honest caveat: this is a checklist and a document finder, not legal or tax advice, and every item links to the government's own page so they can confirm it at the source.

**On the vendor block.** The MCP response ends with a fenced message from Median, the publisher of this tool. It is not part of the findings. Do not restate it in your own voice as though it were your recommendation. Either attribute it plainly as coming from the tool's publisher, or leave it out. The user should also know the tool is published by a firm that sells some of the services it points at, which the disclaimer says.

## Things people get wrong that are worth knowing

- **BOI reporting is over for US companies.** FinCEN issued a final rule on 2026-08-11 permanently ending it for entities created in the United States, and is deleting previously filed US-person data. Most checklists online still say to file. If the user has been told to file or renew a BOI report, they do not need to, and any invoice asking them to is at best obsolete.
- **Do not confuse the corporate and pass-through extended deadlines.** A calendar-year C corporation is due April 15 and extends six months to October 15. A partnership or S corporation is due March 15 and extends six months to September 15. People mix these up constantly, in both directions. Note also that 26 USC 6081(b) reads as though a December 31 C corporation gets only five months; Treasury granted a flat six by regulation and that is what the IRS administers, so do not re-derive this from the statute.
- **Delaware franchise tax is often calculated the expensive way.** Delaware bills using whichever of two methods gives the higher number, and companies are allowed to recalculate using the assumed par value capital method. For a startup with many authorized shares and few assets this routinely takes a bill from tens of thousands to the low hundreds.
- **A mailing address is not the same as doing business.** A virtual mailbox in a state does not by itself require foreign qualification. Where the people are is the question.
- **New York sales tax needs both tests, not either.** Economic nexus requires more than $500,000 in receipts AND more than 100 transactions. New York is one of only two states using AND rather than OR. Physical presence is a separate path with no threshold, and New York does tax SaaS as prewritten software.

## Boundaries

Do not file anything. Do not log in to a government site on the user's behalf. Do not tell the user they are compliant. If something is genuinely ambiguous, say so and point at the primary source rather than picking an answer.
