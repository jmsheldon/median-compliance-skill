# Offline reference

Generated from the same data the MCP server uses. This exists so the skill still works if the server is unreachable. Prefer the server, which is kept current.

Generated: 2026-08-14. Rules: 11. Coverage: US federal, Delaware, New York.


## Questions that change the answer

Settle these BEFORE deriving obligations.

### How was the company incorporated?
Formation platforms bundle services that would otherwise show up as separate annual fees, and they keep the paperwork in their own portal rather than emailing it. Stripe Atlas and Clerky both include the first year of registered agent, so a first-year company will have no registered agent fee anywhere in its books and still be perfectly fine.
- **Stripe Atlas**: First year of registered agent is included, then roughly $100/yr. EIN, founder stock and the 83(b) filing were handled at formation. Documents live in the Atlas dashboard.
- **Clerky**: First year of registered agent is included, then roughly $100/yr. Formation documents live in the Clerky account.
- **Firstbase**: Registered agent is bundled into the formation package. Documents live in the Firstbase dashboard.
- **A law firm**: Filings and confirmations usually went to the attorney, not to the founder's inbox. Expect no confirmation emails in the founder's mail and check with the firm instead.
- **Filed directly with the state**: Confirmations should be in the founder's own email, and a registered agent was either purchased separately or the founder serves as their own where the state allows it.
- **Something else**: Ask where the formation documents live.
- **Not sure**: Treat registered agent and formation-linked obligations as unresolved rather than missing.

### How are the people who work for the company paid?
An employer of record is the legal employer, so it holds the state withholding and unemployment registrations under its own entity, not the company's. A company on an EOR that has no state payroll accounts of its own is correct and compliant. The same missing signal for a company running its own payroll means a genuine registration gap.
- **Through an employer of record (Deel EOR, Remote, Velocity Global)**: The EOR holds state withholding and unemployment registrations. The company should NOT expect to have its own state payroll accounts. Do not report their absence as a gap.
- **The company runs its own payroll (Gusto, Rippling, ADP, Deel US Payroll)**: The company is the employer and must register for withholding and unemployment in each state where an employee works.
- **Through a PEO, co-employment**: Registrations may sit under the PEO's state accounts depending on the state and the arrangement. Confirm per state rather than assuming either way.
- **Contractors only, no W-2 employees**: No state payroll registrations are triggered by contractors, though 1099 reporting still applies and worker classification is worth a look.
- **Nobody is paid yet**: No payroll obligations are triggered.
- **Not sure**: Hold all state payroll registration items at depends_on. Do not guess.

### Have any company fees ever been paid personally by a founder, an investor, or an accelerator?
Compliance fees paid from a personal card never appear in the company's books. Searching the company's bank and card transactions for a franchise tax payment or a registered agent fee and finding nothing is then completely uninformative.
- **Everything goes on the company card**: Financial traces are somewhat more reliable, though still only corroborating.
- **Some things were paid personally**: Company books are not a reliable place to look for compliance evidence. Drop to the registry and document tiers and ask the founder directly.
- **An investor or accelerator covered some of it**: Same as personal payment: the trace is not in the company's books.
- **Not sure**: Treat financial traces as non-dispositive, which is the default anyway.

### What kind of physical presence does the company have in each state?
Foreign qualification turns on whether the company is transacting business in the state. A virtual mailbox is a much weaker indicator than an office or a resident employee, and using one as a mailing address does not by itself establish that a company is doing business there. Getting this wrong in either direction is a real error.
- **A leased office**: Strong indicator of transacting business. Foreign qualification is very likely required.
- **A coworking membership**: Usually a meaningful presence, though it depends on how it is used.
- **A virtual mailbox or mail forwarding address only**: Weak on its own. A mailing address is not the same as transacting business. Ask where the people actually are before concluding anything.
- **The founder works from home in that state**: Often sufficient to require foreign qualification, since the company is being operated from that state.
- **Employees there, no company location**: Usually triggers payroll registration, and often foreign qualification too.
- **No presence, remote customers only**: Customers alone generally do not require foreign qualification, though they can create sales tax nexus.

### Were any services bought for several years at once?
A registered agent bought for three years shows one charge and then nothing. Two silent years look identical to never having had an agent.
- **Yes, some services are prepaid**: Absence of an annual charge means nothing. Look for the original multi-year purchase instead.
- **No, everything renews annually**: An annual charge is a somewhat better corroborating signal.
- **Not sure**: Treat a missing annual charge as uninformative.

### What does the company sell, and is it taxable in the states where it sells?
Sales tax obligations depend on whether the product is taxable in that state, not just on revenue. New York taxes software as a service as prewritten software, while many states do not tax it at all. Registration thresholds are meaningless until taxability is settled.
- **Software as a service**: Taxable in New York and a number of other states, exempt in many. Must be resolved state by state.
- **Physical goods**: Generally taxable. Economic nexus thresholds apply.
- **Professional services**: Exempt in most states, taxable in a few.
- **Not sure**: Hold sales tax items at depends_on.

### When was the company formed?
Several obligations simply have not come due yet for a young company. A first annual report is not late if the first one is not due until next March.
- **Within the last 12 months**: Many recurring obligations have not come due yet. Bundled first-year services are common.
- **More than a year ago**: Recurring obligations should have at least one cycle of evidence behind them.
- **Not sure**: Ask, since it changes whether anything is actually late.

### Was an extension filed for the tax year under review, federal and state separately?
The deadline moves by five or six months on this answer, so assuming either way is dangerous in both directions. Assume an extension and a late filer is told they have months in hand while penalties accrue. Assume none and a founder who did everything right is told they are overdue. It also has to be asked per jurisdiction: a federal Form 7004 does nothing for a state return, and conflating the two is one of the most common founder errors there is.
- **Federal extension filed, state not confirmed**: The federal return runs to the extended date. The state return is still on its original deadline until a separate state extension is confirmed.
- **Both federal and state extensions filed**: Both returns run to their extended dates.
- **No extension was filed**: Both returns were due on their original dates and are late if not filed. Interest runs from the original date either way.
- **Not sure**: No deadline is asserted at all. Check for an accepted extension confirmation before working to any date, and be careful: an accepted extension confirmation and an accepted return confirmation look nearly identical.

### Is the company already registered to do business in each state where it operates?
Several obligations only begin once a company is registered in a state. A biennial statement, for instance, is not owed by a company that has never qualified there, so treating it as outstanding for an unregistered company is simply wrong. This is a separate question from whether registration is required.
- **Yes, registered**: The recurring obligations that follow registration are now live.
- **Not registered**: Post-registration obligations are not owed yet. The live question is whether registration is required at all.
- **Not sure**: Search the state's public entity database. For New York this settles it outright, since foreign corporations appear there with their jurisdiction of formation.

### Does any non-US person or non-US entity own part of the company?
A 25 percent or greater foreign owner of a US disregarded entity or corporation triggers Form 5472, which carries a $25,000 penalty and is one of the most commonly missed filings there is. It also determines whether the company still has any BOI reporting obligation at all.
- **Yes, there is a non-US owner**: Check Form 5472 exposure and, for foreign-formed entities, remaining BOI obligations.
- **No, all owners are US persons**: No Form 5472 from foreign ownership. No BOI reporting for a US-formed entity.
- **Not sure**: Hold Form 5472 at depends_on. The penalty is large enough that guessing is not acceptable.


## What each public registry actually shows

### Delaware Division of Corporations, General Information Name Search (ICIS)
https://icis.corp.delaware.gov/ecorp/entitysearch/NameSearch.aspx
- Exposes: entity_name, file_number, incorporation_date, entity_kind, residency
- Does NOT expose: registered_agent, good_standing, franchise_tax_status, officers, owners
- Paid only: status ($10), status_with_history ($20), good_standing_certificate ($50)

### New York Department of State, Corporation and Business Entity Database
https://apps.dos.ny.gov/publicInquiry/
- Exposes: entity_name, dos_id, initial_filing_date, county, jurisdiction_of_formation, entity_type, current_entity_status, dos_process_address, registered_agent_when_on_file, foreign_qualification_date
- Does NOT expose: good_standing_certificate, franchise_tax_status, owners


## Obligations

### Federal corporate income tax return (Form 1120) (US) `federal-1120`
Applies to: c-corp, benefit-corp
Every C corporation files Form 1120 for each tax year, whether or not it made money and whether or not it had any activity. A loss year still has to be filed, and filing is what starts the clock on carrying that loss forward.
- **Deadline**: The 15th day of the 4th month after year end, so April 15 for a calendar year. If Form 7004 was filed, a calendar-year C corporation gets to September 15 for tax year 2025, which is a 5-month extension and not the 6 months most sources quote.
- **Innocent explanations to rule out first**:
  - An extension was filed, so the return is not late yet. This is extremely common and is not a problem in itself. (common) Check: Look for an accepted Form 7004 and then check the extended deadline rather than the original one.
  - The company was formed part-way through the year and the first return is not due yet. (occasional) Check: Compare the formation date to the first tax year end.
- **If it genuinely was missed**: 5% of unpaid tax per month up to 25%, plus interest. An extension extends the time to file, never the time to pay.
- **How to prove it**:
  - [tier 2, settles it] Pull an IRS account or return transcript for the entity. This is the only source that definitively shows whether a return was accepted. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Check the tax preparer's portal (TaxDome, Canopy, Karbon) for a filed return.
  - [tier 4, corroborating only] Look for an e-file acceptance confirmation from the preparer. Be careful to distinguish an accepted EXTENSION (Form 7004) from an accepted RETURN. They look similar and are routinely confused.
- **Fix**:
  1. Confirm whether Form 7004 was accepted, and note the extended deadline it produced.
  2. If the return is still unfiled, get the books closed for the year first. The return cannot be prepared without them.
  3. File Form 1120 before the extended deadline. Interest runs on unpaid tax from the original April date regardless of the extension.
- **Source**: https://uscode.house.gov/view.xhtml?req=granuleid:USC-prelim-title26-section6081&num=0&edition=prelim (verified 2026-08-13)
- **Note**: Extension length verified against the statute: 26 USC 6081(b) substitutes 5 months for 6 months where a C corporation tax year ends December 31 and begins before January 1, 2026.

### Beneficial ownership information (BOI) report to FinCEN (US) `federal-boi`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit
This requirement is gone for US companies. On 2026-08-11 FinCEN issued a final rule permanently ending BOI reporting for entities created in the United States, and said it will delete previously reported information for US persons. Only certain foreign-formed entities registered to do business in the US still report, and they do not report US persons.
- **Deadline**: No longer applicable to US-formed entities.
- **Innocent explanations to rule out first**:
  - Plenty of checklists, blog posts and AI assistants still tell founders to file BOI. They are working from information that is now out of date. (common) Check: Read FinCEN's own announcement rather than any secondary summary.
- **How to prove it**:
  - [tier 2, settles it] No check is needed for a US-formed entity. Nothing is owed and nothing needs updating.
- **Fix**:
  1. Nothing to do if the company was formed in the United States.
  2. Ignore any reminder, invoice or solicitation asking you to file or renew a BOI report. Those solicitations were already a common scam vector and are now straightforwardly obsolete.
- **Source**: https://www.fincen.gov/news/news-releases/fincen-permanently-ends-beneficial-ownership-reporting-requirements-millions (verified 2026-08-13)
- **Note**: Corroborated against the Treasury press release and reporting in the Journal of Accountancy, Accounting Today and the ABA Banking Journal. fincen.gov was intermittently unreachable at verification time, so re-confirm at the source before citing this publicly.

### Form 5472, foreign-owned US entity information return (US) `federal-5472`
Applies to: c-corp, llc, llc-single-member, benefit-corp
If a non-US person or entity owns 25 percent or more of the company, or the company is a foreign-owned single-member LLC, Form 5472 has to be filed with a pro-forma Form 1120 to report transactions with the foreign owner. This is one of the most commonly missed filings there is, and the penalty is severe.
- **Deadline**: With the federal return, including extensions.
- **Innocent explanations to rule out first**:
  - All owners are US persons, so the form is simply not required. (common) Check: Confirm against the cap table rather than from memory.
  - A foreign investor holds well under 25 percent, which does not trigger the form. (occasional) Check: Check the actual ownership percentage on a fully diluted basis.
- **If it genuinely was missed**: $25,000 per form per year, and it applies even where no tax is owed.
- **How to prove it**:
  - [tier 3, corroborating only] Check the cap table (Carta, Pulley, AngelList) for the citizenship or domicile of holders at 25 percent or more.
  - [tier 4, corroborating only] Check whether the filed return package includes Form 5472. Ask the preparer directly, since it is a separate form that is easy to omit.
- **Fix**:
  1. Establish the ownership percentage of every non-US holder from the cap table.
  2. If any is at 25 percent or more, tell your tax preparer explicitly. Do not assume it was picked up.
  3. If prior years were missed, ask a tax adviser about the reasonable cause process before filing late, since the penalty is assessed per form per year.
- **Source**: https://www.irs.gov/forms-pubs/about-form-5472 (verified 2026-08-13)
- **Note**: Median does not currently file Form 5472. Surface the exposure and route the founder to their tax adviser.

### Federal employment tax returns (Form 941) (US) `federal-941`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit
An employer files Form 941 each quarter to report wages, withheld income tax and payroll taxes. Whether the company files this itself depends entirely on who the legal employer is.
- **Deadline**: The last day of the month after each quarter ends: April 30, July 31, October 31, January 31.
- **Innocent explanations to rule out first**:
  - An employer of record holds the employment relationship, so filings exist under the EOR's EIN rather than the company's. (common) Check: Confirm which product is in use. Deel, for instance, sells both an EOR service and a US payroll service where the client is the employer, and the answer is different for each.
  - The payroll provider files on the company's behalf and the founder never sees the forms. (common) Check: Look in the provider's tax documents section rather than in email.
- **How to prove it**:
  - [tier 2, settles it] Pull the IRS business account transcript for the employment tax periods.
  - [tier 3, settles it] Check the payroll provider's tax filings section. Gusto, Rippling and ADP all expose filed 941s directly. If the provider is acting as an EOR, you will not see filings under your own EIN and that is expected.
- **Fix**:
  1. Establish who the legal employer is before doing anything else.
  2. If the company is the employer, confirm the payroll provider is filing and depositing on time.
  3. If quarters were genuinely missed, address deposits first, since the deposit penalties accrue faster than the filing penalties.
- **Source**: https://www.irs.gov/forms-pubs/about-form-941 (verified 2026-08-13)

### Delaware annual report and franchise tax (DE) `de-annual-report-franchise-tax`
Applies to: c-corp, s-corp, benefit-corp
Every Delaware corporation files an annual report and pays franchise tax by March 1, whether or not it earned anything. The tax is the price of having the entity, not a tax on income, so a pre-revenue company still owes it.
- **Deadline**: March 1 each year, for the prior calendar year.
- **Cost**: $50 annual report fee for a non-exempt domestic corporation, plus franchise tax. The minimum franchise tax is $175 under the authorized shares method or $400 under the assumed par value capital method.
- **Innocent explanations to rule out first**:
  - The founder paid it from a personal card, so it never appears in the company's books. (common) Check: Check the Delaware portal directly rather than the company's bank feed.
  - The registered agent paid it as part of their service and billed it inside their own annual invoice. (common) Check: Check the registered agent's account or invoice detail.
  - The company was incorporated part-way through last year, so the first report is not due until next March. (occasional) Check: Compare the incorporation date to the March 1 immediately after it.
- **If it genuinely was missed**: $200 penalty plus 1.5% interest per month on the tax and penalty.
- **How to prove it**:
  - [tier 2, settles it] Log in to the Delaware Division of Corporations franchise tax portal with the file number. It shows the filing and payment history directly. https://corp.delaware.gov/paytaxes/
  - [tier 4, corroborating only] Look for a payment confirmation from the Delaware Division of Corporations, or from the registered agent if they filed it on the company's behalf.
  - [tier 5, corroborating only] Look for a payment to the State of Delaware around February each year. Treat this as corroboration only. Founders very often pay this personally, and registered agents often bundle it into their own invoice.
- **Fix**:
  1. Log in at the Delaware franchise tax portal with the corporation's file number to see exactly what is filed and paid.
  2. If the amount looks very large, recalculate using the assumed par value capital method. Delaware bills using whichever method produces the higher number, and a startup with many authorized shares and few assets is usually far better off under the second method. This single step routinely takes a bill from tens of thousands down to the low hundreds.
  3. File the report and pay before March 1 to avoid the $200 penalty and monthly interest.
- **Source**: https://corp.delaware.gov/paytaxes/ (verified 2026-08-13)

### Delaware registered agent (DE) `de-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit
A Delaware entity must continuously maintain a registered agent with a physical Delaware address to receive legal process and state notices. Losing the agent is how companies quietly fall out of good standing without ever hearing about it.
- **Deadline**: Continuous. There is no filing date, the agent simply has to exist at all times.
- **Cost**: Typically $50 to $300 per year, depending on the provider.
- **Innocent explanations to rule out first**:
  - The first year of registered agent service was included in the incorporation package. Stripe Atlas and Clerky both bundle year one, and Firstbase bundles it into its formation product. A first-year company having no separate agent fee anywhere is completely normal. (common) Check: Ask which platform the company was incorporated through.
  - The agent was prepaid for several years, so most years show no charge at all. (occasional) Check: Look for a single larger payment at formation rather than an annual one.
  - The founder pays the agent personally. (occasional) Check: Ask, or check the agent's portal.
  - Delaware's free entity search does not show the registered agent at all, so searching it and seeing nothing tells you nothing. (common) Check: Use the paid status lookup ($10) or the agent's own portal. Do not treat the free search as evidence either way.
- **How to prove it**:
  - [tier 1, corroborating only] The registered agent appears on the paid Delaware entity status lookup, NOT on the free name search. Do not conclude anything from the free search. https://icis.corp.delaware.gov/ecorp/entitysearch/NameSearch.aspx
  - [tier 3, settles it] Check the formation platform or agent account: Stripe Atlas, Clerky, Firstbase, CSC, CT Corporation, Harvard Business Services, Registered Agents Inc or Northwest. This is the fastest reliable answer.
  - [tier 5, corroborating only] Look for an annual charge from a registered agent provider. Corroboration only, and unreliable for the reasons below.
- **Fix**:
  1. Identify the current agent from the formation platform or from the paid Delaware status lookup.
  2. If there genuinely is no agent, appoint one immediately. Delaware can void the charter for failure to maintain an agent, and it is inexpensive to fix.
  3. Confirm the agent has a current contact address for you, since this is where lawsuits and state notices land.
- **Source**: https://corp.delaware.gov/agents/ (verified 2026-08-13)
- **Note**: This obligation is the single most common source of false positives in compliance tooling. A missing fee proves nothing. Never report this as a gap on the strength of a bank feed.

### New York Application for Authority (foreign qualification) (NY) `ny-foreign-qualification`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp
A company formed in another state that is transacting business in New York has to register with the New York Department of State before doing so. Until it does, it cannot bring a lawsuit in New York courts, and it can be liable for back fees and taxes for the whole unregistered period.
- **Deadline**: Before transacting business in New York.
- **Cost**: $225 statutory filing fee, plus a Certificate of Existence from the state of formation dated within the last year.
- **Innocent explanations to rule out first**:
  - The company is registered but under a slightly different legal name than the one you searched, for example with or without a trailing 'Inc.' (occasional) Check: Search the database on a partial name rather than the exact one.
  - The New York address is a virtual mailbox and nobody actually works in New York, in which case registration may genuinely not be required. (occasional) Check: Establish where the people are, not where the mail goes.
  - An attorney handled the filing and the confirmation went to them rather than to the founder. (common) Check: Ask counsel, or search the state database, which is faster.
- **If it genuinely was missed**: The company cannot maintain an action in New York courts until it registers, and New York can assess fees and taxes for the entire period it was doing business unregistered.
- **How to prove it**:
  - [tier 1, settles it] Search the company name in the New York Department of State entity database. A registered foreign corporation appears there with its jurisdiction of formation and its qualification date. Genuine absence from this database is real evidence, unlike the Delaware case. Search a few name variants before concluding, since the registered name may differ slightly from the trading name. https://apps.dos.ny.gov/publicInquiry/
  - [tier 4, corroborating only] Look for a filing receipt from the NY Department of State, or a Certificate of Authority document.
- **Fix**:
  1. Search the New York Department of State entity database first, since it settles the question in about a minute and costs nothing.
  2. If registration is genuinely needed, order a Certificate of Existence from Delaware. It has to be dated within the last year, and Delaware charges $50 for it.
  3. File the Application for Authority with the NY Department of State and pay the $225 fee.
  4. Expect the biennial statement and New York franchise tax obligations to begin once registered.
- **Source**: https://dos.ny.gov/application-authority-foreign-business-corporation (verified 2026-08-13)
- **Note**: Filing governed by NY Business Corporation Law section 1304.

### New York biennial statement (NY) `ny-biennial-statement`
Applies to: c-corp, s-corp, llc, llc-single-member, benefit-corp
Every domestic and foreign business corporation and LLC registered in New York files a short statement every two years confirming its address for service of process and its chief executive officer.
- **Deadline**: Every two years, during the calendar month in which the company originally filed or qualified. New York only accepts the filing during that month.
- **Cost**: $9.
- **Innocent explanations to rule out first**:
  - The company is not yet registered in New York, so nothing is owed. (common) Check: Settle the foreign qualification question first.
  - It is an off year. The statement is biennial, so there is a full year in the cycle where nothing is due. (common) Check: Count two-year intervals from the initial filing date.
  - The registered agent files it automatically as part of their service. (common) Check: Check the agent's portal.
- **How to prove it**:
  - [tier 1, settles it] The NY Department of State entity record shows the initial filing date, which tells you the anniversary month. Filing status for the current period is visible on the entity record. https://apps.dos.ny.gov/publicInquiry/
  - [tier 4, corroborating only] Look for a $9 receipt from the NY Department of State e-Statement service.
- **Fix**:
  1. Find the anniversary month from the initial DOS filing date on the entity record.
  2. File online through the NY Department of State e-Statement service during that month and pay $9.
- **Source**: https://dos.ny.gov/biennial-statements-business-corporations-and-limited-liability-companies (verified 2026-08-13)
- **Note**: Required by NY Business Corporation Law section 408 for corporations and LLC Law section 301(e) for LLCs.

### New York general business corporation franchise tax (Form CT-3) (NY) `ny-ct3`
Applies to: c-corp, benefit-corp
A corporation doing business in New York files a franchise tax return and owes at least a fixed dollar minimum tax, which is based on New York receipts rather than on profit. A loss-making company still owes the minimum.
- **Deadline**: Three and a half months after year end, so April 15 for a calendar year filer. Form CT-5 extends it by six months, to roughly October 15. A federal Form 7004 does nothing for New York: the state extension is a separate filing and founders conflate the two constantly.
- **Cost**: A fixed dollar minimum applies even at a loss. The amount depends on the New York receipts bracket, so check the current table on the linked page rather than assuming a figure.
- **Innocent explanations to rule out first**:
  - A CT-5 extension was filed, so the return is not late yet. (common) Check: Look for the accepted extension and work from the extended date.
  - The company genuinely has no New York nexus, because its only New York connection is a mail-forwarding address. (occasional) Check: Settle where the people actually work.
- **How to prove it**:
  - [tier 2, settles it] Check the NY Department of Taxation and Finance Online Services account for filed returns and open periods. https://www.tax.ny.gov/online/
  - [tier 4, corroborating only] Look for a filed CT-3 or an accepted CT-5 extension. As with the federal return, be careful not to mistake an accepted extension for an accepted return.
- **Fix**:
  1. Settle whether the company is doing business in New York. This drives both this return and the foreign qualification question, so answer it once.
  2. If it is, confirm whether a CT-5 extension was filed and note the extended deadline.
  3. Budget for the fixed dollar minimum tax even in a loss year.
- **Source**: https://www.tax.ny.gov/bus/ct/article9a.htm (verified 2026-08-13)
- **Note**: The fixed dollar minimum amount is deliberately not hardcoded here. The bracket table changes and an out of date figure would be worse than sending the founder to the current table.

### New York sales tax registration (NY) `ny-sales-tax-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp
A company selling taxable products or services to New York customers must register as a sales tax vendor before making taxable sales. New York treats software as a service as prewritten software, which means SaaS is taxable here even though many states exempt it.
- **Deadline**: Before making taxable sales if there is physical presence. Within 30 days of crossing the economic nexus thresholds for a remote seller.
- **Innocent explanations to rule out first**:
  - The company is well below the economic nexus thresholds and has no New York physical presence, so no registration is required. (common) Check: Check New York receipts and transaction count for the last four quarters. Both tests must be exceeded, not just one.
  - What the company sells is not taxable in New York. (occasional) Check: Confirm the product classification. SaaS is taxable in New York; most professional services are not.
- **How to prove it**:
  - [tier 2, settles it] Check for an active Certificate of Authority for sales tax in the NY Tax Department Online Services account. https://www.tax.ny.gov/online/
  - [tier 3, corroborating only] Pull revenue by customer state from Stripe or the billing system to test the economic nexus thresholds.
- **Fix**:
  1. Establish product taxability in New York first. If the product is not taxable, nothing else here matters.
  2. If there is New York physical presence and taxable sales, register as a sales tax vendor. There is no threshold to clear in that case.
  3. If there is no physical presence, test both economic nexus thresholds before registering. Registering unnecessarily creates filing obligations that are annoying to unwind.
- **Source**: https://www.tax.ny.gov/bus/st/register.htm (verified 2026-08-13)

### New York withholding and unemployment insurance registration (NY) `ny-payroll-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit
An employer with an employee working in New York registers for state income tax withholding and unemployment insurance. Who has to do this depends entirely on who the legal employer is.
- **Deadline**: Before the first payroll in the state.
- **Innocent explanations to rule out first**:
  - An employer of record is the legal employer, so the registrations exist under the EOR rather than the company. (common) Check: Confirm which product is in use. Deel sells both an EOR service and a US payroll service where the client is the employer, and the answer differs between them.
  - The payroll provider registered on the company's behalf during onboarding. (common) Check: Check the provider's tax setup section for the state account numbers.
- **How to prove it**:
  - [tier 2, settles it] Check the NY Department of Taxation and Finance and Department of Labor accounts for an active withholding and UI registration.
  - [tier 3, settles it] The payroll provider dashboard lists which state tax accounts are registered and active. This is the fastest answer. If the provider is an EOR, the company will have no accounts of its own and that is expected.
- **Fix**:
  1. Confirm the employment model before anything else, since it decides whether the company owes this at all.
  2. If the company is the employer, register for withholding with the Tax Department and for unemployment insurance with the Department of Labor.
  3. Have the payroll provider add the state account numbers so filings and deposits go out automatically.
- **Source**: https://www.tax.ny.gov/bus/wt/whtidx.htm (verified 2026-08-13)


## States not covered yet

Do not invent rules for these. Report them as uncovered and link the state's own pages.

What typically comes into play:
- Foreign qualification with the Secretary of State, if the company is transacting business there
- A registered agent in that state, which is normally required once qualified
- State income or franchise tax registration and filing
- Payroll withholding and unemployment insurance registration, if the company is the legal employer of someone working there
- Sales tax registration, if the company sells something taxable to customers there

- **California (CA)**: [Secretary of State](https://www.sos.ca.gov/business-programs) | [Tax authority](https://www.ftb.ca.gov/)
- **Texas (TX)**: [Secretary of State](https://www.sos.state.tx.us/corp/) | [Tax authority](https://comptroller.texas.gov/taxes/)
- **Florida (FL)**: [Secretary of State](https://dos.fl.gov/sunbiz/) | [Tax authority](https://floridarevenue.com/taxes/)
- **Washington (WA)**: [Secretary of State](https://www.sos.wa.gov/corporations-charities) | [Tax authority](https://dor.wa.gov/)
- **Massachusetts (MA)**: [Secretary of State](https://www.sec.state.ma.us/divisions/corporations/corporations.htm) | [Tax authority](https://www.mass.gov/orgs/massachusetts-department-of-revenue)
- **Illinois (IL)**: [Secretary of State](https://www.ilsos.gov/departments/business_services/home.html) | [Tax authority](https://tax.illinois.gov/)
- **New Jersey (NJ)**: [Secretary of State](https://www.njportal.com/DOR/BusinessFormation) | [Tax authority](https://www.nj.gov/treasury/taxation/)
- **Pennsylvania (PA)**: [Secretary of State](https://www.dos.pa.gov/BusinessCharities/Business/Pages/default.aspx) | [Tax authority](https://www.revenue.pa.gov/)
- **Colorado (CO)**: [Secretary of State](https://www.sos.state.co.us/pubs/business/main.htm) | [Tax authority](https://tax.colorado.gov/)
- **Georgia (GA)**: [Secretary of State](https://sos.ga.gov/corporations-division-georgia-secretary-state) | [Tax authority](https://dor.georgia.gov/)
