# Offline reference

Generated from the same data the MCP server uses, so the skill still works if the server is unreachable. Prefer the server: it is corrected centrally and this snapshot goes stale.

Generated 2026-08-14. 156 obligations across 13 jurisdictions: US, DE, NY, CA, TX, FL, PA, CO, GA, WA, MA, IL, NJ.

Rows marked NOT FULLY VERIFIED carry a real obligation whose fee or deadline could not be confirmed at the source. Their specifics are withheld on purpose. Do not fill the gap from your own knowledge; send the reader to the source link.


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

### A few yes or no questions about things only you can know.
Some obligations turn on a fact that does not show up in any document a tool can read: whether you hold foreign bank accounts over $10,000, whether you granted options this year, whether you sponsor a retirement plan, whether you took more than $10,000 in cash. Without an answer these either get shown to everyone, which is noise, or get hidden from everyone, which is worse. So they are asked.
- **Yes**: The obligation applies and its deadline and penalty are shown.
- **No**: The obligation is marked as not applying to you and drops out of the report.
- **Not sure**: It stays an open question. It is never treated as either applying or not applying.

### Does any non-US person or non-US entity own part of the company?
A 25 percent or greater foreign owner of a US disregarded entity or corporation triggers Form 5472, which carries a $25,000 penalty and is one of the most commonly missed filings there is. It also determines whether the company still has any BOI reporting obligation at all.
- **Yes, there is a non-US owner**: Check Form 5472 exposure and, for foreign-formed entities, remaining BOI obligations.
- **No, all owners are US persons**: No Form 5472 from foreign ownership. No BOI reporting for a US-formed entity.
- **Not sure**: Hold Form 5472 at depends_on. The penalty is large enough that guessing is not acceptable.


## What each public registry actually shows

Verified by running real searches, not from documentation. States publish more free than most people assume.

### CA: California Secretary of State bizfile Online Business Search
https://bizfileonline.sos.ca.gov/search/business
- Exposes free: entity_name, entity_number, initial_filing_date, status, entity_type, jurisdiction_of_formation, agent_for_service_of_process_name, standing_sos, standing_ftb, standing_agent, standing_vcfcf, principal_address, mailing_address, statement_of_information_due_date, section_1505_corporate_agent_authorized_employees, free_pdf_images_of_statements_of_information_and_other_filings
- Does NOT expose: certified_certificate_of_status, limited_liability_partnership_records, general_partnership_records, association_records, federal_ein, officer_or_director_name_search, corporate_income_or_franchise_tax_amounts, sellers_permit_or_sales_tax_registration_status, edd_payroll_or_unemployment_registration_status, workers_compensation_coverage, shareholder_or_member_ownership, financial_statements
- Paid: certificate_of_status ($5), special_handling_fee_for_certificates_and_certified_or_uncertified_copies ($10), substituted_service_of_process_through_secretary_of_state ($50)

### CO: Colorado Secretary of State Business Database Search
https://www.coloradosos.gov/biz/BusinessEntityCriteriaExt.do
- Exposes free: entity name, entity ID number, entity type, status including Good Standing, Delinquent and Noncompliant, formation date, registered agent name plus Colorado street address and a separate mailing address, principal office street address and mailing address as two separate fields, periodic report month, shown on the Summary page, which neither Pennsylvania nor Georgia has an equivalent of, filed document images, downloadable free with no login, certificate of good standing, generated free with no login and no payment, search by registered agent, reserved-name holder, trade-name registrant or trademark registrant
- Does NOT expose: officers, directors, members or managers for any entity type, including LLCs and corporations, search by officer, beneficial ownership, ownership percentages, the registered agent's Colorado ID used for the post July 1 2025 verification, a certificate of good standing link on a delinquent record, where the link disappears rather than erroring

### DE: Delaware Division of Corporations, General Information Name Search (ICIS)
https://icis.corp.delaware.gov/ecorp/entitysearch/NameSearch.aspx
- Exposes free: entity_name, file_number, incorporation_date, entity_kind, residency, registered_agent, registered_agent_address
- Does NOT expose: good_standing, franchise_tax_status, officers, owners
- Paid: status ($10), status_with_history ($20), good_standing_certificate ($50)

### FL: Florida Division of Corporations Sunbiz Search Records
https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
- Exposes free: entity_name, document_number, fei_ein_number, date_filed, state_of_formation, status, last_event, event_date_filed, principal_address, mailing_address, registered_agent_name_and_address, registered_agent_name_changed_date, registered_agent_address_changed_date, officer_and_director_names_titles_and_addresses, annual_report_years_and_filed_dates, free_pdf_images_of_annual_reports_and_other_filings, search_by_entity_name, search_by_officer_or_registered_agent, search_by_registered_agent_name, search_by_fei_ein, search_by_document_number, search_by_zip_code, search_by_street_address, search_by_trademark
- Does NOT expose: certificate_of_status, corporate_income_tax_filing_history, sales_and_use_tax_certificate_of_registration_status, reemployment_tax_account_status, workers_compensation_coverage, shareholder_or_member_ownership_percentages, financial_statements, franchise_or_privilege_tax_standing
- Paid: certificate_of_status_corporation_general_partnership_or_limited_partnership ($8.75), certificate_of_status_limited_liability_company ($5), application_for_reinstatement_following_administrative_dissolution_profit_corporation ($600)

### GA: Georgia Secretary of State Corporations Division Business Search (eCorp)
https://ecorp.sos.ga.gov/BusinessSearch
- Exposes free: entity name, control number, entity type, status, observed values including Active/Compliance, Active/Noncompliance, Withdrawn, Admin. Dissolved, Dissolved, Merged and Void, registered agent name, Georgia street address and county, principal office address, jurisdiction or state of formation, date of formation or registration, last annual registration year, which is the field that settles whether the annual registration is current, business purpose for corporations, NAICS code for LLCs, officers for corporations (CEO, CFO, Secretary) as reported on the annual registration, for domestic and foreign corporations alike, search by name, control number, officer name or registered agent name, each with starts-with, contains or exact match, so a free reverse officer lookup works, name, control number, business type, principal office address, agent name and status directly in the results grid before opening a record
- Does NOT expose: LLC members or managers (the LLC record carries no officer section at all, substituting NAICS code), any mailing address; the record carries only the principal office address and the agent's physical address, and there is no field called registered office address, filing history, document images or a change log, beneficial ownership, ownership percentages, financial or tax data, certificates of existence or certified copies, which are paid orders

### IL: Illinois Secretary of State Business Entity Search (Department of Business Services database)
https://apps.ilsos.gov/businessentitysearch/
- Exposes free: Official entity name, Date of formation or registration, Jurisdiction (domestic Illinois or the foreign home state), Name of registered agent, Address of registered office, Status (active/inactive), Names and addresses of the president and secretary, for corporations, Names and addresses of any managers, for LLCs, File number (also usable as a search key), Search by Business Name, Registered Agent, President, Secretary, Manager, File Number, Keyword or Partial Word, Coverage of corporations, not-for-profit corporations, limited partnerships, LLCs and LLPs
- Does NOT expose: Shareholders or LLC members, beyond the corporate president and secretary and LLC managers that are shown, Ownership percentages or cap table, Paid-in capital or franchise tax paid, Financial statements, revenue or payroll, Full officer and director lists beyond president and secretary, Bulk data: the database is for individual searches only and bulk copying or downloading is prohibited by criminal statute (720 ILCS 5/16D-3, 5/16D-4), Automated access: submitting the free search returns a reCAPTCHA 'confirm you are a person, not a robot' challenge before any result, so the File Detail Report cannot be pulled programmatically, Whether the annual report filing date or report year is displayed could not be confirmed; the Secretary of State's published field list does not include it, Bulk purchase of the Corporate Database is contract only and its price is not published (call 217-782-6961), so no fee figure is carried here
- Paid: Certificate of Good Standing, Corporation or LLC ($25), Certificate of Good Standing, Not-for-Profit ($5), Certificate of Good Standing, Fact or No Record / Abstract of Corporate Record, Limited Partnership ($25), Photocopy or certified copy, LLC ($25), Photocopy or certified copy, Limited Partnership ($25), Copy or certified copy of any document relating to a corporation, or a certificate (805 ILCS 5/15.15(a)) ($25)

### MA: Massachusetts Secretary of the Commonwealth, Corporations Division business entity search
https://corp.sec.state.ma.us/corpweb/corpsearch/CorpSearch.aspx
- Exposes free: Entity name, prior names and the date a name was changed, Identification Number and Old ID Number, Entity type (Domestic Profit Corporation, Foreign Limited Liability Company, nonprofit, LP, etc.), Date of Organization in Massachusetts, or Date of Registration in Massachusetts for foreign entities, Home jurisdiction and date organized there, for foreign entities, Current Fiscal Month/Day, which determines the corporate annual report due date, Principal office address and Massachusetts office address, Registered Agent (corporations) or Resident Agent (LLCs and LPs) name and address, Officers and Directors of a corporation: full table of title, individual name and address, Managers of an LLC, and persons authorized to execute recordable instruments affecting real property, Whether business entity stock is publicly traded, Authorized and issued stock: class, par value per share, total authorized, total issued and outstanding, Full filing history with viewable document images, Search by Individual Name across entities (officer, director or manager), which most states do not offer free
- Does NOT expose: LLC MEMBER names and ownership: the LLC record lists managers and real-property signatories only, with no member field and no ownership percentage, Shareholder register or per-holder ownership percentages for corporations (only aggregate authorized and issued share counts), EIN or FEIN (the URL parameter is named FEIN but carries the state ID number), Financial statements, revenue, assets or payroll, An explicit Active/Dissolved status label on the entity summary; standing must be inferred from the filing history or purchased as a certificate, Tax good standing, which is a separate DOR certificate
- Paid: Certificate of Good Standing, domestic profit corporation (not a tax good standing) ($12), Certificate of Good Standing, foreign corporation ($12), Certificate of Good Standing, LLC ($25), Certificate of Good Standing, limited partnership ($25), Certificate of Legal Existence, corporation, base tier with up to 1 name change (2 or more name changes $12, with officers $12, with amendments $20, with amendments and officers $25) ($7), Certificate of Legal Existence, LLC or limited partnership ($12), Certified copy of Articles of Organization or Foreign Corporation Certificate of Registration ($12), All other certified copies, first page (plus $2.00 per additional page) ($7)

### NJ: New Jersey Business Entity Name Search (free) and Business Records Service (paid), Division of Revenue and Enterprise Services
https://www.njportal.com/DOR/BusinessNameSearch/
- Exposes free: Whether a business name exists on the registered business database, returned regardless of status, The entity's New Jersey 10-digit Entity ID, City of the entity's address, Entity type code (for example DP for domestic profit), Incorporated Date (the formation date), returned as a column in the free results table, Name availability for a new business formation (a separate search mode), Keyword and Entity ID search modes, Free monitoring on your own business account: Corp Watch (alerts on filings posted and status changes such as revocation), Annual Report Filing Due alerts, and the NJ Tax Filing Calendar
- Does NOT expose: Entity status or standing: the free search explicitly returns matches 'regardless of status', so it cannot confirm good standing, Registered agent and registered office details, Officers, directors, members or managers, Ownership percentages or cap table, Formation documents or any filed document images, Annual report history, or CBT/tax standing, EIN and financial data
- Paid: Status report (all business entities) ($5), Status report online convenience fee ($1.25), Corporate and limited partnership standing certificate (short and long form) ($25), Short form standing certificate for LLCs and LLPs ($50), Long form standing certificate for LLCs and LLPs ($100), Corporate and limited partnership name availability certificate ($25), Name availability certificate for LLCs and LLPs ($50), Photocopies of any document, per page ($0.1), Certified copy, per document (the Registry Fee Schedule states this flatly with no entity carve-out; the $50 LLC figure appears only in narrative on https://www.nj.gov/treasury/revenue/copiesentities.shtml) ($25), No Record Certificate per entity name searched (corporations) ($25), No Record Certificate per entity name searched (LLCs) ($50), Expedited service surcharge, corporations, non-profits and LPs, per transaction (over-the-counter only, 8.5 business hours) ($15), Expedited service surcharge, LLCs and LLPs, per filing (over-the-counter only, 8.5 business hours) ($25), Same-day service fee, per document ($50), 2 hour service fee, per document ($500), 1 hour service fee, per document ($1000), Bulk Access Status Reports, per record ($0.0185)

### NY: New York Department of State, Corporation and Business Entity Database
https://apps.dos.ny.gov/publicInquiry/
- Exposes free: entity_name, dos_id, initial_filing_date, county, jurisdiction_of_formation, entity_type, current_entity_status, dos_process_address, registered_agent_when_on_file, foreign_qualification_date
- Does NOT expose: good_standing_certificate, franchise_tax_status, owners

### PA: Pennsylvania Department of State Business Entity Search (Business Filing Services)
https://file.dos.pa.gov/
- Exposes free: entity name, entity number (file number), entity type, filing type and filing subtype, registered office, a single field that prints EITHER a Pennsylvania street address OR the name of a Commercial Registered Office Provider such as CT Corporation System, county, principal address, jurisdiction of formation, shown as Formed In, initial filing date, status, officers with names and titles, plus governors, filing history including Annual Reports, with field-level Changed From and Changed To detail per filing
- Does NOT expose: a separate named registered agent field (Pennsylvania carries one registered office field instead, so an agent that reports it 'checked the registered agent in PA' has read a field that may hold either a provider name or a street address), search by officer or by registered agent (name or file number only, with Advanced adding filing type, status and date range), beneficial ownership, member or shareholder lists, document images or certificates without a logged-in account and purchase, certified proof of good standing without purchase
- Paid: Subsistence Certificate (certificate of good standing), domestic entity ($40), certified copy, base fee plus $3 per page ($55), plain photocopy, base fee plus $3 per page ($15), record search listing entity number, name, address and file date ($15), printout of the computer screen in the bureau reception room, per page ($3)

### TX: Texas Comptroller Franchise Tax Account Status Search
https://comptroller.texas.gov/taxes/franchise/account-status/search
- Exposes free: entity_name, texas_taxpayer_number, mailing_address, right_to_transact_business_in_texas, state_of_formation, sos_registration_status, effective_sos_registration_date, texas_sos_file_number, registered_agent_name, registered_office_street_address, public_information_report_officers_and_directors, public_information_report_year, search_by_name_taxpayer_number_or_sos_file_number, public_api
- Does NOT expose: ownership_information_report_contents, financial_institution_public_information_reports, formation_documents, franchise_tax_report_amounts_or_revenue, certificate_of_account_status_for_reinstatement_or_termination, sales_tax_permit_status, twc_unemployment_tax_account_status, workers_compensation_coverage_or_non_subscriber_status, ownership_percentages, financial_statements
- Paid: sosdirect_entity_search ($1), certificate_of_fact_including_certificate_of_existence_or_status ($15), long_form_certificate_of_existence ($25), certified_copies_per_certificate ($15), certified_copies_per_page ($1), plain_uncertified_copies_per_page ($0.1), apostille_related_to_a_business_entity_filing ($15)

### WA: Washington Corporations and Charities Filing System (CCFS)
https://ccfs.sos.wa.gov/
- Exposes free: Entity name and any former names, Unified Business Identifier (UBI) number, Entity type (profit corporation, LLC, LP, LLP, nonprofit, social purpose corporation), Business status (Active, Delinquent, Administratively Dissolved, Terminated), Formation or registration date and home jurisdiction for foreign entities, Annual report expiration date (the recurring due date), Registered agent name, physical registered office address and agent type (commercial or non-commercial), Principal office address, Governors (officers, directors, members or managers) as reported on the annual report, Filing history and images of filed documents on public record, Public list of commercial registered agents
- Does NOT expose: Ownership percentages or cap table; the Secretary of State states that ownership changes are not recorded by that office, Shareholder or member identities beyond whoever is listed as a governor, EIN or state tax account balances, Financial statements, revenue or payroll, Workers' compensation or unemployment insurance account status (those live at L&I Verify and ESD), Annual reports filed with a future effective date, which do not show on public record until effective
- Paid: Certificate of Existence / Good Standing ($20), Certificate of Existence / Long Form ($20), Certificate of Fact on Record ($20), Photocopy of any single recorded document ($10), Photocopy of charter documents ($20), Photocopy of annual reports ($10), Certified copies (surcharge on top of copy fees) ($10), Apostille / Certification ($15)


## Obligations


## US (37)

### Federal corporate income tax return (Form 1120) `federal-1120`
Applies to: c-corp, benefit-corp | category: tax
Every C corporation files Form 1120 for each tax year, whether or not it made money and whether or not it had any activity. A loss year still has to be filed, and filing is what starts the clock on carrying that loss forward.
- **Deadline**: The 15th day of the 4th month after year end, so April 15 for a calendar year. Form 7004 extends it by six months, to October 15 for a calendar-year filer. Note that September 15 is the extended date for partnerships and S corporations, not for a C corporation, and the two get mixed up constantly.
- **Rule out first**:
  - An extension was filed, so the return is not late yet. This is extremely common and is not a problem in itself. (common) Check: Look for an accepted Form 7004 and then check the extended deadline rather than the original one.
  - The company was formed part-way through the year and the first return is not due yet. (occasional) Check: Compare the formation date to the first tax year end.
- **If it genuinely was missed**: 5% of unpaid tax per month up to 25%, plus interest. There is also a minimum penalty for a return more than 60 days late, $525 for returns due after 2025-12-31, which can bite a loss-making company that owes no tax at all. An extension extends the time to file, never the time to pay.
- **How to prove it**:
  - [tier 2, settles it] Pull an IRS account or return transcript for the entity. This is the only source that definitively shows whether a return was accepted. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Check the tax preparer's portal (TaxDome, Canopy, Karbon) for a filed return.
  - [tier 4, corroborating only] Look for an e-file acceptance confirmation from the preparer. Be careful to distinguish an accepted EXTENSION (Form 7004) from an accepted RETURN. They look similar and are routinely confused.
- **Fix**:
  1. Confirm whether Form 7004 was accepted, and note the extended deadline it produced.
  2. If the return is still unfiled, get the books closed for the year first. The return cannot be prepared without them.
  3. File Form 1120 before the extended deadline. Interest runs on unpaid tax from the original April date regardless of the extension.
- **Source**: https://www.irs.gov/instructions/i7004 (verified 2026-08-14)
- **Note**: Extension length is 6 months. 26 USC 6081(b) reads 5 months for a December 31 C corporation year beginning before 2026, but Treasury granted a flat 6 months by regulation under 6081(a), which is what the IRS administers: the Form 7004 instructions list only Form 1041 filers and June 30 C corporations as exceptions. Do not re-derive this from the statute alone.

### Beneficial ownership information (BOI) report to FinCEN `federal-boi`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
This requirement is gone for US companies. FinCEN issued a final rule on 2026-08-11, effective 2026-08-14, permanently ending BOI reporting for entities created in the United States, and it will delete previously reported information for US persons. Only certain foreign-formed entities registered to do business in the US still report, and they do not report US persons.
- **Deadline**: No longer applicable to US-formed entities.
- **Rule out first**:
  - Plenty of checklists, blog posts and AI assistants still tell founders to file BOI. They are working from information that is now out of date. (common) Check: Read FinCEN's own announcement rather than any secondary summary.
- **How to prove it**:
  - [tier 2, settles it] No check is needed for a US-formed entity. Nothing is owed and nothing needs updating.
- **Fix**:
  1. Nothing to do if the company was formed in the United States.
  2. Ignore any reminder, invoice or solicitation asking you to file or renew a BOI report. Those solicitations were already a common scam vector and are now straightforwardly obsolete.
- **Source**: https://www.fincen.gov/news/news-releases/fincen-permanently-ends-beneficial-ownership-reporting-requirements-millions (verified 2026-08-13)
- **Note**: Corroborated against the Treasury press release and reporting in the Journal of Accountancy, Accounting Today and the ABA Banking Journal. fincen.gov was intermittently unreachable at verification time, so re-confirm at the source before citing this publicly.

### Form 5472, foreign-owned US entity information return `federal-5472`
Applies to: c-corp, llc, llc-single-member, benefit-corp | category: information-report
If a non-US person or entity owns 25 percent or more of the company, or the company is a foreign-owned single-member LLC, Form 5472 has to be filed with a pro-forma Form 1120 to report transactions with the foreign owner. This is one of the most commonly missed filings there is, and the penalty is severe.
- **Deadline**: With the federal return, including extensions.
- **Rule out first**:
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

### Federal employment tax returns (Form 941) `federal-941`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
An employer files Form 941 each quarter to report wages, withheld income tax and payroll taxes. Whether the company files this itself depends entirely on who the legal employer is.
- **Deadline**: The last day of the month after each quarter ends: April 30, July 31, October 31, January 31.
- **Rule out first**:
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

### Employer Identification Number (EIN) `federal-ein`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An EIN is your company's federal tax ID number. You need one to open a business bank account, run payroll, file a business tax return, or be taxed as a corporation or partnership. It is free directly from the IRS, and any service charging you for one is charging for paperwork you can do yourself.
- **Deadline**: No fixed deadline. Get one before your first payroll, your first business tax return, or opening a business bank account. Apply online, or by phone, fax or mail if you cannot apply online (international applicants without an SSN or ITIN apply by phone, fax or mail).
- **Rule out first**:
  - A single-member LLC with no employees and no excise tax liability is not required to have an EIN and may correctly be using the owner's SSN. (common) Check: Confirm the entity has no employees, has not elected corporate or S treatment, and files on Schedule C.
  - The EIN exists but the CP 575 was lost, which is extremely common because the IRS issues it once and never reissues it. (common) Check: Request a 147C verification letter from the IRS Business and Specialty Tax Line at 800-829-4933.
  - The entity was formed very recently and is inside the normal window before its first payroll or return. (occasional) Check: Compare the state formation date against the first payroll date or first required return due date.
- **How to prove it**:
  - [tier 2, settles it] Sign in to the IRS Business Tax Account at irs.gov/businessaccount and confirm the EIN is listed and linked to the legal entity name. https://www.irs.gov/businesses/business-tax-account
  - [tier 4, settles it] Locate the CP 575 EIN confirmation notice, or a 147C letter requested from the IRS Business and Specialty Tax Line, and check the legal name and address match the entity.
  - [tier 4, corroborating only] Read the EIN off the top of any previously filed federal return (1120, 1120-S, 1065, 941) and confirm it matches the entity's legal name.
  - [tier 5, corroborating only] Check the business bank account opening documents, since US banks require an EIN to open a non-sole-proprietor business account.
- **Fix**:
  1. Apply online at irs.gov for an immediate EIN if the responsible party has an SSN or ITIN.
  2. If applying from outside the US without an SSN or ITIN, file Form SS-4 by fax or mail and expect several weeks.
  3. Store the CP 575 with the corporate records; request a 147C letter if it was lost.
  4. Confirm the responsible party on file is a natural person and still correct, and file Form 8822-B within 60 days if it is not.
- **Source**: https://www.irs.gov/businesses/small-businesses-self-employed/get-an-employer-identification-number (verified 2026-08-14)
- **Note**: IRS states verbatim: "You never have to pay a fee for an EIN" and "You can apply for only 1 EIN per responsible party per day." The rule that the responsible party must be a natural person is on a separate IRS page (irs.gov/businesses/small-businesses-self-employed/responsible-parties-and-nominees): "Your responsible party must be a person, not an entity. The only exception is for government entities."

### Form 7004, Automatic Extension of Time to File a Business Return `federal-business-return-extension-7004`
Applies to: c-corp, s-corp, llc, partnership, benefit-corp | category: tax
Form 7004 buys you more time to file the return, not more time to pay the tax. You must still estimate and pay what you owe by the original due date or interest and late payment penalties start running. It is automatic, so the IRS will only contact you if the request is denied.
- **Deadline**: File on or before the original due date of the return. Extension lengths: most Form 1120 series filers get 6 months, so a calendar year 2025 Form 1120 due April 15 2026 is extended to October 15 2026. A C corporation whose tax year ends June 30 and begins before January 1 2026 gets 7 months, so a June 30 2025 year end due September 15 2025 is extended to April 15 2026. For tax years beginning in 2026 the automatic extension period is 6 months for everyone. Forms 1065 and 1120-S get 6 months, so a calendar year 2025 return due March 16 2026 is extended to September 15 2026.
- **Rule out first**:
  - No extension exists because the return was simply filed on time by the original due date. (common) Check: Check the account transcript for the return posting date against the original due date.
  - The IRS no longer sends approval notices for accepted extensions, so the absence of a letter is expected and proves nothing. (common) Check: Look for the e-file acceptance acknowledgment or the transcript entry rather than a paper notice.
  - A federally declared disaster postponement automatically extended the deadline without any 7004 being filed. (occasional) Check: Check the IRS disaster relief page for the entity's county and tax year.
- **If it genuinely was missed**: No penalty for the extension itself. Failing to pay the estimated tax due by the original due date triggers the late payment penalty of 0.5% per month up to 25%, plus interest.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript for the EIN and tax period and look for the extension transaction code posting the extended due date. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Check the preparer's filing software for the 7004 acceptance record for that EIN and year.
  - [tier 4, settles it] Obtain the e-file acceptance acknowledgment for the Form 7004 showing the submission ID and accepted timestamp.
  - [tier 5, corroborating only] Look for an estimated tax payment made on or near the original due date, which often accompanies an extension filing.
- **Fix**:
  1. If the original due date has not passed, e-file Form 7004 and pay the estimated balance due at the same time.
  2. If the original due date has passed, do not file Form 7004; file the actual return as fast as possible. For Forms 1120 and 1040 that stops the 5% per month late filing penalty. For Forms 1065 and 1120-S it stops a penalty of $255 per partner or shareholder per month, which is charged even when no tax is owed.
  3. Pay any estimated tax immediately even if the return is not ready, because payment and filing are separate obligations.
  4. Request First Time Abate or reasonable cause relief once the late return is filed.
- **Source**: https://www.irs.gov/pub/irs-efile/f1041-form-7004-due-dates-py2026.pdf (verified 2026-08-14)
- **Note**: IMPORTANT CORRECTION TO A WIDELY REPEATED BELIEF. 26 USC 6081(b) does say that for a C corporation tax year ending December 31 and beginning before January 1 2026, "5 months" is substituted for "6 months". That statutory floor is NOT what taxpayers actually get. Treasury exercised its separate authority under 26 USC 6081(a) and 26 CFR 1.6081-3(a) grants "an automatic 6-month extension of time to file its income tax return" to corporations generally, and the only exception in 1.6081-3(e) is for a C corporation year ending June 30 and beginning before January 1 2026, which substitutes "7-month" for "6-month". There is no December 31 five month carve-out in the regulation. Three independent primary sources confirm 6 months for calendar year C corps: (1) 26 CFR 1.6081-3(a) and (e), verified at https://www.govinfo.gov/content/pkg/CFR-2023-title26-vol15/pdf/CFR-2023-title26-vol15-sec1-6081-3.pdf; (2) Instructions for Form 7004 (Rev. December 2025), which state "The automatic extension period for time to file is generally 6 months. Exceptions apply for certain filers of Form 1041 and for C corporations with tax years ending June 30" and list no December 31 exception; (3) this IRS Form 7004 Due Dates PY2026 chart, which states "Extension requests for most Form 1120 series filers... are due 3 1/2 months after the tax period ends, and timely requests are granted a 6-month extension" and "Corporation returns whose tax year ends in June (YYYY06) are due 2 1/2 months after the tax period ends, and timely requests are granted a 7-month extension". Conclusion: a calendar year 2025 Form 1120 on extension is due OCTOBER 15 2026, not September 15 2026. September 15 2026 is the extended due date for calendar year 2025 Forms 1065 and 1120-S. Statute text verified at https://uscode.house.gov/view.xhtml?req=granuleid:USC-prelim-title26-section6081&num=0&edition=prelim.

### Form 1120-S, U.S. Income Tax Return for an S Corporation `federal-form-1120s-s-corp-income-tax-return`
Applies to: s-corp | category: tax
An S corporation does not usually pay federal income tax itself. It files Form 1120-S and passes profit and loss through to shareholders on Schedule K-1, which they report on their personal returns. The deadline is a month earlier than a C corporation's, and the late filing penalty is charged per shareholder per month even when no tax is owed.
- **Deadline**: Due the 15th day of the 3rd month after the tax year ends, so March 15 for a calendar year. For tax year 2025 that fell on Sunday March 15 2026, moving the deadline to March 16 2026. Form 7004 gives an automatic 6 month extension, so the extended due date for calendar year 2025 is September 15 2026.
- **Rule out first**:
  - The S election was filed but the IRS has not yet issued CP261, so the entity is still filing as a C corporation in the interim. (common) Check: Look for the Form 2553 filing receipt or fax confirmation and call the IRS Business and Specialty Tax Line to confirm the election status.
  - The entity is on extension and the September 15 extended due date has not yet passed. (common) Check: Check for an accepted Form 7004 for the tax year.
  - The S election was revoked or terminated, so Form 1120 is now the correct return. (occasional) Check: Look for a revocation statement in the corporate records and confirm which return type posts on the transcript.
  - The election was made effective for a later year, so earlier years correctly show Form 1120. (occasional) Check: Read the effective date on line E of the filed Form 2553.
- **If it genuinely was missed**: For returns on which no tax is due, $255 for each month or part of a month the return is late, up to 12 months, multiplied by the number of people who were shareholders during any part of the tax year. The minimum penalty for a return required to be filed in 2026 that is more than 60 days late is the smaller of the tax due or $525.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript for the EIN and confirm an 1120-S posted for each tax year since the S election took effect. https://www.irs.gov/individuals/get-transcript
  - [tier 4, settles it] Obtain the IRS CP261 notice accepting the S election, then the signed 1120-S and its e-file acceptance for each year.
  - [tier 4, corroborating only] Collect each shareholder's Schedule K-1 and confirm the count of K-1s matches the shareholder register.
  - [tier 5, corroborating only] Check for shareholder distributions and reasonable compensation payroll in the ledger, which indicate active S corporation operation.
- **Fix**:
  1. Confirm the S election is actually in effect and get the effective date in writing from the IRS before filing anything.
  2. File all delinquent Forms 1120-S oldest year first; the per shareholder penalty compounds fast, so speed matters more than perfection.
  3. Issue corrected Schedules K-1 to shareholders and amend affected personal returns if the K-1s were wrong or never issued.
  4. Request First Time Abate or reasonable cause relief, and cite Rev. Proc. 84-35 style relief arguments where applicable.
  5. Verify the S corporation is paying reasonable compensation through payroll, because a zero salary S corporation is a separate exposure.
- **Source**: https://www.irs.gov/instructions/i1120s (verified 2026-08-14)
- **Note**: Verbatim: "Generally, an S corporation must file Form 1120-S by the 15 day of the 3rd month after the end of its tax year." Penalty amount corroborated at https://www.irs.gov/payments/failure-to-file-penalty, which lists the per shareholder per month base rate as $255 after 12/31/2025 and $245 for 01/01/2025 to 12/31/2025. Extended due date corroborated by the IRS Form 7004 Due Dates PY2026 chart.

### Form 1065, U.S. Return of Partnership Income `federal-form-1065-partnership-return`
Applies to: partnership, llc | category: tax
A partnership, and any LLC with two or more members that has not elected corporate treatment, files Form 1065 each year and issues a Schedule K-1 to every partner. The partnership itself normally pays no federal income tax; the partners report their share on their own returns. Partners cannot correctly file their personal returns until they have their K-1.
- **Deadline**: Due the 15th day of the 3rd month after the tax year ends, so March 15 for a calendar year. For tax year 2025 that fell on Sunday March 15 2026, moving to March 16 2026. Form 7004 gives an automatic 6 month extension, so the extended due date for calendar year 2025 is September 15 2026.
- **Rule out first**:
  - The LLC is single-member and therefore a disregarded entity, so Schedule C is correct and no Form 1065 is due. (common) Check: Check the operating agreement and cap table for a second member; a spouse in a community property state may also be treated as a single member.
  - The entity is on extension and the September 15 extended due date has not passed. (common) Check: Check for an accepted Form 7004 for the tax year.
  - The partnership had no income, deductions or credits for the year and qualifies for a narrow no-activity exception. (rare) Check: Confirm zero activity in the books and read the exceptions in the Form 1065 instructions before relying on this.
  - The LLC elected corporate or S treatment, so Form 1120 or 1120-S is correct. (occasional) Check: Look for a filed Form 8832 or Form 2553 and confirm the return type on the transcript.
- **If it genuinely was missed**: $255 for each month or part of a month the return is late, up to 12 months, multiplied by the number of partners during any part of the tax year. A separate penalty applies for failure to furnish Schedule K-1 to a partner.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript for the EIN and confirm a Form 1065 posted for each tax year. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Check the preparer's portal for the 1065 e-file acceptance record for each year.
  - [tier 4, settles it] Obtain the signed Form 1065 with its e-file acceptance acknowledgment, and the full set of Schedules K-1 issued to partners.
  - [tier 4, corroborating only] Compare the partnership or operating agreement's member list against the number of K-1s issued.
  - [tier 5, corroborating only] Look for partner distributions or guaranteed payments in the ledger, which indicate an operating partnership.
- **Fix**:
  1. Confirm the entity's default classification and whether any election changed it.
  2. File delinquent Forms 1065 oldest year first and issue the missing Schedules K-1 to every partner.
  3. Tell partners immediately if their K-1s were missing or wrong, since they may need to amend personal returns.
  4. Request penalty relief; partnerships with 10 or fewer partners meeting the conditions have historically sought relief under Rev. Proc. 84-35, and First Time Abate may apply.
  5. Confirm whether the partnership is subject to the centralized partnership audit regime and has designated a partnership representative.
- **Source**: https://www.irs.gov/instructions/i1065 (verified 2026-08-14)
- **Note**: The instructions page confirms verbatim that "Every domestic partnership must file Form 1065". The specific due date and 6 month extension were verified on the IRS Form 7004 Due Dates PY2026 chart at https://www.irs.gov/pub/irs-efile/f1041-form-7004-due-dates-py2026.pdf, which shows Form 1065 due 2 1/2 months after the tax period ends (tax period 202612 due 03/15/2027) and states that timely extension requests are granted a 6 month extension, putting the extended date at the 15th day of the 9th month after the tax period ends. CORRECTED 2026-08-14: an earlier version of this note said the chart "treats an extension request as timely if received by the 15th day of the 6th month after the end of the tax period." That is wrong on both counts. The request is due at the original due date, 2 1/2 months after the tax period ends, and the 6 months is the length of the extension granted, not the request window. Penalty base rate of $255 per partner per month is from https://www.irs.gov/payments/failure-to-file-penalty, re-verified 2026-08-14, which lists for "Forms 1065, 1066, and 8985" a rate of $255.00 after 12/31/2025 and $245.00 for 01/01/2025 to 12/31/2025, keyed to the return due date without extension. A calendar year 2025 Form 1065 is due 03/16/2026, so $255 is the rate. Repeated attempts to extract the "When To File" and "Penalties" sections directly from the i1065 HTML page were truncated by the fetch tool on 2026-08-14 as well, so those two figures rest on the corroborating IRS pages named above rather than on i1065 itself.

### Schedule C reporting for a single-member LLC (disregarded entity) `federal-schedule-c-single-member-llc`
Applies to: llc-single-member | category: tax
A single-member LLC is invisible to the IRS for income tax by default. You report its income and expenses on Schedule C of your own Form 1040, exactly as a sole proprietor would. The LLC still protects you under state law, but it does not create a separate federal tax return unless you elect corporate treatment.
- **Deadline**: Filed with your personal Form 1040, due April 15 for a calendar year, with an automatic 6 month extension to October 15 via Form 4868. The extension does not extend the time to pay.
- **Rule out first**:
  - The LLC elected S corporation treatment, so income flows through a Form 1120-S and Schedule K-1 instead of Schedule C. This is very common for profitable single-member LLCs. (common) Check: Look for a filed Form 2553 and the IRS CP261 acceptance notice.
  - The LLC is a rental real estate holding entity, so the activity correctly appears on Schedule E rather than Schedule C. (common) Check: Check the nature of the activity and whether substantial services are provided to tenants.
  - The LLC was formed but never began operations, so there is nothing to report and no Schedule C is required. (common) Check: Confirm there were no gross receipts, no deductible expenses and no bank activity for the year.
  - The owner is a nonresident alien with no US trade or business and no effectively connected income, so no Form 1040 filing arises. Note this does not remove the Form 5472 obligation. (occasional) Check: Determine the owner's tax residency and whether the LLC has US effectively connected income; then check federal-form-5472 separately.
- **If it genuinely was missed**: Standard Form 1040 late filing penalty of 5% of the unpaid tax per month or part month up to 25%, plus the 0.5% per month late payment penalty.
- **How to prove it**:
  - [tier 1, corroborating only] Check the state Secretary of State registry to confirm the LLC has exactly one member of record and is in good standing.
  - [tier 2, settles it] Order the owner's individual Return Transcript or Wage and Income Transcript and confirm a Schedule C is present for the business. https://www.irs.gov/individuals/get-transcript
  - [tier 4, settles it] Obtain the owner's filed Form 1040 with Schedule C attached and match the business name, address and principal business code to the LLC.
  - [tier 5, corroborating only] Compare business bank account deposits for the year against the gross receipts reported on Schedule C line 1.
- **Fix**:
  1. Reconstruct the year's income and expenses from bank and payment processor statements.
  2. File or amend the owner's Form 1040 with a complete Schedule C.
  3. Compute and pay self-employment tax on Schedule SE at the same time.
  4. Set up quarterly estimated tax payments going forward to avoid the underpayment penalty.
  5. Evaluate whether an S election would reduce self-employment tax before the next tax year begins.
- **Source**: https://www.irs.gov/businesses/small-businesses-self-employed/single-member-limited-liability-companies (verified 2026-08-14)
- **Note**: Verbatim: "For income tax purposes, an LLC with only one member is treated as an entity disregarded as separate from its owner, unless it files Form 8832 and affirmatively elects to be treated as a corporation." Note that a disregarded single-member LLC is still treated as a separate entity for employment tax and certain excise taxes, and files payroll returns under its own EIN.

### Self-employment tax (Schedule SE) `federal-self-employment-tax`
Applies to: llc-single-member, partnership, llc | category: tax
If you own a disregarded LLC or are a general partner, your share of business profit is subject to self-employment tax on top of income tax. This is the Social Security and Medicare tax that an employer and employee would normally split, and you pay both halves. It surprises founders because it applies to profit you never withdrew from the business.
- **Deadline**: Reported on Schedule SE with the annual Form 1040, due April 15 for a calendar year. Paid in practice through quarterly estimated tax payments.
- **Rule out first**:
  - Net earnings were under $400 for the year, so no Schedule SE is required. (common) Check: Check Schedule C line 31 or the K-1 self-employment earnings box for the year.
  - The owner takes a W-2 salary through an S corporation, so the compensation is subject to FICA through payroll rather than self-employment tax. (common) Check: Confirm an S election is in effect and look for a W-2 issued to the owner.
  - The member is a genuine limited partner or passive investor whose distributive share is excluded from self-employment earnings. (occasional) Check: Read box 14 of the Schedule K-1 and confirm the member does not materially participate in management.
  - The business had a loss for the year, so there are no net earnings to tax. (common) Check: Confirm the loss on Schedule C line 31 or on the K-1.
- **If it genuinely was missed**: No separate penalty; underpayment feeds the Form 1040 late payment penalty and the estimated tax underpayment penalty.
- **How to prove it**:
  - [tier 2, settles it] Order the owner's individual Return Transcript and confirm Schedule SE self-employment tax is present and consistent with Schedule C or K-1 income. https://www.irs.gov/individuals/get-transcript
  - [tier 2, settles it] Check the owner's Social Security earnings record at ssa.gov/myaccount to confirm self-employment earnings were credited for the year. https://www.ssa.gov/myaccount/
  - [tier 4, settles it] Obtain the filed Schedule SE and reconcile line 2 to Schedule C line 31 or to box 14 code A of the Schedule K-1.
  - [tier 5, corroborating only] Compare owner draws and transfers out of the business account against reported net earnings.
- **Fix**:
  1. Recompute net earnings from self-employment for each open year.
  2. Amend the affected Forms 1040 to add Schedule SE and pay the tax.
  3. Begin quarterly estimated payments that cover both income tax and self-employment tax.
  4. Model whether an S election plus reasonable compensation would lower the total burden for future years.
- **Source**: https://www.irs.gov/businesses/small-businesses-self-employed/self-employment-tax-social-security-and-medicare-taxes (verified 2026-08-14)
- **Note**: Verbatim: "The self-employment tax rate is 15.3%", comprising 12.4% Social Security and 2.9% Medicare. The Social Security portion applies only up to the annual wage base, which is indexed each year and was not verified in this pass; the Medicare portion is uncapped and an Additional Medicare Tax applies above statutory thresholds.

### Quarterly estimated tax for pass-through owners (Form 1040-ES) `federal-individual-estimated-tax`
Applies to: llc-single-member, partnership, llc, s-corp | category: tax
Nobody withholds tax from your business profit, so you have to send the IRS money four times a year yourself. If you wait until April, you owe an underpayment penalty even if you pay the full balance on time. This is the single most common cash-flow surprise for first-year founders.
- **Deadline**: For tax year 2026: April 15 2026, June 15 2026, September 15 2026, and January 15 2027. You can skip the January payment if you file the return and pay in full by February 1 2027.
- **Rule out first**:
  - The owner covers the liability through extra withholding on a spouse's W-2 or their own paycheck, which is treated as paid evenly across the year and can be more effective than estimates. (common) Check: Check line 25 withholding on the joint Form 1040 against total tax.
  - Expected tax owed is under $1,000 after withholding and credits, so no estimated payments are required. (common) Check: Compute expected tax less withholding and refundable credits for the year.
  - The prior year safe harbor is already satisfied by payments made, so no penalty arises even though the current year liability is much larger. (common) Check: Compare payments to date against 100% or 110% of the prior year total tax.
  - This is the owner's first year with business income and no prior year liability existed, which can eliminate the penalty entirely. (occasional) Check: Check whether the prior year return showed zero tax and covered a full 12 months.
- **If it genuinely was missed**: An underpayment penalty imposed on each underpayment for the number of days it remains unpaid. Safe harbor: pay 90% of the current year tax or 100% of the prior year tax, whichever is smaller, rising to 110% of prior year tax if prior year AGI exceeded $150,000 ($75,000 if married filing separately).
- **How to prove it**:
  - [tier 2, settles it] Sign in to the individual IRS Online Account and review the Payment Activity by year to confirm four estimated payments posted. https://www.irs.gov/payments/online-account-for-individuals
  - [tier 2, settles it] Order the individual Account Transcript and confirm estimated tax payment postings for each quarter. https://www.irs.gov/individuals/get-transcript
  - [tier 4, corroborating only] Review the prior year return for Form 2210 and any underpayment penalty assessed, which shows whether the safe harbor was met.
  - [tier 5, corroborating only] Look for four IRS debits from the owner's personal bank account near the quarterly due dates.
- **Fix**:
  1. Compute the shortfall for the current year and pay it immediately, since the penalty accrues daily.
  2. Use the annualized income installment method on Form 2210 if income was uneven, which often reduces or eliminates the penalty.
  3. Set the remaining quarterly payments to hit the prior year safe harbor, which is certain, rather than guessing at current year income.
  4. Schedule the payments in EFTPS or IRS Direct Pay in advance so they are not missed.
- **Source**: https://www.irs.gov/pub/irs-pdf/f1040es.pdf (verified 2026-08-14)
- **Note**: Due dates and the safe harbor read directly from page 5 of the 2026 Form 1040-ES PDF. Verbatim trigger: "You expect to owe at least $1,000 in tax for 2026, after subtracting your withholding and refundable credits." Verbatim on the January payment: "You don't have to make the payment due January 15, 2027, if you file your 2026 tax return by February 1, 2027, and pay the entire balance due with your return."

### Corporate estimated tax installments `federal-corporate-estimated-tax`
Applies to: c-corp, benefit-corp | category: tax
A profitable C corporation cannot wait until the return is due to pay its tax. It must prepay in four installments during the year, and it must pay electronically. Missing installments creates an underpayment penalty even if the full balance is paid with the return.
- **Deadline**: Four installments due by the 15th day of the 4th, 6th, 9th and 12th months of the tax year. For a calendar year corporation that is April 15, June 15, September 15 and December 15.
- **Rule out first**:
  - The corporation expects total tax under $500, most often because it is pre-revenue or operating at a loss, so no installments are required. (common) Check: Review the year to date profit and loss and the prior year return for taxable income.
  - The corporation has net operating loss carryforwards that eliminate current year taxable income. (common) Check: Check the NOL carryforward schedule against projected taxable income.
  - This is the corporation's first tax year, where the prior year safe harbor is unavailable but the required annual payment may still be met by an annualized computation. (occasional) Check: Run the annualized income installment method on Form 2220.
- **If it genuinely was missed**: Underpayment penalty computed on Form 2220. The IRS states a corporation that does not make estimated tax payments when due may be subject to an underpayment penalty for the period of underpayment.
- **How to prove it**:
  - [tier 2, settles it] Sign in to EFTPS with the entity's EIN and review the payment history for four estimated tax payments in the tax year. https://www.eftps.gov/
  - [tier 2, settles it] Order the business Account Transcript and confirm estimated tax payment postings by quarter. https://www.irs.gov/individuals/get-transcript
  - [tier 4, corroborating only] Check the filed Form 1120 for an attached Form 2220 and any penalty computed on it.
  - [tier 5, corroborating only] Look for four EFTPS debits from the corporate bank account near the installment dates.
- **Fix**:
  1. Project taxable income for the year and compute the required installments.
  2. Enroll in EFTPS immediately if not already enrolled, because enrollment takes several business days and payments must be made electronically.
  3. Catch up the missed installments now to stop further accrual.
  4. File Form 2220 with the return and use the annualized method if income was seasonal or back-loaded.
- **Source**: https://www.irs.gov/instructions/i1120 (verified 2026-08-14)
- **Note**: Verbatim: "The corporation must make installment payments of estimated tax if it expects its total tax for the year (less applicable credits) to be $500 or more", "The installments are due by the 15th day of the 4th, 6th, 9th, and 12th months of the tax year", and "The corporation must use electronic funds transfer to make installment payments of estimated tax." Form 1120-W was obsoleted after 2022; the live rule now sits in the Form 1120 instructions.

### Form 2553, Election by a Small Business Corporation (S election) `federal-form-2553-s-election`
Applies to: s-corp, c-corp, llc, llc-single-member | category: entity
Form 2553 is what actually makes you an S corporation. Forming an LLC or corporation in your state does nothing by itself. The deadline is tight and measured from the start of the tax year you want it to apply to, and missing it is the most common reason a founder pays more self-employment tax than they needed to.
- **Deadline**: File no more than 2 months and 15 days after the beginning of the tax year the election is to take effect, or at any time during the tax year preceding the tax year it is to take effect. For a calendar year election effective January 1, that is March 15. Late election relief under Rev. Proc. 2013-30 is available within 3 years and 75 days of the intended effective date by writing FILED PURSUANT TO REV. PROC. 2013-30 at the top of page 1.
- **Rule out first**:
  - The CP261 was mailed to a prior address or the registered agent and never reached the founder, though the election is valid and in effect. (common) Check: Call the IRS Business and Specialty Tax Line to confirm the election date on the account, then file Form 8822-B to fix the address.
  - The entity deliberately remains a C corporation, which is the right answer for a startup planning venture funding, foreign shareholders, or QSBS treatment under section 1202. (common) Check: Ask whether the cap table includes non-individual or nonresident alien holders, or whether QSBS is part of the plan.
  - The election was filed recently and the IRS has not finished processing it; CP261 routinely takes 60 days or more. (common) Check: Check the mailing or fax date on the Form 2553 submission record.
  - The entity is ineligible, for example it has a nonresident alien shareholder, so the absence of an election is correct rather than an oversight. (occasional) Check: Review the cap table against the eligibility requirements.
- **How to prove it**:
  - [tier 2, settles it] Call the IRS Business and Specialty Tax Line at 800-829-4933 and ask them to confirm the S election effective date on the account.
  - [tier 2, settles it] Order the business Account Transcript and confirm the filing requirement code shows 1120-S rather than 1120. https://www.irs.gov/individuals/get-transcript
  - [tier 4, settles it] Obtain the IRS CP261 Notice of Acceptance as an S Corporation, which is the definitive confirmation the election is in effect.
  - [tier 4, corroborating only] Retrieve the signed Form 2553 with the certified mail receipt or fax confirmation showing the submission date.
  - [tier 5, corroborating only] Look for owner payroll running alongside distributions, which is the operating signature of an S corporation.
- **Fix**:
  1. Confirm the entity is eligible before filing anything, especially the nonresident alien shareholder and one class of stock tests.
  2. If within 3 years and 75 days of the intended effective date, file under Rev. Proc. 2013-30 with the required reasonable cause statement and all shareholder consents.
  3. If outside that window, elect prospectively for the next tax year rather than trying to backdate.
  4. File the S corporation returns consistent with the requested effective date once relief is granted.
  5. Start reasonable compensation payroll for owner-employees, because an S election without payroll creates a new exposure.
- **Source**: https://www.irs.gov/instructions/i2553 (verified 2026-08-14)
- **Note**: Verbatim deadline: "No more than 2 months and 15 days after the beginning of the tax year the election is to take effect, or At any time during the tax year preceding the tax year it is to take effect." Eligibility quotes: "It has no more than 100 shareholders", "It has only one class of stock (disregarding differences in voting rights)", "It has no nonresident alien shareholders (other than as potential current beneficiaries of an ESBT)."

### Form 8832, Entity Classification Election (check-the-box) `federal-form-8832-entity-classification`
Applies to: llc, llc-single-member, partnership | category: entity
By default an LLC is a disregarded entity if it has one owner and a partnership if it has two or more. Form 8832 is how you override that default and elect to be taxed as a corporation instead. Most founders reach it on the way to an S election, and it locks you in for five years once used.
- **Deadline**: The election cannot take effect more than 75 days before the date it is filed, nor more than 12 months after the date it is filed. A date outside that range defaults to the nearest boundary. Late relief under Rev. Proc. 2009-41 is available within 3 years and 75 days of the requested effective date.
- **Rule out first**:
  - The entity is happy with its default classification, so no election is needed and its absence is correct. (common) Check: Confirm the number of members and that the returns filed match the default treatment.
  - The entity filed Form 2553 for S treatment, which is deemed to include the corporate classification election, so no separate Form 8832 exists. (common) Check: Look for the Form 2553 and the CP261 acceptance notice.
  - The entity is a corporation formed under state law, which is a per se corporation with no election available or needed. (common) Check: Check the state formation documents for articles of incorporation rather than articles of organization.
  - The IRS acknowledgment letter was lost or sent to an old address although the election is valid. (occasional) Check: Call the IRS Business and Specialty Tax Line to confirm the classification on the account.
- **If it genuinely was missed**: The IRS states penalties apply to returns filed inconsistent with the entity's election. Failure to attach a copy of Form 8832 to the return does not invalidate the election, but penalties may be assessed against persons required to attach it who do not.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript and confirm the filing requirement matches the elected classification. https://www.irs.gov/individuals/get-transcript
  - [tier 4, settles it] Obtain the IRS letter acknowledging the Form 8832 election and confirm the effective date it states.
  - [tier 4, corroborating only] Retrieve the signed Form 8832 with proof of mailing and confirm the date entered on the effective date line.
  - [tier 4, corroborating only] Check whether a copy of the Form 8832 was attached to the first return filed after the election.
- **Fix**:
  1. Determine the entity's current default and actual classification before changing anything.
  2. If a past election was intended but never filed, seek late relief under Rev. Proc. 2009-41 within 3 years and 75 days of the requested effective date.
  3. Amend any returns filed inconsistent with the classification the entity actually has.
  4. Check the 60 month limitation before electing again, since a second change is generally blocked for five years after the effective date of the first.
- **Source**: https://www.irs.gov/pub/irs-pdf/f8832.pdf (verified 2026-08-14)
- **Note**: The HTML instructions page at irs.gov/instructions/i8832 returned HTTP 404; the official form PDF, which contains the instructions, was fetched instead. Verbatim: "Generally, an election specifying an eligible entity's classification cannot take effect more than 75 days prior to the date the election is filed, nor can it take effect later than 12 months after the date the election is filed" and "Once an eligible entity makes an election to change its classification, the entity generally cannot change its classification by election again during the 60 months after the effective date of the election." The 60 month bar does not apply where the prior election was made by a newly formed entity effective on its formation date.

### Section 83(b) election on restricted stock `federal-section-83b-election`
Applies to: c-corp, s-corp, benefit-corp, llc | category: tax
If you receive founder stock or restricted stock that vests over time, an 83(b) election tells the IRS to tax you now on today's tiny value instead of later on each vesting date at whatever the shares are then worth. For a founder whose stock is worth almost nothing at grant, this is usually the difference between a trivial tax bill and a catastrophic one. The deadline is 30 days and there is no extension and no relief for missing it.
- **Deadline**: Must be filed no later than 30 days after the date the property was transferred. This is a hard statutory deadline; the IRS cannot waive it.
- **Rule out first**:
  - The stock was fully vested at grant with no substantial risk of forfeiture, so no 83(b) election was needed and its absence is correct. (common) Check: Read the stock purchase agreement for a vesting schedule or company repurchase right.
  - The election was mailed and is valid, but no IRS acknowledgment exists because the IRS does not routinely acknowledge 83(b) elections. (common) Check: Rely on the certified mail receipt and the signed copy; absence of an IRS letter is expected, not evidence of failure.
  - No copy is attached to the tax return because that requirement was removed by T.D. 9779, so its absence from the return proves nothing. (common) Check: Look for the standalone mailing evidence instead of checking the return.
  - The holder received options rather than stock, and 83(b) applies only on exercise of an early-exercisable option, not on grant of the option itself. (occasional) Check: Confirm whether the instrument is an option or actual shares, and whether any early exercise occurred.
- **How to prove it**:
  - [tier 3, corroborating only] Check the cap table platform (Carta, Pulley, AngelList) for an uploaded 83(b) election and its filing date.
  - [tier 4, settles it] Obtain the signed election (Form 15620 or a conforming written statement) together with the USPS certified mail receipt and the return receipt or Track and Confirm printout showing IRS delivery within 30 days of the transfer.
  - [tier 4, settles it] Compare the stock purchase agreement or grant date against the postmark date on the mailing receipt to confirm the 30 day window was met.
  - [tier 4, corroborating only] Check the company's records for the copy of the election that the service provider must furnish to the service recipient.
- **Fix**:
  1. Establish the exact transfer date and count 30 days; if the window is still open, file immediately by certified mail with return receipt.
  2. If the window has closed, there is no relief. Stop and quantify the exposure: compute the spread at each vesting date and the resulting ordinary income and payroll tax.
  3. Consider whether the shares can be repurchased and reissued, which restarts the clock, and get securities and tax counsel before doing so.
  4. Record the outcome in the cap table so future grants are handled correctly.
  5. Put a standing 30 day reminder on every future equity grant.
- **Source**: https://uscode.house.gov/view.xhtml?req=granuleid:USC-prelim-title26-section83&num=0&edition=prelim (verified 2026-08-14)
- **Note**: 26 USC 83(b)(2) verbatim: an election "shall be made not later than 30 days after the date of such transfer." Corroborated by IRS Form 15620 (Rev. 4-2025) at https://www.irs.gov/pub/irs-pdf/f15620.pdf: "An 83(b) election must be filed no later than 30 days after the date the property was transferred" and "Submit this completed and signed Form 15620 to the IRS via mail with the IRS office with which the person who performs the services files a federal income tax return." Use of Form 15620 is voluntary; a conforming written statement under Treas. Reg. 1.83-2 also works. The requirement to attach a copy to the tax return was removed by T.D. 9779 (2016-33 I.R.B.): "These final regulations remove the second sentence in section 1.83-2(c) of the existing regulations, which requires that a taxpayer submit a copy of a section 83(b) election with the taxpayer's tax return."

### Form 8822-B, Change of Address or Responsible Party `federal-form-8822b-responsible-party`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
The IRS keeps one named human on file as your company's responsible party, set when you got your EIN. If that person leaves, or your business address changes, you have 60 days to tell the IRS. Founders miss this constantly, and the consequence is that IRS notices go to someone who no longer works there.
- **Deadline**: Report a change in responsible party within 60 days of the change. Address changes should also be reported using this form.
- **Rule out first**:
  - Nothing has actually changed since the EIN was issued, so no filing is due. (common) Check: Compare the SS-4 responsible party and address against today's officer list and address.
  - The change was reported on a subsequent tax return's address field, which updates the address of record even without Form 8822-B. (common) Check: Check whether the most recent return carried the new address and whether IRS mail is arriving there.
  - The change happened within the last 60 days and the window is still open. (occasional) Check: Date the departure or move and count 60 days.
  - The form was filed but the IRS does not send an acknowledgment for Form 8822-B, so no confirmation letter is expected. (common) Check: Rely on the mailing receipt and confirm the change by phone.
- **How to prove it**:
  - [tier 1, corroborating only] Check the state Secretary of State filing for the current officers, members and principal address and compare to what the IRS holds.
  - [tier 2, settles it] Call the IRS Business and Specialty Tax Line at 800-829-4933 and ask which responsible party and address are currently on file for the EIN.
  - [tier 4, settles it] Retrieve the filed Form 8822-B with proof of mailing dated within 60 days of the change.
  - [tier 4, corroborating only] Compare the responsible party named on the original SS-4 or CP 575 against the current officer or member list.
- **Fix**:
  1. Identify the correct current responsible party, who must be a natural person with an SSN or ITIN.
  2. File Form 8822-B now even if the 60 day window has passed, since late is materially better than never.
  3. Confirm by phone that the IRS record updated, because there is no acknowledgment letter.
  4. Check that no IRS correspondence was missed at the old address, and order an account transcript to look for unresolved notices.
- **Source**: https://www.irs.gov/forms-pubs/about-form-8822-b (verified 2026-08-14)
- **Note**: Verbatim: "Changes in responsible parties must be reported to the IRS within 60 days." The IRS page states no penalty for late filing, so none is asserted here. The practical harm is missed notices, not a stated fine.

### Form 944, Employer's Annual Federal Tax Return `federal-form-944-annual-employment-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Form 944 is the once-a-year alternative to filing Form 941 four times, meant for very small employers. The critical point founders get wrong is that you do not choose it: the IRS assigns it in writing. If they told you to file 944 and you file 941s instead, both are wrong.
- **Deadline**: Due January 31 following the year reported. For tax year 2025 the due date was February 2 2026 because January 31 2026 fell on a weekend, or February 10 2026 if all deposits were made on time and in full.
- **Rule out first**:
  - The employer was never notified to file Form 944 and correctly files quarterly Forms 941 instead. (common) Check: Check the filing requirement code on the account transcript.
  - The employer was moved from 944 to 941 status by the IRS in a later year, so the pattern of returns changes mid-history for a legitimate reason. (occasional) Check: Look for the IRS notice changing the filing requirement and match it to the year the return type changed.
  - The employer paid no wages at all during the year, so nothing was due. (common) Check: Confirm no W-2s were issued for the year.
- **If it genuinely was missed**: Failure to file penalty of 5% of the unpaid tax per month or part month, up to 25%, plus failure to deposit penalties.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript and confirm the employment tax filing requirement is Form 944 rather than Form 941. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Check the payroll provider's tax settings for whether the account is configured as a 944 filer, and pull the filed return.
  - [tier 4, settles it] Locate the IRS letter notifying the employer to file Form 944, which is the only thing that establishes the requirement.
  - [tier 5, corroborating only] Confirm total annual payroll tax debits are consistent with a liability at or below the $1,000 threshold.
- **Fix**:
  1. Confirm in writing which form the IRS expects, by transcript or by calling 800-829-4933.
  2. File the correct delinquent returns for each year and pay the trust fund portion first.
  3. If the wrong form was filed, contact the IRS to have the account corrected rather than filing duplicates.
  4. Request to change filing requirements for future years if the liability level no longer fits.
- **Source**: https://www.irs.gov/instructions/i944 (verified 2026-08-14)
- **Note**: Verbatim: "For 2025, file Form 944 by February 2, 2026. However, if you made deposits on time in full payment of the taxes due for the year, you may file the return by February 10, 2026" and the controlling point, "if the IRS notified you to file Form 944, you must file Form 944 (and not quarterly Forms 941) even if your tax liability for 2025 exceeds $1,000."

### Form 940, Federal Unemployment (FUTA) Tax Return `federal-form-940-futa`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp | category: unemployment
FUTA is an employer-only tax that funds unemployment benefits; you never withhold it from employee pay. It applies to the first $7,000 of each employee's annual wages, and most employers get a large credit for the state unemployment tax they already pay. You file it once a year on Form 940.
- **Deadline**: Due January 31 following the year reported. For tax year 2025 the due date was February 2 2026 because January 31 fell on a weekend, or February 10 2026 if all FUTA tax was deposited when due. Deposits are quarterly, required once cumulative liability exceeds $500.
- **Rule out first**:
  - The organization is a section 501(c)(3) exempt from tax under section 501(a), whose employees are generally not subject to FUTA tax at all. (common) Check: Confirm 501(c)(3) status on the IRS Tax Exempt Organization Search, and check the narrow exception for wages paid on behalf of a non-501(c)(3) organization.
  - Neither the $1,500 quarterly wage test nor the 20 week test was met, so no Form 940 is due. (common) Check: Review quarterly wage totals and weeks with at least one employee for the current and preceding year.
  - The business has no employees and pays only contractors or a sole owner taking draws, neither of which is FUTA wages. (common) Check: Confirm no W-2s were issued; note that an S corporation owner-employee's W-2 wages are FUTA wages.
  - Cumulative FUTA liability stayed at or below $500 for the year, so no quarterly deposits were required even though the annual return still is. (common) Check: Compute 0.6% of FUTA wages for the year and compare to $500.
- **If it genuinely was missed**: Failure to file penalty of 5% of the unpaid tax per month or part month, up to 25%, plus failure to deposit penalties.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript for the EIN and confirm a Form 940 posted for each year wages were paid. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Download the filed Form 940 and its acceptance confirmation from the payroll provider's tax documents section.
  - [tier 4, corroborating only] Reconcile Form 940 line 3 total payments to employees against the total of the four Forms 941 and the Forms W-2 for the year.
  - [tier 5, corroborating only] Look for quarterly FUTA deposits in EFTPS or the bank feed in years with meaningful headcount.
- **Fix**:
  1. Determine the first year either FUTA test was met.
  2. File all delinquent Forms 940 and pay the tax and interest.
  3. Check whether the state is a credit reduction state for any affected year, which increases the effective FUTA rate and is computed on Schedule A of Form 940.
  4. Confirm state unemployment tax was paid, because the 5.4% credit depends on timely state payments.
  5. Request First Time Abate or reasonable cause relief once current.
- **Source**: https://www.irs.gov/instructions/i940 (verified 2026-08-14)
- **Note**: Verbatim: "The FUTA tax applies to the first $7,000 you pay to each employee during a calendar year", "The FUTA tax is 6.0% (0.060) for 2025", "a maximum credit of up to 5.4% (0.054) against this FUTA tax", and "Continue carrying your tax liability over until your cumulative tax is more than $500. At that point, you must deposit your tax for the quarter." The commonly quoted 0.6% effective rate is arithmetic from the quoted 6.0% and 5.4% figures and holds only where the state is not a credit reduction state. Nonprofit exclusion verbatim: "Religious, educational, scientific, charitable, and other organizations described in section 501(c)(3) and exempt from tax under section 501(a) generally aren't subject to FUTA tax. However, a section 501(c)(3) organization is subject to FUTA tax when paying wages to employees on behalf of a non-section 501(c)(3) organization." For that reason nonprofit is excluded from entity_types here.

### Federal employment tax deposit schedule and EFTPS `federal-employment-tax-deposits`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Withheld payroll tax is not your money; you are holding it in trust and must hand it over on a fixed schedule that is separate from filing the return. Which schedule you are on is set by how much tax you reported in a lookback period, not by how big you feel. Miss a deposit and the penalty starts at 2% and climbs to 15%.
- **Deadline**: Monthly schedule depositors deposit by the 15th day of the following month. Semiweekly schedule depositors deposit by the following Wednesday for Wednesday, Thursday or Friday paydays, and by the following Friday for Saturday, Sunday, Monday or Tuesday paydays. If you accumulate $100,000 or more of employment taxes on any day, you must deposit by the next business day and you immediately become a semiweekly depositor. If the total liability for the quarter is under $2,500, you may pay it with the return instead of depositing.
- **Rule out first**:
  - Quarterly liability is under $2,500 so the employer legitimately pays with the return and no separate deposits appear. (common) Check: Total the quarter's employment tax liability and compare to $2,500.
  - A payroll provider remits under its own bank account and master EFTPS enrollment, so no debits appear under the client's own EFTPS login. (common) Check: Request the provider's tax payment confirmations and check the client's EFTPS enrollment status.
  - A deposit shortfall under $2,500 was made up by the shortfall makeup date, which is not a failure to deposit. This is a different $2,500 rule from the pay-with-return rule and the two are easily confused. (occasional) Check: Compare the shortfall amount and the makeup date against the rule in Publication 15.
  - The employer is a monthly depositor, so a single deposit on the 15th covers a whole month of pay runs and looks sparser than expected. (common) Check: Confirm the deposit schedule from the lookback period computation.
- **If it genuinely was missed**: Failure to deposit penalty on the unpaid deposit: 2% if 1 to 5 calendar days late, 5% if 6 to 15 days late, 10% if more than 15 days late, and 15% if not paid within 10 days of the first IRS notice or an immediate payment demand. The tiers replace each other rather than stacking.
- **How to prove it**:
  - [tier 2, settles it] Sign in to EFTPS with the EIN and pull the payment history report for the period, matching each deposit to a pay date. https://www.eftps.gov/
  - [tier 2, settles it] Order the business Account Transcript and look for failure to deposit penalty assessments and the deposit posting dates. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Pull the payroll provider's tax payment log and confirm each liability has a matching remittance with a settlement date.
  - [tier 4, corroborating only] Check Form 941 Schedule B for semiweekly depositors and confirm the daily liability record matches the deposits made.
  - [tier 5, corroborating only] Trace EFTPS debits in the bank feed and confirm the count and timing align with the pay calendar.
- **Fix**:
  1. Determine the correct deposit schedule from the lookback period before doing anything else.
  2. Deposit all outstanding trust fund amounts immediately via EFTPS, since the penalty tier escalates with time and withheld tax can become a personal liability of responsible officers.
  3. Enroll in EFTPS now if not enrolled, allowing several business days for activation.
  4. Reconcile deposits to liabilities by quarter and file Form 941-X where the reported liability was wrong.
  5. Request penalty abatement for reasonable cause or under First Time Abate once fully current.
- **Source**: https://www.irs.gov/publications/p15 (verified 2026-08-14)
- **Note**: Verbatim from Publication 15: "If the amount of employment taxes you deposited during the lookback period is $50,000 or less, you're a monthly schedule depositor", "If you accumulate $100,000 or more of employment taxes on any day during a deposit period, you must deposit the taxes by the next business day", and "You must use EFT to make all federal tax deposits." Lookback period and semiweekly timing corroborated at https://www.irs.gov/taxtopics/tc757: "The lookback period for Form 941 filers is the 12 months (covering four quarters) starting July 1st of the second preceding year and ending on June 30th of the prior year." Penalty tiers verified at https://www.irs.gov/payments/failure-to-deposit-penalty.

### Forms W-2 and W-3, Wage and Tax Statements `federal-form-w2-w3`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
Every employee gets a Form W-2 by the end of January, and the same data goes to the Social Security Administration on Form W-3. Both deadlines are the same date, which trips up employers used to having extra time to file after furnishing. If you file 10 or more information returns of any kind combined, W-2s must be filed electronically.
- **Deadline**: Furnish Copies B, C and 2 to employees and file Copy A with the SSA by January 31 following the year reported. If January 31 falls on a weekend or holiday the date moves to the next business day. For tax year 2025, filed in the 2026 season, both deadlines were February 2 2026 because January 31 2026 was a Saturday. For tax year 2026 both deadlines are February 1 2027 because January 31 2027 is a Sunday.
- **Rule out first**:
  - The company has no employees and issues only Forms 1099-NEC to contractors, so no W-2 is due. (common) Check: Confirm no wages were run and review worker classification for anyone treated as a contractor who behaves like an employee.
  - The payroll provider filed under its own agent EIN, so nothing appears under the client's SSA account. (occasional) Check: Ask the provider which EIN the W-2s were filed under and request the acceptance receipt.
  - Employees received electronic W-2s through the payroll portal after consenting, so no paper copies exist. (common) Check: Confirm affirmative electronic delivery consent is on file and that the forms were posted by the deadline.
  - The owner of a single-member LLC or a partner takes draws rather than wages, which are correctly not reported on a W-2. (common) Check: Confirm the entity is not taxed as a corporation, since owner draws are not wages for a disregarded entity or partnership.
- **If it genuinely was missed**: Section 6721 and 6722 information return penalties apply per form, per failure. See federal-information-return-penalties for the 2026 tiers.
- **How to prove it**:
  - [tier 2, settles it] Sign in to SSA Business Services Online and confirm the W-2 submission status and wage report for each year under the EIN. https://www.ssa.gov/bso/bsowelcome.htm
  - [tier 2, settles it] Order the IRS Wage and Income Transcript for an employee and confirm a W-2 from the employer posted for the year. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Download the W-2s and the SSA acceptance receipt from the payroll provider's year-end tax documents.
  - [tier 4, corroborating only] Reconcile Form W-3 totals to the sum of the four Forms 941 for the year; a mismatch triggers an IRS or SSA reconciliation notice.
  - [tier 5, corroborating only] Compare total payroll expense in the general ledger against total W-2 Box 1 wages.
- **Fix**:
  1. Produce and furnish the missing W-2s to employees immediately, since employees cannot file accurate personal returns without them.
  2. File Copy A and Form W-3 with the SSA electronically through Business Services Online.
  3. Reconcile the W-3 to the four Forms 941 and file Form 941-X or Form W-2c where they disagree.
  4. File corrected Forms W-2c for any errors in name, SSN or amounts.
  5. Request penalty relief citing reasonable cause, and note that penalties are reduced when corrected within 30 days.
- **Source**: https://www.irs.gov/instructions/iw2w3 (verified 2026-08-14)
- **Note**: Verbatim: "Mail or electronically file Copy A of Form(s) W-2 and Form W-3 with the SSA by February 1, 2027", "Generally, you must furnish Copies B, C, and 2 of Form W-2 to your employees by February 1, 2027", and "You must e-file Forms W-2... if you are required to file at least 10 information returns." SCOPE NOTE added 2026-08-14: the live revision at irs.gov/instructions/iw2w3 is the TAX YEAR 2026 revision, so its February 1 2027 dates govern W-2s filed in early 2027, not the 2026 filing season. The tax year 2025 instance of the same January 31 rule was February 2 2026, January 31 2026 having been a Saturday, which is corroborated by the identical shift the IRS applies to Forms 940 and 944 for 2025 ("The due date for filing Form 940 for 2025 is February 2, 2026"). Both years are now stated on the row so a reader working a 2025 close is not handed a 2027 date.

### Form 1099-NEC, Nonemployee Compensation `federal-form-1099-nec`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
When you pay a freelancer, consultant or unincorporated vendor for services, you report it on Form 1099-NEC. Both the copy to the contractor and the copy to the IRS are due January 31, with no extra time for filing electronically. Collect a Form W-9 before you pay anyone, because chasing tax IDs in January is how this goes wrong.
- **Deadline**: File with the IRS and furnish to the recipient by January 31 following the payment year. Section 6071(c) requires filing on or before January 31 using either paper or electronic procedures, so unlike most information returns there is no later electronic deadline.
- **Rule out first**:
  - The vendor is a corporation, including an LLC taxed as a C or S corporation, so no 1099-NEC is required. This is the single most common reason a large vendor has no 1099. (common) Check: Read the federal tax classification checkbox on the vendor's Form W-9.
  - Payments were made by credit card, debit card or a third party settlement organization, in which case the processor reports on Form 1099-K and the payer must not also issue a 1099-NEC. (common) Check: Check the payment method in the ledger; card and most marketplace payments are excluded from 1099-NEC.
  - Total payments to that vendor fell below the reporting threshold for the year. (common) Check: Total all payments to the vendor for the calendar year and compare to $600 for TY2025 or $2,000 for TY2026 onwards.
  - The vendor is a foreign person performing services outside the United States, which is reported on Form 1042-S if at all, not Form 1099-NEC. (occasional) Check: Check for a Form W-8BEN or W-8BEN-E on file and determine where the services were performed.
  - The payment was for goods or merchandise rather than services, which is not reportable on Form 1099-NEC. (common) Check: Review the invoice for what was actually purchased.
- **If it genuinely was missed**: Section 6721 and 6722 penalties per return. For 2026: $60 if filed up to 30 days late, $130 if filed 31 days late through August 1, $340 if after August 1 or not filed, and $680 for intentional disregard with no maximum.
- **How to prove it**:
  - [tier 2, settles it] Order the IRS Wage and Income Transcript for the recipient's TIN and confirm the 1099-NEC posted from your EIN. https://www.irs.gov/individuals/get-transcript
  - [tier 2, settles it] Check the IRS FIRE or IRIS system submission status and receipt for the filing under your Transmitter Control Code. https://www.irs.gov/filing/e-file-information-returns
  - [tier 3, corroborating only] Pull the 1099 filing report and acceptance confirmations from the accounting or filing platform (QuickBooks, Bill.com, Track1099, Gusto).
  - [tier 4, settles it] Collect the signed Forms W-9 for every vendor paid, then match the vendor payment ledger against the 1099s actually issued.
  - [tier 5, corroborating only] Run a vendor payment report for the year filtered above the threshold and compare the vendor count to the number of 1099s issued.
- **Fix**:
  1. Pull a vendor payment report for each open year and filter to non-corporate payees above the threshold, excluding card and marketplace payments.
  2. Request Forms W-9 from any vendor without one on file, and begin 24% backup withholding on future payments if they refuse.
  3. File the late 1099-NECs as soon as possible, because the penalty tier increases at 30 days and again after August 1.
  4. Furnish the recipient copies at the same time, since the recipient penalty under section 6722 is separate from the filing penalty.
  5. Change the vendor onboarding process so a W-9 is collected before the first payment is released.
- **Source**: https://www.irs.gov/instructions/i1099mec (verified 2026-08-14)
- **Note**: THRESHOLD CHANGE. Verbatim from the instructions: "For tax years beginning after 2025, the minimum threshold amount for reporting certain payments required to be reported on certain information returns and/or perform backup withholding on those payments increased to $2,000 and may be adjusted for inflation beginning in calendar year 2027." The $600 rule still governs TY2025 returns filed in January 2026; $2,000 governs TY2026 returns filed in early 2027. Deadline verbatim: "Section 6071(c) requires you to file Form 1099-NEC on or before January 31, using either paper or electronic filing procedures." Corporation exception verbatim: "The exemption from reporting payments made to corporations does not apply to payments for legal services." Penalty tiers from https://www.irs.gov/payments/information-return-penalties.

### Form 1099-MISC, Miscellaneous Information `federal-form-1099-misc`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
Form 1099-MISC covers business payments that are not compensation for services: rent you pay a landlord, prizes and awards, royalties, and gross proceeds paid to an attorney. Unlike the 1099-NEC, you get extra time to file with the IRS if you file electronically. The recipient copy is still due January 31.
- **Deadline**: Furnish to the recipient by January 31. File with the IRS by February 28 if filing on paper, or March 31 if filing electronically.
- **Rule out first**:
  - Rent was paid to a real estate agent or property manager, in which case the payer does not file; the agent handles the reporting to the property owner. (common) Check: Check whether the payee on the lease is a management company acting as agent.
  - The landlord or payee is a corporation, so the general corporate exemption applies. (common) Check: Read the federal tax classification on the payee's Form W-9.
  - The office is a coworking membership or short-term license rather than a lease, and is commonly treated as a service rather than rent. (occasional) Check: Read the agreement to determine whether it conveys an interest in real property or is a service arrangement.
  - Payments were made by credit card, so the card processor reports on Form 1099-K and the payer must not double report. (common) Check: Check the payment method in the ledger.
  - A legal payment was for the attorney's services and was correctly reported in box 1 of Form 1099-NEC rather than as gross proceeds on Form 1099-MISC. (occasional) Check: Determine whether the payment was fees for services or settlement proceeds passing through the attorney.
- **If it genuinely was missed**: Section 6721 and 6722 penalties per return. For 2026: $60 up to 30 days late, $130 through August 1, $340 after August 1 or not filed, and $680 for intentional disregard with no maximum.
- **How to prove it**:
  - [tier 2, settles it] Order the IRS Wage and Income Transcript for the recipient TIN and confirm the 1099-MISC posted from your EIN. https://www.irs.gov/individuals/get-transcript
  - [tier 2, settles it] Check the IRS IRIS or FIRE submission receipt for the filing. https://www.irs.gov/filing/e-file-information-returns
  - [tier 3, corroborating only] Pull the 1099 filing summary and acceptance confirmations from the accounting or filing platform.
  - [tier 4, settles it] Review the lease agreement and the rent ledger, then confirm a 1099-MISC was issued to any non-corporate landlord above the threshold.
  - [tier 5, corroborating only] Run a general ledger report for rent, royalties and legal settlement accounts and compare to the 1099-MISCs issued.
- **Fix**:
  1. Review rent, royalty, prize and legal settlement accounts for each open year against the payee list.
  2. Obtain Forms W-9 for any payee lacking one.
  3. File the late Forms 1099-MISC and furnish recipient copies immediately.
  4. Correct any 1099s filed in the wrong box or with the wrong TIN by filing a corrected return.
  5. Request penalty relief for reasonable cause where the failure was inadvertent and promptly corrected.
- **Source**: https://www.irs.gov/instructions/i1099mec (verified 2026-08-14)
- **Note**: Same combined instructions document as Form 1099-NEC. Verbatim thresholds for the 2026 revision: rents "$2,000 or more" (box 1), other income and prizes "$2,000 or more" (box 3), royalties "$10 or more", and "At least $600 in gross proceeds paid to an attorney (box 10)", which was not raised. IRS filing deadlines verbatim: "February 28, if you file on paper" and "March 31, if you file electronically." Note that in a year where February 28 falls on a weekend the paper date shifts to the next business day.

### Mandatory electronic filing of information returns (10 or more) `federal-information-return-efile-threshold`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
The old 250-form paper threshold is gone. If you file 10 or more information returns of all types combined in a year, every one of them must be filed electronically. The count aggregates across form types, so six 1099-NECs plus five W-2s puts you over the line even though neither alone would.
- **Deadline**: Applies to the filing of each information return at its own deadline. The threshold has applied since returns required to be filed on or after January 1 2024, per Treasury Decision 9972.
- **Rule out first**:
  - The company files fewer than 10 information returns in total, so paper filing remains permitted. (common) Check: Add up W-2s, 1099s, 1095s and any other information returns for the year.
  - A payroll provider or filing platform transmitted everything electronically on the company's behalf, so no in-house TCC exists. (common) Check: Request the provider's transmission receipts and IRS acceptance records.
  - The company obtained a hardship waiver on Form 8508 for the year. (rare) Check: Look for the approved Form 8508 waiver in the tax file.
- **If it genuinely was missed**: Filing on paper when electronic filing is required is treated as a failure to file, exposing the filer to the section 6721 per return penalties.
- **How to prove it**:
  - [tier 2, settles it] Confirm the entity has an active IRIS Transmitter Control Code or a FIRE account, and pull the electronic submission receipts for the year. https://www.irs.gov/filing/e-file-information-returns
  - [tier 3, corroborating only] Pull the filing platform's transmission log showing electronic submission and IRS acceptance for every return in the batch.
  - [tier 4, settles it] Count all information returns required for the year across W-2, 1099, 1095 and 3921 types and compare the total to 10.
  - [tier 5, corroborating only] Count distinct reportable vendors and employees in the ledger as a rough proxy for the return count.
- **Fix**:
  1. Count all information returns for the year in aggregate to confirm the threshold is met.
  2. Register for IRIS or FIRE well before January, since obtaining a Transmitter Control Code takes time.
  3. Use a filing platform or the payroll provider rather than building the capability in-house for a small volume.
  4. Refile electronically any returns that were improperly paper filed and request penalty relief.
- **Source**: https://www.irs.gov/filing/e-file-information-returns (verified 2026-08-14)
- **Note**: Verbatim: "if you have 10 or more information returns, you must file them electronically." Aggregation rule verbatim from https://www.irs.gov/instructions/i1099gi: "If you are required to file 10 or more information returns during the year, you must e-file. The 10-or-more requirement does not apply separately to each type of form." The IRS example given is that four Forms 1098 plus six Forms 1099-A requires e-filing.

### Information return penalties (sections 6721 and 6722) `federal-information-return-penalties`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
Late or wrong 1099s and W-2s carry a penalty per form, and it doubles roughly twice as the year goes on. There are actually two parallel penalties: one for filing late with the IRS and a matching one for getting the copy to the recipient late. If the IRS decides you ignored the rule on purpose there is no cap at all.
- **Deadline**: Measured against each information return's own due date. Correcting within 30 days of the due date keeps you in the cheapest tier; correcting by August 1 keeps you in the middle tier.
- **Rule out first**:
  - All returns were filed on time, so no penalty exists and the absence of an assessment is the correct outcome. (common) Check: Compare submission timestamps to the due dates.
  - The IRS proposed a penalty on Notice 972CG but it was abated after a reasonable cause response, so nothing was ultimately assessed. (occasional) Check: Look for the abatement letter and confirm the account transcript shows the reversal.
  - A TIN mismatch notice (CP2100) was received but the payer completed the required B-notice solicitation process, which is a defense rather than a failure. (occasional) Check: Confirm first and second B notices were sent to the payee within the required windows.
  - Penalties were assessed against a payroll provider or filing agent rather than the company. (rare) Check: Check whose EIN was the transmitter of record.
- **If it genuinely was missed**: Per return for 2026: up to 30 days late $60; 31 days late through August 1 $130; after August 1 or not filed $340; intentional disregard $680. For 2025: $60, $130, $330 and $660. Annual caps differ for small and large businesses and are inflation adjusted; there is no maximum penalty for intentional disregard.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript and look for assessed information return penalties by year, or review IRS Notice 972CG proposing the penalty. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Pull the filing platform's transmission timestamps and compare each to the statutory due date to size the exposure by tier.
  - [tier 4, settles it] Review any IRS Notice 972CG or CP2100/CP2100A received, which identify the specific returns and TIN mismatches at issue.
  - [tier 5, corroborating only] Look for an IRS penalty debit in the bank feed and trace it back to the notice that assessed it.
- **Fix**:
  1. File any missing returns immediately, because the tier escalates at 30 days and again after August 1.
  2. Respond to Notice 972CG within the stated window with a reasonable cause statement; ignoring it converts a proposal into an assessment.
  3. Run the TIN Matching service before filing next year to prevent mismatch penalties.
  4. Complete the B-notice process for any payee whose TIN the IRS flagged, and begin backup withholding where required.
- **Source**: https://www.irs.gov/payments/information-return-penalties (verified 2026-08-14)
- **Note**: Tier amounts are verbatim from the IRS penalties page for 2026 and 2025. The IRS page deliberately does not publish the dollar caps, stating only: "The maximum penalty is different for small businesses and large businesses including government entities. There is no maximum penalty for intentional disregard." The unindexed statutory caps in 26 USC 6721, verified at https://uscode.house.gov/view.xhtml?req=granuleid:USC-prelim-title26-section6721&num=0&edition=prelim, are $3,000,000 general, $500,000 if corrected within 30 days and $1,500,000 if corrected by August 1, with small business (under $5M gross receipts) caps of $1,000,000, $175,000 and $500,000. Those are base statutory figures and the live caps are inflation adjusted; the adjusted amounts could not be retrieved from any .gov page in this pass, so do not quote a specific cap figure to a client without re-verifying.

### Form 1099-K, Payment Card and Third Party Network Transactions `federal-form-1099-k`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
This is a form you usually receive rather than file. Stripe, PayPal, Shopify and similar processors report your gross sales to the IRS on Form 1099-K. The number is gross, before refunds and fees, so it will be higher than your revenue and you need to reconcile it or the IRS will think you underreported.
- **Deadline**: Furnished to you by January 31 following the year reported. If you are the payment settlement entity doing the filing, the IRS deadlines are February 28 on paper or March 31 electronically.
- **Rule out first**:
  - Volume through a third party settlement organization did not clear both halves of the test, which requires payments exceeding $20,000 AND more than 200 transactions. Failing either one means no 1099-K was issued even though real revenue exists. (common) Check: Pull the annual volume and transaction count from the processor dashboard.
  - Reported gross exceeds book revenue because the 1099-K is before refunds, chargebacks and processor fees. This is expected, not a discrepancy. (common) Check: Build a reconciliation from 1099-K gross to net revenue showing fees and refunds as reconciling items.
  - The 1099-K was issued under an owner's SSN or an old entity name because the processor account was opened before the entity existed. (occasional) Check: Check the taxpayer details on the processor account and update them, then look for the 1099-K on the owner's individual transcript.
  - Payments were routed through a platform that reports under its own merchant of record arrangement, so no 1099-K comes to the company directly. (occasional) Check: Confirm the merchant of record on the platform agreement.
- **If it genuinely was missed**: Section 6721 and 6722 penalties apply to the filer, which for most companies is the processor rather than the company itself.
- **How to prove it**:
  - [tier 2, settles it] Order the IRS Wage and Income Transcript for the entity's EIN and list every 1099-K reported against it for the year. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Download the Form 1099-K from each processor's dashboard (Stripe, PayPal, Square, Shopify) and confirm the EIN and legal name on it are correct.
  - [tier 4, settles it] Reconcile the gross amount on each 1099-K to the revenue reported on the tax return, documenting refunds, chargebacks and processor fees as the bridge.
  - [tier 5, corroborating only] Compare processor payout deposits in the bank feed to the gross 1099-K amount and quantify the fee and refund difference.
- **Fix**:
  1. Collect every 1099-K for the year and reconcile the total to reported gross receipts before filing.
  2. Correct the taxpayer name and TIN on any processor account reporting under the wrong entity.
  3. If a 1099-K reported income that is not yours or is duplicated, document it and report the reconciliation on the return rather than ignoring the form.
  4. Amend the return if reported revenue was genuinely understated.
- **Source**: https://www.irs.gov/businesses/understanding-your-form-1099-k (verified 2026-08-14)
- **Note**: Verbatim: "Third party settlement organizations (TPSOs) (payment apps and online marketplaces) are required to report payments on Form 1099-K when the total amount of payments you receive for goods or services through the platform exceeds $20,000 in more than 200 transactions" and "you'll get a Form 1099-K from your payment card processor no matter how many payments you got or how much they were for." This threshold has moved repeatedly in recent years; the $20,000 and 200 transaction test is what the IRS is currently publishing, but neither the landing page nor the Form 1099-K instructions tie the figure to a named tax year, so confirm the applicable year before relying on it for a specific filing season.

### Form W-9 collection and 24% backup withholding `federal-backup-withholding-w9`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: tax
Before you pay a contractor or vendor, get a signed Form W-9 with their taxpayer ID. If they will not give you a valid one, the law requires you to hold back 24% of the payment and send it to the IRS. If you skip both steps, the IRS can come after you for the tax you failed to withhold.
- **Deadline**: The IRS publishes no deadline for collecting a Form W-9. It keys the obligation to the payment rather than to onboarding: backup withholding at 24% is required on a reportable payment when the payee has not furnished a correct TIN (BWH-B), or when the IRS notifies you of underreported interest or dividends (BWH-C). Collecting the W-9 before the first payment is a practice recommendation, not an agency rule. Once withheld, the tax is deposited on the same schedule as other withheld taxes and reported annually on Form 945.
- **Rule out first**:
  - All vendors provided valid TINs, so no backup withholding is required and its absence is correct. (common) Check: Confirm a W-9 is on file for each payee and that no CP2100 notice was received.
  - Payments were made by card or through a third party settlement organization, where the processor rather than the payer handles any backup withholding. (common) Check: Check the payment method for the vendors in question.
  - The payee is a foreign person who provided a Form W-8BEN or W-8BEN-E, which takes them out of backup withholding and into the chapter 3 withholding regime instead. (occasional) Check: Look for the W-8 series form and then check federal-form-1042-1042s.
  - The vendor is a corporation for which no reportable payment arises, so no W-9 was strictly necessary even though best practice is to collect one. (common) Check: Confirm the payee's classification and the nature of the payment.
- **If it genuinely was missed**: The payer can become liable for the amount that should have been withheld, plus information return penalties for filing 1099s with missing or incorrect TINs.
- **How to prove it**:
  - [tier 2, settles it] Run the payee TINs through the IRS TIN Matching service in e-Services to confirm each name and TIN combination matches IRS records. https://www.irs.gov/tax-professionals/taxpayer-identification-number-tin-matching
  - [tier 2, settles it] Check whether IRS Notice CP2100 or CP2100A was received, which lists the specific payees with mismatched TINs.
  - [tier 3, corroborating only] Check the AP or payments platform for W-9 collection status flags on each vendor record.
  - [tier 4, settles it] Audit the vendor master file and confirm a signed, dated Form W-9 exists for every payee who received a reportable payment.
  - [tier 5, corroborating only] Look for a Form 945 deposit pattern, which indicates backup withholding is actually being remitted.
- **Fix**:
  1. Request a Form W-9 from every payee lacking one, using the required solicitation process.
  2. Begin 24% backup withholding on future payments to any payee who does not supply a valid TIN.
  3. Run TIN Matching on the entire vendor file before the next 1099 season.
  4. Complete the first and second B-notice process for any payee named on a CP2100 notice.
  5. Register for and file Form 945 if backup withholding is actually withheld.
- **Source**: https://www.irs.gov/businesses/small-businesses-self-employed/backup-withholding (verified 2026-08-14)
- **Note**: Verbatim rate: "There are situations when the payer is required to withhold at the current rate of 24 percent." The IRS page describes BWH-B (failure to provide a correct TIN) and BWH-C (underreporting of interest and dividends) as the two triggers. CORRECTED 2026-08-14: an earlier version of this row stated the deadline as "collect the W-9 before the first payment." The IRS page states no such rule. It puts the duty on the payee ("When you open a new account, make an investment, or begin to receive payments reportable on Form 1099, you must furnish your TIN in writing") and makes the payer's liability turn on whether a correct TIN was furnished for a reportable payment, not on when a form was gathered. The recommendation is retained but is now labelled as ours. Note that the same threshold increase to $2,000 for tax years beginning after 2025 governs when backup withholding is required on 1099-reportable payments, per the Instructions for Forms 1099-MISC and 1099-NEC.

### Form 3921, Exercise of an Incentive Stock Option `federal-form-3921-iso-exercise`
Applies to: c-corp, s-corp, benefit-corp | category: information-report
Every time an employee exercises an incentive stock option, the company must file a Form 3921 for that transfer and give the employee a copy. Startups miss this constantly because it feels like a cap table event rather than a tax filing. The employee needs it to compute alternative minimum tax, so failing to send it creates a problem for them as well as a penalty for you.
- **Deadline**: Furnish the statement to the employee by January 31 following the calendar year of exercise. File with the IRS by February 28 on paper or March 31 electronically. For calendar year 2025 exercises the paper date was March 2 2026 because February 28 2026 fell on a weekend.
- **Rule out first**:
  - All options exercised were nonqualified stock options rather than ISOs, so Form 3921 does not apply and the spread was instead reported on the Form W-2. (common) Check: Read the grant documents for ISO designation and check for the W-2 box 12 code V reporting.
  - No options were exercised during the year, only granted or vested, and neither of those is a reportable event. (common) Check: Pull the exercise log from the cap table platform for the calendar year.
  - The cap table provider filed the Forms 3921 on the company's behalf, so no in-house filing record exists. (common) Check: Ask the provider for the filing confirmations and the recipient statement delivery log.
  - The exercising person is a nonresident alien not receiving a Form W-2, which is an explicit exception in the instructions. (rare) Check: Confirm the individual's status and whether the company issues them a W-2.
- **If it genuinely was missed**: Section 6721 and 6722 penalties per return: for 2026, $60 up to 30 days late, $130 through August 1, $340 after August 1 or not filed, and $680 for intentional disregard.
- **How to prove it**:
  - [tier 2, settles it] Order the employee's IRS Wage and Income Transcript and confirm a Form 3921 posted from the company's EIN for the year. https://www.irs.gov/individuals/get-transcript
  - [tier 2, settles it] Check the IRS IRIS or FIRE submission receipt for the 3921 batch. https://www.irs.gov/filing/e-file-information-returns
  - [tier 3, corroborating only] Pull the exercise report for the calendar year from the cap table platform (Carta, Pulley, Shareworks) and compare the ISO exercise count to the number of Forms 3921 filed.
  - [tier 4, settles it] Review board consents and stock option exercise notices for the year and confirm which grants were ISOs rather than NSOs.
  - [tier 5, corroborating only] Look for exercise price payments received into the company bank account during the year, each of which should correspond to a share transfer.
- **Fix**:
  1. Pull a complete ISO exercise log for every open year from the cap table system.
  2. File the missing Forms 3921 with the IRS and furnish the employee statements immediately, since employees may have filed AMT calculations without them.
  3. Notify affected employees, because they may need to amend personal returns.
  4. Have the cap table provider file automatically going forward and confirm it in writing.
  5. Request penalty relief for reasonable cause where the failure was inadvertent and promptly corrected.
- **Source**: https://www.irs.gov/instructions/i3921 (verified 2026-08-14)
- **Note**: Verbatim trigger: "Every corporation which in any calendar year transfers to any person a share of stock pursuant to that person's exercise of an incentive stock option described in section 422(b) must, for that calendar year, file Form 3921 for each transfer made during that year." SCOPE CORRECTED 2026-08-14: an earlier version of this row limited entity_types to c-corp and benefit-corp. The instructions say "Every corporation" and neither section 422(b) nor the instructions carve out an S corporation, so s-corp is now in scope. An S corporation may grant incentive stock options and must file Form 3921 on exercise. The Form 3921 instructions do not carry the due dates themselves; they point to the General Instructions for Certain Information Returns at https://www.irs.gov/instructions/i1099gi, which supply the January 31 recipient date and the February 28 paper / March 31 electronic IRS dates.

### Form 8300, Report of Cash Payments Over $10,000 `federal-form-8300-cash-payments`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
If your business takes in more than $10,000 in cash from one buyer, in one transaction or a series of related ones, you have 15 days to report it. Cash includes cashier's checks and money orders, not just currency. This is an anti-money-laundering rule and the penalties for deliberately ignoring it are severe.
- **Deadline**: File within 15 days after the date the cash transaction occurred. Furnish a written statement to each person named on the form by January 31 of the year following the reportable transaction.
- **Rule out first**:
  - The business is entirely card, ACH and wire based and never receives cash, which is true of nearly all software and services companies. (common) Check: Scan the ledger for any cash receipt account activity at all.
  - Payments over $10,000 were received by wire or personal check, neither of which is cash for this purpose. (common) Check: Confirm the instrument used; personal checks and wires are excluded from the definition of cash.
  - Multiple cash payments from the same customer were genuinely unrelated and each stayed under the threshold, with no 12 month aggregation trigger. (occasional) Check: Review the related transaction rules and the 12 month aggregation window against the customer's payment history.
  - The transaction was reported to FinCEN by the bank on a Currency Transaction Report, which is a separate obligation and does not substitute for Form 8300. (rare) Check: Confirm whether the business itself filed Form 8300; the bank's CTR does not discharge the business's duty.
- **If it genuinely was missed**: The IRS states penalties apply and are adjusted annually for inflation, but publishes no dollar amounts on this page. Criminal penalties can apply to willful failure to file.
- **How to prove it**:
  - [tier 2, settles it] Check the FinCEN BSA E-Filing System account for submitted Forms 8300 and their acknowledgments. https://bsaefiling.fincen.treas.gov/
  - [tier 4, settles it] Obtain the filed Form 8300 and its BSA E-Filing acknowledgment, and the copy of the written statement furnished to the payer.
  - [tier 4, corroborating only] Review sales invoices and receipts for the payment method recorded on large transactions.
  - [tier 5, corroborating only] Review the general ledger and deposit records for cash, cashier's check and money order receipts over $10,000, and for structured deposits just under the threshold.
- **Fix**:
  1. Identify every reportable cash receipt in open years from the ledger and deposit records.
  2. File the delinquent Forms 8300 through the FinCEN BSA E-Filing System and mark them late with an explanation.
  3. Furnish the required written statements to each named payer.
  4. Get counsel involved before filing if the failures look willful or if structuring is a possibility, because criminal exposure changes the calculus.
  5. Write a cash receipts policy with a $10,000 flag so the 15 day clock is never missed again.
- **Source**: https://www.irs.gov/businesses/small-businesses-self-employed/form-8300-and-reporting-cash-payments-of-over-10000 (verified 2026-08-14)
- **Note**: Verbatim: "Generally, if you're in a trade or business and receive more than $10,000 in cash in a single transaction or in related transactions, you must file Form 8300", "You must file Form 8300 within 15 days after the date the cash transaction occurred", and "You must e-file your Forms 8300 if you're required to file at least 10 information returns of one or more type(s) other than Form 8300 during a calendar year." No penalty dollar amounts are stated on the IRS page, so none are asserted here.

### FBAR, FinCEN Form 114, Report of Foreign Bank and Financial Accounts `federal-fbar-fincen-114`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
If your company holds foreign bank accounts that together topped $10,000 at any point in the year, you file an FBAR. It goes to FinCEN through a separate e-filing system, not with your tax return, which is why people miss it. A single day above the threshold triggers it, and the threshold is the combined total of all foreign accounts, not each one.
- **Deadline**: Due April 15 following the calendar year reported, with an automatic extension to October 15. You do not need to request the extension.
- **Rule out first**:
  - The company holds no foreign financial accounts at all, which is true of most domestic-only businesses. (common) Check: Review the chart of accounts and bank list for any non-US institution.
  - Aggregate foreign balances never exceeded $10,000 at any point in the year, so no filing is due. (common) Check: Take the maximum value of each foreign account during the year and sum them, rather than using year-end balances.
  - The account is held with a US financial institution's foreign branch or is a US account denominated in foreign currency, neither of which is necessarily a foreign financial account. (occasional) Check: Determine where the account is physically maintained, which is the controlling test.
  - The FBAR was filed by an officer personally for signature authority, and the entity filing is separate; seeing one does not confirm or deny the other. (occasional) Check: Check the BSA E-Filing history for both the individual and the entity.
  - A payment platform balance is not a foreign bank account, so a foreign-currency wallet may not trigger the requirement. (occasional) Check: Determine whether the provider is a foreign financial institution holding a reportable account.
- **If it genuinely was missed**: The IRS states civil FBAR penalty maximums are adjusted annually for inflation and warns that published amounts may not be current. No specific dollar figures are asserted here.
- **How to prove it**:
  - [tier 2, settles it] Sign in to the FinCEN BSA E-Filing System and retrieve the submitted FBAR and its BSA Identifier acknowledgment for each year. https://bsaefiling.fincen.treas.gov/
  - [tier 4, settles it] Obtain the filed FinCEN Form 114 with its BSA tracking ID and confirm all foreign accounts are listed with maximum values.
  - [tier 4, settles it] Collect year-end and peak balance statements for every foreign account to establish whether the aggregate crossed $10,000.
  - [tier 5, corroborating only] Review the trial balance for foreign-denominated cash accounts and any wires to or from non-US institutions.
- **Fix**:
  1. Build a complete list of foreign accounts and their maximum values for every open year.
  2. File delinquent FBARs through the BSA E-Filing System using the delinquent FBAR submission procedures, which require a statement of the reason for filing late.
  3. Do not file quietly if there is also unreported income; consult counsel about the appropriate disclosure program first.
  4. Check whether Form 8938 (Statement of Specified Foreign Financial Assets) is separately required, since it has different thresholds and is filed with the tax return.
- **Source**: https://www.irs.gov/businesses/small-businesses-self-employed/report-of-foreign-bank-and-financial-accounts-fbar (verified 2026-08-14)
- **Note**: Verbatim: "the aggregate value of those foreign financial accounts exceeded $10,000 at any time during the calendar year reported", the deadline is "April 15 following the calendar year reported" with "an automatic extension to October 15 if you fail to meet the FBAR annual due date of April 15. You don't need to request an extension to file the FBAR", and "You must file the FBAR electronically through FinCEN's BSA E-Filing System. You don't file the FBAR with your federal tax return." fincen.gov timed out on repeated fetch attempts, so this rests on the IRS page alone; penalty figures were deliberately not asserted because the IRS page itself warns its amounts may be stale.

### Forms 1042 and 1042-S, withholding on payments to foreign persons `federal-form-1042-1042s-foreign-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
When you pay a foreign person US-source income such as royalties, interest, dividends or certain service fees, you are a withholding agent and the default rate is 30% unless a tax treaty lowers it. You report on Form 1042-S and file the summary on Form 1042. Founders paying overseas contractors often assume a 1099 is the answer; for a foreign payee it is not.
- **Deadline**: Forms 1042-S must be filed with the IRS and furnished to the recipient by March 15 of the following calendar year, whether filed on paper or electronically. There is no extra time for electronic filing and the recipient and IRS deadlines are the same date.
- **Rule out first**:
  - The foreign contractor performed all services outside the United States, making the income foreign-source and outside the withholding and 1042-S regime entirely. This is the most common and usually correct explanation for a startup with overseas developers. (common) Check: Establish where the work was physically performed and document it, along with a Form W-8BEN.
  - A valid treaty claim on Form W-8BEN reduced the rate to zero, so no withholding appears even though a 1042-S may still be required. (occasional) Check: Read the treaty article and limitation on benefits claim on the W-8 and confirm a 1042-S was still filed.
  - The payee is a US person or a US entity owned by foreign persons, so Form 1099 applies rather than Form 1042-S. (common) Check: Check whether the payee provided a Form W-9 or a Form W-8.
  - Payments were made to a foreign entity's US branch treated as a US payee. (rare) Check: Review the W-8BEN-E chapter 3 status boxes.
- **If it genuinely was missed**: Section 6721 and 6722 information return penalties apply. The withholding agent can also be liable for tax that should have been withheld but was not.
- **How to prove it**:
  - [tier 2, settles it] Order the business Account Transcript for the EIN and confirm a Form 1042 posted for each year with foreign payments. https://www.irs.gov/individuals/get-transcript
  - [tier 3, corroborating only] Check the AP or contractor payment platform for foreign payee tax form collection status and any withholding applied.
  - [tier 4, settles it] Collect the Forms W-8BEN or W-8BEN-E on file for every foreign payee and confirm they are current and complete, including a treaty claim where a reduced rate was applied.
  - [tier 4, settles it] Obtain the filed Forms 1042-S and the Form 1042 and reconcile total payments and withholding between them.
  - [tier 5, corroborating only] Review international wires and foreign contractor payments in the ledger and match them to a W-8 on file.
- **Fix**:
  1. Inventory all payments to non-US payees for each open year and determine the source of the income, which turns on where services were performed.
  2. Collect current Forms W-8BEN or W-8BEN-E for every foreign payee, since a stale or missing form defaults you to 30% withholding.
  3. File delinquent Forms 1042-S and Form 1042 and deposit any tax that should have been withheld.
  4. Quantify the withholding agent liability before filing, and involve international tax counsel if the amounts are material.
  5. Put a W-8 collection step into vendor onboarding for any non-US payee.
- **Source**: https://www.irs.gov/instructions/i1042s (verified 2026-08-14)
- **Note**: Verbatim: "Every withholding agent must file an information return on Form 1042-S to report amounts paid during the preceding calendar year" and "Forms 1042-S, whether filed on paper or electronically, must be filed with the IRS and be furnished to the recipient of the income by March 15 of the following calendar year." The 30% default rate is verbatim from https://www.irs.gov/individuals/international-taxpayers/nra-withholding: "Most types of U.S. source income received by a foreign person are subject to U.S. tax of 30%." The March 15 due date for Form 1042 itself was NOT independently verified; only the Form 1042-S date was confirmed. The IRS Form 7004 due dates chart for PY2026 does show Form 1042 tax period 202512 due 03/16/2026, consistent with a March 15 rule shifted for the weekend.

### ACA Forms 1094-C and 1095-C, Applicable Large Employer reporting `federal-aca-1094c-1095c`
Applies to: c-corp, s-corp, llc, partnership, benefit-corp, nonprofit | category: information-report
Once you average 50 or more full-time and full-time-equivalent employees, the Affordable Care Act requires you to offer coverage and to prove it with an annual filing. You give each full-time employee a Form 1095-C and file the whole set with the IRS under a Form 1094-C transmittal. The threshold counts part-timers in aggregate, so companies cross it before they expect to.
- **Deadline**: For calendar year 2025: furnish Form 1095-C to each full-time employee by March 2 2026, and file with the IRS by March 2 2026 on paper or March 31 2026 electronically. The underlying statutory rule is February 28 for paper and March 31 for electronic filing, with the furnishing deadline extended by regulation.
- **Rule out first**:
  - The company averaged fewer than 50 full-time equivalents in the prior year, so it is not an ALE and no filing is due. (common) Check: Run the month by month FTE computation for the prior calendar year rather than relying on current headcount.
  - Headcount crossed 50 only in the current year, so ALE status and the filing obligation begin next year, not this one. (common) Check: Confirm which calendar year the threshold was first met; ALE status is based on the preceding year.
  - A benefits administrator or PEO filed on the company's behalf, so no in-house record exists. (common) Check: Request the AIR receipt ID and acceptance status from the administrator.
  - Many workers are genuine independent contractors and are correctly excluded from the full-time equivalent count. (occasional) Check: Review worker classification, since misclassification would change both the ALE determination and the coverage exposure.
- **If it genuinely was missed**: Section 6721 and 6722 information return penalties apply per form. Separate employer shared responsibility payments under section 4980H can apply for failing to offer adequate coverage, which is a much larger exposure than the reporting penalty.
- **How to prove it**:
  - [tier 2, settles it] Check the IRS AIR (Affordable Care Act Information Returns) system for the transmission receipt and acceptance status for each year.
  - [tier 3, corroborating only] Pull the 1094-C and 1095-C filing package and acceptance confirmations from the payroll or benefits administrator.
  - [tier 4, settles it] Recompute the full-time equivalent count month by month for the prior calendar year to confirm ALE status, since this is the threshold question.
  - [tier 4, settles it] Check for IRS Letter 226-J proposing an employer shared responsibility payment, which indicates the IRS has already assessed the coverage question.
  - [tier 5, corroborating only] Review health insurance premium payments in the ledger as an indicator of whether group coverage was actually offered.
- **Fix**:
  1. Recompute ALE status for each year in question before assuming a failure exists.
  2. File the delinquent Forms 1094-C and 1095-C and furnish the employee statements.
  3. Respond to any Letter 226-J within the stated window, because the shared responsibility payment dwarfs the reporting penalty.
  4. Correct any 1095-C coding errors, particularly the line 14 and 16 offer and safe harbor codes, which drive the 4980H assessment.
  5. Engage a benefits advisor if coverage was not offered at all, since that is a substantive compliance problem and not just a filing one.
- **Source**: https://www.irs.gov/instructions/i109495c (verified 2026-08-14)
- **Note**: Verbatim from the instructions: "An ALE Member must furnish a Form 1095-C to each of its full-time employees by March 2, 2026, for the 2025 calendar year" and "Forms 1094-C and 1095-C are required to be filed by March 2, 2026, or March 31, 2026, if filing electronically." ALE threshold verbatim from https://www.irs.gov/affordable-care-act/employers: "If you have 50 or more full-time employees, including full-time equivalent employees, you are an applicable full-time employer and need to issue statements to employees and file an annual information return." The alternative manner of furnishing (posting a notice and providing statements on request) could not be verified on either page and is not asserted here.

### Form I-9, Employment Eligibility Verification `federal-form-i9-employment-eligibility`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
Every person you hire in the US must complete a Form I-9 and you must inspect their identity and work authorization documents within three business days. You never file it with anyone; you keep it and produce it if an inspector asks. Founders skip this because nothing is due to a government agency, which is exactly why it is a common audit finding.
- **Deadline**: The employee completes Section 1 at the time of hire. The employer completes Section 2 within three business days of the hire. Retain the form for three years after the date of hire or one year after the date employment is terminated, whichever is later.
- **Rule out first**:
  - The company has no employees and engages only independent contractors, for whom no I-9 is required. (common) Check: Confirm no W-2s were issued, and separately assess worker classification risk.
  - I-9s are stored electronically in the HR platform rather than in a physical binder, so a paper file search finds nothing. (common) Check: Check the HR system's I-9 module and export the completed forms.
  - Forms for departed employees were properly purged after the retention period expired, which is permitted and often advisable. (common) Check: Compute the retention date as three years after hire or one year after termination, whichever is later, for each missing person.
  - Employees work entirely outside the United States, so no I-9 is required for them. (occasional) Check: Confirm the work location and whether the individual is a US employee or a foreign entity's employee.
- **If it genuinely was missed**: Civil penalties apply for paperwork violations and for knowingly employing unauthorized workers. Specific dollar amounts were not verified in this pass and are deliberately not stated.
- **How to prove it**:
  - [tier 3, corroborating only] Check the HR platform (Gusto, Rippling, Justworks) for I-9 completion status per employee and any E-Verify case records.
  - [tier 4, settles it] Pull the I-9 binder or electronic I-9 system and confirm a completed form exists for every current employee and for former employees still inside the retention window.
  - [tier 4, settles it] Compare Section 2 completion dates against each employee's hire date to confirm the three business day rule was met.
  - [tier 4, corroborating only] Reconcile the employee roster from the Forms W-2 for the year against the I-9 file to find gaps.
- **Fix**:
  1. Audit the I-9 file against the full employee roster and identify missing or incomplete forms.
  2. Complete missing I-9s now, using today's actual date; never backdate, because backdating converts a paperwork violation into a far more serious problem.
  3. Correct errors by drawing a line through the wrong entry, entering the correct information, and initialing and dating the change.
  4. Attach a signed memo to any late-completed form explaining when and why it was completed.
  5. Move to an electronic I-9 system with completion deadlines built into onboarding.
- **Source**: https://www.govinfo.gov/content/pkg/CFR-2023-title8-vol1/xml/CFR-2023-title8-vol1-sec274a-2.xml (verified 2026-08-14)
- **Note**: uscis.gov returned HTTP 403 and ecfr.gov redirected off-host, so 8 CFR 274a.2 was read from the 2023 CFR edition on govinfo.gov instead. Verbatim: employee "Completes section 1 ... on the Form I-9 at the time of hire"; employer must "Complete section 2 ... on the Form I-9 within three business days of the hire"; retention "three years after the date of the hire or one year after the date the individual's employment is terminated, whichever is later." Because this is the 2023 CFR edition rather than the live eCFR, subsection lettering may have shifted, though the substantive rules are long-standing. Civil penalty amounts are inflation-adjusted annually and were not verified, so none are stated.

### Form 5500, Annual Return/Report of Employee Benefit Plan `federal-form-5500-benefit-plan`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: information-report
If you sponsor a 401(k) or certain other benefit plans, the plan itself files an annual return with the Department of Labor. This is separate from your company tax return and has its own deadline seven months after the plan year ends. Even a solo 401(k) has to start filing once its assets cross $250,000.
- **Deadline**: Due the last day of the seventh month after the plan year ends, which is July 31 for a calendar year plan. Form 5558 filed on or before the normal due date obtains an automatic extension.
- **Rule out first**:
  - The company sponsors no retirement or ERISA welfare plan at all, so nothing is due. (common) Check: Confirm no plan document exists and no deferrals appear in payroll.
  - The plan is a one-participant solo 401(k) with under $250,000 in assets, which is exempt from filing until it crosses that threshold. (common) Check: Check the plan's year-end asset value against $250,000.
  - The recordkeeper or third party administrator filed on the sponsor's behalf, so the sponsor holds no copy. (common) Check: Search the EFAST2 public database by sponsor name, which will show the filing regardless of who submitted it.
  - Benefits are provided through a PEO's plan rather than a company-sponsored plan, so the PEO files. (occasional) Check: Read the PEO agreement to determine who the plan sponsor of record is.
  - The plan year is not the calendar year, so a filing that appears late against July 31 is actually timely. (occasional) Check: Read the plan year end from the plan document and recompute the seventh-month deadline.
- **If it genuinely was missed**: DOL and IRS penalties apply for late or missing filings and can be substantial per day. Specific amounts were not verified in this pass and are deliberately not stated. The DOL Delinquent Filer Voluntary Compliance Program offers materially reduced penalties for voluntary correction.
- **How to prove it**:
  - [tier 1, settles it] Search the DOL EFAST2 public filing database by plan sponsor name or EIN and confirm a filing exists for each plan year. https://www.efast.dol.gov/portal/app/disseminatePublic
  - [tier 2, settles it] Sign in to EFAST2 and retrieve the filing acknowledgment ID for each submitted Form 5500. https://www.efast.dol.gov/
  - [tier 3, corroborating only] Request the signed Form 5500 and the audit report, if required, from the third party administrator or recordkeeper (Guideline, Human Interest, Fidelity).
  - [tier 4, settles it] Review the plan document and adoption agreement to establish the plan year end and the first year a filing was required.
  - [tier 5, corroborating only] Look for 401(k) deferral remittances in the payroll register and bank feed, which indicate an active plan exists.
- **Fix**:
  1. Identify the plan year end and every year a filing was required.
  2. Use the DOL Delinquent Filer Voluntary Compliance Program to file late returns at sharply reduced penalties; this is far cheaper than waiting to be caught.
  3. Engage the recordkeeper or a TPA to prepare the delinquent filings and the audit if the plan has 100 or more participants.
  4. Confirm deferrals were remitted within the DOL timing rules, since late deposits are a separate prohibited transaction requiring correction on Form 5330.
- **Source**: https://www.irs.gov/retirement-plans/form-5500-corner (verified 2026-08-14)
- **Note**: dol.gov/agencies/ebsa returned HTTP 403, so this was verified on irs.gov. Verbatim: due "the last day of the seventh month after the plan year ends (July 31 for a calendar year plan)." Solo 401(k) threshold verbatim from https://www.irs.gov/retirement-plans/one-participant-401k-plans: "A one-participant 401(k) plan is generally required to file an annual report on Form 5500-EZ if it has $250,000 or more in assets at the end of the year." EXTENSION LENGTH DELETED 2026-08-14. An earlier version of this note carried a specific Form 5558 extension length sourced from a search summary rather than a primary page. https://www.irs.gov/forms-pubs/about-form-5558 was fetched on 2026-08-14 and states only that the form applies for "a one-time extension of time to file" Forms 5500, 5500-SF, 5500-EZ and 8955-SSA. It does not state a duration or an extended date. Rather than leave an unverified number in place, the length is now omitted entirely; read it off the current Form 5558 instructions before quoting one.

### EEO-1 Component 1 report (EEOC) `federal-eeo1-component1`
**NOT FULLY VERIFIED.** The obligation is real; its fee, deadline and penalty could not be confirmed at the source and are withheld. Confirm at the source link.
Applies to: c-corp, s-corp, llc, partnership, benefit-corp, nonprofit | category: information-report
Employers above a headcount threshold file an annual demographic snapshot of their workforce with the Equal Employment Opportunity Commission, broken down by job category, race, ethnicity and sex. It is not a tax filing and has nothing to do with the IRS. The collection window opens and closes on dates the EEOC announces each year.
- **Deadline**: Annual data collection. The EEOC announces the opening and closing dates of each collection cycle; no fixed statutory date is published on the EEOC pages reviewed. Check eeoc.gov for the current cycle's deadline.
- **Rule out first**:
  - The company has fewer than 100 employees and is not a covered federal contractor, so no report is due. This covers the large majority of startups. (common) Check: Pull the headcount for the snapshot period and confirm no covered federal contracts exist.
  - The EEOC collection for the year has not opened yet, so the absence of a filing is expected. (occasional) Check: Check the current collection status on eeoc.gov.
  - Headcount crossed 100 only recently and the first covered snapshot period has not yet occurred. (occasional) Check: Compare the headcount history to the workforce snapshot period definition for the collection year.
  - The employees are engaged through a PEO that files under its own arrangement. (occasional) Check: Read the PEO agreement and confirm which entity is the employer of record for EEO-1 purposes.
- **How to prove it**:
  - [tier 2, settles it] Sign in to the EEOC Component 1 Online Filing System and confirm a certified filing exists for each collection year. https://eeocdata.org/eeo1
  - [tier 3, corroborating only] Check the HRIS for the EEO job category and demographic fields needed to build the report.
  - [tier 4, settles it] Retrieve the certified EEO-1 report and its confirmation for each year filed.
  - [tier 4, settles it] Pull a headcount snapshot from the payroll system for the applicable workforce snapshot period and compare to the 100 or 50 employee thresholds.
- **Fix**:
  1. Confirm coverage by measuring headcount during the workforce snapshot period and checking for covered federal contracts.
  2. Register in the EEOC Component 1 Online Filing System, which requires a company identification number the EEOC issues.
  3. Build the demographic data collection into onboarding, using voluntary self-identification, before the next collection opens.
  4. File as soon as the collection is open and contact the EEOC Filer Support Team about any prior-year gaps.
- **Source**: https://www.eeoc.gov/data/eeo-data-collections (verified 2026-08-14)
- **Note**: Marked needs-review because the deadline could not be verified, and it stays needs-review after a re-fetch on 2026-08-14. Neither EEOC page fetched states a filing deadline; the collection opens and closes on dates announced annually. As of 2026-08-14 the EEOC data collections page states verbatim "The 2024 EEO-1 Component 1 Data Collection is CLOSED" and "Updates regarding the 2025 EEO-1 Component 1 data collection will be posted to this page as they become available", so no open cycle and no deadline for 2025 data is published. The coverage threshold IS verified verbatim: "all private sector employers with 100 or more employees, and federal contractors with 50 or more employees meeting certain criteria" and, from https://www.eeoc.gov/employers/small-business/legal-requirements, "Employers who have at least 100 employees and federal contractors who have at least 50 employees are required to complete and submit an EEO-1 Report." The commonly cited $50,000 federal contract dollar threshold is NOT stated on any EEOC page fetched and is deliberately omitted; verify against 41 CFR 60-1.7 before asserting it.

### Form 990 series annual return for exempt organizations `federal-form-990-series-nonprofit-annual-return`
Applies to: nonprofit | category: tax
A tax-exempt organization still files an annual return; exemption from tax is not exemption from filing. Which version you file depends on your size, from a short electronic postcard for the smallest organizations up to the full Form 990. Miss three years in a row and the IRS revokes your exempt status automatically, with no hearing and no discretion.
- **Deadline**: Due the 15th day of the 5th month after the close of the organization's accounting period, which is May 15 for a calendar year organization. Form 8868 gives an automatic 6 month extension, to November 15 for a calendar year filer. For the 2025 tax year the original date was Friday May 15 2026 and the extended date is Monday November 16 2026, because November 15 2026 falls on a Sunday.
- **Rule out first**:
  - The organization filed Form 990-N, which is a brief electronic notice that displays differently in Tax Exempt Organization Search than a full return and can look like nothing was filed. (common) Check: Search the 990-N filing database within Tax Exempt Organization Search specifically.
  - The organization is a church or an integrated auxiliary of a church, which is not required to file an annual return at all. (occasional) Check: Confirm the organization's classification and the church exception in the Form 990 instructions.
  - The organization is on extension via Form 8868 and the extended date has not passed. For tax year 2025 that date is November 16 2026, not November 15, because November 15 2026 is a Sunday. (common) Check: Check for an accepted Form 8868 for the year.
  - The fiscal year is not the calendar year, so a return that looks late against May 15 is actually timely. (occasional) Check: Read the accounting period end from the determination letter or the prior return and recompute the fifth-month deadline.
  - Returns lag in the public database, so a recent filing may not yet appear in Tax Exempt Organization Search. (common) Check: Check the e-file acceptance record rather than relying on the public database for the most recent year.
- **If it genuinely was missed**: The IRS states $20 a day for each day the return is late, capped at the lesser of $10,500 or 5 percent of the organization's gross receipts for the year, and $10 a day against responsible individuals capped at $5,000. A higher daily rate applies to large organizations, but the IRS page's most recent worked example is for the 2022 tax year (gross receipts over $1,094,500, $105 a day, maximum $54,500) and these amounts are inflation adjusted annually, so no current-year large-organization figure is asserted here.
- **How to prove it**:
  - [tier 1, settles it] Search IRS Tax Exempt Organization Search by EIN and review the filed Form 990 series returns and the current exempt status. https://apps.irs.gov/app/eos/
  - [tier 1, settles it] Check the IRS Automatic Revocation of Exemption List for the organization's EIN. https://www.irs.gov/charities-non-profits/automatic-revocation-of-exemption
  - [tier 2, settles it] Order the exempt organization account transcript for the EIN to see filings and any assessed penalties. https://www.irs.gov/individuals/get-transcript
  - [tier 4, corroborating only] Obtain the signed Form 990 series return and its e-file acceptance for each year.
  - [tier 5, corroborating only] Compare gross receipts and total assets in the accounting records to the 990-N, 990-EZ and 990 thresholds to confirm the correct form was used.
- **Fix**:
  1. Check the Automatic Revocation List first, because whether exemption is still alive changes everything that follows.
  2. If not revoked, file all delinquent returns immediately, since the third consecutive missed year triggers automatic revocation with no discretion.
  3. If revoked, apply for reinstatement on Form 1023 or 1024 and seek retroactive reinstatement under the applicable Revenue Procedure, which has its own strict timing.
  4. Notify donors and grantors if exemption lapsed, since their deductions and grant eligibility are affected.
  5. Confirm state charitable registration status as well, which usually depends on the federal filing.
- **Source**: https://www.irs.gov/charities-non-profits/annual-exempt-organization-return-due-date (verified 2026-08-14)
- **Note**: Due date verbatim: "Form 990, 990-EZ, or 990-PF must be filed by the 15th day of the 5th month after the end of your organization's accounting period." Form thresholds verbatim from https://www.irs.gov/charities-non-profits/form-990-series-which-forms-do-exempt-organizations-file-filing-phase-in. Automatic revocation verbatim from https://www.irs.gov/charities-non-profits/automatic-revocation-of-exemption: "Organizations that do not file for three consecutive years automatically lose their tax-exempt status" under section 6033(j), and "An automatic revocation is effective on the original filing due date of the third annual return or notice." Form 8868 extension verbatim from https://www.irs.gov/forms-pubs/about-form-8868: "automatic 6-month extension of time to file its return." DATE CORRECTED 2026-08-14: an earlier version gave the tax year 2025 extended date as November 15 2026. That is a Sunday, so the date is Monday November 16 2026. PENALTY CAVEAT: re-verified 2026-08-14 at https://www.irs.gov/charities-non-profits/annual-exempt-organization-return-penalties-for-failure-to-file. The small-organization figures ($20 a day, lesser of $10,500 or 5 percent of gross receipts, $10 a day against responsible persons capped at $5,000) are stated on that page without a year. The large-organization figures on it are worked examples for the 2021 and 2022 TAX YEARS (not, as this note previously said, returns required to be filed in 2022): 2021, gross receipts over $1,084,000, $105 a day, maximum $54,000; 2022, gross receipts over $1,094,500, $105 a day, maximum $54,500. Those thresholds and caps are inflation adjusted annually, so do not quote a large-organization daily rate or cap as a current-year amount without re-verifying.

### Form 990-T, Exempt Organization Business Income Tax Return `federal-form-990t-ubit`
Applies to: nonprofit | category: tax
A nonprofit that runs a business unrelated to its exempt purpose pays regular corporate income tax on that activity. Advertising revenue, unrelated merchandise sales and certain sponsorship income are common triggers. It is a separate return from the Form 990 and it comes with an actual tax bill.
- **Deadline**: Due the 15th day of the 5th month after the end of the tax year for most exempt organizations, so May 15 for a calendar year. Trusts described in section 401(a), IRAs, SEPs, SIMPLEs, Roth IRAs, Coverdell ESAs and Archer MSAs file by the 15th day of the 4th month instead.
- **Rule out first**:
  - Gross unrelated business income is under $1,000 for the year, so no Form 990-T is required. (common) Check: Total the gross unrelated business income before expenses and compare to $1,000.
  - The revenue qualifies as a qualified sponsorship payment, or falls within the royalty, passive rent or volunteer labor exclusions, so it is not unrelated business income at all. (common) Check: Test the revenue against the statutory modifications and exclusions in the Form 990-T instructions.
  - The activity is substantially related to the exempt purpose, so no unrelated business income arises despite looking commercial. (common) Check: Document how the activity furthers the exempt purpose.
  - The activity generated a loss, so no tax is due even though a return may still be required. (occasional) Check: Confirm gross income exceeded $1,000, since the filing test is on gross income and not net.
- **If it genuinely was missed**: Standard late filing and late payment penalties apply. Specific amounts are not stated on the source page and are not asserted here.
- **How to prove it**:
  - [tier 1, corroborating only] Review the organization's public Form 990, Part VIII revenue detail, for revenue coded as unrelated business income, then check whether a 990-T was filed. https://apps.irs.gov/app/eos/
  - [tier 2, settles it] Order the exempt organization account transcript for the EIN and confirm whether a Form 990-T posted for each year with unrelated business income. https://www.irs.gov/individuals/get-transcript
  - [tier 4, settles it] Obtain the filed Form 990-T with its e-file acceptance, and the workpapers allocating expenses between related and unrelated activities.
  - [tier 5, corroborating only] Review the revenue accounts for advertising, sponsorship, merchandise and rental income streams that may be unrelated business income.
- **Fix**:
  1. Identify every revenue stream that may be unrelated business income and test each against the exclusions.
  2. File delinquent Forms 990-T and pay the tax and interest.
  3. Allocate expenses between related and unrelated activities on a defensible basis and document the methodology.
  4. Assess whether the unrelated activity is large enough to threaten exempt status, which is a separate and more serious question than the tax.
- **Source**: https://www.irs.gov/instructions/i990t (verified 2026-08-14)
- **Note**: Verbatim: filing is required "if it has gross income of $1,000 or more from a regularly conducted unrelated trade or business" and "All other organizations must file Form 990-T by the 15th day of the 5th month after the end of their tax years." Note the filing test is gross income, not net profit, so a loss-making unrelated activity can still require a return.

### Form 1023 or 1023-EZ, Application for Recognition of Exemption under 501(c)(3) `federal-form-1023-exemption-application`
Applies to: nonprofit | category: entity
Incorporating as a nonprofit in your state does not make you tax exempt or make donations deductible. You have to apply to the IRS and be recognized. There is a 27 month window from formation, and if you file inside it your exemption is backdated to the day you were formed, which matters for every donation received in the meantime.
- **Deadline**: File within 27 months after the end of the month in which the organization was legally formed to have exempt status effective from the date of formation. File later and the effective date is generally the date the application was filed.
- **Cost**: $600 user fee for Form 1023; $275 user fee for Form 1023-EZ. Paid through Pay.gov when the application is filed.
- **Rule out first**:
  - The application is pending; IRS processing routinely takes many months, and the organization may operate and solicit while it waits. (common) Check: Check the Pay.gov receipt and the IRS acknowledgment of the submitted application.
  - The organization is a church, which is automatically treated as exempt and is not required to apply. (occasional) Check: Confirm the organization meets the IRS church characteristics.
  - The organization is exempt under a different subsection, such as 501(c)(4) or 501(c)(6), which uses Form 1024 rather than Form 1023. (occasional) Check: Read the determination letter for the subsection cited.
  - The organization operates under a fiscal sponsor's exemption and has deliberately not sought its own. (occasional) Check: Look for a fiscal sponsorship agreement naming the sponsoring 501(c)(3).
  - The determination letter exists but predates the searchable database records, or the organization is listed under a former name. (occasional) Check: Search Tax Exempt Organization Search by EIN rather than by name.
- **How to prove it**:
  - [tier 1, settles it] Search IRS Tax Exempt Organization Search by EIN or name and confirm the organization appears as recognized, with its determination letter available. https://apps.irs.gov/app/eos/
  - [tier 1, corroborating only] Check the state Secretary of State registry for the exact legal formation date, which starts the 27 month clock.
  - [tier 4, settles it] Obtain the IRS determination letter and read the effective date of exemption stated on it.
  - [tier 4, settles it] Retrieve the Pay.gov payment confirmation and the submitted Form 1023 or 1023-EZ, and compare the submission date to the 27 month window from formation.
- **Fix**:
  1. Establish the exact legal formation date and compute the 27 month deadline before choosing a strategy.
  2. File Form 1023 or 1023-EZ with the Pay.gov user fee; check the 1023-EZ eligibility worksheet carefully, since many organizations are not eligible for the short form.
  3. If the 27 month window has closed, request retroactive recognition on Schedule E of Form 1023 with a reasonable cause explanation.
  4. Tell donors the status honestly in the interim, since deductibility depends on recognition being granted.
  5. File the required Form 990 series returns for the interim years, because the filing obligation and the three-year revocation clock run regardless.
- **Source**: https://www.irs.gov/charities-non-profits/application-for-recognition-of-exemption (verified 2026-08-14)
- **Note**: 27 month rule verbatim: "Generally, if you file Form 1023 within 27 months after the end of the month in which you were legally formed, and we approve your application, the effective date of your exempt status will be your legal date of formation." User fees verbatim from https://www.irs.gov/charities-non-profits/form-1023-and-1023-ez-amount-of-user-fee: "The user fee for Form 1023 is $600", "The user fee for Form 1023-EZ is $275", and "The user fees must be paid through Pay.gov when the application is filed." FEE CAVEAT, tightened 2026-08-14: the fee page was re-fetched and it states the $600 and $275 amounts and that they are "subject to change", but it cites no revenue procedure and carries no effective date. An earlier version of this note attributed the fees to Appendix A of Revenue Procedure 2026-4 or 2026-5; that attribution was not on the page fetched and has been removed rather than asserted. The dollar amounts stand on the IRS fee page itself; re-verify before quoting them to a client.


## DE (2)

### Delaware annual report and franchise tax `de-annual-report-franchise-tax`
Applies to: c-corp, s-corp, benefit-corp | category: entity
Every Delaware corporation files an annual report and pays franchise tax by March 1, whether or not it earned anything. The tax is the price of having the entity, not a tax on income, so a pre-revenue company still owes it.
- **Deadline**: March 1 each year, for the prior calendar year.
- **Cost**: $50 annual report fee for a non-exempt domestic corporation, plus franchise tax. The minimum franchise tax is $175 under the authorized shares method or $400 under the assumed par value capital method.
- **Rule out first**:
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

### Delaware registered agent `de-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
A Delaware entity must continuously maintain a registered agent with a physical Delaware address to receive legal process and state notices. Losing the agent is how companies quietly fall out of good standing without ever hearing about it.
- **Deadline**: Continuous. There is no filing date, the agent simply has to exist at all times.
- **Cost**: Typically $50 to $300 per year depending on the provider. This is a private market price, not a state fee, so treat it as an estimate rather than a published figure.
- **Rule out first**:
  - The first year of registered agent service was included in the incorporation package. Stripe Atlas and Clerky both bundle year one, and Firstbase bundles it into its formation product. A first-year company having no separate agent fee anywhere is completely normal. (common) Check: Ask which platform the company was incorporated through.
  - The agent was prepaid for several years, so most years show no charge at all. (occasional) Check: Look for a single larger payment at formation rather than an annual one.
  - The founder pays the agent personally. (occasional) Check: Ask, or check the agent's portal.
  - You searched Delaware and saw only a results list. The agent is on the entity detail page, one click further in, not in the list. (common) Check: Open the entity detail page rather than reading the search results. The agent name and address are there for free.
- **How to prove it**:
  - [tier 1, settles it] Search the entity name in Delaware's free entity search, then open the entity DETAIL page. The detail page shows the registered agent name and address, the file number and the incorporation date at no cost. The results list alone does not, so you have to click through. This settles who the agent is in about a minute. It does not tell you whether the entity is in good standing, which is a paid lookup. https://icis.corp.delaware.gov/ecorp/entitysearch/NameSearch.aspx
  - [tier 3, settles it] Check the formation platform or agent account: Stripe Atlas, Clerky, Firstbase, CSC, CT Corporation, Harvard Business Services, Registered Agents Inc or Northwest. This is the fastest reliable answer.
  - [tier 5, corroborating only] Look for an annual charge from a registered agent provider. Corroboration only, and unreliable for the reasons below.
- **Fix**:
  1. Look the agent up free on the Delaware entity detail page. The state publishes the agent name, address, phone and residency at no charge; only status and good standing are paid.
  2. If there genuinely is no agent, appoint one immediately. Delaware can void the charter for failure to maintain an agent, and it is inexpensive to fix.
  3. Confirm the agent has a current contact address for you, since this is where lawsuits and state notices land.
- **Source**: https://delcode.delaware.gov/title8/c001/sc02/index.html (verified 2026-08-13)
- **Note**: The single most common source of false positives in compliance tooling. A missing fee proves nothing. Never report this as a gap on the strength of a bank feed. Requirement is 8 Del. C. sections 131 to 136; forfeiture of the charter for failure to maintain an agent is section 136.


## NY (5)

### New York Application for Authority (foreign qualification) `ny-foreign-qualification`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp | category: entity
A company formed in another state that is transacting business in New York has to register with the New York Department of State before doing so. Until it does, it cannot bring a lawsuit in New York courts, and it can be liable for back fees and taxes for the whole unregistered period.
- **Deadline**: Before transacting business in New York.
- **Cost**: $225 statutory filing fee, plus a Certificate of Existence from the state of formation dated within the last year.
- **Rule out first**:
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

### New York biennial statement `ny-biennial-statement`
Applies to: c-corp, s-corp, llc, llc-single-member, benefit-corp | category: entity
Every domestic and foreign business corporation and LLC registered in New York files a short statement every two years. A corporation reports its chief executive officer name and business address, its principal executive office, the address for service of process, and the number of directors and how many are women. An LLC reports only the address for service of process, with no officer information.
- **Deadline**: Every two years, during the calendar month in which the company originally filed or qualified. New York only accepts the filing during that month.
- **Cost**: $9.
- **Rule out first**:
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

### New York general business corporation franchise tax (Form CT-3) `ny-ct3`
Applies to: c-corp, benefit-corp | category: tax
A corporation doing business in New York files a franchise tax return and owes at least a fixed dollar minimum tax, which is based on New York receipts rather than on profit. A loss-making company still owes the minimum.
- **Deadline**: Three and a half months after year end, so April 15 for a calendar year filer. Form CT-5 gives six months, to roughly October 15, and an Article 9-A taxpayer holding a valid six-month extension may then request up to two further three-month extensions, so the real outer limit is twelve months. A federal Form 7004 does nothing for New York: the state extension is a separate filing and founders conflate the two constantly.
- **Cost**: A fixed dollar minimum applies even at a loss. The amount depends on the New York receipts bracket, so check the current table on the linked page rather than assuming a figure.
- **Rule out first**:
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

### New York sales tax registration `ny-sales-tax-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp | category: sales-tax
A company selling taxable products or services to New York customers must register as a sales tax vendor before making taxable sales. New York treats software as a service as prewritten software, which means SaaS is taxable here even though many states exempt it.
- **Deadline**: Before making taxable sales if there is physical presence. Within 30 days of crossing the economic nexus thresholds for a remote seller.
- **Rule out first**:
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

### New York withholding and unemployment insurance registration `ny-payroll-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
An employer with an employee working in New York registers for state income tax withholding and unemployment insurance. Who has to do this depends entirely on who the legal employer is.
- **Deadline**: Liability attaches as of the first day of the calendar quarter in which the employer pays $300 or more in remuneration ($500 for household employers), not simply before the first payroll. Separately, new hires must be reported within 20 days of the hiring date.
- **Rule out first**:
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


## CA (18)

### California Statement of Information (stock corporation) `ca-statement-of-information-stock-corp`
Applies to: c-corp, s-corp, benefit-corp | category: entity
Every California stock corporation, and every out-of-state corporation registered to do business here, files a Statement of Information with the Secretary of State listing its officers, directors, addresses and agent for service of process. The first one is due within 90 days of registration, then every year inside a six month window that ends in your anniversary month. If you skip it the Franchise Tax Board bills a $250 penalty on the Secretary of State's behalf and the entity can be suspended.
- **Deadline**: The initial statement is due within 90 days of initial registration. After that it is annual: the Secretary of State publishes a six month filing window keyed to the month of incorporation or registration, and the statement must be filed inside that window each year.
- **Cost**: $25.00, the same for a domestic and a foreign stock corporation ($20.00 filing fee plus a $5.00 disclosure fee).
- **Rule out first**:
  - A registered agent or formation service filed the statement and paid the $25 from its own account, so nothing appears in the company's bank feed. (common) Check: Read the Statement of Info Due Date and Standing - SOS fields on bizfile Online, which reflect the filing no matter who paid it.
  - The corporation was formed or registered recently and its first filing window has not closed yet. (common) Check: Compare the Initial Filing Date shown on bizfile Online against the displayed Statement of Info Due Date.
  - The statement was filed on paper or by mail and the online record lags by a few business days. (occasional) Check: Re-check bizfile Online after the Secretary of State's published processing time, or check the entity's bizfile account.
- **If it genuinely was missed**: $250 penalty imposed by the Secretary of State and collected by the Franchise Tax Board. Failure to file may also result in suspension or forfeiture of the entity.
- **How to prove it**:
  - [tier 1, settles it] Search the entity on bizfile Online Business Search, expand the result row, and read the 'Statement of Info Due Date' and 'Standing - SOS' fields in the detail drawer. https://bizfileonline.sos.ca.gov/search/business
  - [tier 1, settles it] Open the free PDF image of the most recently filed Statement of Information from the same detail drawer and check the filing date. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, settles it] Log in to the entity's bizfile Online account and review its filing history. https://bizfileonline.sos.ca.gov/
  - [tier 5, corroborating only] Look for a $25.00 payment to 'CA Secretary of State' in the bank or card feed around the anniversary month.
- **Fix**:
  1. Look up the entity on bizfile Online and read the Statement of Info Due Date and Standing - SOS fields.
  2. File the Statement of Information through bizfile Online and pay the $25.00 fee.
  3. If the Franchise Tax Board already assessed the $250 penalty, submit an Email Penalty Waiver Request to the Secretary of State.
- **Source**: https://www.sos.ca.gov/business-programs/business-entities/statements (verified 2026-08-14)
- **Note**: Filing window and the suspension/forfeiture consequence come from the cited Secretary of State page. Fee, cadence and the 90 day initial deadline come from the Secretary of State's live forms page, https://www.sos.ca.gov/business-programs/business-entities/forms/corporations-statement-information, fetched 2026-08-14: 'Statement of Information - Domestic and Foreign Stock: Due within 90 days of initial registration and every year thereafter. Online Only $25.00'. Corrected 2026-08-14: an earlier version named paper Forms SI-200 and SI-350 off the 2018 Business Entities Fee Schedule (https://bpd.cdn.sos.ca.gov/pdf/be-fee-schedule-062018.pdf). Those form numbers are no longer what the agency administers; the corporation Statement of Information is filed online only, and the $25.00 covers domestic and foreign stock corporations alike. The $250 penalty amount comes from https://www.ftb.ca.gov/file/business/types/corporations/index.html.

### California Statement of Information (LLC) `ca-statement-of-information-llc`
Applies to: llc, llc-single-member | category: entity
California LLCs, including single member LLCs, file a Statement of Information with the Secretary of State. The first one is due within 90 days of registration. After that, unlike corporations, the LLC version is due every two years rather than every year. Skipping it triggers a $250 penalty collected by the Franchise Tax Board and can get the LLC suspended.
- **Deadline**: The initial statement is due within 90 days of initial registration, then every two years. The Secretary of State publishes a six month filing window keyed to the month of organization or registration; the statement must be filed inside that window every second year.
- **Cost**: $20.00, domestic or foreign.
- **Rule out first**:
  - It is an off year. The LLC statement is biennial, so a gap of roughly two years between filings is correct, not a miss. (common) Check: Read the Statement of Info Due Date on bizfile Online rather than counting years since the last filing.
  - A registered agent service filed and paid it, so there is no charge in the company's own accounts. (common) Check: Check Standing - SOS and the filed Statement of Information image on bizfile Online.
  - The LLC was organized recently and the first window is still open. (common) Check: Compare Initial Filing Date to the displayed due date on bizfile Online.
- **If it genuinely was missed**: $250 penalty imposed by the Secretary of State and collected by the Franchise Tax Board. Failure to file may also result in suspension or forfeiture.
- **How to prove it**:
  - [tier 1, settles it] Search the LLC on bizfile Online Business Search, expand the row, and read 'Statement of Info Due Date' and 'Standing - SOS'. https://bizfileonline.sos.ca.gov/search/business
  - [tier 1, settles it] Download the free PDF of the last filed Statement of Information from the entity detail drawer. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, settles it] Log in to the LLC's bizfile Online account and review filing history. https://bizfileonline.sos.ca.gov/
  - [tier 5, corroborating only] Look for a $20.00 payment to 'CA Secretary of State'.
- **Fix**:
  1. Check the LLC's Statement of Info Due Date on bizfile Online.
  2. File the Statement of Information through bizfile Online and pay $20.00.
  3. Request an Email Penalty Waiver from the Secretary of State if the $250 penalty was assessed.
- **Source**: https://www.sos.ca.gov/business-programs/business-entities/statements (verified 2026-08-14)
- **Note**: Cadence, the 90 day initial deadline and the $20.00 fee come from the Secretary of State's live forms page, https://www.sos.ca.gov/business-programs/business-entities/forms/limited-liability-companies-statement-information, fetched 2026-08-14: 'Statement of Information: Due within 90 days of initial registration and every two years thereafter. Online Only $20.00'. Corrected 2026-08-14: an earlier version named paper Forms LLC-12 and LLC-12NC off the 2018 Business Entities Fee Schedule (https://bpd.cdn.sos.ca.gov/pdf/be-fee-schedule-062018.pdf). Those are no longer the filing route the agency administers; the LLC statement is filed online only. The $250 penalty comes from https://www.ftb.ca.gov/file/business/types/limited-liability-company/index.html.

### California Statement of Information (nonprofit corporation) `ca-statement-of-information-nonprofit`
Applies to: nonprofit | category: entity
California nonprofit corporations file a Statement of Information with the Secretary of State within 90 days of registering and every two years after that. It lists the officers, the principal address and the agent for service of process. It is separate from, and in addition to, registering with the Attorney General's charity registry.
- **Deadline**: The initial statement is due within 90 days of initial registration, then every two years, inside the Secretary of State's published six month filing window keyed to the month of incorporation.
- **Cost**: $20.00.
- **Rule out first**:
  - It is an off year in the two year cycle. (common) Check: Read the Statement of Info Due Date on bizfile Online instead of assuming an annual cadence.
  - A board member or the organization's counsel filed it personally. (occasional) Check: Check the filed Statement of Information image on bizfile Online.
  - The nonprofit is an unincorporated association or a trust, so it never had a Secretary of State corporate record to begin with. (occasional) Check: Confirm the legal form; only corporations appear in bizfile Online. Unincorporated charities still register with the Attorney General.
- **If it genuinely was missed**: $250 penalty imposed by the Secretary of State and collected by the Franchise Tax Board. Failure to file may also result in suspension or forfeiture.
- **How to prove it**:
  - [tier 1, settles it] Search the nonprofit on bizfile Online Business Search and read 'Statement of Info Due Date' and 'Standing - SOS' in the expanded row. https://bizfileonline.sos.ca.gov/search/business
  - [tier 1, settles it] Open the free PDF of the last filed Statement of Information from the entity detail drawer. https://bizfileonline.sos.ca.gov/search/business
  - [tier 5, corroborating only] Look for a $20.00 payment to 'CA Secretary of State'.
- **Fix**:
  1. Look up the entity on bizfile Online and read the Statement of Info Due Date.
  2. File the Statement of Information through bizfile Online and pay $20.00.
  3. Separately confirm the Attorney General charity registration is current.
- **Source**: https://www.sos.ca.gov/business-programs/business-entities/statements (verified 2026-08-14)
- **Note**: Cadence, the 90 day initial deadline and the $20.00 fee come from the Secretary of State's live forms page, https://www.sos.ca.gov/business-programs/business-entities/forms/corporations-statement-information, fetched 2026-08-14: 'Statement of Information - Nonprofit: Due within 90 days of initial registration and every two years thereafter. Online Only $20.00'. Corrected 2026-08-14: an earlier version named paper Form SI-100 off the 2018 Business Entities Fee Schedule. The nonprofit statement is now filed online only.

### California $800 minimum franchise tax (corporations) `ca-minimum-franchise-tax`
Applies to: c-corp, s-corp, benefit-corp | category: tax
Every corporation incorporated, registered or doing business in California owes an $800 minimum franchise tax each year. You owe it whether the company made money, lost money or did nothing at all. Newly incorporated or newly qualified corporations are exempt for their first taxable year.
- **Deadline**: The minimum franchise tax is due in the first quarter of each accounting period.
- **Cost**: $800 per taxable year (minimum). Actual tax is the greater of the minimum or the tax computed on net income.
- **Rule out first**:
  - It is the corporation's first taxable year, which is exempt from the minimum franchise tax for corporations newly incorporated or qualified on or after January 1, 2020. (common) Check: Compare the Initial Filing Date on bizfile Online with the taxable year in question.
  - The corporation's income tax exceeded $800, so the payment shows as a larger tax amount rather than a separate $800 line. (common) Check: Read the tax line on the filed Form 100 or 100S.
  - The payment was made from a parent entity's account or by the founder personally and booked as a shareholder contribution. (occasional) Check: Check MyFTB for payments actually credited to the entity's account.
- **How to prove it**:
  - [tier 1, corroborating only] Check the 'Standing - FTB' field on bizfile Online; a value of 'Suspended - FTB' indicates an unresolved Franchise Tax Board problem. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, settles it] Log in to the Franchise Tax Board MyFTB business account and review the entity's balance and payment history. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Read the filed Form 100 or Form 100S and confirm the tax line is at least $800.
  - [tier 5, corroborating only] Look for an $800 payment to 'Franchise Tax Board' in the bank feed in the first quarter of the year.
- **Fix**:
  1. Open MyFTB and confirm which taxable years show an unpaid balance.
  2. Pay the $800 using Web Pay or the applicable voucher.
  3. If the entity shows 'Suspended - FTB' on bizfile Online, file all delinquent returns and pay balances, then request revivor from the Franchise Tax Board.
- **Source**: https://www.ftb.ca.gov/file/business/types/corporations/index.html (verified 2026-08-14)
- **Note**: Re-verified 2026-08-14. The cited FTB page states: 'Every corporation that is incorporated, registered, or doing business in California must pay the $800 minimum franchise tax' and 'On or after January 1, 2020, newly incorporated or qualified corporations are not required to pay the minimum franchise tax in their first taxable year.' The first year waiver is therefore still live for 2026, not a lapsed relief measure. The cited page does NOT state the payment date; the deadline stated here ('due the first quarter of each accounting period') is quoted from https://www.ftb.ca.gov/file/business/types/corporations/s-corporations.html, which was fetched the same day. The same FTB page adds a second waiver this row does not model: a corporation is also exempt from the minimum tax where it did no business in California during the tax year AND the tax year was 15 days or fewer.

### California S corporation return (Form 100S) and 1.5% tax `ca-scorp-franchise-return-100s`
Applies to: s-corp | category: tax
California does not fully respect the federal S election. An S corporation still pays California tax at 1.5% on its California source income, on top of the $800 minimum, and files Form 100S. The 1.5% applies even in the first year, when the $800 minimum is waived.
- **Deadline**: The return is due the 15th day of the 3rd month after the close of the taxable year. S corporations filing after the original due date get an automatic 6 month extension to file, which is not an extension to pay.
- **Rule out first**:
  - The company filed Form 100 rather than 100S because California had not yet recognized or the entity had not yet made the S election for that year. (occasional) Check: Check which return form was filed and whether the federal S election was in effect for that taxable year.
  - It is the first taxable year, so the $800 minimum was waived and only the 1.5% on net income appears. (common) Check: Confirm the entity's first taxable year against the Initial Filing Date on bizfile Online.
  - The return is on the automatic 6 month extension and simply is not filed yet. (common) Check: Compare today's date to the original due date plus 6 months, and check MyFTB for an extension payment.
- **How to prove it**:
  - [tier 1, corroborating only] Check 'Standing - FTB' on bizfile Online for a suspension signal. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, settles it] Check MyFTB for the entity's filed returns and balances. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Read the filed Form 100S for the year and confirm the 1.5% tax computation and the tax line.
  - [tier 5, corroborating only] Look for estimated tax payments to the Franchise Tax Board during the year.
- **Fix**:
  1. Confirm the correct return form (100S) for the year in MyFTB.
  2. File Form 100S and pay the greater of the 1.5% tax or the $800 minimum.
  3. Pay any balance by the original due date, because the extension covers filing only.
- **Source**: https://www.ftb.ca.gov/file/business/types/corporations/s-corporations.html (verified 2026-08-14)

### California C corporation franchise or income tax return (Form 100) `ca-ccorp-franchise-return-100`
Applies to: c-corp, benefit-corp | category: tax
A California C corporation, including a benefit corporation, files a corporate franchise or income tax return with the Franchise Tax Board each year and pays the greater of the tax on net income or the $800 minimum. Corporations that file after the original due date get an automatic 7 month extension to file, but not to pay.
- **Deadline**: The return is due the 15th day of the 4th month after the close of the taxable year. Corporations filing after the original due date are granted an automatic 7 month extension, which for tax year 2019 and later puts the extended due date at the 15th day of the 11th month after the close of the tax year. The extension is to file, not to pay.
- **Rule out first**:
  - The return is on the automatic 7 month extension and is not late. (common) Check: Check MyFTB for the extension and whether the estimated tax was paid by the original due date.
  - A benefit corporation is treated as an ordinary stock corporation for California tax, so there is no separate benefit corporation return to find. (common) Check: Confirm the entity type on bizfile Online and look for Form 100 rather than a special form.
  - The corporation is a member of a combined report and its income is reported on the parent's return. (occasional) Check: Ask for the combined report and confirm the entity appears on the affiliate schedule.
- **If it genuinely was missed**: Returns filed after the extended due date are treated as delinquent, with penalties computed from the original due date.
- **How to prove it**:
  - [tier 1, corroborating only] Check 'Standing - FTB' on bizfile Online. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, settles it] Check MyFTB for filed returns, extensions and balances. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Read the filed Form 100 for the year.
  - [tier 5, corroborating only] Look for Franchise Tax Board estimated payments and an extension payment (FTB 3539).
- **Fix**:
  1. Confirm the entity's taxable year end and the corresponding return due date with the Franchise Tax Board.
  2. File Form 100 and pay the greater of the computed tax or the $800 minimum.
  3. Use FTB 3539 to make an extension payment if the return will be late.
- **Source**: https://www.ftb.ca.gov/file/business/types/corporations/index.html (verified 2026-08-14)
- **Note**: The 7 month automatic extension, the delinquency rule and the $800 minimum are stated on the cited FTB page. Corrected 2026-08-14: the due date is no longer unstated. FTB's business due dates page is at https://www.ftb.ca.gov/file/when-to-file/due-dates-business.html (the path this row previously tried returned 404). Fetched 2026-08-14, it gives, for a C corporation, 'Return due date: 15th day of the 4th month after the close of your tax year' and 'Extended due date: Tax Year 2019 and later - 15th day of the 11th month after the close of the tax year.'

### California $800 LLC annual tax `ca-llc-annual-tax-800`
Applies to: llc, llc-single-member | category: tax
Every LLC doing business in or organized in California owes an $800 annual tax to the Franchise Tax Board. Single member LLCs owe it too, even though they are disregarded for federal income tax. You keep owing it every year until you formally cancel the LLC, whether or not the LLC trades.
- **Deadline**: Due by the 15th day of the 4th month of the taxable year. For a first year LLC it is due the 15th day of the 4th month from the date of registration with the Secretary of State. Paid with LLC Tax Voucher, FTB 3522.
- **Cost**: $800 per taxable year.
- **Rule out first**:
  - The LLC first registered between the 2021 and 2023 tax years and used the temporary first year exemption, so there is legitimately no $800 for that first year. (occasional) Check: Compare the Initial Filing Date on bizfile Online to the exemption window (tax years beginning on or after January 1, 2021 and before January 1, 2024).
  - The LLC cancelled under the short form cancellation within one year of organizing, which removes the first year $800. (rare) Check: Look for a filed Form LLC-4/8 on bizfile Online.
  - A parent company or the founder paid the $800 personally, so nothing hits the LLC's own bank feed. (common) Check: Check MyFTB for payments credited to the LLC's account.
- **How to prove it**:
  - [tier 1, corroborating only] Check 'Standing - FTB' on bizfile Online for a suspension signal. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, settles it] Check MyFTB for the LLC's account balance and $800 payments by year. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Read the filed Form 568 and confirm the annual tax line.
  - [tier 5, corroborating only] Look for an $800 payment to 'Franchise Tax Board' with an FTB 3522 reference.
- **Fix**:
  1. Open MyFTB and identify which taxable years show an unpaid annual tax.
  2. Pay the $800 via Web Pay or with FTB 3522 for each open year.
  3. If the LLC is inactive and will not be used again, file the cancellation with the Secretary of State so the $800 stops accruing.
- **Source**: https://www.ftb.ca.gov/file/business/types/limited-liability-company/index.html (verified 2026-08-14)

### California LLC fee on total California income `ca-llc-fee-tiered`
Applies to: llc, llc-single-member | category: tax
On top of the $800 annual tax, a California LLC pays a separate fee once its California income passes $250,000. The fee is a flat amount per income band, not a percentage, and it is based on gross California income rather than profit, so a loss making LLC can still owe it.
- **Deadline**: Estimate and pay the fee by the 15th day of the 6th month of the current tax year, using Estimated Fee for LLCs, FTB 3536.
- **Cost**: $900 if California income is $250,000 to $499,999. $2,500 if $500,000 to $999,999. $6,000 if $1,000,000 to $4,999,999. $11,790 if $5,000,000 or more. No fee below $250,000.
- **Rule out first**:
  - California income was under $250,000, so no fee is due at all. (common) Check: Check total California income on the filed Form 568 against the $250,000 floor.
  - The LLC has income inside and outside California and only the California apportioned share crosses the threshold. (common) Check: Review Schedule R and the California source income computation on the return.
  - The fee was paid with the return rather than as a separate 6th month estimate, so there is one combined payment instead of two. (occasional) Check: Check MyFTB payment history and the Form 568 fee line.
- **If it genuinely was missed**: Failure to pay the estimated LLC fee by the original return due date results in penalties and interest.
- **How to prove it**:
  - [tier 2, settles it] Check MyFTB for LLC fee payments and any estimated fee underpayment notices. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Read the filed Form 568 and confirm the LLC fee line against the total California income reported.
  - [tier 5, corroborating only] Look for a payment to the Franchise Tax Board matching one of the four band amounts, referenced to FTB 3536.
- **Fix**:
  1. Compute total California income for the year and map it to the correct band.
  2. Pay the estimated fee by the 15th day of the 6th month using FTB 3536.
  3. Reconcile the estimate against the actual fee on Form 568 and settle any difference by the original return due date.
- **Source**: https://www.ftb.ca.gov/file/business/types/limited-liability-company/index.html (verified 2026-08-14)

### California LLC Return of Income (Form 568) `ca-llc-return-568`
Applies to: llc, llc-single-member | category: tax
A California LLC files Form 568 with the Franchise Tax Board each year. This is the return that reports the $800 annual tax and the income based LLC fee. Single member LLCs file it too, even though the IRS disregards them.
- **Deadline**: Form 568 is due the 15th day of the 3rd month after the close of the tax year for an LLC classified as a partnership, and the 15th day of the 4th month after the close of the tax year for a single member LLC owned by an individual or a non pass through entity. If the LLC files on extension, use Payment for Automatic Extension for LLCs, FTB 3537.
- **Rule out first**:
  - The LLC is on extension and the return is not yet due. (common) Check: Check MyFTB for an extension payment on FTB 3537 and compare against the extended due date.
  - The LLC elected corporate taxation, so it files Form 100 or 100S rather than Form 568. (occasional) Check: Check the entity's federal classification election and which California form was filed.
  - The LLC is a foreign non registered LLC treated as a partnership with California source income, which files Form 565 instead. (rare) Check: Confirm registration status on bizfile Online and whether the LLC is doing business in California.
- **How to prove it**:
  - [tier 1, corroborating only] Check 'Standing - FTB' on bizfile Online; suspension often follows unfiled returns. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, settles it] Check MyFTB for the filing record and any non filer notices. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Obtain the filed Form 568 for the year, including the annual tax and fee lines.
- **Fix**:
  1. Confirm in MyFTB which years have no Form 568 on file.
  2. Prepare and file Form 568 for each open year, including the $800 annual tax and any LLC fee.
  3. If the LLC was suspended, clear all filings and balances and request revivor.
- **Source**: https://www.ftb.ca.gov/file/business/types/limited-liability-company/index.html (verified 2026-08-14)
- **Note**: Corrected 2026-08-14: the due date is no longer left as 'the original return due date' with no date behind it. FTB's business due dates page, https://www.ftb.ca.gov/file/when-to-file/due-dates-business.html, fetched 2026-08-14, gives 'LLC classified as a partnership: Return due date 15th day of the 3rd month after the close of your tax year' and 'Single member LLC (owned by an individual or a non-pass through entity): Return due date 15th day of the 4th month after the close of your tax year.'

### California Partnership Return of Income (Form 565) `ca-partnership-return-565`
Applies to: partnership | category: tax
A partnership with California source income files a California Partnership Return of Income, Form 565, with the Franchise Tax Board. The partnership itself is a pass through, so the tax lands on the partners, but the information return still has to be filed.
- **Deadline**: The return is due the 15th day of the 3rd month after the close of the tax year. The extended filing due date is the 15th day of the 10th month after the close of the tax year.
- **Rule out first**:
  - The entity is an LLC treated as a partnership, in which case it files Form 568 rather than Form 565. (common) Check: Check the legal form on bizfile Online and confirm which return was filed.
  - The partnership is on extension and the return is not yet due. (common) Check: Check MyFTB for the extension record.
  - The partnership has no California source income and no California activity, so no California return is required. (occasional) Check: Review the apportionment workpapers and the partners' California sourcing.
- **How to prove it**:
  - [tier 2, settles it] Check MyFTB for the partnership's filing record. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Obtain the filed Form 565 and the partner Schedule K-1s for the year.
- **Fix**:
  1. Confirm whether the entity files Form 565 (partnership) or Form 568 (LLC).
  2. Diary the 15th day of the 3rd month after year end, and the 15th day of the 10th month if the return goes on extension.
  3. File the return and issue California Schedule K-1s to partners.
- **Source**: https://www.ftb.ca.gov/file/when-to-file/due-dates-business.html (verified 2026-08-14)
- **Note**: Corrected 2026-08-14. The due date is no longer unstated and the source no longer points at the LLC page. FTB's business due dates page, fetched 2026-08-14, gives for a General Partnership: 'Return due date 15th day of the 3rd month after the close of your tax year', 'Extended filing due date 15th day of the 10th month after the close of your tax year', 'Annual tax: You're not required to pay an annual tax' and 'Annual fee: You're not required to pay the annual fee', with Form 565 named. Note the scope limit the same page exposes: a general partnership owes no $800 annual tax, but a limited partnership, LLP or LLLP filing Form 565 does owe $800, due the 15th day of the 3rd month after the close of the tax year. The general partnership filing threshold is still not asserted here; no fetched FTB page states one.

### California agent for service of process `ca-agent-for-service-of-process`
Applies to: c-corp, s-corp, llc, llc-single-member, benefit-corp, nonprofit | category: registered-agent
California requires corporations, LLCs, limited partnerships and limited liability partnerships to name an agent for service of process, which is the person or company that legally accepts lawsuits on your behalf. The agent's name and address are public. General partnerships are not on the list of entities required by statute to designate one.
- **Deadline**: Designated at formation or registration and kept current thereafter. A change is reported on the Statement of Information or by a separate change filing.
- **Cost**: No separate fee when the agent is designated or changed on a Statement of Information filed within the normal filing period.
- **Rule out first**:
  - An officer or the founder serves as the agent personally, so there is no vendor invoice or subscription to find. (common) Check: Read the agent name on bizfile Online; an individual name rather than a corporate agent is normal and compliant.
  - The agent is a registered corporate agent filed under California Corporations Code section 1505, so the record shows the agent company and its authorized employees rather than a street address for the entity. (common) Check: Expand the entity on bizfile Online and read the '1505' agent block.
  - The entity is a general partnership or limited liability partnership, which does not appear in the bizfile Online Business Search at all. (occasional) Check: Confirm the entity type; LLP and GP filings must be requested on the paper Business Entity Records Order Form.
- **How to prove it**:
  - [tier 1, settles it] Search the entity on bizfile Online Business Search; the Agent name appears as a column in results and the full agent detail plus 'Standing - Agent' appears in the expanded row. https://bizfileonline.sos.ca.gov/search/business
  - [tier 3, corroborating only] If a commercial agent is used, check the agent provider's customer portal for an active service contract.
  - [tier 4, settles it] Read the agent block on the most recently filed Statement of Information PDF, available free from bizfile Online. https://bizfileonline.sos.ca.gov/search/business
  - [tier 5, corroborating only] Look for a recurring annual subscription to a registered agent provider.
- **Fix**:
  1. Look up the entity on bizfile Online and read the Agent field and 'Standing - Agent'.
  2. If the agent has resigned or moved, file a Statement of Information or a change of agent filing naming a current agent who consents to serve.
  3. Keep the agent's address current so service of process and state notices actually arrive.
- **Source**: https://www.sos.ca.gov/business-programs/business-entities/service-process (verified 2026-08-14)
- **Note**: The cited page states that corporations, limited liability companies, limited partnerships and limited liability partnerships are required by statute to designate an agent for service of process, and that limited liability partnerships, general partnerships and associations are not contained in the Business Search.

### California foreign corporation qualification `ca-foreign-qualification-corporation`
Applies to: c-corp, s-corp, benefit-corp, nonprofit | category: entity
A corporation formed outside California qualifies to do business here by filing a Statement and Designation by Foreign Corporation with the Secretary of State, together with a certificate of good standing from its home state. Once qualified it becomes subject to California franchise tax. A corporation that does business in California without qualifying is still subject to the franchise tax.
- **Deadline**: Before transacting intrastate business in California.
- **Cost**: $100.00 for a foreign stock corporation. $30.00 for a foreign nonstock, nonprofit corporation.
- **Rule out first**:
  - The company's California contacts do not amount to transacting intrastate business, for example only remote sales into the state, so no qualification was required. (common) Check: Assess the actual California activity against the intrastate business standard, and check whether a franchise tax account exists.
  - The entity qualified under a slightly different legal name or a registered DBA, so a name search misses it. (occasional) Check: Search bizfile Online by entity number and by every known name variant, not just the trading name.
  - A law firm or formation agent handled and paid for the qualification. (common) Check: Search bizfile Online for the entity record, which exists regardless of who filed it.
- **How to prove it**:
  - [tier 1, settles it] Search the corporation on bizfile Online Business Search; a qualified foreign corporation appears with Entity Type 'Stock Corporation - Out of State' and a 'Formed In' value naming the home state. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, corroborating only] Check MyFTB for a California franchise tax account opened for the entity. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Obtain the endorsed Statement and Designation by Foreign Corporation and the certificate of good standing that was filed with it.
  - [tier 5, corroborating only] Look for a $100 payment to the CA Secretary of State around the time California operations began.
- **Fix**:
  1. Search bizfile Online by name and by entity number to confirm whether a foreign registration exists.
  2. If not, obtain a certificate of good standing from the home state and file the Statement and Designation by Foreign Corporation with the $100 fee.
  3. Register with the Franchise Tax Board and bring any back year franchise tax filings current.
- **Source**: https://www.ftb.ca.gov/file/business/types/corporations/index.html (verified 2026-08-14)
- **Note**: The qualification mechanism, the certificate of good standing requirement and the rule that an unqualified corporation doing business in California is still subject to franchise tax come from the cited FTB page. The $100.00 and $30.00 fees come from the Secretary of State Business Entities Fee Schedule, https://bpd.cdn.sos.ca.gov/pdf/be-fee-schedule-062018.pdf.

### California foreign LLC registration `ca-foreign-qualification-llc`
Applies to: llc, llc-single-member | category: entity
An LLC formed outside California registers to do business here by filing an Application to Register a Foreign Limited Liability Company, Form LLC-5, with the Secretary of State. Registering triggers the $800 annual LLC tax and the Statement of Information cycle.
- **Deadline**: Before transacting intrastate business in California.
- **Cost**: $70.00 (Form LLC-5).
- **Rule out first**:
  - The LLC only sells remotely into California and does not transact intrastate business, so no registration is required. (common) Check: Evaluate the California activity, and separately check whether a seller's permit obligation exists under the $500,000 economic nexus rule.
  - The LLC registered under a modified name because its true name was unavailable in California. (occasional) Check: Search bizfile Online for name variants and by entity number.
  - An employer of record or PEO handles California employment, which does not by itself create a registration record for the LLC. (occasional) Check: Confirm whether the LLC itself has any California nexus beyond the employment arrangement.
- **How to prove it**:
  - [tier 1, settles it] Search the LLC on bizfile Online Business Search and check the 'Formed In' column for a non California jurisdiction alongside an active California record. https://bizfileonline.sos.ca.gov/search/business
  - [tier 2, corroborating only] Check MyFTB for the LLC's California account and $800 annual tax history. https://www.ftb.ca.gov/myftb/
  - [tier 4, settles it] Obtain the endorsed Form LLC-5.
  - [tier 5, corroborating only] Look for a $70 payment to the CA Secretary of State.
- **Fix**:
  1. Search bizfile Online to confirm whether the LLC has a California registration.
  2. File Form LLC-5 with the $70.00 fee if registration is required.
  3. Expect the $800 annual tax and the biennial Statement of Information to start once registered.
- **Source**: https://bpd.cdn.sos.ca.gov/pdf/be-fee-schedule-062018.pdf (verified 2026-08-14)
- **Note**: Fee and form number come from the Secretary of State Business Entities Fee Schedule (rev. 06/2018) which lists 'Application to Register a Foreign Limited Liability Company (Form LLC-5) $70.00'. Downstream $800 annual tax consequence is from https://www.ftb.ca.gov/file/business/types/limited-liability-company/index.html.

### California employer registration and Personal Income Tax withholding (EDD) `ca-payroll-withholding-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Once you pay more than $100 in wages in a calendar quarter you must register as an employer with the Employment Development Department within 15 days. That one registration covers everything: you then withhold State Disability Insurance and Personal Income Tax from employee pay and remit it.
- **Deadline**: Register within 15 days of paying more than $100 in wages in a calendar quarter.
- **Rule out first**:
  - An employer of record or PEO is the employer of record for California staff and holds the EDD registration under its own account. (common) Check: Ask the EOR or PEO which entity's EDD account the wages are reported under, and confirm in e-Services for Business.
  - Everyone in California is a genuine independent contractor paid on 1099, so no wages were paid and no registration is due. (occasional) Check: Test the workers against California's worker classification rules before accepting this; misclassification is the usual failure mode.
  - Wages in the quarter were $100 or less, which is below the registration trigger. (rare) Check: Check total California wages paid in each calendar quarter against the $100 threshold.
- **How to prove it**:
  - [tier 2, settles it] Log in to EDD e-Services for Business and confirm an active employer payroll tax account number and filed DE 9 / DE 9C returns. https://edd.ca.gov/en/payroll_taxes/
  - [tier 3, corroborating only] Check the payroll provider (Gusto, Rippling, ADP) for the registered California account number and tax filing status.
  - [tier 4, settles it] Read the quarterly DE 9 and DE 9C returns and the payroll register showing SDI and PIT withheld.
  - [tier 5, corroborating only] Look for EDD payroll tax debits in the bank feed on the payroll cycle.
- **Fix**:
  1. Confirm whether an EDD employer payroll tax account already exists, including under a PEO or EOR.
  2. Register through EDD e-Services for Business within 15 days of crossing $100 in quarterly wages.
  3. Backfile any missing DE 9 and DE 9C returns and remit withheld SDI and PIT.
- **Source**: https://edd.ca.gov/en/payroll_taxes/am_i_required_to_register_as_an_employer/ (verified 2026-08-14)

### California Unemployment Insurance and Employment Training Tax (EDD) `ca-unemployment-insurance-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
California unemployment insurance is not a separate signup. The same EDD employer registration that covers withholding also makes you liable for Unemployment Insurance and the Employment Training Tax, which are employer paid taxes on employee wages rather than deductions from pay.
- **Deadline**: Register within 15 days of paying more than $100 in wages in a calendar quarter. UI and ETT are then reported and paid on the quarterly cycle.
- **Rule out first**:
  - A PEO or employer of record reports the wages under its own UI account, so the company has no UI account of its own. (common) Check: Ask the PEO for the account the wages are reported under and reconcile headcount to their filings.
  - UI and ETT are bundled into a single EDD payment with SDI and PIT, so there is no separate line to spot in the bank feed. (common) Check: Break out the components on the DE 9 rather than reading the bank feed.
  - The employer is new and has been assigned the new employer rate, so the rate notice looks generic rather than experience rated. (common) Check: Confirm the assigned rate in e-Services for Business.
- **How to prove it**:
  - [tier 2, settles it] Log in to EDD e-Services for Business and confirm the UI rate assigned to the account and the quarterly DE 9 filings. https://edd.ca.gov/en/payroll_taxes/
  - [tier 3, corroborating only] Check the payroll provider for the California UI rate on file and confirm it matches the EDD notice.
  - [tier 4, settles it] Read the EDD annual UI contribution rate notice for the account.
  - [tier 5, corroborating only] Look for EDD debits that include the employer paid UI and ETT components.
- **Fix**:
  1. Confirm the EDD employer account and the assigned UI rate in e-Services for Business.
  2. Make sure the payroll provider holds the current UI rate, since a stale rate under or over collects all year.
  3. File any missing quarterly DE 9 returns and pay UI and ETT due.
- **Source**: https://edd.ca.gov/en/payroll_taxes/am_i_required_to_register_as_an_employer/ (verified 2026-08-14)
- **Note**: The cited EDD page states the employer must pay Unemployment Insurance (UI) and Employment Training Tax (ETT) on employee wages and withhold SDI and PIT, all off the same registration.

### California workers' compensation insurance (mandatory from one employee) `ca-workers-compensation`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
California gives you no choice here. If you employ even one person you must carry workers' compensation insurance. There is no small employer exemption and no opt out, and the penalties for going without are among the harshest in the country, including criminal exposure.
- **Deadline**: Coverage must be in force from the first day you have an employee, and maintained continuously.
- **Rule out first**:
  - A PEO or employer of record provides the workers' compensation coverage under its master policy, so no policy exists in the company's own name. (common) Check: Ask the PEO for a certificate of insurance naming the employees, and confirm the coverage period.
  - Premium is collected inside the payroll run as a pay as you go deduction rather than as a separate annual premium invoice. (common) Check: Check the payroll provider's workers' comp module and pull the declarations page.
  - The business genuinely has no employees yet, only owners who are excluded or contractors. (occasional) Check: Confirm there are no W-2 employees on the California payroll register, and test contractor classification.
  - The company self insures under a certificate from the Office of Self-Insurance Plans. (rare) Check: Ask for the certificate of consent to self insure.
- **If it genuinely was missed**: Criminal: a fine of not less than $10,000 or imprisonment in the county jail for up to one year, or both. State penalties up to $100,000 against illegally uninsured employers. A stop order prohibiting the use of employee labor until coverage is obtained; failing to observe the stop order is itself a misdemeanor punishable by up to 60 days in county jail, a fine of up to $10,000, or both. Alongside the stop order the Division of Labor Standards Enforcement assesses the greater of twice the premiums the employer would have paid while uninsured or $1,500 per employee employed while uninsured. Where a worker's injury was compensable, a Workers' Compensation Appeals Board penalty of $10,000 per employee on the payroll at the time of injury, or $2,000 per employee where the case was non-compensable, to a maximum of $100,000.
- **How to prove it**:
  - [tier 1, settles it] Search the employer in the California Workers' Compensation Coverage Inquiry maintained by WCIRB to confirm an active policy. https://www.caworkcompcoverage.com/
  - [tier 3, corroborating only] Check the insurance broker portal or the payroll provider's pay as you go workers' comp module for an active policy.
  - [tier 4, settles it] Obtain the current workers' compensation policy declarations page showing the named insured, policy period and California coverage.
  - [tier 5, corroborating only] Look for recurring workers' compensation premium payments or a pay as you go deduction on each payroll run.
- **Fix**:
  1. Confirm active coverage through the California Workers' Compensation Coverage Inquiry and pull the declarations page.
  2. If coverage is missing, bind a policy immediately, because exposure runs from the first uninsured day.
  3. If a stop order was issued, obtain coverage and clear the order before resuming use of employee labor.
- **Source**: https://www.dir.ca.gov/dwc/faqs.html (verified 2026-08-14)
- **Note**: The mandate and all penalty amounts are quoted from the cited Division of Workers' Compensation FAQ, which cites California Labor Code sections 3700, 3700.5 and 3722. Corrected 2026-08-14: an earlier version attached the up to $10,000 fine to the stop order itself and omitted the Labor Code section 3722(b) assessment entirely. The FAQ states the $10,000 fine and 60 day jail term are for failure to observe the stop order, and that DLSE separately assesses 'the greater of (1) twice the amount the employer would have paid in workers' compensation premiums during the period the employer was uninsured ... or (2) the sum of one thousand five hundred dollars ($1,500) per employee employed during the period the employer was uninsured'. The $2,000 per employee non-compensable tier is section 3722(d) and (f). The WCIRB coverage inquiry URL in the evidence list is an actionable lookup, not the source of the rule.

### California seller's permit and $500,000 economic nexus `ca-sellers-permit-and-economic-nexus`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
If you sell or lease tangible goods in California, even temporarily, you register with the CDTFA and hold a seller's permit. An out of state seller with no physical presence is pulled in once combined sales for delivery into California exceed $500,000 in the preceding or current calendar year. There is no separate transaction count test in California.
- **Deadline**: Register before making taxable sales. Out of state retailers become required to register once the $500,000 threshold is exceeded in the preceding or current calendar year.
- **Rule out first**:
  - The business sells only services or only non taxable items, so no seller's permit is required. (common) Check: Confirm the revenue is genuinely for services and not bundled with tangible goods.
  - All California sales run through a marketplace facilitator that collects and remits the tax, so the seller sees no CDTFA remittance of its own. (common) Check: Check the marketplace's tax reporting and confirm the facilitator is the party collecting.
  - California sales are under $500,000 and there is no physical presence, so the remote seller threshold has not been crossed. (common) Check: Total combined California delivery sales for the preceding and current calendar year, including related persons.
  - A temporary seller's permit was used for a short run of sales in one location for 90 days or less. (rare) Check: Check the CDTFA account for a temporary permit record.
- **How to prove it**:
  - [tier 1, settles it] Verify the seller's permit number in the CDTFA online permit verification tool. https://www.cdtfa.ca.gov/
  - [tier 2, settles it] Log in to the CDTFA online services account and confirm an active seller's permit and filed sales and use tax returns. https://onlineservices.cdtfa.ca.gov/
  - [tier 3, corroborating only] Check the tax automation provider (Avalara, TaxJar, Stripe Tax) for a registered California jurisdiction and its filing calendar.
  - [tier 5, corroborating only] Look for CDTFA remittances on the monthly or quarterly filing cycle.
- **Fix**:
  1. Total combined California delivery sales for the preceding and current calendar year against the $500,000 threshold.
  2. Register online with the CDTFA for a seller's permit or a Certificate of Registration for Use Tax.
  3. Configure the tax engine for California state, local and district tax, since district use tax follows the same $500,000 rule.
- **Source**: https://www.cdtfa.ca.gov/industry/wayfair.htm (verified 2026-08-14)
- **Note**: The $500,000 threshold, the absence of a transaction count test, the inclusion of related persons and the April 1, 2019 effective date come from the cited CDTFA Wayfair page. The general seller's permit requirement and the temporary permit rule come from https://www.cdtfa.ca.gov/services/permits-licenses.htm.

### California Attorney General charity registration and annual RRF-1 `ca-charity-registration`
Applies to: nonprofit | category: information-report
A California nonprofit that holds charitable assets registers with the Attorney General's Registry of Charities and Fundraisers, and this is separate from incorporating with the Secretary of State. You have 30 days from first receiving charitable assets. After that you renew each year on Form RRF-1.
- **Deadline**: Initial registration must occur within 30 days of first receiving charitable assets. Form RRF-1 renews the registration annually and reports on the prior fiscal year.
- **Cost**: $50 initial registration fee.
- **Rule out first**:
  - The organization has not yet received any charitable assets, so the 30 day clock has not started. (common) Check: Identify the date of the first charitable contribution or asset received and count 30 days from there.
  - The registration is current but the RRF-1 for the most recent fiscal year is not yet due, since it reports on the prior fiscal year. (common) Check: Check the registration status and the RRF-1 due date in the Registry Search record.
  - The organization is a type exempt from registration, such as certain religious organizations or government entities. (occasional) Check: Confirm the exemption category against the Attorney General's registration guidance before concluding no filing is due.
- **How to prove it**:
  - [tier 1, settles it] Search the organization in the Attorney General's Registry of Charities and Fundraisers Registry Search and read its registration status. https://rct.doj.ca.gov/Verification/Web/Search.aspx
  - [tier 2, settles it] Log in to the organization's Registry of Charities online account and review filing history.
  - [tier 4, settles it] Obtain the filed Form CT-1 initial registration and the most recent Form RRF-1.
  - [tier 5, corroborating only] Look for the $50 initial registration payment to the Department of Justice.
- **Fix**:
  1. Search the Registry of Charities and Fundraisers to confirm the organization's registration status.
  2. If unregistered, file the initial registration and pay the $50 fee within 30 days of first receiving charitable assets.
  3. File Form RRF-1 for each delinquent year and bring the registration back to current status.
- **Source**: https://oag.ca.gov/charities/initial-reg (verified 2026-08-14)


## TX (11)

### Texas franchise tax report `tx-franchise-tax-report`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp | category: tax
Texas has no corporate income tax but it does have a franchise tax, a privilege tax on gross receipts. Most startups pay nothing because revenue is below the no tax due threshold, but you are still in the system. The threshold is generous: $2,470,000 of annualized total revenue for 2025 and $2,650,000 for 2026.
- **Deadline**: The annual franchise tax report is due May 15.
- **Rule out first**:
  - Annualized total revenue is at or below the no tax due threshold, so there is genuinely no tax and no payment to find. (common) Check: Compare annualized total revenue to the threshold for that report year and confirm 'Right to Transact Business' is ACTIVE in the account status search.
  - For the 2024 report year and later the No Tax Due Report was discontinued, so an entity below the threshold correctly has no No Tax Due Report on file. (common) Check: Confirm the entity filed a Public Information Report or Ownership Information Report instead, which is what replaced it.
  - The entity is a member of a combined group and its revenue is reported on the reporting entity's franchise tax report. (occasional) Check: Ask for the combined group report and confirm the entity appears on the affiliate schedule.
  - The entity is a passive general partnership or another excepted entity that is not a taxable entity. (occasional) Check: Confirm the entity type and passive status against the Comptroller's exception rules.
- **How to prove it**:
  - [tier 1, settles it] Search the entity in the Comptroller's Franchise Tax Account Status Search by name, taxpayer number or SOS file number and read the 'Right to Transact Business in Texas' field. ACTIVE means franchise tax obligations are current. https://comptroller.texas.gov/taxes/franchise/account-status/search
  - [tier 2, settles it] Log in to Webfile and review the entity's franchise tax filing history and any outstanding reports. https://comptroller.texas.gov/taxes/file-pay/
  - [tier 4, settles it] Obtain the filed franchise tax report for the report year showing annualized total revenue.
  - [tier 5, corroborating only] Look for a payment to the Texas Comptroller around mid May.
- **Fix**:
  1. Look up 'Right to Transact Business in Texas' in the Franchise Tax Account Status Search.
  2. If it is not ACTIVE, log in to Webfile and identify which report years are outstanding.
  3. File the outstanding franchise tax reports and the required information report, then confirm the status flips back to ACTIVE.
- **Source**: https://comptroller.texas.gov/taxes/franchise/ (verified 2026-08-14)
- **Note**: Thresholds ($2,470,000 for 2025 and $2,650,000 for 2026), rates (0.75% general, 0.375% retail and wholesale, 0.331% EZ computation under $20M revenue) and the May 15 due date are stated on the cited Comptroller page.

### Texas Public Information Report (Form 05-102) `tx-public-information-report`
Applies to: c-corp, s-corp, llc, llc-single-member, benefit-corp | category: information-report
This is the filing people miss. Even when your revenue is below the no tax due threshold and you owe zero franchise tax, you still have to file a Public Information Report listing your officers and directors. Since the 2024 report year the No Tax Due Report was discontinued, so the PIR is the filing that keeps you in good standing.
- **Deadline**: Filed with the annual franchise tax report, due May 15.
- **Rule out first**:
  - The entity is a veteran owned business within its first five years, which is exempt from information reports. (rare) Check: Confirm the veteran owned designation and the formation date.
  - The entity files an Ownership Information Report instead, because it is not a corporation, LLC, LP, professional association or financial institution. Ownership Information Reports are confidential and never display publicly. (common) Check: Confirm the entity's legal form; absence from the public page is expected for OIR filers and proves nothing.
  - The displayed PIR is from an older report year because the newest one has not been processed or was sourced from the Secretary of State. (common) Check: Check Webfile for the submission record rather than relying on the public display year.
  - The entity is a financial institution, whose PIRs are regulated by the Texas Department of Banking and are not listed on the public page. (rare) Check: Confirm the entity is a financial institution and check with the Department of Banking.
- **How to prove it**:
  - [tier 1, settles it] Open the entity in the Franchise Tax Account Status Search; the most recent Public Information Report officers and directors are displayed on the detail page, with the report year. https://comptroller.texas.gov/taxes/franchise/account-status/search
  - [tier 2, settles it] Log in to Webfile and confirm the Public Information Report was submitted for each report year. https://comptroller.texas.gov/taxes/file-pay/
  - [tier 4, settles it] Order copies of Public Information Reports from open.records@cpa.texas.gov or the Comptroller Open Records Section.
- **Fix**:
  1. Check 'Right to Transact Business in Texas' and the displayed PIR year in the Franchise Tax Account Status Search.
  2. File Form 05-102 through Webfile for each outstanding report year.
  3. Note that registered agent, registered office and general partner changes cannot be made on the PIR and must be filed with the Secretary of State separately.
- **Source**: https://comptroller.texas.gov/taxes/franchise/filing-requirements.php (verified 2026-08-14)
- **Note**: The rule that entities at or below the No Tax Due Threshold must still file Form 05-102 or Form 05-167 for the 2024 report year and later, and that the No Tax Due Report was discontinued for reports originally due on or after Jan. 1, 2024, is quoted from the cited page. The entity type split and the veteran owned five year exception are stated on the Franchise Tax Account Status page at https://comptroller.texas.gov/taxes/franchise/account-status/search.

### Texas Ownership Information Report (Form 05-167) `tx-ownership-information-report`
Applies to: partnership, nonprofit | category: information-report
If your entity is a taxable entity but is not a corporation, LLC, limited partnership, professional association or financial institution, you file an Ownership Information Report instead of a Public Information Report. Unlike the PIR it is confidential, so it will never show up on the public status page.
- **Deadline**: Filed with the annual franchise tax report, due May 15.
- **Rule out first**:
  - Ownership Information Reports are confidential and will not display on the public account status page, so absence from the public record is expected and means nothing. (common) Check: Check Webfile or ask the entity for its filed copy. Never infer non filing from the public page.
  - The partnership qualifies as passive and is not required to file information reports at all. (occasional) Check: Test the partnership against the Comptroller's passive entity criteria for the period.
  - The entity is actually a limited partnership, which files a Public Information Report rather than an OIR. (occasional) Check: Confirm the legal form; LPs are on the PIR list.
- **How to prove it**:
  - [tier 1, corroborating only] Check 'Right to Transact Business in Texas' in the Franchise Tax Account Status Search as an indirect signal that information reports are current. https://comptroller.texas.gov/taxes/franchise/account-status/search
  - [tier 2, settles it] Log in to Webfile and confirm Form 05-167 was submitted for the report year. This is the only reliable check, since OIRs are confidential. https://comptroller.texas.gov/taxes/file-pay/
  - [tier 4, settles it] Obtain the entity's own copy of the filed Form 05-167.
- **Fix**:
  1. Confirm the entity's legal form to determine whether Form 05-102 or Form 05-167 applies.
  2. Check Webfile for submitted information reports; do not rely on the public status page for OIR filers.
  3. File any outstanding Form 05-167 for each report year.
- **Source**: https://comptroller.texas.gov/taxes/franchise/account-status/search (verified 2026-08-14)
- **Note**: The OIR scope, the confidentiality rule and the passive partnership exception are stated verbatim on the Franchise Tax Account Status page. Note that a nonprofit corporation is generally exempt from franchise tax; this obligation applies only to a nonprofit entity that is in fact a taxable entity, which is unusual.

### Texas nonprofit corporation Periodic Report (Form 802) `tx-nonprofit-periodic-report`
Applies to: nonprofit | category: entity
Texas does not make nonprofits file an annual report. Instead the Secretary of State can ask for a Periodic Report, and it can only ask once every four years. The catch is that the clock is short once the request arrives: you get 30 days before you forfeit the right to transact business.
- **Deadline**: Required not more than once every four years, upon written request by the Secretary of State. The report must be filed within 30 days of the date the request is sent. After forfeiture, the corporation can cure by filing within 120 days of the date of mailing of the notice of forfeiture.
- **Cost**: $5 for the periodic report. Periodic report after forfeiture of the right to do business: $5 plus a late fee, where the late fee is the greater of $5 or $1 for each month the report remains unfiled, not to exceed $25. Periodic report after involuntary termination: $25.
- **Rule out first**:
  - No request has been sent. The report is only due when the Secretary of State asks for it, so a nonprofit with no report on file for years is usually perfectly compliant. (common) Check: Confirm whether a written request was ever issued; absence of a filed Periodic Report is not evidence of a miss.
  - The request went to the registered agent's address and was handled by the agent without the board seeing it. (common) Check: Ask the registered agent for correspondence received from the Secretary of State and check SOSDirect for a filed report.
  - The nonprofit is unincorporated or is a trust, so it has no Secretary of State corporate filing at all. (occasional) Check: Confirm the legal form; only nonprofit corporations file Form 802.
- **If it genuinely was missed**: Failure to file within 30 days of the request forfeits the corporation's right to transact business in Texas. After 120 days the Secretary of State involuntarily terminates a Texas nonprofit corporation or revokes a foreign nonprofit corporation's registration.
- **How to prove it**:
  - [tier 1, corroborating only] Check the entity in the Comptroller's Franchise Tax Account Status Search for SOS Registration Status. https://comptroller.texas.gov/taxes/franchise/account-status/search
  - [tier 2, settles it] Search the entity in SOSDirect and review its filing history for a Periodic Report and any forfeiture entry. https://www.sos.state.tx.us/corp/sosda/index.shtml
  - [tier 4, settles it] Locate the Secretary of State's written request letter in the registered agent's mail, since the 30 day clock runs from the date it was sent.
- **Fix**:
  1. Check SOSDirect for the entity's filing history and any forfeiture notation.
  2. If a request was received, file Form 802 with the $5 fee within 30 days.
  3. If the right to transact business was already forfeited, file within 120 days of the forfeiture notice mailing date to cure before involuntary termination.
- **Source**: https://www.sos.state.tx.us/corp/nonprofitfaqs.shtml (verified 2026-08-14)
- **Note**: Frequency, the 30 day deadline, the 120 day cure and the forfeiture consequence are quoted from the cited Texas Secretary of State nonprofit FAQ. Fee amounts come from Texas Secretary of State Form 806 Fee Schedule (rev. 10/25), https://www.sos.state.tx.us/corp/forms/806_boc.pdf. Re-fetched and re-read on 2026-08-14 on sos.state.tx.us, the official Texas Secretary of State website (www.sos.texas.gov redirects to it), so this row is primary sourced. It was previously downgraded to needs-review purely because .us is not a .gov TLD, which is a domain-shape objection and not a doubt about the content.

### Texas limited partnership Periodic Report (Form 804) `tx-limited-partnership-periodic-report`
Applies to: partnership | category: entity
Like the nonprofit version, a Texas limited partnership files a Periodic Report only when the Secretary of State requests it, not on a fixed annual calendar. The fee and the late fees are much steeper than the nonprofit equivalent.
- **Deadline**: Filed on request from the Secretary of State. The exact request frequency was not confirmed from a primary source here.
- **Cost**: $50 for the periodic report. Periodic report after forfeiture of the right to do business: $50 plus a late fee of $25 per month, not to exceed $100. Periodic report after involuntary termination or revocation: $225.
- **Rule out first**:
  - No request has been issued, so nothing is due. The report is request driven, not calendar driven. (common) Check: Confirm whether the Secretary of State ever sent a request; an empty filing history is normal.
  - The entity is a general partnership rather than a limited partnership, and general partnerships are not filing entities that owe this report. (common) Check: Confirm the legal form in SOSDirect.
  - The registered agent received and filed the report without the partners being involved. (occasional) Check: Check the SOSDirect filing history for a filed Form 804.
- **If it genuinely was missed**: Failure to file leads to forfeiture of the right to do business and, if uncured, involuntary termination or revocation of registration.
- **How to prove it**:
  - [tier 1, corroborating only] Check SOS Registration Status in the Comptroller's Franchise Tax Account Status Search. https://comptroller.texas.gov/taxes/franchise/account-status/search
  - [tier 2, settles it] Search the partnership in SOSDirect and review its filing history for a Periodic Report and any forfeiture entry. https://www.sos.state.tx.us/corp/sosda/index.shtml
  - [tier 4, settles it] Locate the Secretary of State's written request letter received by the registered agent.
- **Fix**:
  1. Check SOSDirect for the partnership's filing history and any forfeiture notation.
  2. File Form 804 with the $50 fee if a request was received.
  3. If forfeited, file promptly to limit the $25 per month late fee, which caps at $100.
- **Source**: https://www.sos.state.tx.us/corp/forms/806_boc.pdf (verified 2026-08-14)
- **Note**: All fee and late fee amounts are quoted from Texas Secretary of State Form 806 Fee Schedule (rev. 10/25), which was fetched. The request frequency for limited partnerships was NOT confirmed from a fetched primary source and is deliberately left unstated. Re-fetched and re-read on 2026-08-14 on sos.state.tx.us, the official Texas Secretary of State website (www.sos.texas.gov redirects to it), so this row is primary sourced. It was previously downgraded to needs-review purely because .us is not a .gov TLD, which is a domain-shape objection and not a doubt about the content.

### Texas registered agent and registered office `tx-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, benefit-corp, nonprofit, partnership | category: registered-agent
Every Texas filing entity, domestic or foreign, must maintain a registered agent and a registered office in Texas. The registered office has to be a real physical Texas address where someone can be served during business hours, so a PO box will not work. Since 2010 the agent has to positively consent in writing to serve.
- **Deadline**: Maintained continuously from formation or registration. Changes are filed on Form 401 and the agent's consent on Form 401-A.
- **Cost**: Change of registered agent or registered office (Form 401): $15, or $5 for a nonprofit corporation or cooperative association. Consent of registered agent to appointment (Form 401-A): $15, or $5 for a nonprofit corporation or cooperative association. Rejection of appointment (Form 428) and resignation of registered agent (Form 402): no fee.
- **Rule out first**:
  - A founder or officer serves as the agent at the company's own Texas office, so there is no vendor invoice to find. (common) Check: Read the Registered Agent Name in the Franchise Tax Account Status Search; an individual name is normal and compliant.
  - The agent is a national provider such as CT Corporation System or CSC and the fee is bundled into a multi state compliance package. (common) Check: Check the provider's portal for the Texas entity, and confirm the agent name in the public record.
  - The public record shows a stale agent because a change was filed recently and the SOS status only updates each business day. (occasional) Check: Re-check the next business day, or confirm directly in SOSDirect.
- **How to prove it**:
  - [tier 1, settles it] Open the entity in the Comptroller's Franchise Tax Account Status Search and read the 'Registered Agent Name' and 'Registered Office Street Address' fields, which are populated from Secretary of State data. https://comptroller.texas.gov/taxes/franchise/account-status/search
  - [tier 2, settles it] Search the entity in SOSDirect and review the current registered agent filing. https://www.sos.state.tx.us/corp/sosda/index.shtml
  - [tier 4, settles it] Obtain the filed Form 401-A consent of registered agent.
  - [tier 5, corroborating only] Look for a recurring annual subscription to a commercial registered agent provider.
- **Fix**:
  1. Read the Registered Agent Name and Registered Office Street Address in the Franchise Tax Account Status Search.
  2. If the agent has resigned or the address is stale, file Form 401 with the $15 fee and obtain the agent's Form 401-A consent.
  3. Remember that registered agent and registered office changes cannot be made through the Public Information Report; they must go to the Secretary of State.
- **Source**: https://www.sos.state.tx.us/corp/registeredagents.shtml (verified 2026-08-14)
- **Note**: The requirement, the physical Texas address rule and the written consent requirement under BOC section 5.201(b) are quoted from the cited Texas Secretary of State registered agents page. Fees come from Form 806 Fee Schedule (rev. 10/25), https://www.sos.state.tx.us/corp/forms/806_boc.pdf. Registered agent and office data is independently visible on the .gov Comptroller page at https://comptroller.texas.gov/taxes/franchise/account-status/search. Re-fetched and re-read on 2026-08-14 on sos.state.tx.us, the official Texas Secretary of State website (www.sos.texas.gov redirects to it), so this row is primary sourced. It was previously downgraded to needs-review purely because .us is not a .gov TLD, which is a domain-shape objection and not a doubt about the content.

### Texas foreign entity registration `tx-foreign-entity-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An out of state corporation or LLC registers to transact business in Texas by filing an Application for Registration with the Secretary of State. Texas charges $750, which is one of the higher foreign registration fees in the country. The real sting is the late fee: transact business for more than ninety days without registering and you owe an extra registration fee for every year you were unregistered.
- **Deadline**: Before transacting business in Texas. A foreign entity that has transacted business in Texas for more than ninety days without registering incurs a late filing fee.
- **Cost**: $750 for a foreign for-profit corporation, LLC, professional corporation, professional LLC, limited partnership, out-of-state financial institution, professional association, business trust or series LLC (Forms 301, 303, 304, 305, 306, 309, 311, 312, 313). $25 for a foreign nonprofit corporation, cooperative association or credit union (Forms 302, 309). Foreign limited liability partnership: $200 per partner in Texas, not less than $200 nor more than $750 (Forms 307, 308).
- **Rule out first**:
  - The entity's Texas activity does not amount to transacting business, for example only remote sales, so no registration was required. (common) Check: Assess the actual Texas activity, and separately check whether a sales tax permit obligation exists under the $500,000 remote seller rule.
  - The entity registered under a fictitious or assumed name in Texas because its true name was unavailable. (occasional) Check: Search SOSDirect by every known name variant and by file number, not just the trading name.
  - Registration is within the first ninety days of transacting business, so no late fee has accrued yet. (occasional) Check: Compare the date Texas activity actually began with the Effective SOS Registration Date.
  - Counsel or a formation agent filed and paid, so no $750 appears in the company's own bank feed. (common) Check: Check the public registration record, which exists regardless of who paid.
- **If it genuinely was missed**: A late filing fee equal to the registration fee for each full or partial calendar year that the foreign entity transacted business in Texas without being registered.
- **How to prove it**:
  - [tier 1, settles it] Search the entity in the Comptroller's Franchise Tax Account Status Search and read 'State of Formation', 'SOS Registration Status' and 'Effective SOS Registration Date'. https://comptroller.texas.gov/taxes/franchise/account-status/search
  - [tier 2, settles it] Search SOSDirect for the entity's registration record and effective date. https://www.sos.state.tx.us/corp/sosda/index.shtml
  - [tier 4, settles it] Obtain the filed Application for Registration (Form 301 or 304) with its acknowledgment of filing.
  - [tier 5, corroborating only] Look for a $750 payment to the Texas Secretary of State around the time Texas operations began.
- **Fix**:
  1. Search the Franchise Tax Account Status Search and SOSDirect to confirm whether a Texas registration exists and when it took effect.
  2. If unregistered, file the applicable Application for Registration with the $750 fee.
  3. Quantify the late filing fee exposure, which is one registration fee for each full or partial calendar year of unregistered activity beyond ninety days, and budget for it before filing.
- **Source**: https://www.sos.state.tx.us/corp/forms/806_boc.pdf (verified 2026-08-14)
- **Note**: All fees, the ninety day rule and the per year late filing fee formula are quoted from Texas Secretary of State Form 806 Fee Schedule (rev. 10/25), which was fetched and read. Re-fetched and re-read on 2026-08-14 on sos.state.tx.us, the official Texas Secretary of State website (www.sos.texas.gov redirects to it), so this row is primary sourced. It was previously downgraded to needs-review purely because .us is not a .gov TLD, which is a domain-shape objection and not a doubt about the content.

### Texas state income tax withholding (none) `tx-state-income-tax-withholding`
**NOT FULLY VERIFIED.** The obligation is real; its fee, deadline and penalty could not be confirmed at the source and are withheld. Confirm at the source link.
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Texas does not levy a personal income tax, so there is no state income tax withholding registration and no state withholding account to open. You still handle federal withholding, and you still register separately for state unemployment tax with the Texas Workforce Commission.
- **Deadline**: Not applicable.
- **Rule out first**:
  - There is no Texas withholding account number because none exists. An empty field in a payroll system is correct, not a gap. (common) Check: Confirm the Texas Workforce Commission unemployment tax account is present instead; that is the state registration Texas employers actually need.
  - An employee lives in another state that does tax income, so withholding appears for that state and not for Texas. (occasional) Check: Check the employee's work and residence state and the corresponding state registrations.
- **How to prove it**:
  - [tier 1, corroborating only] Review the Comptroller's list of all taxes and fees administered in Texas and confirm no personal income tax or wage withholding tax appears. https://comptroller.texas.gov/taxes/
  - [tier 2, settles it] Confirm the payroll provider has no Texas state income tax withholding account configured, because none exists to configure.
  - [tier 4, settles it] Review Texas employee payslips and confirm no state income tax line is withheld.
- **Fix**:
  1. Do not attempt to register for Texas state income tax withholding; there is no such account.
  2. Confirm the Texas Workforce Commission unemployment tax account exists and is active.
  3. Confirm federal withholding and deposits are being handled correctly.
- **Source**: https://comptroller.texas.gov/taxes/ (verified 2026-08-14)
- **Note**: The Comptroller's complete list of taxes and fees was fetched on 2026-08-14 and contains no personal income tax and no wage withholding tax, which is strong evidence of absence. However no fetched .gov page states affirmatively that Texas has no personal income tax, so this is marked needs-review rather than asserted from an explicit statement. The constitutional prohibition (Texas Constitution Article VIII) could not be fetched because statutes.capitol.texas.gov now serves a JavaScript application that returns no text to a fetcher.

### Texas unemployment tax registration (TWC) `tx-unemployment-tax-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
Texas employers register with the Texas Workforce Commission for unemployment tax. You become liable once you pay $1,500 in total gross wages in a calendar quarter, or once you have had at least one employee in twenty different weeks in a calendar year, whichever comes first. A 501(c)(3) nonprofit is on a different headcount test: four or more employees during 20 different weeks, not one. Either way you then have ten days to register.
- **Deadline**: Register with the Texas Workforce Commission within ten days of becoming liable under the Texas Unemployment Compensation Act.
- **Rule out first**:
  - A PEO or employer of record reports Texas wages under its own TWC account, so the company has no account of its own. (common) Check: Ask the PEO which TWC account the wages are reported under and reconcile headcount to their filings.
  - Liability thresholds have not been crossed yet, for example a single part time hire whose wages stay under $1,500 in every quarter and who has not worked twenty weeks. (common) Check: Total gross wages by calendar quarter and count the number of distinct weeks with at least one employee.
  - Everyone in Texas is a genuine contractor on 1099, so there are no wages and no liability. (occasional) Check: Test worker classification before accepting this.
  - The twenty week count is being read as consecutive weeks. It is not; the weeks need not be consecutive and the employee need not be the same person. (occasional) Check: Recount distinct weeks with at least one employee across the calendar year.
- **How to prove it**:
  - [tier 2, settles it] Log in to the TWC Unemployment Tax Services portal and confirm an active TWC account number and filed quarterly wage reports. https://www.twc.texas.gov/programs/unemployment-tax
  - [tier 3, corroborating only] Check the payroll provider for the Texas TWC account number and the SUTA rate on file.
  - [tier 4, settles it] Obtain the TWC quarterly wage reports and the annual tax rate notice for the account.
  - [tier 5, corroborating only] Look for quarterly TWC debits in the bank feed at the end of the month following each quarter.
- **Fix**:
  1. Determine the exact date liability was triggered by testing both the $1,500 quarterly wage test and the twenty week test.
  2. Register with TWC within ten days of that date through Unemployment Tax Registration.
  3. Backfile any missing quarterly wage reports and pay contributions, remembering the first $9,000 paid to each employee per calendar year is taxable.
- **Source**: https://www.twc.texas.gov/programs/unemployment-tax/determine-tax-account (verified 2026-08-14)
- **Note**: Re-verified on the cited TWC page 2026-08-14, which states 'Employers who pay wages must register with the Texas Workforce Commission (TWC) within ten days of becoming liable under TUCA' and, under Who is a Liable Employer, 'An employing unit that pays $1,500 or more in total gross wages in a calendar quarter or has at least one employee during twenty different weeks in a calendar year regardless of the wages.' Corrected 2026-08-14 for scope: this row carries the nonprofit entity type, and the same page gives nonprofits a different test, 'An employing unit that is a 501(c)(3) non-profit organization and has four or more employees during 20 different weeks in a calendar year.' The one-employee test was therefore overstated for nonprofits.

### Texas workers' compensation (optional, with non-subscriber duties) `tx-workers-compensation-elective`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
Texas is the outlier. Workers' compensation insurance is optional for most private employers here, with no employee count threshold that forces you in. But opting out is not free: if you go without coverage you are a non-subscriber, you must file a notice of no coverage with the state every year between February 1 and April 30, and you lose the common law defenses that make workers' comp a bargain in the first place. The separate duty to report work injuries applies only once you have five or more employees.
- **Deadline**: File the notice of no coverage with the Division of Workers' Compensation between February 1 and April 30 of each calendar year, and also after hiring your first employee and after terminating a Texas workers' compensation policy. Employers with five or more employees must additionally report each work-related injury with more than one day of lost time, and each work-related illness or death, within one month and seven days of the death, of knowledge of the illness, or of the start of lost time.
- **Rule out first**:
  - The employer is a lawful non-subscriber. Absence of a workers' compensation policy in Texas is not a violation the way it is in California or Florida. (common) Check: Confirm the non-subscriber notice was filed with the state and that employees were notified. That is the actual obligation, not the policy.
  - Coverage exists through a PEO or employer of record master policy rather than a policy in the company's own name. (common) Check: Ask the PEO for a certificate of insurance covering the Texas employees.
  - The employer bought an occupational accident or employer liability policy, which looks like workers' comp in the ledger but is not a subscription. (occasional) Check: Read the policy form; only a Texas workers' compensation policy makes the employer a subscriber.
  - The business has no Texas employees yet, only contractors or out of state staff. (occasional) Check: Check the Texas payroll register for W-2 employees.
- **How to prove it**:
  - [tier 1, settles it] Search the employer in the Texas Department of Insurance workers' compensation coverage verification to see whether an active policy exists. https://www.tdi.texas.gov/wc/employer/index.html
  - [tier 2, settles it] Check the employer's DWC Employer E-File record for a filed non-subscriber notice. https://www.tdi.texas.gov/wc/employer/index.html
  - [tier 4, settles it] Obtain either the workers' compensation policy declarations page or the filed non-subscriber notice, whichever applies.
  - [tier 5, corroborating only] Look for workers' compensation premium payments, or for occupational accident or employer liability policy premiums, which non-subscribers often buy instead.
- **Fix**:
  1. Decide deliberately whether to subscribe, because the choice is real in Texas and it changes your liability exposure.
  2. If you do not subscribe, file the non-subscriber notice with the state and give employees written notice of the non-subscriber status.
  3. If you have five or more employees, set up a process to report work-related injuries with more than one day of lost time, and all work-related illnesses and deaths, to the Division of Workers' Compensation within one month and seven days.
- **Source**: https://www.tdi.texas.gov/wc/nonsubscriber.html (verified 2026-08-14)
- **Note**: Corrected 2026-08-14 on two counts. First, the deadline is not unstated: TDI's non-subscriber page, fetched 2026-08-14, says the notice of no coverage 'should be filed. Between February 1 and April 30 of each calendar year. After hiring the first employee. After terminating a Texas workers' compensation policy.' Second, the injury reporting duty was previously stated without its scope limit; the same page qualifies it 'Required for employers with five or more employees' and 'Due within one month and seven days from the date of death, knowledge of the work-related illness, or after lost time began.' The optional nature of coverage is on https://www.tdi.texas.gov/wc/employer/index.html: 'In Texas, private employers can choose to carry workers' compensation insurance coverage, but it is not required in most cases.' Governing law cited by TDI: Texas Labor Code 406.004, 406.005, 406.007 and 411.032.

### Texas sales and use tax permit and $500,000 remote seller safe harbor `tx-sales-tax-permit-and-nexus`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
Texas requires a sales and use tax permit before you make taxable sales in the state. A remote seller with no Texas presence stays outside the system while total Texas revenue is under $500,000 in the preceding twelve calendar months. Once you cross it, Texas gives you a generous ramp: you start collecting on the first day of the fourth month after the month you crossed.
- **Deadline**: A remote seller must obtain a permit and begin collecting and remitting state and local use tax no later than the first day of the fourth month after the month in which the seller exceeds the $500,000 safe harbor amount.
- **Rule out first**:
  - Texas revenue is under $500,000 in the preceding twelve calendar months and there is no physical presence, so the safe harbor applies and no permit is required. (common) Check: Total Texas revenue on a rolling twelve calendar month basis, not on a calendar year basis.
  - The threshold was crossed recently and the seller is inside the ramp period, which runs to the first day of the fourth month after the crossing month. (common) Check: Identify the month the $500,000 was exceeded and add three full months.
  - All Texas sales run through a marketplace provider that collects and remits, so the seller has no Texas remittance of its own. (common) Check: Confirm the marketplace is acting as the collecting party for those sales.
  - The business sells only non taxable services in Texas. (occasional) Check: Test the specific service against the Texas taxable services list before concluding it is out of scope.
- **How to prove it**:
  - [tier 1, settles it] Verify the permit in the Comptroller's Sales Taxpayer Search. https://mycpa.cpa.state.tx.us/staxpayersearch/
  - [tier 2, settles it] Log in to Webfile and confirm an active sales and use tax permit and the filed return history. https://comptroller.texas.gov/taxes/file-pay/
  - [tier 3, corroborating only] Check the tax automation provider for a registered Texas jurisdiction and its filing calendar.
  - [tier 5, corroborating only] Look for Texas Comptroller remittances on the monthly or quarterly cycle.
- **Fix**:
  1. Total Texas revenue for the preceding twelve calendar months and compare to the $500,000 safe harbor.
  2. If exceeded, apply for a Texas sales and use tax permit and set the collection start date to the first day of the fourth month after the crossing month.
  3. Configure the tax engine for Texas state and local use tax, and consider the single local use tax rate election for remote sellers.
- **Source**: https://comptroller.texas.gov/taxes/sales/remote-sellers.php (verified 2026-08-14)
- **Note**: The $500,000 safe harbor, the preceding twelve calendar months measurement and the first day of the fourth month collection start are quoted from the cited Comptroller page.


## FL (13)

### Florida annual report (profit corporation) `fl-annual-report-profit-corp`
Applies to: c-corp, s-corp, benefit-corp | category: entity
Florida makes every registered entity file an annual report with the Division of Corporations between January 1 and May 1. It is not a financial report, it just confirms your addresses, officers and registered agent. Miss May 1 and a flat $400 late fee is added, and the state will not waive it.
- **Deadline**: The first annual report must be delivered between January 1 and May 1 of the year following the calendar year in which the entity was formed or qualified. Subsequent reports are due between January 1 and May 1 each year. An entity that has not filed by the third Friday in September is administratively dissolved or revoked at the close of business on the fourth Friday in September.
- **Cost**: $150.00 if filed by May 1. $550.00 if received after May 1 ($150.00 plus the $400 late fee).
- **Rule out first**:
  - A registered agent or compliance service filed the annual report and paid the fee, so nothing appears in the company's own bank feed. (common) Check: Open the entity on Sunbiz and read the Annual Reports table, which lists each report year and its filed date regardless of who paid.
  - The entity was formed late in the prior year, so its first annual report is not due until between January 1 and May 1 of the following year. (common) Check: Compare the Date Filed on the Sunbiz record with the annual report window.
  - An amended annual report was filed later in the year, which is normal and does not mean the original was late. (occasional) Check: Read the Annual Reports table on Sunbiz; the first report filed in a calendar year is the annual report and later ones are amendments.
- **If it genuinely was missed**: A $400 late fee applies to reports filed after May 1, and there is no provision to abate or waive it. Failure to file by the third Friday in September results in administrative dissolution or revocation on the fourth Friday in September.
- **How to prove it**:
  - [tier 1, settles it] Search the entity on Sunbiz by name or document number and read the Annual Reports table, which lists Report Year and Filed Date, plus the Status field. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 1, settles it] Open the free PDF image of the filed annual report from the entity detail page. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 2, settles it] Log in to the Sunbiz e-filing account and review the entity's filing history. https://services.sunbiz.org/
  - [tier 5, corroborating only] Look for a payment to 'Florida Department of State' in the first four months of the year.
- **Fix**:
  1. Look up the entity on Sunbiz and read the Status field and the Annual Reports table.
  2. File the annual report through Sunbiz and pay the fee, adding the $400 late fee if filing after May 1.
  3. If the entity was administratively dissolved or revoked, file for reinstatement with the Division of Corporations. The reinstatement fee depends on entity type; for a Florida profit corporation it is $600 under section 607.0122(13). Confirm the amount for your entity type on the Division of Corporations fee schedule before paying.
- **Source**: https://dos.fl.gov/sunbiz/manage-business/efile/annual-report/ (verified 2026-08-14)
- **Note**: Filing window, fees, the $400 late fee and the administrative dissolution timing are stated on the cited Division of Corporations page. The January 1 to May 1 statutory window is confirmed independently at https://www.flsenate.gov/Laws/Statutes/2024/607.1622 (section 607.1622(4)).

### Florida annual report (LLC) `fl-annual-report-llc`
Applies to: llc, llc-single-member | category: entity
Florida makes every registered entity file an annual report with the Division of Corporations between January 1 and May 1. It is not a financial report, it just confirms your addresses, officers and registered agent. Miss May 1 and a flat $400 late fee is added, and the state will not waive it.
- **Deadline**: The first annual report must be delivered between January 1 and May 1 of the year following the calendar year in which the entity was formed or qualified. Subsequent reports are due between January 1 and May 1 each year. An entity that has not filed by the third Friday in September is administratively dissolved or revoked at the close of business on the fourth Friday in September.
- **Cost**: $138.75 if filed by May 1. $538.75 if received after May 1 ($138.75 plus the $400 late fee).
- **Rule out first**:
  - A registered agent or compliance service filed the annual report and paid the fee, so nothing appears in the company's own bank feed. (common) Check: Open the entity on Sunbiz and read the Annual Reports table, which lists each report year and its filed date regardless of who paid.
  - The entity was formed late in the prior year, so its first annual report is not due until between January 1 and May 1 of the following year. (common) Check: Compare the Date Filed on the Sunbiz record with the annual report window.
  - An amended annual report was filed later in the year, which is normal and does not mean the original was late. (occasional) Check: Read the Annual Reports table on Sunbiz; the first report filed in a calendar year is the annual report and later ones are amendments.
- **If it genuinely was missed**: A $400 late fee applies to reports filed after May 1, and there is no provision to abate or waive it. Failure to file by the third Friday in September results in administrative dissolution or revocation on the fourth Friday in September.
- **How to prove it**:
  - [tier 1, settles it] Search the entity on Sunbiz by name or document number and read the Annual Reports table, which lists Report Year and Filed Date, plus the Status field. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 1, settles it] Open the free PDF image of the filed annual report from the entity detail page. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 2, settles it] Log in to the Sunbiz e-filing account and review the entity's filing history. https://services.sunbiz.org/
  - [tier 5, corroborating only] Look for a payment to 'Florida Department of State' in the first four months of the year.
- **Fix**:
  1. Look up the entity on Sunbiz and read the Status field and the Annual Reports table.
  2. File the annual report through Sunbiz and pay the fee, adding the $400 late fee if filing after May 1.
  3. If the entity was administratively dissolved or revoked, file for reinstatement with the Division of Corporations. The reinstatement fee depends on entity type; for a Florida profit corporation it is $600 under section 607.0122(13). Confirm the amount for your entity type on the Division of Corporations fee schedule before paying.
- **Source**: https://dos.fl.gov/sunbiz/manage-business/efile/annual-report/ (verified 2026-08-14)
- **Note**: Filing window, fees, the $400 late fee and the administrative dissolution timing are stated on the cited Division of Corporations page. The January 1 to May 1 statutory window is confirmed independently at https://www.flsenate.gov/Laws/Statutes/2024/605.0212 (section 605.0212(3)).

### Florida annual report (nonprofit corporation) `fl-annual-report-nonprofit`
Applies to: nonprofit | category: entity
Florida makes every registered entity file an annual report with the Division of Corporations between January 1 and May 1. It is not a financial report, it just confirms your addresses, officers and registered agent. Nonprofit corporations are not subject to the $400 late fee that hits other entity types.
- **Deadline**: The first annual report must be delivered between January 1 and May 1 of the year following the calendar year in which the entity was formed or qualified. Subsequent reports are due between January 1 and May 1 each year. An entity that has not filed by the third Friday in September is administratively dissolved or revoked at the close of business on the fourth Friday in September.
- **Cost**: $61.25.
- **Rule out first**:
  - A registered agent or compliance service filed the annual report and paid the fee, so nothing appears in the company's own bank feed. (common) Check: Open the entity on Sunbiz and read the Annual Reports table, which lists each report year and its filed date regardless of who paid.
  - The entity was formed late in the prior year, so its first annual report is not due until between January 1 and May 1 of the following year. (common) Check: Compare the Date Filed on the Sunbiz record with the annual report window.
  - An amended annual report was filed later in the year, which is normal and does not mean the original was late. (occasional) Check: Read the Annual Reports table on Sunbiz; the first report filed in a calendar year is the annual report and later ones are amendments.
  - There is no $400 late fee for nonprofits, so a report filed after May 1 shows the same $61.25 fee and looks identical to an on time filing. (common) Check: Read the Filed Date in the Sunbiz Annual Reports table rather than inferring timeliness from the amount paid.
- **If it genuinely was missed**: Nonprofit corporations are not subject to the $400 late fee. Failure to file by the third Friday in September still results in administrative dissolution or revocation on the fourth Friday in September.
- **How to prove it**:
  - [tier 1, settles it] Search the entity on Sunbiz by name or document number and read the Annual Reports table, which lists Report Year and Filed Date, plus the Status field. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 1, settles it] Open the free PDF image of the filed annual report from the entity detail page. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 2, settles it] Log in to the Sunbiz e-filing account and review the entity's filing history. https://services.sunbiz.org/
  - [tier 5, corroborating only] Look for a payment to 'Florida Department of State' in the first four months of the year.
- **Fix**:
  1. Look up the entity on Sunbiz and read the Status field and the Annual Reports table.
  2. File the annual report through Sunbiz and pay the fee.
  3. If the entity was administratively dissolved or revoked, file for reinstatement with the Division of Corporations. The reinstatement fee depends on entity type; for a Florida profit corporation it is $600 under section 607.0122(13). Confirm the amount for your entity type on the Division of Corporations fee schedule before paying.
- **Source**: https://dos.fl.gov/sunbiz/manage-business/efile/annual-report/ (verified 2026-08-14)
- **Note**: Filing window, fees, the $400 late fee and the administrative dissolution timing are stated on the cited Division of Corporations page. The January 1 to May 1 statutory window is confirmed independently at https://www.flsenate.gov/Laws/Statutes/2024/607.0122 (section 607.0122(17), annual report $61.25).

### Florida annual report (limited partnership or LLLP) `fl-annual-report-lp`
Applies to: partnership | category: entity
Florida makes every registered entity file an annual report with the Division of Corporations between January 1 and May 1. It is not a financial report, it just confirms your addresses, officers and registered agent. Miss May 1 and a flat $400 late fee is added, and the state will not waive it.
- **Deadline**: The first annual report must be delivered between January 1 and May 1 of the year following the calendar year in which the entity was formed or qualified. Subsequent reports are due between January 1 and May 1 each year. An entity that has not filed by the third Friday in September is administratively dissolved or revoked at the close of business on the fourth Friday in September.
- **Cost**: $500.00 if filed by May 1. $900.00 if received after May 1 ($500.00 plus the $400 late fee).
- **Rule out first**:
  - A registered agent or compliance service filed the annual report and paid the fee, so nothing appears in the company's own bank feed. (common) Check: Open the entity on Sunbiz and read the Annual Reports table, which lists each report year and its filed date regardless of who paid.
  - The entity was formed late in the prior year, so its first annual report is not due until between January 1 and May 1 of the following year. (common) Check: Compare the Date Filed on the Sunbiz record with the annual report window.
  - An amended annual report was filed later in the year, which is normal and does not mean the original was late. (occasional) Check: Read the Annual Reports table on Sunbiz; the first report filed in a calendar year is the annual report and later ones are amendments.
  - The entity is a general partnership, which is not registered with the Division of Corporations and therefore files no annual report at all. (common) Check: Confirm the legal form; only limited partnerships and LLLPs appear on Sunbiz with an annual report obligation.
- **If it genuinely was missed**: A $400 late fee applies to reports filed after May 1, and there is no provision to abate or waive it. Failure to file by the third Friday in September results in administrative dissolution or revocation on the fourth Friday in September.
- **How to prove it**:
  - [tier 1, settles it] Search the entity on Sunbiz by name or document number and read the Annual Reports table, which lists Report Year and Filed Date, plus the Status field. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 1, settles it] Open the free PDF image of the filed annual report from the entity detail page. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 2, settles it] Log in to the Sunbiz e-filing account and review the entity's filing history. https://services.sunbiz.org/
  - [tier 5, corroborating only] Look for a payment to 'Florida Department of State' in the first four months of the year.
- **Fix**:
  1. Look up the entity on Sunbiz and read the Status field and the Annual Reports table.
  2. File the annual report through Sunbiz and pay the fee, adding the $400 late fee if filing after May 1.
  3. If the entity was administratively dissolved or revoked, file for reinstatement with the Division of Corporations. The reinstatement fee depends on entity type; for a Florida profit corporation it is $600 under section 607.0122(13). Confirm the amount for your entity type on the Division of Corporations fee schedule before paying.
- **Source**: https://dos.fl.gov/sunbiz/manage-business/efile/annual-report/ (verified 2026-08-14)
- **Note**: Filing window, fees, the $400 late fee and the administrative dissolution timing are stated on the cited Division of Corporations page.

### Florida corporate income tax (Form F-1120) `fl-corporate-income-tax`
Applies to: c-corp, benefit-corp | category: tax
Florida has no personal income tax but it does tax corporate net income at 5.5%. The first $50,000 of net income is exempt, so small C corporations often owe nothing while still having to file. Florida's constitution caps the rate on non natural persons at 5% of net income except where the legislature votes a higher rate by a three fifths majority, which it has.
- **Deadline**: Returns are due the later of: the 1st day of the 5th month after the close of the taxable year, or the 15th day after the due date without extension for the related federal return. For a taxable year ending June 30 the return is due the 1st day of the 4th month, not the 5th. Extensions run 6 months, except for a June 30 year end, where the Department of Revenue grants 7. An extension is not an extension to pay.
- **Rule out first**:
  - Net income was at or below the $50,000 exemption, so the return shows zero tax and there is no payment to find. (common) Check: Read the net income and exemption lines on the filed F-1120.
  - The entity is an S corporation, partnership or disregarded single member LLC, so its income passes through and it is not subject to the corporate income tax in the ordinary case. (common) Check: Confirm the federal tax classification for the year before expecting an F-1120.
  - The return is on extension, which can run up to 6 months in the aggregate. (common) Check: Check the Department of Revenue account for a filed extension and an extension payment.
  - Only one exemption is allowed across a controlled group, so a subsidiary legitimately shows no exemption of its own. (occasional) Check: Review the group's allocation of the single $50,000 exemption under section 220.14(4).
- **How to prove it**:
  - [tier 1, corroborating only] Confirm the entity is active on Sunbiz, since a dissolved entity may explain a filing gap. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 2, settles it] Log in to the Florida Department of Revenue eServices account and review corporate income tax filings and balances.
  - [tier 4, settles it] Obtain the filed Florida Form F-1120 for the year and confirm the net income and exemption lines.
  - [tier 5, corroborating only] Look for Florida Department of Revenue estimated tax payments during the year.
- **Fix**:
  1. Confirm the entity's federal tax classification, since only entities taxed as corporations file the F-1120.
  2. Determine the due date from the taxable year end using the 1st day of the 5th month rule and the federal due date comparison.
  3. File Form F-1120 and pay any balance; note the extension is an extension to file, not to pay.
- **Source**: https://www.flsenate.gov/Laws/Statutes/2024/220.11 (verified 2026-08-14)
- **Note**: The 5.5% rate is section 220.11(2)(a). The $50,000 exemption and the controlled group limit are section 220.14, https://www.flsenate.gov/Laws/Statutes/2024/220.14. The due date and the 6 month aggregate extension are section 220.222, https://www.flsenate.gov/Laws/Statutes/2024/220.222. Section 220.1105 provides an automatic rate adjustment mechanism, but its adjustment window covers only fiscal years 2018-2019 through 2020-2021, so the statutory 5.5% governs. Corrected 2026-08-14 for how the Department of Revenue actually administers the due date: its corporate income tax page, https://floridarevenue.com/taxes/taxesfees/Pages/corporate.aspx, fetched 2026-08-14, states that for tax years ending June 30 the return is due the 1st day of the 4th month following the close of the tax year, and that extensions are valid for 6 months with the exception of June 30 year ends, which get 7. The rate table on the same page confirms 5.5% for taxable years beginning on or after 1/1/2022, so 5.5% is the 2026 rate. floridarevenue.com is the Department of Revenue site but is not a .gov domain, so source_url stays on flsenate.gov.

### Florida registered agent `fl-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, benefit-corp, nonprofit, partnership | category: registered-agent
Florida entities must name and maintain a registered agent with a Florida street address. The agent's name and address are public on Sunbiz. If the agent changes, you can report it on the annual report instead of filing a separate change document, which is a small saving worth knowing.
- **Deadline**: Designated at formation or qualification and maintained continuously. A change reported on the annual report is treated as a statement of change under section 607.0502 or 607.1508 for corporations, or section 605.0114 for LLCs.
- **Cost**: Designation of and acceptance by registered agent for a corporation: $35. Statement of change of registered agent or registered office for a corporation, if not included on the annual report: $35. For an LLC the registered agent designation is $25 as part of the $125 total to file Articles of Organization.
- **Rule out first**:
  - An officer or the founder serves as the registered agent at a Florida address, so there is no vendor invoice. (common) Check: Read the Registered Agent Name on Sunbiz; an individual name is normal and compliant.
  - The agent was changed on the annual report rather than by a separate $35 filing, so no standalone change document appears in the filing history. (common) Check: Compare the Name Changed date on the agent block with the annual report filed dates.
  - A national provider handles the agent role as part of a bundled multi state package. (common) Check: Check the provider portal and confirm the agent name on Sunbiz.
- **How to prove it**:
  - [tier 1, settles it] Open the entity on Sunbiz and read the 'Registered Agent Name & Address' block, including the Name Changed and Address Changed dates. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 1, settles it] Search Sunbiz by Registered Agent Name to find every entity an agent covers. https://search.sunbiz.org/Inquiry/CorporationSearch/ByOfficerRegisteredAgentName
  - [tier 4, settles it] Read the registered agent block on the PDF image of the most recent annual report, available free from Sunbiz. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 5, corroborating only] Look for a recurring annual subscription to a commercial registered agent provider.
- **Fix**:
  1. Open the entity on Sunbiz and read the registered agent name, address and change dates.
  2. If the agent has resigned or the address is stale, update it on the next annual report, or file a standalone change for $35 if you cannot wait.
  3. Confirm the agent address is a Florida street address, since state notices and service of process go there.
- **Source**: https://www.flsenate.gov/Laws/Statutes/2024/607.1622 (verified 2026-08-14)
- **Note**: The rule that a differing registered agent on the annual report counts as a statement of change is section 607.1622(2) for corporations and section 605.0212(5) for LLCs. Corporation fees are section 607.0122(4) and (5), https://www.flsenate.gov/Laws/Statutes/2024/607.0122. The LLC $25 registered agent component of the $125 Articles of Organization total is from https://dos.fl.gov/sunbiz/forms/fees/.

### Florida foreign corporation certificate of authority `fl-foreign-qualification-corporation`
Applies to: c-corp, s-corp, benefit-corp, nonprofit | category: entity
A corporation formed outside Florida may not transact business in Florida until it obtains a certificate of authority from the Department of State. Florida's statute lists a long set of activities that do not count as transacting business, including selling through independent contractors and soliciting orders that require acceptance outside the state.
- **Deadline**: Before transacting business in Florida.
- **Cost**: $70.00 total: $35.00 filing fee plus $35.00 registered agent designation. The statutory filing fee for an application for certificate of authority by a foreign corporation is $35 under section 607.0122(14).
- **Rule out first**:
  - The company's Florida contacts fall inside the section 607.1501(2) safe list, for example only bank accounts, only independent contractor sales, or only order solicitation accepted out of state. (common) Check: Test the actual Florida activity against the section 607.1501(2) list before concluding qualification was required.
  - The entity qualified under a modified name because its true name was unavailable in Florida. (occasional) Check: Search Sunbiz by FEI/EIN and by name variants, not just the trading name.
  - Counsel or a formation agent filed and paid the qualification. (common) Check: Search Sunbiz for the entity record, which exists regardless of who paid.
- **If it genuinely was missed**: A foreign corporation that fails to file its annual report may not prosecute or maintain any action in any Florida court until the report is filed and all fees and penalties are paid, and is subject to cancellation of its certificate of authority.
- **How to prove it**:
  - [tier 1, settles it] Search the corporation on Sunbiz; a qualified foreign corporation carries an 'F' prefixed document number and its detail page shows the state of incorporation and the date it qualified in Florida. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 1, settles it] Search Sunbiz by FEI/EIN to catch entities registered under a name variant. https://search.sunbiz.org/Inquiry/CorporationSearch/ByFeiNumber
  - [tier 4, settles it] Obtain the filed application for certificate of authority and the certificate itself.
  - [tier 5, corroborating only] Look for a $70 payment to the Florida Department of State around the time Florida activity began.
- **Fix**:
  1. Search Sunbiz by name, by FEI/EIN and by document number to confirm whether a Florida registration exists.
  2. If qualification is required, file the application for certificate of authority with the $70 total fee.
  3. Expect the January 1 to May 1 annual report cycle to start once qualified.
- **Source**: https://www.flsenate.gov/Laws/Statutes/2024/607.1501 (verified 2026-08-14)
- **Note**: The prohibition on transacting business without a certificate of authority and the list of activities that do not constitute transacting business are section 607.1501. The $35 statutory fee is section 607.0122(14), https://www.flsenate.gov/Laws/Statutes/2024/607.0122. The $70 combined total including the $35 registered agent designation is from https://dos.fl.gov/sunbiz/forms/fees/. The litigation bar and cancellation consequence are section 607.1622(6).

### Florida foreign LLC registration `fl-foreign-qualification-llc`
Applies to: llc, llc-single-member | category: entity
An LLC formed outside Florida registers with the Division of Corporations before transacting business in Florida. Registering starts the January 1 to May 1 annual report cycle, with the $400 late fee attached if you miss it.
- **Deadline**: Before transacting business in Florida.
- **Cost**: $125.00 total: $100.00 filing fee plus $25.00 registered agent designation.
- **Rule out first**:
  - The LLC only sells remotely into Florida and does not transact business there, so no registration is required. (common) Check: Assess actual Florida activity, and separately test the $100,000 sales tax economic nexus rule, which is a different question.
  - The LLC registered under a modified name. (occasional) Check: Search Sunbiz by FEI/EIN and name variants.
  - An employer of record handles Florida staff, which does not by itself create an LLC registration record. (occasional) Check: Confirm whether the LLC itself has Florida activity beyond the employment arrangement.
- **If it genuinely was missed**: An LLC that fails to file its annual report may not maintain or defend any action in a Florida court until the report is filed and all fees and penalties are paid, and is subject to cancellation of its certificate of authority.
- **How to prove it**:
  - [tier 1, settles it] Search the LLC on Sunbiz; a registered foreign LLC carries an 'M' or 'F' style document number and its detail page shows the jurisdiction of formation and the Florida qualification date. https://search.sunbiz.org/Inquiry/CorporationSearch/ByName
  - [tier 1, settles it] Search Sunbiz by FEI/EIN to catch name variants. https://search.sunbiz.org/Inquiry/CorporationSearch/ByFeiNumber
  - [tier 4, settles it] Obtain the filed application by foreign LLC for authorization to transact business in Florida.
  - [tier 5, corroborating only] Look for a $125 payment to the Florida Department of State.
- **Fix**:
  1. Search Sunbiz by name and FEI/EIN to confirm whether a Florida registration exists.
  2. File the foreign LLC application with the $125 total fee if registration is required.
  3. Diary the January 1 to May 1 annual report window, since the $400 late fee applies to LLCs.
- **Source**: https://dos.fl.gov/sunbiz/forms/fees/ (verified 2026-08-14)
- **Note**: The $100 filing fee plus $25 registered agent fee, totalling $125, is stated on the cited Division of Corporations fee page. The litigation bar and cancellation consequence are Florida Statutes section 605.0212(6), https://www.flsenate.gov/Laws/Statutes/2024/605.0212.

### Florida reemployment tax registration `fl-reemployment-tax-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
Florida calls its state unemployment tax reemployment tax. You become a liable employer once you pay at least $1,500 in wages in a calendar quarter, or once you have employed at least one person for any part of a day in each of 20 different calendar weeks in a year. The 20 weeks do not have to be consecutive. The headcount test is different for a 501(c)(3) nonprofit, which is liable at four or more employees across those 20 weeks rather than one, and different again in agriculture, at five or more workers across 20 weeks or a $10,000 cash payroll in a quarter.
- **Deadline**: Register by the end of the month following the calendar quarter in which you become an employer. Example given by the Department of Revenue: start the business in January and cross $1,500 in wages by the end of March, and registration is due by the end of April.
- **Rule out first**:
  - A PEO or employer of record reports Florida wages under its own reemployment tax account, so the company has no RT account of its own. (common) Check: Ask the PEO which account the wages are reported under and reconcile headcount to their filings.
  - Neither threshold has been crossed: quarterly wages stayed under $1,500 and no employee has worked in 20 different calendar weeks. (common) Check: Total wages by calendar quarter and count distinct calendar weeks with at least one employee across both the current and preceding calendar year.
  - Only domestic service workers are employed, which is tested under a separate rule and is excluded from the general threshold computation. (rare) Check: Apply the domestic service rules in section 443.1215(1)(d)2. and 443.1215(2)(a) rather than the general test.
  - Workers are genuine independent contractors, so no wages in employment were paid. (occasional) Check: Test worker classification before accepting this.
- **How to prove it**:
  - [tier 2, settles it] Log in to the Florida Department of Revenue eServices reemployment tax account and confirm an active RT account number and filed RT-6 quarterly reports.
  - [tier 3, corroborating only] Check the payroll provider for the Florida RT account number and the SUTA rate on file.
  - [tier 4, settles it] Obtain the filed RT-6 Employer's Quarterly Report and the annual reemployment tax rate notice.
  - [tier 5, corroborating only] Look for quarterly Florida Department of Revenue debits after each calendar quarter.
- **Fix**:
  1. Identify the exact quarter or week in which liability was triggered under section 443.1215(1)(a).
  2. Register for a Florida reemployment tax account with the Department of Revenue.
  3. Backfile any missing RT-6 quarterly reports and pay contributions due.
- **Source**: https://www.flsenate.gov/Laws/Statutes/2024/443.1215 (verified 2026-08-14)
- **Note**: The $1,500 quarterly wage test, the 20 different calendar weeks test and the domestic and agricultural carve outs are quoted from section 443.1215. Corrected 2026-08-14 on two counts, both from the Department of Revenue reemployment tax page, https://floridarevenue.com/taxes/taxesfees/Pages/reemployment.aspx, fetched 2026-08-14. First, the registration deadline is not unknown: the page states 'Register with the Department by the end of the month following the calendar quarter in which you become an employer.' Second, the one-employee-for-20-weeks test was overstated for the nonprofit entity type carried on this row; the same page states the test for a 501(c)(3) nonprofit is 'four or more employees for a day (or portion of a day) during any 20 weeks in a calendar year', and for agriculture 'five or more workers ... during any 20 weeks in a calendar year, or a $10,000 cash payroll in any calendar quarter'. In the statute those sit in section 443.1216(3) and (5) rather than in 443.1215 itself. floridarevenue.com is the Department of Revenue site but is not a .gov domain, so source_url stays on flsenate.gov.

### Florida workers' compensation insurance (four employee threshold, one in construction) `fl-workers-compensation`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
Florida ties the workers' compensation requirement to headcount, and the threshold depends on your industry. Ordinary businesses are covered once they have four or more employees. Construction is far stricter: one employee triggers it. Agriculture has its own carve out based on regular and seasonal worker counts.
- **Deadline**: Coverage must be in force once the applicable employee threshold is met, and maintained continuously.
- **Rule out first**:
  - The employer has three or fewer employees and is not in construction, so no coverage is required at all. (common) Check: Count employees against the four employee threshold, and confirm the industry is not construction, where one employee triggers the requirement.
  - Corporate officers or LLC members have filed exemption certificates, so the countable employee number is lower than the headcount suggests. (common) Check: Pull the filed exemption certificates and recount only non exempt employees.
  - A PEO or employer of record provides coverage under its master policy, so no policy exists in the company's own name. (common) Check: Ask the PEO for a certificate of insurance covering the Florida employees.
  - The workers are agricultural labor within the section 440.02(20)(c)2. exclusion, or domestic servants in private homes. (occasional) Check: Test the workforce against the specific regular and seasonal counts in the statute, which are 5 or fewer regular and fewer than 12 seasonal at one time.
- **How to prove it**:
  - [tier 1, settles it] Search the employer in the Florida Division of Workers' Compensation Proof of Coverage database to confirm an active policy. https://www.myfloridacfo.com/division/wc/
  - [tier 4, settles it] Obtain the workers' compensation policy declarations page showing the named insured, Florida coverage and policy period.
  - [tier 4, settles it] Obtain any filed exemption certificates for officers or LLC members, which reduce the countable employee number.
  - [tier 5, corroborating only] Look for workers' compensation premium payments or a pay as you go deduction on each payroll run.
- **Fix**:
  1. Count Florida employees and determine whether the four employee threshold or the one employee construction threshold applies.
  2. Confirm coverage in the Division of Workers' Compensation Proof of Coverage database and pull the declarations page.
  3. If in construction, bind coverage from the first employee, since there is no small employer grace in that industry.
- **Source**: https://www.flsenate.gov/Laws/Statutes/2024/440.02 (verified 2026-08-14)
- **Note**: All thresholds are quoted from Florida Statutes section 440.02(20)(b)2. and 440.02(20)(c). The Proof of Coverage database URL in the evidence list is on myfloridacfo.com, which is not a .gov domain; it is listed as an actionable lookup, not as the source of the rule.

### Florida sales and use tax registration (certificate of registration) `fl-sales-tax-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
Before you can operate as a dealer in Florida you have to register with the Department of Revenue and get a certificate of registration, and you need a separate certificate for each place of business. The certificate must be displayed at the business, it cannot be transferred to anyone else, and you cannot get a local business licence without it.
- **Deadline**: The application must be submitted to the department before the person, firm, copartnership or corporation may engage in such business.
- **Rule out first**:
  - The business sells only services or items outside the taxable base, so it is not a dealer and needs no certificate. (common) Check: Test the specific revenue streams against the chapter 212 taxable base, including commercial rent and admissions which catch people out.
  - All Florida sales run through a marketplace provider that is the dealer for those sales. (common) Check: Confirm the marketplace is registered and collecting, and check whether the seller has any direct sales outside the marketplace.
  - Multiple certificates exist because a separate one is issued for each place of business, so a single location lookup can miss the others. (occasional) Check: Check every Florida location, since section 212.18(3)(b) issues a separate certificate per place of business.
  - The business is a remote seller under the $100,000 threshold and has no Florida presence. (common) Check: Total Florida taxable remote sales for the previous calendar year against the $100,000 figure in section 212.0596.
- **How to prove it**:
  - [tier 1, settles it] Verify the certificate number in the Florida Department of Revenue's Certificate/Resale Authorization verification tool.
  - [tier 2, settles it] Log in to the Department of Revenue eServices account and confirm an active sales and use tax certificate and the DR-15 filing history.
  - [tier 4, settles it] Inspect the certificate of registration displayed at the place of business, which the statute requires to be posted conspicuously.
  - [tier 5, corroborating only] Look for Florida Department of Revenue remittances on the monthly or quarterly cycle.
- **Fix**:
  1. Determine whether the business is a dealer under chapter 212 for each revenue stream.
  2. Apply to the Florida Department of Revenue for a certificate of registration for each place of business before engaging in business.
  3. Display the certificate at each location and begin filing the DR-15 on the assigned cycle.
- **Source**: https://www.flsenate.gov/Laws/Statutes/2024/212.18 (verified 2026-08-14)
- **Note**: The registration requirement, the per place of business certificate, the display requirement, the non assignability and the bar on obtaining a local licence without a valid certificate are all quoted from section 212.18(3). The Florida Department of Revenue publishes its guidance on floridarevenue.com, which is not a .gov domain, so it is not cited as the source here. The rule stated is taken from the Florida Statutes on flsenate.gov, which is a .gov domain and was actually fetched.

### Florida remote seller economic nexus ($100,000) `fl-sales-tax-economic-nexus`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
An out of state seller with no Florida presence becomes a Florida dealer once its taxable remote sales into Florida exceed $100,000. Florida measures this on the previous calendar year, and unlike some states it uses a pure dollar test with no transaction count.
- **Deadline**: A person making a substantial number of remote sales is a dealer. The threshold is measured against the previous calendar year.
- **Rule out first**:
  - Previous calendar year Florida taxable remote sales were $100,000 or less, so no registration is required. (common) Check: Total the sales prices of taxable remote sales into Florida for the previous calendar year specifically, not a trailing twelve months.
  - The sales are facilitated by a marketplace provider, which is separately made responsible under section 212.05965, so the seller has no direct obligation for those transactions. (common) Check: Split marketplace facilitated sales from direct sales and test only the direct sales against the threshold.
  - The seller sells only services or intangibles, which are outside the remote sale definition that covers tangible personal property. (occasional) Check: Confirm the products are not tangible personal property under the section 212.0596(1)(a) definition.
  - The threshold was crossed only in the current year, so the previous calendar year test has not yet been met. (occasional) Check: Apply the previous calendar year measurement in section 212.0596(1)(b) rather than a current year running total.
- **How to prove it**:
  - [tier 2, settles it] Check the Florida Department of Revenue eServices account for an active registration and the DR-15 filing history.
  - [tier 3, corroborating only] Check the tax automation provider's nexus dashboard for Florida and confirm the threshold calculation matches a previous calendar year basis.
  - [tier 4, settles it] Pull a Florida destination sales report by calendar year from the billing or commerce system and compare the total sales price to $100,000.
  - [tier 5, corroborating only] Look for Florida Department of Revenue remittances.
- **Fix**:
  1. Total taxable remote sales into Florida for the previous calendar year and compare to $100,000.
  2. If exceeded, register with the Florida Department of Revenue as a dealer and begin collecting.
  3. Separate marketplace facilitated sales from direct sales, since the marketplace provider carries its own obligation under section 212.05965.
- **Source**: https://www.flsenate.gov/Laws/Statutes/2024/212.0596 (verified 2026-08-14)
- **Note**: The $100,000 figure, the previous calendar year measurement and the absence of a transaction count test are quoted from section 212.0596(1)(b) and (2). The Florida Department of Revenue publishes its guidance on floridarevenue.com, which is not a .gov domain, so it is not cited as the source here. The rule stated is taken from the Florida Statutes on flsenate.gov, which is a .gov domain and was actually fetched.

### Florida state income tax withholding (none) `fl-state-income-tax-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Florida's constitution bars the state from taxing the income of natural persons who are residents or citizens beyond what is creditable against federal tax, which in practice means there is no Florida personal income tax. So there is no state withholding account to open. You still register for reemployment tax and handle federal withholding.
- **Deadline**: Not applicable.
- **Rule out first**:
  - There is no Florida withholding account number because none exists. An empty field in a payroll system is correct, not a gap. (common) Check: Confirm instead that a Florida reemployment tax account exists, which is the state registration Florida employers actually need.
  - An employee lives in a state that does tax income, so withholding appears for that state and not for Florida. (occasional) Check: Check the employee's work and residence state and the corresponding state registrations.
- **How to prove it**:
  - [tier 1, settles it] Read Florida Constitution Article VII, Section 5(a), which bars a state tax on the income of natural persons beyond the federal credit amount. https://www.flsenate.gov/Laws/Constitution
  - [tier 2, settles it] Confirm the payroll provider has no Florida state income tax withholding account configured, because none exists.
  - [tier 4, settles it] Review Florida employee payslips and confirm no state income tax line is withheld.
- **Fix**:
  1. Do not attempt to register for Florida state income tax withholding; there is no such account.
  2. Confirm the Florida reemployment tax account exists and quarterly RT-6 reports are being filed.
  3. Confirm federal withholding and deposits are handled correctly.
- **Source**: https://www.flsenate.gov/Laws/Constitution (verified 2026-08-14)
- **Note**: Florida Constitution Article VII, Section 5(a) NATURAL PERSONS: 'No tax upon estates or inheritances or upon the income of natural persons who are residents or citizens of the state shall be levied by the state, or under its authority, in excess of the aggregate of amounts which may be allowed to be credited upon or deducted from any similar tax levied by the United States or any state.' Section 5(b) caps the rate on non natural persons at 5% of net income except at a greater rate authorized by a three fifths vote of each house, which is the constitutional basis for the 5.5% corporate rate in section 220.11.


## PA (11)

### Pennsylvania Annual Report (DSCB:15-146) `pa-annual-report`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
Pennsylvania now requires nearly every registered business to file an Annual Report with the Department of State. This is new as of 2025 and replaced the old once-per-decade decennial report, so founders who formed before 2025 often do not know it exists. The report confirms your entity name, registered office address, and principal officers.
- **Deadline**: Business and nonprofit corporations file January 1 to June 30. LLCs file January 1 to September 30. LPs, LLPs, business trusts and professional associations file January 1 to December 31. The first report is due the calendar year after formation in PA or after initial foreign registration.
- **Cost**: $7 for business corporations, LLCs, LPs and LLPs; $0 for nonprofit corporations and for LPs or LLCs with a not-for-profit purpose
- **Rule out first**:
  - The entity was formed or registered this calendar year, so its first Annual Report is not due until next year. (common) Check: Compare the formation or foreign registration date on the SOS record against the current year.
  - A nonprofit filed at the $0 fee, so no payment trace exists even though the report was filed on time. (occasional) Check: Check the filing history on the SOS record rather than looking for a bank debit.
  - The filing window for this entity type has not opened or closed yet, so absence mid-year is expected. (common) Check: Match the entity type to its window (corporations June 30, LLCs September 30, others December 31).
- **If it genuinely was missed**: Beginning with reports due in 2027, failure to file leads to administrative dissolution, termination or cancellation six months after the due date, and the entity name becomes available to any other filing association.
- **How to prove it**:
  - [tier 1, settles it] Search the entity by name or entity number at file.dos.pa.gov and open the filing history to confirm an Annual Report is recorded for the current year. https://file.dos.pa.gov/
  - [tier 2, settles it] Log into the PA Business Filing Services account used for the entity and review filed documents and receipts. https://file.dos.pa.gov/
  - [tier 5, corroborating only] Look for a $7 card or bank debit to the Pennsylvania Department of State during the filing window.
- **Fix**:
  1. Look up the entity at file.dos.pa.gov and confirm the most recent Annual Report year on record
  2. File the missing Annual Report online through Business Filing Services and pay the $7 fee
  3. If the entity was already administratively dissolved for non-filing, file for reinstatement and bring all reports current
- **Source**: https://www.pa.gov/agencies/dos/programs/business/types-of-filings-and-registrations/annual-reports (verified 2026-08-14)

### Pennsylvania Certificate of Annual Registration (LLPs, LLLPs, restricted professional companies) `pa-certificate-annual-registration`
Applies to: llc, llc-single-member, partnership | category: information-report
Pennsylvania charges a separate per-member annual registration on limited liability partnerships, limited liability limited partnerships, and restricted professional companies such as professional LLCs. This is completely separate from the $7 Annual Report and is far more expensive. Licensed professional firms are the ones that get caught by it.
- **Deadline**: On or before April 15 of each year following the year being reported.
- **Cost**: Restricted professional companies pay $700 times the number of members as of December 31 of the reported year. LLPs and LLLPs pay $470 times the number of general partners as of December 31 of the reported year. Only members or partners licensed to practice and with a principal residence in Pennsylvania are counted.
- **Rule out first**:
  - The entity is an ordinary LLC rather than a restricted professional company, so this filing never applied to it. (common) Check: Check the entity's registration type on the SOS record and whether the members hold professional licenses.
  - No members or partners have a Pennsylvania principal residence, so the counted headcount is zero. (occasional) Check: Review the residency of each licensed member against the counting rule on the filing instructions.
- **If it genuinely was missed**: A $500 penalty is assessed if not filed by May 15, and it becomes a lien on the entity's assets.
- **How to prove it**:
  - [tier 1, settles it] Search the entity at file.dos.pa.gov and confirm whether a Certificate of Annual Registration is on file for the reporting year. https://file.dos.pa.gov/
  - [tier 4, settles it] Obtain the filed Certificate of Annual Registration and confirm the member or partner count used matches the December 31 headcount.
  - [tier 5, corroborating only] Look for a payment to the PA Department of State that is a round multiple of $700 or $470 around April.
- **Fix**:
  1. Determine whether the entity is an LLP, LLLP or restricted professional company
  2. Count the licensed members or general partners resident in Pennsylvania as of December 31
  3. File the Certificate of Annual Registration and pay the per-member fee before April 15 to avoid the $500 penalty
- **Source**: https://www.pa.gov/agencies/dos/programs/business/types-of-filings-and-registrations/certificates-of-annual-registration (verified 2026-08-14)
- **Note**: Verified on the Department of State page for the registration filed in 2026 covering reporting year 2025. Both the RPC and the LLP or LLLP lines use the same December 31 reference date of the reported year, so an earlier note claiming the page mixed those dates was wrong. RPC members are counted only where they were licensed to practice the professional service on December 31 and had a principal residence in Pennsylvania on December 31. LLP and LLLP general partners are counted where a natural person had a Pennsylvania principal residence on December 31, or where an entity partner was organized under Pennsylvania law on December 31.

### Pennsylvania registered office address `pa-registered-office`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
Pennsylvania does not use the registered agent model that most states use. Instead your entity must keep a registered office address in Pennsylvania where service of process can be delivered. You may instead use a Commercial Registered Office Provider, but that is an option rather than a requirement.
- **Deadline**: Must be maintained continuously from formation or foreign registration, and updated whenever the address changes.
- **Cost**: $5 to file a change of registered office
- **Rule out first**:
  - The founder uses their own Pennsylvania business address as the registered office, so there is no provider invoice to find. (common) Check: Compare the registered office address on the SOS record to the company's own premises.
  - A Commercial Registered Office Provider is named on the record instead of a street address, which is permitted. (occasional) Check: Confirm the CROP name appears on the SOS record and the provider account is current.
- **How to prove it**:
  - [tier 1, settles it] Search the entity at file.dos.pa.gov and read the registered office address shown on the record. https://file.dos.pa.gov/
  - [tier 3, corroborating only] If a Commercial Registered Office Provider is used, confirm the account is active and paid in that provider's portal.
  - [tier 5, corroborating only] Look for a recurring annual charge from a registered office provider.
- **Fix**:
  1. Pull the entity record at file.dos.pa.gov and verify the registered office address is current and in Pennsylvania
  2. File a change of registered office for $5 if the address is stale
  3. Engage a Commercial Registered Office Provider if the company has no physical Pennsylvania address
- **Source**: https://www.pa.gov/agencies/dos/resources/business-resources/frequently-asked-questions (verified 2026-08-14)
- **Note**: Confirmed at the Department of State FAQ: 'Pennsylvania does not use registered agents' and 'Our records indicate a registered office address.' A Pennsylvania address is required, and per the same FAQ 'the only entities not required to have a Pennsylvania address are trademarks and fictitious names.' REFINED 2026-08-14 after running live searches at file.dos.pa.gov: the public record carries one field labelled Registered Office, and it prints EITHER a street address OR a Commercial Registered Office Provider's company name. Comcast Corporation and one Hershey record both show 'Corporation Service Company' or 'CT Corporation System' with no street, while a non-CROP Hershey record shows a real street address. Pennsylvania's own filing-history data also contains a field named 'Registered Agent Physical Address 1', so do not tell a client Pennsylvania has no concept of an agent; tell them the record has one field that can hold either thing.

### Pennsylvania Foreign Registration Statement `pa-foreign-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An entity formed outside Pennsylvania must register with the Department of State before doing business in the state. You file a Foreign Registration Statement together with a docketing statement. Foreign corporations also have to publish notice in two newspapers.
- **Deadline**: Before the entity begins doing business in Pennsylvania.
- **Cost**: $250 for the Foreign Registration Statement
- **Rule out first**:
  - The company's Pennsylvania contact is limited enough that it is not doing business there and no registration is required. (common) Check: Test for a physical location, PA employees, or repeated in-state contracting rather than isolated sales.
  - The entity registered under a slightly different or assumed name because its true name was unavailable in Pennsylvania. (occasional) Check: Search the SOS registry by officer or by the entity's home-state name variants.
- **How to prove it**:
  - [tier 1, settles it] Search the entity name at file.dos.pa.gov and confirm a foreign registration record exists with an active status. https://file.dos.pa.gov/
  - [tier 4, settles it] Obtain the filed Foreign Registration Statement (DSCB:15-412) and the docketing statement acknowledgment.
  - [tier 5, corroborating only] Look for a $250 payment to the Pennsylvania Department of State.
- **Fix**:
  1. Determine whether Pennsylvania activity rises to doing business
  2. File the Foreign Registration Statement (DSCB:15-412) and docketing statement (DSCB:15-134A) with the $250 fee
  3. Complete the newspaper advertising requirement if the entity is a foreign corporation
- **Source**: https://www.pa.gov/agencies/dos/programs/business/fees-and-payments (verified 2026-08-14)
- **Note**: Requirement and forms confirmed at the Department of State foreign associations page; the $250 fee confirmed on the fee schedule.

### Pennsylvania Corporate Net Income Tax `pa-corporate-net-income-tax`
Applies to: c-corp, benefit-corp | category: tax
Pennsylvania taxes the net income of C corporations doing business in the state. The rate is on a legislated multi-year decline, so the rate that applies depends on the tax year you are filing. Benefit corporations are taxed as ordinary business corporations.
- **Deadline**: Annual corporate tax report, with the rate set by tax year.
- **Rule out first**:
  - The entity is an S corporation, LLC or partnership, so it owes no corporate net income tax and income flows to the owners instead. (common) Check: Confirm the federal tax classification on the most recent federal return.
  - The corporation had a loss year, so tax due was zero even though the return was filed. (common) Check: Read the filed return for the year rather than looking for a payment.
- **How to prove it**:
  - [tier 2, settles it] Log into myPATH and confirm the corporate net income tax account is registered and returns are filed for each year. https://mypath.pa.gov/
  - [tier 4, settles it] Review the filed RCT-101 or the current PA corporate tax report and the federal return it ties to.
  - [tier 5, corroborating only] Look for estimated tax payments to the PA Department of Revenue during the year.
- **Fix**:
  1. Confirm the entity's federal tax classification
  2. Register for corporate net income tax in myPATH if not already registered
  3. File the outstanding corporate tax reports using the rate in force for each tax year
- **Source**: https://www.pa.gov/agencies/revenue/resources/tax-rates.html (verified 2026-08-14)
- **Note**: Department of Revenue rate page states 7.99 percent for 2025 and 7.49 percent for 2026, declining annually to 4.99 percent by 2031. Confirm the rate for the specific tax year being filed.

### Pennsylvania Personal Income Tax on pass-through income `pa-personal-income-tax-passthrough`
Applies to: s-corp, llc, llc-single-member, partnership | category: tax
Pennsylvania taxes pass-through business income at the flat personal income tax rate in the owners' hands. S corporations, LLCs and partnerships generally do not pay entity-level net income tax, but they do have filing obligations and their owners owe PA personal income tax on their share.
- **Deadline**: Annual, aligned with the Pennsylvania personal income tax return cycle.
- **Rule out first**:
  - A single-member LLC is disregarded, so its activity is reported on the owner's own return and there is no separate entity filing to find. (common) Check: Confirm the LLC has not elected corporate treatment, then look at the owner's PA-40 Schedule C.
  - The entity has no Pennsylvania-sourced income and no PA-resident owners, so nothing is owed. (occasional) Check: Review the apportionment and the residency of each owner.
- **How to prove it**:
  - [tier 2, settles it] Log into myPATH and review the entity's registered tax accounts and filed pass-through returns. https://mypath.pa.gov/
  - [tier 4, settles it] Review the PA-20S/PA-65 information return and the RK-1 or NRK-1 schedules issued to owners.
  - [tier 5, corroborating only] Look for owner-level estimated payments to the PA Department of Revenue.
- **Fix**:
  1. Confirm the entity's federal classification and whether it is disregarded
  2. File the PA-20S/PA-65 and issue RK-1 or NRK-1 schedules to owners
  3. Ensure owners report their share and make estimated payments as needed
- **Source**: https://www.pa.gov/agencies/revenue/resources/tax-rates.html (verified 2026-08-14)
- **Note**: Personal income tax rate confirmed at 3.07 percent on the Department of Revenue rate page.

### Pennsylvania employer withholding registration `pa-employer-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
If you pay anyone wages in Pennsylvania you must register as an employer and withhold Pennsylvania personal income tax at a flat rate from both resident and nonresident employees. The registration clock runs from the first wage payment rather than ahead of it, and there is no dollar threshold. You register through myPATH and you need your federal EIN first. Your deposit frequency depends on how much you withhold.
- **Deadline**: Register within 10 business days of the first payment of wages, not before the first payroll. Deposit frequency is set by expected quarterly withholding: quarterly under $300, monthly for $300 or more but less than $1,000, semi-monthly for $1,000 or more but less than $5,000, and semi-weekly at $5,000 or more per quarter or $20,000 or more per calendar year.
- **Rule out first**:
  - Everyone paid is a genuine 1099 contractor rather than an employee, so no withholding account is required. (common) Check: Test the workers against employee classification factors and review the 1099-NEC filings.
  - A payroll provider registered the account under its own filing arrangement, so the founder never saw the registration. (common) Check: Ask the payroll provider for the PA withholding account number and confirm it in myPATH.
  - The company has employees but none work in or reside in Pennsylvania. (occasional) Check: Review the work location and residence of each employee.
- **How to prove it**:
  - [tier 2, settles it] Log into myPATH and confirm an active employer withholding account number plus filed quarterly returns and W-2 transmittals. https://mypath.pa.gov/
  - [tier 3, corroborating only] Check the payroll provider's tax service dashboard for the registered PA withholding ID and its filing status.
  - [tier 4, settles it] Review payroll registers and filed PA W-3 reconciliations against amounts actually remitted.
  - [tier 5, corroborating only] Look for recurring withholding remittances to the PA Department of Revenue on the bank statement.
- **Fix**:
  1. Obtain a federal EIN if the company does not have one
  2. Complete the PA Online Business Tax Registration in myPATH to open an employer withholding account within 10 business days of the first wage payment
  3. File any missing quarterly returns and W-2 reconciliations and remit the tax withheld
- **Source**: https://www.pacodeandbulletin.gov/Display/pacode?file=/secure/pacode/data/061/chapter113/s113.3b.html (verified 2026-08-14)
- **Note**: CORRECTED 2026-08-14. An earlier version said register before the first payroll. 61 Pa. Code 113.3b instead keys registration to the first wage payment: an employer making payment of wages for the first time to a resident individual, or to a nonresident performing services in Pennsylvania, must register within 10 business days of that payment. There is no dollar or wage threshold. The Department's employer withholding web page and REV-415 state no deadline at all, which is how the wrong version survived. Do not cross-apply the separate 30 day Unemployment Compensation registration deadline, which is a different agency and a different rule. The regulation still names Form PA-100; the current administrative path is myPATH. Flat withholding rate is 3.07 percent per REV-415 and https://www.pa.gov/agencies/revenue/resources/tax-rates.html. Deposit bands confirmed in REV-415 at https://www.pa.gov/content/dam/copapwp-pagov/en/revenue/documents/formsandpublications/formsforbusinesses/employerwithholding/documents/rev-415.pdf; the $20,000 per calendar year figure is an alternative semi-weekly trigger, not a standalone annual rule.

### Pennsylvania local Earned Income Tax and Local Services Tax withholding `pa-local-eit-lst`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Pennsylvania is the state that catches out-of-state founders, because local withholding is a separate obligation from state withholding and it is administered per worksite by county Tax Collection District collectors rather than by the state. A home-based employee's residence counts as a worksite, so a single remote hire in Pennsylvania can create a local filing duty. You withhold Earned Income Tax at the higher of the employee's resident rate or the work-location nonresident rate, plus the flat Local Services Tax.
- **Deadline**: EIT is remitted to the worksite Tax Collection District collector within 30 days of the end of each calendar quarter. Monthly filing applies where a single collector covers multiple worksites. LST is deducted each pay period at the worksite.
- **Rule out first**:
  - The employer has no Pennsylvania worksite at all, so there is nothing to withhold locally even though state withholding may apply. (common) Check: Confirm no employee works from a Pennsylvania location, including from home.
  - The payroll provider files EIT and LST under a bulk filer arrangement, so remittances appear under the provider's name rather than the collector's. (common) Check: Ask the provider for copies of the quarterly local returns and the collector receipts.
  - The worksite municipality levies no LST, or the employee is below the low-income exemption, so no LST is deducted. (occasional) Check: Check the Official Tax Register entry for that municipality in the DCED lookup.
- **How to prove it**:
  - [tier 1, settles it] Look up each worksite address in the DCED Municipal Statistics tool to identify the PSD code, EIT rate, LST, and the assigned Tax Collection District collector. https://apps.dced.pa.gov/munstats-public/FindLocalTax.aspx
  - [tier 2, settles it] Log into the applicable TCD collector's employer portal (for example Keystone Collections or Berkheimer) and confirm quarterly EIT and LST returns are filed.
  - [tier 4, settles it] Collect a completed Residency Certification Form for each employee and confirm the resident and nonresident PSD codes and rates used in payroll.
  - [tier 5, corroborating only] Look for quarterly remittances to a local tax collector rather than to the Commonwealth.
- **Fix**:
  1. List every Pennsylvania worksite including home-based employee addresses
  2. Use the DCED Municipal Statistics lookup to get the PSD code, EIT rate, LST and collector for each worksite
  3. Collect a Residency Certification Form from every Pennsylvania employee
  4. Register with the correct Tax Collection District collector and file the missing quarterly EIT and LST returns
- **Source**: https://dced.pa.gov/local-government/local-income-tax-information/ (verified 2026-08-14)
- **Note**: DCED states employers with Pennsylvania worksites must withhold and remit both local EIT and LST. Combined municipal and school district LST is capped at $52 per year per taxpayer regardless of how many political subdivisions the person works in. CORRECTED 2026-08-14: the $12,000 low-income exemption is MANDATORY only where the political subdivision levies the LST at a rate exceeding $10. Where the rate is $10 or less the exemption is permitted rather than required, so do not state it as a flat statewide exemption. The 30 day quarterly remittance rule also has an alternative: a multi-jurisdiction employer may elect to remit to its headquarters tax collection district instead, but only if it files withholdings and wage data electronically on a monthly basis. Detail confirmed at https://dced.pa.gov/local-government/local-income-tax-information/act32-faq/ and https://dced.pa.gov/local-government/local-income-tax-information/local-withholding-tax-faqs/ and https://dced.pa.gov/local-government/local-income-tax-information/local-services-tax/

### Pennsylvania Unemployment Compensation employer registration `pa-unemployment-compensation`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
Pennsylvania has no wage or weeks threshold for unemployment coverage. A single part-time worker makes you a liable employer, which is stricter than most states. Pennsylvania is also unusual in that employees contribute too, through a small withholding from their wages.
- **Deadline**: Register within 30 days after services covered by the UC Law are first performed for the employer.
- **Rule out first**:
  - The company has no employees and pays only genuine independent contractors, so no UC account is required. (common) Check: Test worker classification and confirm only 1099-NEC filings exist.
  - The employer is inside the 30 day registration window after its first covered payroll. (occasional) Check: Compare the first covered payroll date to today.
  - A payroll provider holds the UC registration, so the founder has never seen the account number. (common) Check: Request the PA UC account number and rate notice from the payroll provider.
- **If it genuinely was missed**: A 3 percent Increase for UC Delinquency is added to the tax rate that would otherwise be assigned, and a penalty of up to $10,000 per assessment may apply.
- **How to prove it**:
  - [tier 2, settles it] Log into myPATH or the UC employer system and confirm an active UC account number with quarterly wage reports filed. https://mypath.pa.gov/
  - [tier 3, corroborating only] Check the payroll provider's dashboard for the registered PA UC account number and assigned rate.
  - [tier 4, settles it] Review the annual UC contribution rate notice issued to the employer and the quarterly UC-2 and UC-2A filings.
  - [tier 5, corroborating only] Look for quarterly UC contribution payments to the PA Department of Labor and Industry.
- **Fix**:
  1. Register with the Office of UC Tax Services through myPATH within 30 days of the first covered service
  2. File any missing quarterly UC-2 and UC-2A wage reports
  3. Pay outstanding contributions to stop the 3 percent delinquency rate increase from compounding
- **Source**: https://www.pa.gov/agencies/dli/programs-services/unemployment/for-employers/uc-tax-payment (verified 2026-08-14)
- **Note**: For 2026 the newly liable non-construction contribution rate is .038220 and the newly liable construction rate is .105924. The taxable wage base is $10,000 per employee per calendar year and employee UC withholding is 0.07 percent. Rates confirmed at https://www.pa.gov/agencies/dli/resources/for-employers-and-educators/how-to-file/uc-tax/yearly-tax-highlights

### Pennsylvania workers compensation insurance `pa-workers-comp`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
Pennsylvania requires workers compensation coverage from the very first employee, with no headcount grace. The penalties are criminal and they accrue for each day you are uninsured, and individuals responsible for the company can be charged personally. Pennsylvania runs its own insurer, the State Workers' Insurance Fund, as an assured source of coverage.
- **Deadline**: Coverage must be in force for the entire period any employee is employed.
- **Rule out first**:
  - The only people working are the sole proprietor or general partners, who are on the excluded persons list. (common) Check: Confirm there are no other workers and check the roles against the exclusion list.
  - Qualifying executive officers filed exclusions with the carrier, so they do not appear as covered lives on the policy. (occasional) Check: Obtain the filed exclusion applications and confirm the ownership tests are met.
  - The public coverage search is sourced from the PCRB rather than maintained by the bureau, so a real policy can fail to appear or lag. (common) Check: Request the certificate of insurance directly from the carrier rather than relying on the search.
- **If it genuinely was missed**: Misdemeanor conviction carries a $2,500 fine and up to one year imprisonment for each day in violation. Intentional violation is a felony carrying a $15,000 fine and up to seven years imprisonment for each day. A separate assessment of $200 a day up to 30 days applies for failing to respond to a Department request for coverage information.
- **How to prove it**:
  - [tier 1, corroborating only] Run the employer through the Pennsylvania workers compensation insurance coverage search to see whether a policy is on file. https://www.pa.gov/agencies/dli/resources/for-claimants-workers/workers--compensation-insurance-search-form-
  - [tier 4, settles it] Obtain the certificate of insurance or the SWIF policy declarations page and confirm the policy period covers the whole employment period.
  - [tier 5, corroborating only] Look for workers compensation premium payments to a carrier or to SWIF.
- **Fix**:
  1. Confirm the current employee headcount including part-time workers
  2. Obtain a policy from a licensed carrier or from the State Workers' Insurance Fund
  3. For qualifying executive officers, file exclusion applications with the carrier rather than assuming exclusion
  4. If coverage lapsed, calculate exposure on a per-day basis and contact the Bureau's Compliance Section
- **Source**: https://www.pa.gov/content/dam/copapwp-pagov/en/dli/documents/individuals/workers-compensation/publications/documents/libc-200.pdf (verified 2026-08-14)
- **Note**: Executive officers with an ownership interest in a subchapter S corporation, at least a 5 percent interest in a subchapter C corporation, or who serve unpaid in a nonprofit, may apply for exclusion. Treatment of LLC members is NOT addressed on any Pennsylvania .gov page located, so do not advise an LLC member they can opt out without confirming with the Bureau.

### Pennsylvania sales tax license and economic nexus `pa-sales-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
Any business selling taxable goods or services in Pennsylvania needs a sales tax license, with no dollar threshold for in-state sellers. Out-of-state sellers cross into a collection duty purely on sales volume: Pennsylvania measures economic nexus by dollars only and has no transaction-count test. The license is free and you get it through myPATH.
- **Deadline**: In-state sellers register before making taxable sales. Remote sellers register once Pennsylvania gross sales exceed $100,000, measured by calendar year.
- **Cost**: No fee to apply for the sales tax license
- **Rule out first**:
  - Everything the company sells into Pennsylvania is a non-taxable service or an exempt product, so no license is required despite real revenue. (common) Check: Map the product or service to Pennsylvania taxability rules rather than assuming all revenue is taxable.
  - Pennsylvania sales are under $100,000 for the calendar year, so the remote seller duty has not been triggered. (common) Check: Total Pennsylvania gross sales by calendar year from the sales ledger.
  - Sales run through a marketplace facilitator that collects and remits on the seller's behalf. (common) Check: Confirm the marketplace is registered as a facilitator and review its tax reports.
- **How to prove it**:
  - [tier 2, settles it] Log into myPATH and confirm an active sales tax license number with returns filed for each period. https://mypath.pa.gov/
  - [tier 3, corroborating only] Check the billing or tax platform (for example Stripe Tax or Avalara) for a registered Pennsylvania jurisdiction and its collection start date.
  - [tier 4, settles it] Review the issued sales tax license and the filed PA-3 returns against the sales ledger by ship-to state.
  - [tier 5, corroborating only] Look for sales tax remittances to the PA Department of Revenue.
- **Fix**:
  1. Total Pennsylvania gross sales by calendar year and test against $100,000
  2. Apply for the sales tax license through myPATH at no cost
  3. File any missing returns and remit tax for periods after nexus was established
- **Source**: https://www.pa.gov/agencies/revenue/resources/tax-types-and-information/sales-use-and-hotel-occupancy-tax/online-retailers (verified 2026-08-14)
- **Note**: The Department of Revenue states economic presence is measured by sales threshold only with no transactional count requirement, and that the $100,000 threshold is measured by calendar year. NOTE a conflict in Pennsylvania's own material: SUT Bulletin 2019-01 describes the test as gross sales in the previous twelve months. The current web guidance (calendar year) is treated as operative. Do not cite the PA-100 form as the registration path; every current page names myPATH. The online retailers page cited above does not address cost; the no-fee claim comes from the PA Business One-Stop Hub, which states there is no fee to submit the application, at https://hub.business.pa.gov/Home/HelpCenterDetail/eCommerceorOnlineRetailorGraphicDesign


## CO (8)

### Colorado Periodic Report `co-periodic-report`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
Colorado reporting entities must file a Periodic Report each year with the Secretary of State. Unlike most states the due date is not a fixed calendar date: each entity gets its own periodic report month based on when it registered. Miss it and the entity goes Delinquent.
- **Deadline**: Due in the entity's assigned periodic report month, which is shown on the entity's Summary page in the SOS business database. It may be filed two months before or two months after that month without penalty.
- **Cost**: $25 online
- **Rule out first**:
  - The entity is inside its four-month grace window, so the report is not yet late even though this year's filing is absent. (common) Check: Compare today's date against the periodic report month plus two months.
  - The entity is a general partnership or other non-reporting entity that never owed a Periodic Report. (occasional) Check: Confirm the entity type against the list of reporting entities in the SOS FAQ.
  - The entity was registered recently and its first report month has not arrived yet. (common) Check: Check the formation date against the assigned periodic report month.
- **If it genuinely was missed**: $50 late filing penalty, and the entity's status becomes Delinquent if no report is filed.
- **How to prove it**:
  - [tier 1, settles it] Search the entity in the Colorado SOS business database, open the Summary page, and read both the periodic report month and the current status. https://www.coloradosos.gov/biz/BusinessEntityCriteriaExt.do
  - [tier 2, settles it] Review the filing history and receipts under the SOS account used to manage the entity.
  - [tier 5, corroborating only] Look for a $25 payment to the Colorado Secretary of State, or $75 if filed late with the penalty.
- **Fix**:
  1. Look up the entity's periodic report month on its SOS Summary page
  2. File the Periodic Report online and pay $25, or $75 if the late penalty applies
  3. If the status is Delinquent, file a Statement Curing Delinquency to restore Good Standing
- **Source**: https://www.coloradosos.gov/pubs/business/FAQs/reports.html (verified 2026-08-14)
- **Note**: Fee of $25 and late penalty of $50 confirmed on the Colorado business fee schedule at https://www.coloradosos.gov/pubs/info_center/fees/business.html

### Colorado registered agent `co-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
Almost every entity on record with the Colorado Secretary of State must continuously maintain a registered agent with a physical Colorado street address. Colorado tightened the eligibility rules effective July 1 2025 to fight fraudulent filings, so an agent that was fine before may no longer qualify. The agent must consent to the appointment.
- **Deadline**: Must be maintained continuously, and updated whenever the agent or address changes.
- **Cost**: $10 to file a statement of change regarding the registered agent
- **Rule out first**:
  - A founder who lives in Colorado serves as the agent personally, so there is no vendor invoice to find. (common) Check: Match the agent name on the SOS record to a founder with a Colorado residence and valid Colorado ID.
  - The registered agent address differs from the principal office address, which is normal and not a defect. (common) Check: Confirm the registered agent address is a physical Colorado street address rather than a PO box.
- **If it genuinely was missed**: Failure to maintain a registered agent can result in delinquent status and leave the entity unable to defend a lawsuit.
- **How to prove it**:
  - [tier 1, settles it] Open the entity's Summary page in the Colorado SOS database and read the registered agent name and Colorado street address. https://www.coloradosos.gov/biz/BusinessEntityCriteriaExt.do
  - [tier 3, corroborating only] If a commercial registered agent is used, confirm the account is active and paid in the provider's portal.
  - [tier 5, corroborating only] Look for a recurring annual registered agent subscription charge.
- **Fix**:
  1. Pull the entity Summary page and confirm the listed agent still meets the post July 1 2025 eligibility rules
  2. Confirm the agent holds a valid Colorado driver's license or ID, or that the entity agent is in good standing with a Colorado place of business
  3. File a change of registered agent for $10 if the current agent no longer qualifies
- **Source**: https://www.coloradosos.gov/pubs/business/FAQs/regAgent.html (verified 2026-08-14)
- **Note**: July 1 2025 eligibility changes stem from House Bill 24-1137 and are described at https://www.coloradosos.gov/pubs/business/RAchanges.html. An entity may act as its own registered agent only after first appointing another eligible agent and then filing a change to self-select.

### Colorado Statement of Foreign Entity Authority `co-foreign-authority`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An entity formed outside Colorado must file a Statement of Foreign Entity Authority before transacting business in the state. Once authorized, the entity also picks up the Colorado Periodic Report and registered agent obligations.
- **Deadline**: Before the entity begins transacting business in Colorado.
- **Cost**: $100 online
- **Rule out first**:
  - Colorado activity is limited to remote sales that do not amount to transacting business, so no authority filing is required. (common) Check: Test for a Colorado office, employees, or repeated in-state contracting.
  - The entity registered in Colorado under a different assumed name because its true name was taken. (occasional) Check: Search the registry by registered agent or by name variants.
- **How to prove it**:
  - [tier 1, settles it] Search the entity in the Colorado SOS business database and confirm a foreign entity record exists in Good Standing. https://www.coloradosos.gov/biz/BusinessEntityCriteriaExt.do
  - [tier 4, settles it] Obtain the filed Statement of Foreign Entity Authority and its confirmation.
  - [tier 5, corroborating only] Look for a $100 payment to the Colorado Secretary of State.
- **Fix**:
  1. Determine whether Colorado activity constitutes transacting business
  2. File the Statement of Foreign Entity Authority online and pay $100
  3. Appoint a qualifying Colorado registered agent as part of the filing
- **Source**: https://www.coloradosos.gov/pubs/info_center/fees/business.html (verified 2026-08-14)

### Colorado business income tax return `co-income-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: tax
Any entity that must file a federal income tax return and is doing business in Colorado must also file a Colorado income tax return. C corporations pay at the entity level on a statutory rate of 4.40 percent of Colorado net income, while partnerships and S corporations generally pass income through to owners. The rate is not fixed year to year: Colorado temporarily reduces it in TABOR surplus years, so the operative rate for a given tax year has to be confirmed. An entity is treated as doing business in Colorado if its activity exceeds the protection of Public Law 86-272.
- **Deadline**: Due by the fifteenth day of the fourth month after the end of the tax year, which is April 15 for calendar year filers. Extensions extend time to file but not time to pay.
- **Rule out first**:
  - The company's only Colorado contact is soliciting orders for tangible goods shipped from out of state, which Public Law 86-272 protects from income tax. (common) Check: Test whether Colorado activity goes beyond solicitation, for example services, installation, or in-state employees.
  - The entity had a loss or no Colorado apportioned income, so no tax was due even though a return was required. (common) Check: Read the filed return rather than looking for a payment.
- **If it genuinely was missed**: C corporations that fail to make required quarterly estimated payments face a penalty, though it generally does not apply if net tax liability for the year is under $5,000.
- **How to prove it**:
  - [tier 2, settles it] Log into Colorado Revenue Online and confirm the income tax account is registered and returns are filed for each year. https://tax.colorado.gov/
  - [tier 4, settles it] Review the filed Colorado return (DR 0112 for C corporations, DR 0106 for partnerships and S corporations) against the federal return.
  - [tier 5, corroborating only] Look for estimated tax payments to the Colorado Department of Revenue during the year.
- **Fix**:
  1. Confirm whether Colorado activity exceeds Public Law 86-272 protection
  2. Register the income tax account in Revenue Online
  3. File the outstanding Colorado returns and set up quarterly estimates if liability will exceed $5,000
- **Source**: https://tax.colorado.gov/business-income-tax (verified 2026-08-14)
- **Note**: RATE RESOLVED 2026-08-14 from statute. C.R.S. 39-22-301(1)(d)(I)(K) imposes the corporate tax at 'four and forty one-hundredths percent of the Colorado net income' for income tax years commencing on or after January 1 2022, read from the Colorado Revised Statutes Title 39 compilation at https://content.leg.colorado.gov/sites/default/files/images/olls/crs2024-title-39.pdf. That rate is expressly subject to C.R.S. 39-22-627, under which the executive director TEMPORARILY reduces the income tax rate for a tax year when TABOR excess state revenues exceed statutory thresholds, on a sliding scale starting at four one-hundredths of one percent. So 4.40 percent is the statutory rate, not necessarily the operative rate for tax year 2026; the operative rate depends on an annual excess-revenue certification and must be confirmed for the year being filed. Do not cite 4.63 percent, which is the pre-2020 rate. The $5,000 estimated payment exception is NOT on the Department of Revenue business income tax page as an earlier note claimed; it is C.R.S. 39-22-606(6)(a)(I): 'No addition to tax shall be imposed under subsection (3) of this section for any taxable year if the tax imposed under part 3 of this article shown on the return for such taxable year or, if no return is filed, the tax, is less than five thousand dollars.' Filing requirement, doing-business standard and the fifteenth day of the fourth month due date were confirmed on the Department of Revenue business income tax page. The Department's own Corporate Income Tax Guide revised March 2026 carries a rate table that stops at 2025 and reads 4.4 percent for 2022, 4.4 percent for 2023, 4.25 percent for 2024 and 4.4 percent for 2025, which shows both the TABOR dip and that DOR has published no final 2026 figure.

### Colorado wage withholding account `co-wage-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
If you pay wages that are subject to federal withholding to a Colorado resident, or to a nonresident performing services in Colorado, you must open a Colorado wage withholding account. The account itself is free and never needs renewing. Colorado states the duty as applying for and maintaining an active account rather than as a dated deadline, so treat an account opened late as a gap to close rather than as a missed statutory date. Your filing frequency is driven by how much you withhold in a year.
- **Deadline**: Colorado publishes no registration deadline for this account, so none is asserted here: the duty is simply to apply for and maintain an active account while Colorado wages are paid. Filing frequency: quarterly if annual Colorado withholding is under $7,000, monthly if at least $7,000 and not more than $50,000, and weekly by EFT if more than $50,000.
- **Cost**: No fee for the account and no renewal requirement
- **Rule out first**:
  - The company pays only contractors, so no wage withholding account is needed. (common) Check: Test worker classification and confirm only 1099 filings exist.
  - A remote employee lives in Colorado but the employer registered recently, so early periods show no filings. (occasional) Check: Compare the employee start date to the account open date in Revenue Online.
  - The payroll provider opened and files the account, so the founder never handled it. (common) Check: Request the Colorado withholding account number from the payroll provider and verify it in Revenue Online.
- **How to prove it**:
  - [tier 2, settles it] Log into Colorado Revenue Online and confirm an active wage withholding account with returns filed for each period. https://tax.colorado.gov/
  - [tier 3, corroborating only] Check the payroll provider for the Colorado withholding account number and assigned frequency.
  - [tier 4, settles it] Review the filed Wage Withholding Account Application (CR 0100) and the DR 1093 annual reconciliation.
  - [tier 5, corroborating only] Look for withholding remittances to the Colorado Department of Revenue.
- **Fix**:
  1. Apply as a withholding tax agent through MyBizColorado for in-state businesses or the CR 0100 for out-of-state businesses
  2. File any missing withholding returns for the periods with Colorado wages
  3. Confirm the assigned filing frequency matches actual withholding volume
- **Source**: https://tax.colorado.gov/withholding-accounts (verified 2026-08-14)
- **Note**: CORRECTED 2026-08-14. An earlier version said apply before the first payroll. No Colorado source states that: neither https://tax.colorado.gov/withholding-accounts nor the Colorado Wage Withholding Tax Guide gives any registration timing rule, and the CR 0100 only asks for the anticipated first payroll month, which is a form field rather than a deadline. The unsourced deadline was deleted rather than replaced. Withholding trigger confirmed at https://tax.colorado.gov/withholding-tax-filing-requirements and frequency thresholds at https://tax.colorado.gov/withholding-filing-frequency-due-dates, which also states that weekly filers 'Must file all payments by Electronic Funds Transfer'. No fee and no renewal confirmed at https://tax.colorado.gov/withholding-accounts. NOTE tax.colorado.gov and cdle.colorado.gov return HTTP 403 to plain fetchers, so these were read in a real browser.

### Colorado Unemployment Insurance employer registration `co-unemployment-insurance`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
Colorado uses a wage-or-weeks test, so you become a liable employer once you cross either trigger. Registration happens in the MyUI Employer+ system, which is where you also file wage reports and pay premiums. Nonprofits and household or agricultural employers have their own separate thresholds.
- **Deadline**: Register once liability attaches. Colorado determines and notifies liability through a Liability Determination Notice.
- **Rule out first**:
  - The company has employees but has not yet crossed either the $1,500 quarterly wage test or the 20 week test, so liability has not attached. (common) Check: Total wages by calendar quarter and count the distinct weeks with at least one worker.
  - Only contractors are paid, so there is no covered employment. (common) Check: Test worker classification against the Colorado employment definition.
  - CDLE has not yet issued the Liability Determination Notice even though the employer applied. (occasional) Check: Check the MyUI Employer+ account status rather than waiting for mail.
- **How to prove it**:
  - [tier 2, settles it] Log into MyUI Employer+ and confirm an active UI employer account with wage reports filed and premiums paid. https://cdle.colorado.gov/ui/employers
  - [tier 3, corroborating only] Check the payroll provider for the Colorado UI account number and assigned premium rate.
  - [tier 4, settles it] Review the Liability Determination Notice and the annual premium rate notice issued by CDLE.
  - [tier 5, corroborating only] Look for quarterly UI premium payments to the Colorado Department of Labor and Employment.
- **Fix**:
  1. Total wages by quarter and count weeks with any employee to test liability
  2. Register the employer account in MyUI Employer+
  3. File any missing quarterly wage reports and pay premiums on chargeable wages
- **Source**: https://cdle.colorado.gov/ui/employers/requirements/employer-liability-requirements (verified 2026-08-14)
- **Note**: The 2026 chargeable wage base is $30,600, up from $27,200 in 2025, per https://cdle.colorado.gov/ui/employers/requirements/premiums. The 2026 combined introductory rate is 0.0305 for non-construction, general construction and trades, and 0.062850 for heavy construction, per https://cdle.colorado.gov/ui/employers/requirements/premiums/introductory-rates. NO day-count registration deadline and NO late-registration penalty figure could be sourced from any CDLE page; both are deliberately omitted rather than guessed.

### Colorado workers compensation insurance `co-workers-comp`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
Colorado requires coverage from the first employee. Fines accrue per day you are uninsured and the director can order you to stop operating altogether until you fix it. Colorado has a state chartered insurer, Pinnacol Assurance, which by statute cannot refuse to insure a Colorado employer.
- **Deadline**: Coverage must be in force continuously while anyone is employed under a contract of hire.
- **Rule out first**:
  - The only workers are a sole proprietor or general partners, who are outside coverage by default and must opt in rather than out. (common) Check: Confirm no one else is under a contract of hire and check whether an inclusion endorsement was elected.
  - Qualifying corporate officers or LLC members rejected coverage in writing, so they are not on the policy even though the policy exists. (occasional) Check: Obtain the certified mail rejection notices and confirm each person owns at least 10 percent and manages the business.
  - Coverage is written under a PEO or staffing arrangement, so no policy appears in the company's own name. (occasional) Check: Request the PEO's certificate of insurance naming the client company.
- **If it genuinely was missed**: For every day the employer fails to insure, a fine of not more than $250 for an initial violation, or not less than $250 and not more than $500 for a second and any subsequent violation. The director may also order the employer to cease and desist business operations, and the attorney general institutes injunctive proceedings after such an order. Fines may only be imposed for periods no more than three years before the employer is notified of a potential violation.
- **How to prove it**:
  - [tier 2, settles it] Confirm coverage status with the Division of Workers' Compensation at CDLE for the employer's FEIN. https://cdle.colorado.gov/dwc
  - [tier 4, settles it] Obtain the certificate of insurance or policy declarations page and confirm the policy period covers the entire employment period.
  - [tier 4, settles it] For rejecting owners, obtain the written rejection notice sent by certified mail to the carrier and confirm the 10 percent ownership test is met.
  - [tier 5, corroborating only] Look for workers compensation premium payments to Pinnacol Assurance or another carrier.
- **Fix**:
  1. Confirm whether anyone is working under a contract of hire
  2. Obtain a policy from a licensed carrier or from Pinnacol Assurance, which cannot refuse a Colorado employer
  3. For owners intending to reject coverage, send written rejection by certified mail to the carrier and confirm the 10 percent ownership test
  4. If coverage lapsed, size exposure on a per-day basis subject to the three year lookback cap
- **Source**: https://content.leg.colorado.gov/sites/default/files/images/olls/crs2024-title-08.pdf (verified 2026-08-14)
- **Note**: Threshold from C.R.S. 8-40-203(1)(b), penalties from C.R.S. 8-43-409(1), owner rejection from C.R.S. 8-41-202(4) which sets the ten percent test for both a corporate officer and an LLC member, sole proprietor and partner opt-in from C.R.S. 8-40-302(5)(b), Pinnacol from C.R.S. 8-45-101. IMPORTANT CORRECTION: the widely repeated flat $500 per day figure is the second-violation ceiling, not the initial-violation penalty. Re-verified against the statute on 2026-08-14: 'Not more than two hundred fifty dollars for an initial violation' and 'Not less than two hundred fifty dollars or more than five hundred dollars for a second and any subsequent violation'. Two conditions sit on the three year lookback: it lives in subsection (1.5), which is repealed effective September 1 2033, and under 8-43-409(1.5)(a) a violation occurring more than seven years after the preceding violation ended resets to the initial-violation maximum. CDLE web pages return HTTP 403 to plain fetchers, so the statute was used as the stronger source. C.R.S. 8-43-408 also increases benefits but the compilation states no percentage, so the commonly cited 25 percent increase is NOT included here.

### Colorado sales tax license, economic nexus and home-rule cities `co-sales-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
Colorado requires a sales tax license from any retailer making sales in the state, and remote sellers cross at $100,000 with no transaction-count test. The part that catches founders is that a Colorado state license does NOT cover home-rule self-collecting cities: 72 municipalities and 2 counties run their own license, own return and own tax base. The SUTS portal consolidates filing, but only for home-rule cities that chose to participate.
- **Deadline**: If Colorado sales in the previous calendar year exceeded $100,000, you are subject to licensing and collection for the entire current year. If you cross $100,000 during the current year, the statute sets the start as the first day of the month after the ninetieth day after crossing. Licenses run on a two-year cycle expiring at the end of odd-numbered years; the current period began January 1 2026, and each physical location pays its own $16 renewal.
- **Cost**: State license fee is prorated by when you apply within the two-year cycle: $16 in January to June of an even year, $12 in July to December of an even year, $8 in January to June of an odd year, and $4 in July to December of an odd year. New accounts also post a refundable $50 deposit, returned automatically once the business has collected and paid $50 in state sales tax. Renewal is $16 per physical location. Home-rule self-collecting jurisdictions charge their own separate license fees.
- **Rule out first**:
  - Colorado sales are under $100,000 in both the current and previous calendar year, so the retailer is exempt from state licensing and collection. (common) Check: Total Colorado sales for both calendar years from the sales ledger.
  - The retailer crossed $100,000 recently and is inside the 90 day grace period before collection must begin. (occasional) Check: Find the date cumulative Colorado sales crossed $100,000 and add 90 days, then take the first day of the next month.
  - No home-rule city license exists because the company only ships to state-collected jurisdictions. (common) Check: Check the ship-to cities against the list of self-collecting jurisdictions in DR 1002.
  - A marketplace facilitator collects and remits, so the seller has no direct filings. (common) Check: Confirm the marketplace's facilitator status and review its remittance reports.
- **How to prove it**:
  - [tier 2, settles it] Log into Colorado Revenue Online and confirm an active sales tax license for each physical location plus filed returns. https://tax.colorado.gov/
  - [tier 2, corroborating only] Log into the SUTS remittance portal and confirm which state-collected and participating home-rule jurisdictions are being filed. https://tax.colorado.gov/SUTS-info
  - [tier 4, settles it] Compare the sales ledger by ship-to city against publication DR 1002 to identify any self-collecting jurisdiction where no separate license exists.
  - [tier 5, corroborating only] Look for sales tax remittances to the Colorado Department of Revenue and to individual city finance departments.
- **Fix**:
  1. Total Colorado sales for the current and previous calendar year and test against $100,000
  2. Apply through MyBizColorado or form CR 0100 and pay the prorated license fee plus the $50 deposit
  3. Check every ship-to city against DR 1002 and license separately with each self-collecting home-rule jurisdiction
  4. Register in SUTS to consolidate filing for state-collected and participating home-rule jurisdictions
  5. Confirm whether the retail delivery fee applies and that the current rate is being charged
- **Source**: https://tax.colorado.gov/out-of-state-businesses (verified 2026-08-14)
- **Note**: The enacted economic nexus statute (HB19-1240, C.R.S. 39-26-102(3)(c)) never contained a transaction-count test; the string 'two hundred' appears nowhere in the signed act at https://content.leg.colorado.gov/sites/default/files/2019a_1240_signed.pdf. The 200-transaction alternative existed only in 2018 emergency rules. SB20-099, which would have raised the threshold to $200,000, failed. The 90 day rule is quoted from C.R.S. 39-26-102(3)(c)(I)(B) as 'the first day of the month after the ninetieth day after' crossing; an earlier paraphrase said 'the first day of the first month commencing at least 90 days after', which is the same effect but not the statutory wording. The $50 deposit is required only on the first business location. There are 72 self-collecting municipalities and 2 self-collecting counties; 24 home-rule municipalities are state-collected, so home-rule does not automatically mean self-collecting. SUTS covers participating home-rule jurisdictions only. The Colorado retail delivery fee is currently $0.31 per retail delivery effective July 1 2026, up from $0.28, per https://tax.colorado.gov/retail-delivery-fee-rates


## GA (9)

### Georgia annual registration `ga-annual-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
Every business entity registered with the Georgia Secretary of State must file an annual registration. It refreshes your registered agent, principal office address and, for corporations, your officers. Georgia lets you prepay up to three years at once.
- **Deadline**: Due by April 1 each year, and may be filed as early as January 1. A newly formed Georgia corporation files its initial annual registration within 90 days after its articles of incorporation are filed or become effective, EXCEPT that if the articles are delivered for filing after October 1 the initial registration is filed between January 1 and April 1 of the next year. LLCs, LPs and newly qualified foreign corporations file their first registration between January 1 and April 1 of the year following the initial filing.
- **Cost**: $60 for profit corporations, professional corporations, benefit corporations, LLCs, LPs, LLLPs and trust estates. $40 for nonprofit corporations. $35 for foreign LLPs. $30 for an amended annual registration. Each of those totals already includes a $10 service charge, and the price is identical online and on paper.
- **Rule out first**:
  - The entity prepaid a multi-year registration covering up to three years, so no payment appears in the current year even though it is compliant. (common) Check: Open the entity record at ecorp.sos.ga.gov and read the paid-through year rather than looking for an annual payment.
  - A Georgia corporation formed late in the year has 90 days from incorporation, so its first registration may not be due yet. (occasional) Check: Compare the incorporation date to today plus the 90 day rule.
  - It is early in the calendar year and the April 1 deadline has not arrived yet. (common) Check: Check the current date against April 1.
- **If it genuinely was missed**: $25 late filing penalty. Entities that do not timely file with all required fees may be administratively dissolved or have their authority to transact business revoked.
- **How to prove it**:
  - [tier 1, settles it] Search the entity at ecorp.sos.ga.gov by name, control number, officer or registered agent and check the status plus the most recent annual registration year. A status of active/noncompliance means dissolution is pending this year. https://ecorp.sos.ga.gov/BusinessSearch
  - [tier 2, settles it] Log into the eCorp filer dashboard and review filings and emailed receipts. https://ecorp.sos.ga.gov/Account
  - [tier 5, corroborating only] Look for a $60 or $40 payment to the Georgia Secretary of State between January and April.
- **Fix**:
  1. Search the entity at ecorp.sos.ga.gov and confirm the paid-through year and status
  2. File the annual registration through One Click Annual Registration or the eCorp account and pay the fee plus any $25 late penalty
  3. If a Notice of Administrative Dissolution was issued, file within 60 days of the notice date to avoid dissolution
- **Source**: https://sos.ga.gov/how-to-guide/how-file-annual-registration (verified 2026-08-14)
- **Note**: CORRECTED 2026-08-14. Fee table reflects the Corporations Division schedule effective September 6 2025, read at https://sos.ga.gov/sites/default/files/forms/Reference%20-%20Filing%20Fees_0.pdf and corroborated in HTML at https://sos.ga.gov/how-to-guide/how-file-annual-registration. An earlier version said paper filings carry an extra $10 service charge. That is wrong twice over: the schedule's two columns are 'Online Filing: (Fee + Applicable Service Charge)' and 'Paper Filing: (Fee + Applicable Service Charge)', the $10 applies in BOTH channels, and it is already inside the $60, $40, $35 and $30 totals rather than added to them. The underlying split is $50 + $10, $30 + $10, $25 + $10 and $20 + $10. Treating it as a paper surcharge overstated every paper filing by $10. The late penalty is $25 in both channels. The October 1 carve-out on the 90 day initial registration comes from Rule 590-7-4-.02 at https://rules.sos.ga.gov/gac/590-7-4, with the matching LLC rule at 590-7-22-.02. NOTE sos.ga.gov sits behind a Cloudflare challenge and returns 403 to scripted fetchers; these pages were read in a real browser, and rules.sos.ga.gov served plain fetches.

### Georgia registered agent and registered office `ga-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
Every Georgia entity must continuously maintain a registered agent and registered office in Georgia. The agent's address must be a physical Georgia street address where a person can actually be found, and a PO box or mail drop is not acceptable. An entity cannot serve as its own registered agent in Georgia.
- **Deadline**: Must be maintained continuously. The agent and address are refreshed through the annual registration.
- **Cost**: Included in the annual registration fee when updated through that filing
- **Rule out first**:
  - An officer or the company's attorney serves as registered agent personally, so no vendor invoice exists. (common) Check: Match the agent name on the eCorp record to an officer or counsel with a Georgia street address.
  - The registered agent address differs from the principal office, which is expected and not a defect. (common) Check: Confirm the registered agent address is a Georgia street address and matches the registered office address.
- **How to prove it**:
  - [tier 1, settles it] Search the entity at ecorp.sos.ga.gov and read the registered agent name and Georgia street address on the record. https://ecorp.sos.ga.gov/BusinessSearch
  - [tier 3, corroborating only] If a corporate service company acts as agent, confirm the account is active and paid in that provider's portal.
  - [tier 5, corroborating only] Look for a recurring annual registered agent fee.
- **Fix**:
  1. Pull the entity record at ecorp.sos.ga.gov and confirm the agent and Georgia street address are current
  2. Confirm the entity itself is not listed as its own agent, which Georgia does not permit
  3. Update the agent through an annual registration or amended annual registration
- **Source**: https://sos.ga.gov/page/business-division-faq (verified 2026-08-14)
- **Note**: The registered agent's business office address must be identical with the registered office address.

### Georgia certificate of authority for a foreign entity `ga-certificate-of-authority`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An entity formed outside Georgia must obtain a certificate of authority before transacting business in the state, and must appoint a Georgia registered agent to qualify. Georgia enforces this with a real cash penalty rather than just a filing block. An unqualified entity may also be unable to bring a lawsuit in Georgia.
- **Deadline**: Before transacting business in Georgia. A penalty applies once the entity has been doing business in Georgia over 30 days without qualifying.
- **Cost**: $235 total for a foreign corporation, LLC, LP or LLLP, made up of a $225 filing fee plus a $10 service charge. $210 total for a foreign LLP, made up of $200 plus the same $10. The service charge applies online and on paper alike, so the amount payable is the same in both channels.
- **Rule out first**:
  - Georgia activity has not crossed into transacting business, for example only remote sales shipped into the state. (common) Check: Test for a Georgia office, employees, or repeated in-state contracting against the statutes cited in the SOS FAQ.
  - The entity qualified under an assumed name because its true name was unavailable in Georgia. (occasional) Check: Search eCorp by registered agent or by name variants rather than the exact home-state name.
- **If it genuinely was missed**: $500 for profit corporations. For LLCs, LPs and LLLPs, $500 plus all fees that would have been imposed had the entity registered. For foreign LLPs, $500 for each year or part year of transacting business plus all back fees.
- **How to prove it**:
  - [tier 1, settles it] Search the entity at ecorp.sos.ga.gov and confirm a foreign entity record with an active certificate of authority. https://ecorp.sos.ga.gov/BusinessSearch
  - [tier 4, settles it] Obtain the filed Application for Certificate of Authority and the issued certificate.
  - [tier 5, corroborating only] Look for a $235 payment to the Georgia Secretary of State, or $210 for a foreign LLP.
- **Fix**:
  1. Determine whether Georgia activity constitutes transacting business and for how long it has been going on
  2. File the Application for Certificate of Authority online at ecorp.sos.ga.gov and pay $235, which is the $225 filing fee plus the $10 service charge
  3. Budget for the $500 penalty plus back fees if activity has exceeded 30 days
- **Source**: https://sos.ga.gov/page/business-division-faq (verified 2026-08-14)
- **Note**: FEE CORRECTED 2026-08-14 against the Corporations Division schedule effective September 6 2025. The $225 base did not change, but the amount actually payable is $235, and the $10 service charge is NOT a paper-only surcharge: it applies in both channels. The registration how-to at https://sos.ga.gov/how-to-guide-register-foreign-entity states it directly as 'Pay the $235 fee ($225 filing fee + $10 service charge)'. Penalty amounts and the 30 day trigger are quoted from the Business Division FAQ, which attributes them to O.C.G.A. 14-2-1502 for profit corporations, 14-3-1502 for nonprofit corporations, 14-8-54 for LLPs, 14-9-907 for LPs and LLLPs, and 14-11-711 for LLCs. The O.C.G.A. text itself could not be read from a fetchable primary source, since legis.ga.gov serves bills rather than the code.

### Georgia corporate income tax `ga-corporate-income-tax`
Applies to: c-corp, benefit-corp | category: tax
Georgia taxes the Georgia taxable net income of corporations doing business in the state. The rate for tax years beginning on or after January 1 2026 is 4.99 percent, down from 5.19 percent, and it steps down further from 2027 under a legislated schedule, so confirm the rate for the tax year you are filing. If Georgia recognizes S corporation status, the shareholders pay rather than the corporation.
- **Deadline**: Annual corporate income tax return, aligned with the federal corporate return cycle.
- **Rule out first**:
  - Georgia recognizes the entity's S corporation election, so the shareholders pay the tax instead of the corporation. (common) Check: Confirm the Georgia S election is recognized and review Form 600S and shareholder K-1s.
  - The corporation had a loss year, so no tax was due even though the return was required. (common) Check: Read the filed return rather than looking for a payment.
- **How to prove it**:
  - [tier 2, settles it] Log into the Georgia Tax Center and confirm the corporate income tax account is registered and returns are filed for each year. https://gtc.dor.ga.gov/
  - [tier 4, settles it] Review the filed Georgia Form 600 or 600S against the federal return.
  - [tier 5, corroborating only] Look for estimated tax payments to the Georgia Department of Revenue.
- **Fix**:
  1. Confirm the entity's Georgia tax classification
  2. Register the corporate income tax account in the Georgia Tax Center
  3. File the outstanding Form 600 or 600S returns using the rate in force for each tax year
- **Source**: https://gov.georgia.gov/document/2026-signed-legislation/hb-463/download (verified 2026-08-14)
- **Note**: RESOLVED 2026-08-14. The rate is 4.99 percent for tax years beginning on or after January 1 2026. House Bill 463, signed by the Governor on May 11 2026, amends O.C.G.A. 48-7-20(a.1) to read '4.99 percent for taxable years beginning on or after January 1, 2026' and its caption states the Act acts 'to reduce the rates of taxation on corporate and partnership income'. HB 463 does not itself amend O.C.G.A. 48-7-21, because the corporate rate already tracks the 48-7-20 rate by cross reference: HB 1023 (2024) rewrote 48-7-21(a) to charge corporations 'at the same rate of the tax imposed on individuals under subsection (a.1) of Code Section 48-7-20 for the corresponding taxable year', readable at https://www.legis.ga.gov/api/legislation/document/20232024/227798. The 2026 Employer's Tax Guide states the change is 'effective upon signature of HB 463, but retroactive to taxable years beginning on or after January 1, 2026'. Do not attribute the 2026 rate to HB 1437, HB 1015 or HB 111; none of them set it. The Department of Revenue confirms the change at https://dor.georgia.gov/taxes/important-tax-updates: 'The Georgia income tax rate has been reduced to a flat rate of 4.99%.' CAUTION: the DOR corporate income and net worth tax page at https://dor.georgia.gov/corporate-income-and-net-worth-tax still reads 'The rate of taxation is 5.19% of a corporation's Georgia taxable net income' with no tax year label, and is stale. Do not cite it for the rate. Later years: HB 463 reduces the rate by 0.125 percent annually beginning January 1 2027 until it reaches 3.99 percent, subject to statutory delay conditions. Widely circulated secondary summaries giving 4.49 percent for 2027 do not match the enacted text.

### Georgia net worth tax `ga-net-worth-tax`
Applies to: c-corp, s-corp, benefit-corp | category: tax
Georgia charges corporations a separate net worth tax on top of income tax. It is capped, so it is a nuisance filing rather than a large bill for most startups, but the return is still required even when no tax is due. Founders routinely forget it because it has no federal analogue.
- **Deadline**: An initial net worth return is due on or before the fifteenth day of the third calendar month after incorporation or qualification. For C corporations with net worth years beginning on or after January 1 2017 it is the fourth month. Thereafter it is filed with the annual corporate return.
- **Rule out first**:
  - Net worth is $100,000 or less, so no net worth tax is due, though a return is still required for net worth years beginning on or after January 1 2018. (common) Check: Compute net worth from the balance sheet and compare to the $100,000 threshold, then confirm the return was still filed.
  - The entity is an LLC or partnership rather than a corporation, so the net worth tax does not reach it. (common) Check: Confirm the entity type and its Georgia tax classification.
- **How to prove it**:
  - [tier 2, settles it] Log into the Georgia Tax Center and confirm the net worth tax portion of the corporate return has been filed for each year. https://gtc.dor.ga.gov/
  - [tier 4, settles it] Review the net worth schedule of the filed Georgia Form 600 or 600S.
  - [tier 5, corroborating only] Look for a payment to the Georgia Department of Revenue separate from income tax.
- **Fix**:
  1. Compute the entity's net worth as of the beginning of the net worth year
  2. File the net worth portion of Form 600 or 600S even if net worth is under $100,000
  3. Pay any net worth tax due, which is capped at $5,000
- **Source**: https://dor.georgia.gov/corporate-income-and-net-worth-tax (verified 2026-08-14)
- **Note**: Threshold of $100,000 and maximum tax of $5,000 for net worth over $22 million confirmed on the Department of Revenue page. The page does not address whether LLCs taxed as corporations owe the tax; confirm before relying on the LLC carve-out.

### Georgia withholding tax registration `ga-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Employers paying wages in Georgia must register for a withholding payroll tax number through the Georgia Tax Center and withhold state income tax at the flat rate. Georgia changed the rate partway through 2026, so payroll set up earlier in the year may still be withholding at the old rate. Filing frequency is driven by a lookback period rather than current volume.
- **Deadline**: Register before the first Georgia payroll. Filing status by volume: annual at $800 or less per year, quarterly above $800 per year but $200 or less per month, monthly above $200 per month, and semi-weekly above $50,000 in the lookback period. The lookback period is the twelve months ending June 30 of the immediately preceding calendar year.
- **Rule out first**:
  - The company pays only contractors in Georgia, so no withholding number is required. (common) Check: Test worker classification and confirm only 1099 filings exist.
  - The employer is an annual filer at $800 or less per year, so only one return appears rather than quarterly filings. (occasional) Check: Check the assigned filing status in the Georgia Tax Center before treating missing quarters as a gap.
  - Payroll withheld at 5.19 percent after the rate change because the change was optional from a mid-year date rather than mandatory. (common) Check: Confirm the effective date rule in the current Employer's Withholding Tax Guide.
- **How to prove it**:
  - [tier 2, settles it] Log into the Georgia Tax Center and confirm an active withholding account with Form G-7 returns filed for each period. https://gtc.dor.ga.gov/
  - [tier 3, corroborating only] Check the payroll provider for the Georgia withholding number and assigned filing status.
  - [tier 4, settles it] Review payroll registers and confirm the withholding rate applied changed on the correct effective date.
  - [tier 5, corroborating only] Look for GA-V deposits or EFT remittances to the Georgia Department of Revenue.
- **Fix**:
  1. Register for a withholding payroll tax number in the Georgia Tax Center
  2. Confirm the correct flat withholding rate for each payroll date in the year
  3. File missing Form G-7 returns and remit any GA-V deposits due
- **Source**: https://dor.georgia.gov/document/document/2026-employers-tax-guide-updated-june-2026/download (verified 2026-08-14)
- **Note**: SOURCE CORRECTED 2026-08-14. The previously cited December 2025 revision of the guide now returns HTTP 404; the live document is the 2026 Employer's Withholding Tax Guide updated June 2026, downloaded and read directly. That revision states it reflects Georgia income tax laws signed into effect on May 11 2026 and its withholding tables compute at 4.99 percent, so payroll set up earlier in 2026 at 5.19 percent is the known transition case rather than an error. Verified in the June 2026 document: employers who withheld more than $50,000 in the aggregate during the lookback period are semi-weekly payers and must remit by EFT; the lookback period is the 12 month period that ended the previous June 30; tax withheld exceeding $200.00 per month requires a GA-V payment voucher by the fifteenth of the following month; and the annual band is 'tax withheld or tax required to be withheld is $800.00 or less per year', with quarterly at '$200.00 per month or less, but more than $800.00 per year'. CAUTION on the One-Day Rule: the guide is internally inconsistent. Its narrative says an employer required to withhold 'more than $100,000' for a payday must remit by EFT the next banking day, while its summary table says '$100,000 or more'. Apply the stricter $100,000 or more reading.

### Georgia Department of Labor unemployment insurance registration `ga-unemployment-insurance`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
Georgia uses a wage-or-weeks test for unemployment liability. Once you are liable you file Form DOL-1A immediately after your first Georgia payroll, with no grace period. Georgia advises checking liability before you open, because registering late can mean back taxes plus a penalty.
- **Deadline**: Complete a DOL-1A immediately following the payment of the first Georgia payroll.
- **Rule out first**:
  - The employer has not yet crossed either the 20 week test or the $1,500 quarterly payroll test, so liability has not attached. (common) Check: Total payroll by calendar quarter and count distinct weeks with at least one worker.
  - The rate notice is absent from the mail because Georgia now releases Form DOL-626 only through the Employer Portal. (common) Check: Log into the Employer Portal to retrieve the rate notice rather than expecting a mailed copy.
  - Only contractors are engaged in Georgia, so there is no covered employment. (common) Check: Test worker classification against the Georgia employment definition.
- **If it genuinely was missed**: Late reports may result in a penalty of the greater of $20 or 0.05 percent of the gross payroll, for each month or fraction of a month the report remains delinquent. Unpaid contributions accrue interest at 1.5 percent per month or fraction of a month. A cost of collection fee of 20 percent of any deficiency assessed may also be imposed.
- **How to prove it**:
  - [tier 2, settles it] Log into the Georgia DOL Employer Portal and confirm an active tax account with quarterly reports filed. https://www.dol.state.ga.us/public/uitax/emplportal/login
  - [tier 3, corroborating only] Check the payroll provider for the Georgia DOL account number and assigned rate.
  - [tier 4, settles it] Review the Form DOL-626 annual tax rate notice, which is released through the Employer Portal rather than mailed.
  - [tier 5, corroborating only] Look for quarterly unemployment contributions paid to the Georgia Department of Labor.
- **Fix**:
  1. Test liability against the 20 week and $1,500 quarterly payroll triggers
  2. File Form DOL-1A through Online Employer Tax Registration
  3. File missing quarterly tax and wage reports and pay contributions plus interest
  4. Retrieve the current Form DOL-626 rate notice from the Employer Portal
- **Source**: https://dol.georgia.gov/faqs-employers/employers-faqs-unemployment-insurance (verified 2026-08-14)
- **Note**: SOURCE UPGRADED 2026-08-14. An earlier version rested the wage base and new employer rate on Form DOL-4E, a 2016 revision. Both are now confirmed on the live GDOL employer FAQ cited above: 'New or newly covered employers are assigned a total tax rate of 2.70 percent until such time as they are eligible for a rate calculation based on their experience rating history' and 'Effective January 1, 2013, the taxable wage base in Georgia is $9,500 in accordance with 2012 GA House Bill 347.' Be careful reading that page: it also contains a stale sentence saying tax is paid on the first $8,500, immediately corrected by the $9,500 sentence. GDOL still publishes no 2026 restatement, so confirm the rate against the client's own DOL-626 notice. The administrative assessment component of the total rate is stated to exist but no percentage is published, so it is omitted.

### Georgia workers compensation insurance `ga-workers-comp`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
Georgia is the one of these three states with a real headcount threshold: coverage is required at three or more employees, and part-time workers count. The trap is that officers who exempt themselves still count toward the three, so a three person company where every officer opts out still needs a policy. Georgia has no state fund, so hard-to-place risks go to an assigned risk plan run by NCCI.
- **Deadline**: Coverage begins on the first day of employment once the employer regularly employs three or more persons.
- **Rule out first**:
  - The company regularly employs only one or two people, so it is genuinely under the three employee threshold. (common) Check: Count all workers including part-time, and remember that exempted officers still count toward the threshold.
  - Up to five officers or LLC members filed Form WC-10 exemptions, so they do not appear as covered lives even though a policy exists. (occasional) Check: Obtain the filed WC-10 forms from the insurance company.
  - The coverage verification tool is operated by an outside vendor and can lag or miss a current policy. (common) Check: Request the certificate of insurance directly from the carrier.
- **If it genuinely was missed**: The Board may assess a civil penalty of not less than $500 and not more than $5,000 per occurrence for violation of the duty to provide coverage. Refusing or willfully neglecting to secure coverage is a misdemeanor punishable by a fine of not less than $1,000 and not more than $10,000, imprisonment not to exceed 12 months, or both. Where the employer refuses or willfully neglects to secure insurance, the Board may also assess attorney's fees, civil penalties, and a 10 percent increase in compensation to the employee. An uninsured employer remains responsible for compensable injuries as if it had coverage, regardless of willfulness.
- **How to prove it**:
  - [tier 1, corroborating only] Run the employer through the State Board of Workers' Compensation online coverage verification to see whether a policy is on file. https://sbwc.georgia.gov/online-employers-workers-compensation-coverage-verification
  - [tier 4, settles it] Obtain the certificate of insurance or policy declarations page and confirm the policy period covers the whole employment period.
  - [tier 4, settles it] For exempting officers or LLC members, obtain the Form WC-10 filed with the insurance company, noting the maximum of five.
  - [tier 5, corroborating only] Look for workers compensation premium payments to a carrier.
- **Fix**:
  1. Count every worker including part-time staff and exempted officers to test the three employee threshold
  2. Obtain a policy from a licensed carrier, or apply to the Georgia Workers' Compensation Assigned Risk Plan administered by NCCI if declined
  3. File Form WC-10 with the carrier for any officers or LLC members intending to exempt, up to five
  4. If coverage lapsed while at three or more employees, size exposure for civil penalties and the 10 percent compensation increase
- **Source**: https://sbwc.georgia.gov/employer-information (verified 2026-08-14)
- **Note**: Georgia has no state fund; the residual market is the Georgia Workers' Compensation Assigned Risk Plan administered by NCCI. Sole proprietors and partners are not automatically employees and may elect coverage in writing. The coverage verification tool itself is hosted on a non-government vendor domain.

### Georgia sales and use tax registration and economic nexus `ga-sales-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
Anyone meeting Georgia's definition of a dealer must register for a sales and use tax number, even if every sale is online, out of state, wholesale or exempt. Remote sellers cross on either gross revenue EXCEEDING $100,000 or 200 or more separate retail sales, tested against the previous or current calendar year. Exactly $100,000 with fewer than 200 sales is below the line. Once registered you never renew, as long as ownership and structure stay the same.
- **Deadline**: Register before making taxable sales as a dealer. Remote sellers must collect once either threshold is met in the previous or current calendar year. No renewal is required.
- **Rule out first**:
  - Georgia sales are under both the $100,000 and the 200 transaction tests in the previous and current calendar year. (common) Check: Count Georgia orders and total Georgia gross revenue for both calendar years, since either test alone triggers the duty.
  - A marketplace facilitator collects and remits Georgia tax on the seller's behalf. (common) Check: Confirm the marketplace's facilitator registration and review its remittance reports.
  - The registration exists but shows no recent renewal because Georgia registrations do not require renewal. (common) Check: Confirm the account is active in the Georgia Tax Center rather than looking for a renewal filing.
- **How to prove it**:
  - [tier 2, settles it] Log into the Georgia Tax Center and confirm an active sales and use tax number with returns filed for each period. https://gtc.dor.ga.gov/
  - [tier 3, corroborating only] Check the billing or tax platform for a registered Georgia jurisdiction and its collection start date.
  - [tier 4, settles it] Review the certificate of registration and reconcile filed returns to the sales ledger by ship-to state, including the local tax rate for each delivery location.
  - [tier 5, corroborating only] Look for sales tax remittances to the Georgia Department of Revenue.
- **Fix**:
  1. Count Georgia orders and total Georgia gross revenue for the previous and current calendar year, testing both the $100,000 and 200 transaction legs
  2. Register for a sales and use tax number through the Georgia Tax Center
  3. File missing returns and remit state plus local tax based on each delivery location
- **Source**: https://dor.georgia.gov/media/35301/download (verified 2026-08-14)
- **Note**: Thresholds from Policy Bulletin SUT-2019-02, which remains the operative remote-seller bulletin. WORDING CORRECTED 2026-08-14: the bulletin reads 'Obtained gross revenue, in an amount exceeding $100,000 in the previous or current calendar year' and 'Conducted 200 or more separate retail sales'. An earlier version wrote the revenue leg as '$100,000', which silently pulled a seller sitting at exactly $100,000 over the line. Both legs are written against retail sales of tangible personal property. The gross revenue threshold dropped from $250,000 to $100,000 effective January 1 2020 under House Bill 182; the 200 transaction leg was unchanged. Local tax applies at the rate for the delivery location. The registration FEE is still omitted rather than asserted as zero: no Department of Revenue registration page states a cost, and O.C.G.A. 48-8-59 imposes none, but no primary page affirmatively says the registration is free, so the absence of a fee is inferred rather than sourced.


## WA (10)

### Washington Annual Report (Secretary of State) `wa-annual-report`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
Every registered Washington entity, and every out-of-state entity registered here, must file an Annual Report with the Secretary of State to stay active and keep its UBI in good standing. It confirms your registered agent, principal office and governors. You can file it in the Corporations and Charities Filing System (CCFS) up to 180 days early without moving your due date.
- **Deadline**: Due by the last day of the month in which the business was originally formed or registered in Washington. Filing early does not change the expiration date; the filing window opens 180 days before it.
- **Cost**: $70 for profit business entity types including LLC, LP and LLP. Nonprofit corporations under RCW 24.03A pay $60, reduced to $20 if the nonprofit certifies gross revenue under $500,000 in the most recent fiscal year. Nonprofit Miscellaneous & Mutual (RCW 24.06) is $10.
- **Rule out first**:
  - The report was filed inside the 180-day early window, so the payment and the filing date sit months before the anniversary month you were looking at. (common) Check: Read the expiration date on the CCFS record rather than the filing date.
  - A registered agent service filed and paid it, so there is no charge on the company's own card. (common) Check: Check the CCFS record status directly; then check the agent service's invoice for a pass-through annual report fee.
  - The entity was formed this calendar year, so no annual report is due yet beyond the initial report. (occasional) Check: Compare the formation date on CCFS to the current date.
- **If it genuinely was missed**: Late filing puts the entity in delinquent status and the annual report then costs $95 (a $25 delinquency fee on top of the $70). Nonprofit Miscellaneous & Mutual and Corporation Sole entity types do not have the delinquency fee. Continued failure may lead to administrative dissolution. Reinstatement is $140 plus all missed annual report fees for profit entities; a nonprofit under RCW 24.03A reinstates for $35 plus all missed annual report fees.
- **How to prove it**:
  - [tier 1, settles it] Search the entity by name or UBI in CCFS and read the 'Expiration Date' and status field. Active with a future expiration date means the current annual report is filed. https://ccfs.sos.wa.gov/
  - [tier 2, settles it] Log into the entity's CCFS account and open Notices and Filed Documents to see the accepted annual report confirmation letter. https://ccfs.sos.wa.gov/
  - [tier 5, corroborating only] Look for a $70 (or $95) card charge to WA SECRETARY OF STATE in the month of the anniversary month.
- **Fix**:
  1. Look up the entity in CCFS and note the exact expiration date and current status.
  2. File the Annual Report online in CCFS, paying $70 (or $95 if already delinquent).
  3. If the entity is administratively dissolved, file the reinstatement application and pay $140 plus every missed annual report fee ($35 plus missed fees for a nonprofit under RCW 24.03A).
  4. Set a recurring calendar reminder for 150 days before the expiration date each year.
- **Source**: https://www.sos.wa.gov/corporations-charities/business-entities/maintain-business-compliance/annual-reports (verified 2026-08-14)
- **Note**: Fees confirmed on the SOS fee schedule (https://www.sos.wa.gov/corporations-charities/frequently-asked-questions-faqs/fee-scheduleexpedited-service), which states the profit annual report increased to $70 per WAC 434-112-085(7) and lists 'Annual Report with delinquency fee $95'. Nonprofit $60/$20 confirmed on the nonprofit annual report online filing instructions page, which states '$60 - Default fee / $20 - Reduced fee' and requires certification 'its gross revenue is less than $500,000 in the most recent fiscal year'. CONFLICT RESOLVED 2026-08-14: an earlier pass recorded a conflicting '$80 default or $40 reduced' nonprofit annual report fee. That figure is the nonprofit 24.03A ARTICLES OF INCORPORATION fee, not the annual report; the fee schedule lists nonprofit 'Original Filings $40-80' alongside 'Annual Report $20-60'. The annual report is $60/$20. Delinquency and reinstatement carve-outs confirmed on the same fee schedule: Nonprofit Miscellaneous & Mutual and Corporation Sole 'do not have this fee', and nonprofit 24.03A reinstatement is '$35 + all missed annual report fees'. sos.wa.gov returns HTTP 403 to automated fetchers; these pages were read through a real browser session.

### Washington Registered Agent `wa-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
Washington law requires every domestic entity and every registered foreign entity to designate and continuously maintain a registered agent in the state. The agent accepts lawsuits and official notices for you. The agent's address must be a real physical street address in Washington; PO boxes and mailbox stores are not allowed.
- **Deadline**: Continuous. The agent must be named at formation or registration and kept current; changes are filed on the Annual Report (inside the 180-day window) or on an Amended Annual Report or Statement of Change.
- **Cost**: No fee to change the registered agent or registered office.
- **Rule out first**:
  - The agent is a founder or employee at the company's own Washington office, so there is no third-party agent invoice anywhere. (common) Check: Read the agent name on the CCFS record; a natural person at the business address is a valid non-commercial registered agent.
  - The company recently moved offices and the agent address looks stale, but the change was filed and CCFS has not been refreshed in a cached view. (occasional) Check: Re-pull the CCFS record and check the filing history for a Statement of Change.
- **How to prove it**:
  - [tier 1, settles it] Open the entity in CCFS and read the Registered Agent name and physical address block. https://ccfs.sos.wa.gov/
  - [tier 3, corroborating only] If a commercial registered agent is used, log into that provider's dashboard and confirm the Washington representation is active and paid.
  - [tier 5, corroborating only] Look for an annual subscription charge from a commercial registered agent provider.
- **Fix**:
  1. Pull the CCFS record and confirm the registered agent address is a physical Washington street address.
  2. If it is a PO box, vacant, or the agent has resigned, appoint a new agent with a signed consent to serve.
  3. File the change on the Annual Report if inside the 180-day window, otherwise file an Amended Annual Report or Statement of Change (no fee).
- **Source**: https://www.sos.wa.gov/corporations-charities/business-entities/maintain-business-compliance/registered-agents (verified 2026-08-14)
- **Note**: RCW 23.95.405 requires a domestic entity and a registered foreign entity to designate and maintain a registered agent. Page states the address must be physical, 'PO Boxes or PMBs are prohibited'.

### Washington Foreign Entity Registration `wa-foreign-registration`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
If your company was formed in another state but is doing business in Washington, you must register with the Washington Secretary of State by filing a Foreign Registration Statement. You have to attach a Certificate of Existence or Good Standing from your home state that is no more than 60 days old. Once registered, you owe the same annual report and registered agent duties as a Washington entity.
- **Deadline**: Before transacting business in Washington. The registration statement must be accompanied by a home-state certificate of existence issued no more than 60 days before submission.
- **Cost**: $180 filing fee for all business types. Expedited service is an additional $100.
- **Rule out first**:
  - The company has Washington customers but no physical presence, employees or property here, so foreign registration was never triggered even though it collects Washington sales tax under economic nexus. (common) Check: Confirm whether there is a Washington office, employee, inventory or property; economic nexus for tax is a separate and lower bar than transacting business for registration.
  - The entity registered under a slightly different name because its true name was unavailable in Washington, so a name search misses it. (occasional) Check: Search CCFS by the home-state entity name and also by the registered agent, then check the UBI.
- **If it genuinely was missed**: Back fees may apply where a prior registration lapsed and is being re-established.
- **How to prove it**:
  - [tier 1, settles it] Search the company name in CCFS; a registered foreign entity appears with a Washington UBI and a home jurisdiction listed. https://ccfs.sos.wa.gov/
  - [tier 4, settles it] Ask for the filed Foreign Registration Statement and the SOS confirmation letter from the CCFS Notices and Filed Documents folder.
  - [tier 5, corroborating only] Look for a $180 payment to WA Secretary of State around the date Washington operations began.
- **Fix**:
  1. Confirm whether the activity in Washington amounts to transacting business.
  2. Order a Certificate of Existence from the home state dated within 60 days.
  3. File the Foreign Registration Statement in CCFS with the certificate attached and pay $180.
  4. Appoint a Washington registered agent with a physical in-state address as part of the filing.
- **Source**: https://www.sos.wa.gov/sites/default/files/2025-12/6.2025%20-%20Foreign%20Registration%20Statement%20-%20Profit%20Entity%20Type%20(Fillable%20Form).pdf (verified 2026-08-14)
- **Note**: Fees re-verified 2026-08-14 on the SOS online filing instructions for registering a foreign profit corporation (https://www.sos.wa.gov/corporations-charities/business-entities/online-filing-instructions/register-foreign-non-wa-profit-corporation-online), quoted verbatim: 'Filing Fee: $180 in addition to an online processing fee.'; 'You may add expedited priority for an additional $100 at checkout'; and 'a Certificate of Existence/Good Standing or document of similar import from the home jurisdiction issued no more than 60 days before the date of submission must be attached to this filing.' The $180 is corroborated across LLC, profit corporation, LP and LLP on the SOS fee schedule. The Foreign Registration Statement PDF cited as source_url renders but carries no extractable text layer, so its wording could not be quoted directly. Nonprofit corporations must use the separate Foreign Nonprofit Registration form.

### Washington Business License Application (state tax registration) `wa-business-license`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: tax
Washington uses one Business License Application to register you with the Department of Revenue and several other agencies at once, and it issues your Unified Business Identifier (UBI). This is how you get set up to file and pay B&O tax and collect sales tax, and it is also how you tell the state you are hiring employees. There is a processing fee on top of any endorsement fees.
- **Deadline**: Before you begin doing business in Washington, and again (as an update) when you first hire employees.
- **Cost**: $50 processing fee to open or reopen a business/UBI. $0 to add an additional location. $10 for any other purpose, which includes hiring employees or registering a trade name. $5 annual renewal processing fee. Endorsement fees are additional.
- **Rule out first**:
  - The business is registered and current but its only endorsement renews on a cycle you did not check, so a spot look at one month shows no activity. (common) Check: Check the license expiration date in My DOR rather than looking for a recent payment.
  - A remote seller under $100,000 in Washington receipts with no physical presence has no registration duty at all. (occasional) Check: Pull Washington-sourced gross receipts for the current and prior year and compare to $100,000.
- **If it genuinely was missed**: Renewals received after the expiration date are charged a late penalty fee of half of the endorsement fee or up to $150.
- **How to prove it**:
  - [tier 1, settles it] Look up the UBI in the Department of Revenue's Business Lookup to confirm an active registration and open tax accounts. https://dor.wa.gov/
  - [tier 2, settles it] Log into My DOR and confirm the business license is active and the excise tax account is open, with the current renewal date. https://secure.dor.wa.gov/
  - [tier 4, settles it] Ask for the Business License issued by the Business Licensing Service showing the UBI and endorsements.
  - [tier 5, corroborating only] Look for a $50 or $5 payment to WA Business Licensing Service.
- **Fix**:
  1. Apply for or renew the Business License Application through the Business Licensing Service and pay the $50 (or $5 renewal) processing fee.
  2. Add the employment endorsement/update when hiring the first Washington employee (the $10 'any other purpose' fee).
  3. Confirm in My DOR that the excise tax account is open and the filing frequency is assigned.
- **Source**: https://dor.wa.gov/open-business/apply-business-license/variable-business-license-processing-fees (verified 2026-08-14)
- **Note**: Fee amounts quoted verbatim from the DOR variable processing fees page.

### Washington Business & Occupation (B&O) Tax `wa-bo-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: tax
Washington has no corporate income tax. Instead it taxes your gross receipts through the B&O tax, and you cannot deduct labor, materials, taxes or other costs of doing business. Your rate depends on which of more than 50 activity classifications your revenue falls into, and a service business pays a higher rate as it grows. You report it on the Excise Tax Return in My DOR.
- **Deadline**: Reported on the Excise Tax Return in My DOR on the filing frequency the Department of Revenue assigns you (monthly, quarterly or annual). Filing is required even for a period with no business activity.
- **Cost**: Major classification rates: Retailing .00471; Manufacturing .00484; Wholesaling .00484; Service & other activities .015 if under $1,000,000 of such income in the prior year, .0175 from $1,000,000 to $4,999,999, and .021 at $5 million or more.
- **Rule out first**:
  - The business is on an annual filing frequency, so there are no monthly or quarterly payments to find. (common) Check: Check the assigned filing frequency in My DOR before concluding a return was missed.
  - Returns were filed as 'no business activity' during a period with no Washington revenue, so the payment trace is zero but compliance is intact. (common) Check: Look for the filed return in My DOR rather than for a payment.
  - The whole revenue stream qualified for a deduction or exemption (for example interstate and foreign sales), so gross was reported but tax due was nil. (occasional) Check: Read the deduction detail on the filed return.
- **How to prove it**:
  - [tier 2, settles it] Log into My DOR and open the Excise Tax Return history; confirm returns are filed for every period and that the B&O classification lines match the revenue mix. https://secure.dor.wa.gov/
  - [tier 4, settles it] Pull the filed Excise Tax Returns for the last four quarters and tie the gross amounts to the general ledger revenue accounts.
  - [tier 5, corroborating only] Look for recurring WA DEPT REVENUE excise tax payments matching the assigned filing frequency.
- **Fix**:
  1. Confirm the assigned filing frequency in My DOR and list every unfiled period.
  2. Classify each revenue stream to the correct B&O classification and rate before filing.
  3. File the outstanding Excise Tax Returns, including 'no business activity' returns for empty periods.
  4. If Washington activity went unreported for years, ask DOR about the voluntary disclosure program before filing.
- **Source**: https://dor.wa.gov/taxes-rates/business-occupation-tax/business-occupation-tax-classifications (verified 2026-08-14)
- **Note**: Rates quoted verbatim from the DOR B&O classifications table. 'Washington does not have a corporate income tax' is supported by https://dor.wa.gov/taxes-rates/income-tax, which states Washington 'levies other types of taxes such as business and occupation (B&O) tax, retail sales or use tax, public utility tax, and other taxes'; that page also notes a recently enacted income tax on individuals with adjusted gross income of $1,000,000 or more, which is a personal not corporate tax.

### Washington Retail Sales Tax Registration and Economic Nexus `wa-sales-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
If you make retail sales into Washington you register through the Business License Application and then collect and remit sales tax on the same Excise Tax Return you use for B&O tax. The rate is the 6.5% state portion plus a local rate that depends on where the customer receives the goods or services. Sales tax you collect is a trust fund, not your money.
- **Deadline**: Register before making taxable retail sales or on crossing the economic nexus threshold; remit with the Excise Tax Return on your assigned filing frequency.
- **Cost**: The state sales tax rate is 6.5%. The local rate varies by city and county and is sourced to where the customer receives the goods or services.
- **Rule out first**:
  - The company sells only non-taxable services or wholesale-for-resale, so it is registered and filing but collects no retail sales tax. (common) Check: Check whether the returns report the amounts under wholesaling or a deduction rather than retailing, and whether reseller permits are on file.
  - All Washington sales run through a marketplace facilitator that collects and remits on the seller's behalf. (common) Check: Confirm the marketplace facilitator's collection responsibility and that the seller reports the sales with the marketplace deduction.
  - Washington receipts have stayed under $100,000 in both the current and prior year and there is no physical presence. (occasional) Check: Pull Washington-sourced gross receipts for the current and prior calendar year.
- **How to prove it**:
  - [tier 2, settles it] In My DOR, confirm the retail sales tax account is open and that the retailing B&O and retail sales tax lines are populated on recent Excise Tax Returns. https://secure.dor.wa.gov/
  - [tier 3, corroborating only] In the billing or tax engine (Stripe Tax, Avalara, TaxJar), check whether Washington is registered and whether destination-based local rates are being applied.
  - [tier 4, settles it] Reconcile Washington-sourced revenue in the general ledger against the taxable amounts reported on the filed Excise Tax Returns.
- **Fix**:
  1. Measure Washington-sourced gross receipts for the current and prior calendar year against $100,000.
  2. Register through the Business License Application if the threshold is met or physical presence exists.
  3. Turn on destination-based Washington rates in the billing system using the DOR Tax Rate Lookup.
  4. For historical exposure, contact DOR about voluntary disclosure before filing back returns.
- **Source**: https://dor.wa.gov/education/industry-guides/out-state-businesses-reporting-thresholds-and-nexus (verified 2026-08-14)
- **Note**: Nexus threshold quoted verbatim: 'Has more than $100,000 in combined gross receipts sourced or attributed to Washington.' The 200-transaction threshold was eliminated as of March 14, 2019. The 6.5% state rate is from https://dor.wa.gov/taxes-rates/retail-sales-tax, which states 'The state tax rate is 6.5%.'

### Washington Payroll Withholding (no state wage income tax withholding) `wa-payroll-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Washington has no corporate income tax and no general wage income tax, so there is no state income tax withholding registration the way there is in most states. What you do owe on payroll is Paid Family and Medical Leave premiums, the WA Cares long-term care premium, unemployment tax and workers' compensation. You still update your Business License Application when you hire your first Washington employee.
- **Deadline**: Update the Business License Application when you first hire employees in Washington; PFML and unemployment reporting is quarterly.
- **Cost**: $10 Business License Application processing fee for 'any other purpose', which includes hiring employees.
- **Rule out first**:
  - There is no state withholding account number anywhere in the payroll system because Washington simply does not have wage income tax withholding, not because registration was missed. (common) Check: Confirm the payroll system instead holds an ESD employer account number and an L&I account number for Washington.
  - Washington workers are genuine independent contractors, so no employer payroll registration was triggered. (occasional) Check: Test the relationship against L&I's independent contractor tests, which are stricter than the IRS test for workers' compensation purposes.
- **How to prove it**:
  - [tier 2, settles it] Log into My DOR and confirm the business license shows the employment update, and into ESD eServices/EAMS to confirm an employer account exists. https://secure.dor.wa.gov/
  - [tier 3, corroborating only] In the payroll provider (Gusto, Rippling, ADP), check that Washington is set up with ESD and L&I account numbers and that PFML is switched on.
  - [tier 4, settles it] Pull a Washington employee pay stub and confirm PFML and WA Cares deductions appear and that no state income tax line is present.
- **Fix**:
  1. Update the Business License Application to report hiring employees in Washington.
  2. Confirm an ESD employer account and an L&I workers' compensation account both exist.
  3. Switch on PFML and WA Cares withholding in the payroll system and confirm they appear on employee pay stubs.
- **Source**: https://dor.wa.gov/taxes-rates/income-tax (verified 2026-08-14)
- **Note**: DOR income tax page confirms Washington has no corporate income tax and levies B&O, sales/use and other taxes instead; it notes a recently enacted individual income tax for adjusted gross income of $1,000,000 or more, which is not a wage withholding obligation on employers. The $10 'any other purpose' fee covering hiring employees is from the DOR variable business license processing fees page.

### Washington Paid Family & Medical Leave premiums `wa-paid-family-medical-leave`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Washington runs a state paid leave insurance program funded by a premium on wages, collected through the Employment Security Department. You withhold the employee share from every Washington employee's pay and remit it quarterly. Small employers still have to collect and remit the employee share even though they are excused from paying the employer share.
- **Deadline**: Premiums are reported and paid quarterly to the Employment Security Department.
- **Cost**: The premium rate is 1.13% starting January 1, 2026 (it was 0.92% in 2025). Employers pay 28.57% of the total premium and employees pay 71.43%.
- **Rule out first**:
  - The employer has fewer than 50 Washington employees, so it remits only the employee share and the payment looks small relative to headcount. (common) Check: Confirm the ESD size classification and recompute the expected employee-only share at 71.43% of 1.13% of wages.
  - The employer runs an ESD-approved voluntary plan instead of the state plan, so no state premium is remitted. (rare) Check: Ask for the ESD voluntary plan approval letter.
- **How to prove it**:
  - [tier 2, settles it] Log into ESD eServices/Paid Leave and confirm quarterly reports are filed and premiums paid for every quarter with Washington wages. https://esd.wa.gov/
  - [tier 4, settles it] Check a Washington employee pay stub for the Paid Family and Medical Leave deduction line.
  - [tier 5, corroborating only] Look for quarterly ESD premium payments in the bank feed.
- **Fix**:
  1. Confirm the payroll provider is withholding PFML at the current rate for all Washington employees.
  2. File any missing quarterly Paid Leave reports through ESD and pay the premiums due.
  3. Verify the employer size classification so the correct employer share is applied.
- **Source**: https://esd.wa.gov/about-us/news-release/2025/paid-family-medical-leave-premium-rate-increases-113-2026 (verified 2026-08-14)
- **Note**: ESD news release dated October 29, 2025 states verbatim: 'The premium rate will be 1.13%. The rate for 2025 is 0.92%.' and 'Employers will pay 28.57% of the total premium and employees will pay 71.43%.' and 'Businesses classified by Employment Security as having fewer than 50 employees are not required to pay the employer portion of the premium, unless they opt to do so.' The Social Security wage cap applies to premium-liable wages; the specific 2026 cap was not confirmed on a fetched .gov page.

### Washington Unemployment Insurance registration and quarterly reporting `wa-unemployment-insurance`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
If you have employees working in Washington you almost certainly owe state unemployment tax on their wages, administered by the Employment Security Department. You get your employer account by applying for (or updating) the Department of Revenue business license, then file a combined tax and wage report every quarter. You have to file even in a quarter with no payroll.
- **Deadline**: Quarterly tax and wage reports are due on the last day of the month after the last day of each quarter (April 30, July 31, October 31, January 31).
- **Cost**: There is no single flat new-employer rate. For 2026 a new employer pays 115% of the average rate for all businesses in its industry, with a federal minimum of 1%. New-employer status lasts roughly two and a half to three years, after which the rate is experience-rated.
- **Rule out first**:
  - A zero-payroll quarter was filed as a no-payroll report, so there is a filing but no payment. (common) Check: Look for the filed report in eServices rather than for a payment.
  - The organization is a reimbursable employer (often a 501(c)(3)) so it reimburses ESD for actual benefits rather than paying quarterly tax. (occasional) Check: Check the employer's ESD account type for reimbursable status.
  - The only Washington workers are corporate officers who have been properly excluded from coverage, so taxable wages are nil. (occasional) Check: Check the corporate officer coverage election on file with ESD.
- **If it genuinely was missed**: ESD assesses penalties for late or incomplete tax payments and reports; in some cases a penalty can be waived on request.
- **How to prove it**:
  - [tier 2, settles it] Log into ESD eServices or EAMS and confirm an active employer account plus filed quarterly tax and wage reports for every quarter. https://esd.wa.gov/employer-requirements/unemployment-taxes
  - [tier 4, settles it] Pull the quarterly tax and wage reports and reconcile reported wages to the payroll register.
  - [tier 5, corroborating only] Look for quarterly WA ESD tax payments in the last month of each quarter-end month.
- **Fix**:
  1. Apply for the Department of Revenue business license, or update it, to open the ESD employer account.
  2. File every missing quarterly tax and wage report through eServices or EAMS.
  3. Pay the assessed tax and request penalty waiver where a first-time or reasonable-cause ground exists.
- **Source**: https://esd.wa.gov/employer-requirements/unemployment-taxes (verified 2026-08-14)
- **Note**: ESD states new employers must apply for a license from the Department of Revenue before filing a quarterly tax and wage report, that reports are due 'on the last day of the month after the last day of each quarter', and that reimbursable employers reimburse ESD instead of paying unemployment taxes. CORRECTED 2026-08-14: an earlier pass recorded that no 2026 new-employer rate was published. ESD does publish the rule at https://esd.wa.gov/employer-requirements/unemployment-taxes/how-we-determine-tax-rates, quoted verbatim: 'For 2026, you will pay 115% of the average rate for all businesses in your industry.' with a federal minimum rate of 1%. It is industry-indexed rather than a single percentage, which is why no flat figure is given.

### Washington Workers' Compensation (monopolistic L&I state fund) `wa-workers-comp`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
Washington is one of the few states where you cannot buy workers' compensation from a private insurer. You must buy coverage from the Department of Labor & Industries or be a certified self-insured employer, and you report hours and pay premiums quarterly. This catches founders out constantly, because a national payroll or insurance broker cannot sell you a Washington policy.
- **Deadline**: Coverage must be in place before workers perform work. Employers submit quarterly reports and premium payments based on their industry classification and their workers' hours.
- **Cost**: Premium is rate-per-hour-worked by risk classification, not a flat fee. The specific classification rates were not confirmed on a fetched .gov page.
- **Rule out first**:
  - There is no private workers' compensation policy covering Washington because Washington forbids private coverage; the employer buys from L&I instead. (common) Check: Look for an L&I account in the Verify tool rather than for a private policy.
  - The only people working for the company in Washington are exempt owners: corporate officers (up to 8 may be excluded), or LLC members where management is vested in the members. (common) Check: Apply L&I's LLC and corporate officer exclusion rules to the actual management structure, then confirm no non-exempt worker exists.
  - Washington workers are on a PEO or staffing arrangement, so the L&I account sits under the PEO's name. (occasional) Check: Ask the PEO for its L&I account number and confirm the workers are reported on it.
- **How to prove it**:
  - [tier 1, settles it] Look the business up in L&I's Verify tool, which shows whether a workers' compensation account exists and whether the account is current. https://secure.lni.wa.gov/verify/
  - [tier 2, settles it] Log into the L&I employer account and confirm quarterly reports are filed and premiums paid for every quarter with Washington hours. https://www.lni.wa.gov/insurance/insurance-requirements/
  - [tier 4, settles it] Ask for the certified self-insurance certificate if the employer claims self-insured status.
  - [tier 5, corroborating only] Look for quarterly WA L&I premium payments; the absence of a private workers' comp insurance premium for Washington is expected, not a red flag.
- **Fix**:
  1. Search L&I Verify for an existing account before opening a new one.
  2. Open a workers' compensation account with L&I (or apply for certified self-insurance) before any non-exempt worker starts.
  3. Classify each worker's risk class correctly and file the quarterly hours report.
  4. For LLCs, document which members or managers are excluded under L&I's rules and cover everyone who is not.
- **Source**: https://lni.wa.gov/insurance/insurance-requirements/do-i-need-a-workers-comp-account/index (verified 2026-08-14)
- **Note**: L&I states verbatim: 'Washington State does not allow private workers' compensation coverage. You must purchase your coverage from L&I or be a certified self-insured employer.' and 'If you have workers, whether they are employees or independent contractors, you might be required to provide workers' compensation.' LLC exclusion rules confirmed at https://lni.wa.gov/insurance/insurance-requirements/do-i-need-a-workers-comp-account/llc-members: where management is vested in members, members are generally excluded; where there are managers, 'up to 8 maximum of the managers who are also members of the LLC and who exercise substantial control in the daily management of the company are excluded from coverage'. The 8-officer corporate limit was confirmed 2026-08-14 on the L&I corporate officers page at https://lni.wa.gov/insurance/insurance-requirements/do-i-need-a-workers-comp-account/corporate-officers, quoted verbatim: 'The corporation can [exclude] up to 8 officers. If the corporation has more than 8 officers at any time, the corporation may choose which 8 officers, who meet the above criteria, are exempt.' Carve-out: a family corporation, where all officers are related within the third degree, has no numeric limit on exclusions.


## MA (11)

### Massachusetts Annual Report (Secretary of the Commonwealth, Corporations Division) `ma-annual-report`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
Every Massachusetts entity and every out-of-state entity registered here files an annual report with the Corporations Division. The deadline is different for each entity form, which is the thing founders get wrong: corporations run off their fiscal year end, LLCs off their anniversary date, and nonprofits off a fixed November 1. The LLC fee is $500 a year, one of the highest in the country, and there is no online discount.
- **Deadline**: Business corporations (including benefit corporations): within two and one half months after the close of the corporation's fiscal year end, and the report must arrive at the office, not be postmarked, by then. LLCs: on or before the anniversary date of the filing of the original certificate of organization (foreign LLCs, the anniversary of registration). Limited partnerships: on or before the anniversary date of registration. Nonprofit corporations: due November 1.
- **Cost**: Business corporation: $125.00 by mail, $150.00 if late; $100.00 plus a $10.00 expedite fee electronically or by fax ($125.00 plus $10.00 if late). LLC (domestic and foreign): $500.00 by mail, $500.00 plus a $20.00 expedite fee electronically or by fax. Limited partnership: $500.00 by mail, $450.00 plus a $15.00 expedite fee electronically or by fax. Nonprofit corporation: $15.00 by mail, $15.00 plus a $3.50 expedite fee electronically or by fax.
- **Rule out first**:
  - The Corporations Division entity summary does not display an explicit Active/Dissolved status label, so an absent status string does not mean the entity is delinquent. (common) Check: Read the filing history list for recent annual reports, or buy the Certificate of Good Standing.
  - A corporation with a non-calendar fiscal year is due 2.5 months after ITS year end, so a search in March finds nothing wrong for a June year-end company. (common) Check: Read the 'Current Fiscal Month/Day' field on the entity record and compute 2.5 months from there.
  - The entity is a nonprofit of a type excused from filing (school, hospital, religious organization). (occasional) Check: Confirm the nonprofit's classification against the Corporations Division exemption note.
  - A registered agent or law firm filed and paid, so no charge appears on the company's own accounts. (common) Check: Check the Corporations Division filing history directly.
- **If it genuinely was missed**: For corporations, the late fee is $150.00 instead of $125.00. Failure to file reports (or file tax returns or pay taxes under chapter 62C or 63) for 2 or more consecutive years is a ground for administrative dissolution; the Secretary dissolves the corporation if the ground is not cured within 90 days after notice. A dissolved corporation continues to exist but may not carry on business except to wind up. Reinstatement costs $100.00, and a foreign corporation must file annual reports for the last ten fiscal years before reinstating.
- **How to prove it**:
  - [tier 1, settles it] Look the entity up in the Corporations Division search and open the filing history; annual report filings are listed by date. For corporations also read the 'Current Fiscal Month/Day' field, which is what sets the due date. https://corp.sec.state.ma.us/corpweb/corpsearch/CorpSearch.aspx
  - [tier 4, settles it] Ask for the filed annual report confirmation or purchase a Certificate of Good Standing, which attests that annual reports and fees have been filed and paid.
  - [tier 5, corroborating only] Look for a $500 (LLC) or $125 (corporation) payment to the Commonwealth of Massachusetts around the anniversary or fiscal year end.
- **Fix**:
  1. Identify the correct deadline for the entity form: fiscal-year-end plus 2.5 months for corporations, anniversary date for LLCs and LPs, November 1 for nonprofits.
  2. File the outstanding annual report(s) electronically through the Corporations Division online filing system.
  3. If administratively dissolved, file the Application for Reinstatement ($100.00) after bringing all annual reports current; foreign corporations must file the last ten fiscal years.
  4. For a corporation, verify the fiscal month/day on the record is correct, since a wrong one produces a wrong deadline every year.
- **Source**: https://malegislature.gov/Laws/GeneralLaws/PartI/TitleXXII/Chapter156D/Section16.22 (verified 2026-08-14)
- **Note**: Corporate deadline quoted verbatim from M.G.L. c.156D s.16.22 on malegislature.gov: the annual report must be delivered 'within 21/2 months after the end of the fiscal year of the corporation.' The LLC $500 annual report fee is statutory and quoted verbatim from M.G.L. c.156C s.12: 'The fee for the filing of the annual report required by subsection (c) shall be five hundred dollars.' Foreign LLC annual report $500 is quoted verbatim from M.G.L. c.156C s.48. Dissolution grounds from M.G.L. c.156D s.14.20 and s.14.21. IMPORTANT SOURCING CAVEAT: the CORPORATION ($125 / $150 late / $100 electronic) and NONPROFIT ($15, due November 1) fee and deadline figures come from the Secretary of the Commonwealth Corporations Division fee schedule and subject pages at sec.state.ma.us, which is the official state source but is a .us domain, NOT .gov. M.G.L. c.156D s.1.22 delegates corporate fee-setting to regulation rather than fixing amounts, so no .gov-domain source states them. That fee schedule PDF is also stamped 'updated 3/14/22'. Re-check corporate and nonprofit fees at checkout. LLP annual report fees were not verified.

### Massachusetts Registered Agent (corporations) / Resident Agent (LLCs and LPs) `ma-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
Massachusetts requires a continuously maintained agent for service of process in the Commonwealth, but it uses two different names for it. Corporations maintain a registered agent and a registered office; LLCs and LPs maintain a resident agent. The distinction matters because the change-of-agent forms and the statutes are different.
- **Deadline**: Continuous. Changes are made by filing a Statement of Change of Registered Agent/Registered Office (corporations) or Statement of Change of Resident Agent/Office (LLCs).
- **Cost**: $25.00 by mail for both corporations and LLCs; no fee if filed electronically.
- **Rule out first**:
  - The record says 'Resident Agent' rather than 'Registered Agent' and a checklist keyed to the corporate term reports it missing. (common) Check: For an LLC or LP, look for the resident agent field; the terminology differs by entity form, not the requirement.
  - A founder serves as the agent at the company's own Massachusetts address, so there is no agent invoice. (common) Check: Read the agent name on the public record; an individual resident of the Commonwealth is a valid agent.
- **How to prove it**:
  - [tier 1, settles it] Open the entity in the Corporations Division search; the record shows 'The name and address of the Registered Agent' for corporations and 'The name and address of the Resident Agent' for LLCs. https://corp.sec.state.ma.us/corpweb/corpsearch/CorpSearch.aspx
  - [tier 3, corroborating only] If a commercial agent is used, confirm in that provider's dashboard that the Massachusetts appointment is active.
  - [tier 5, corroborating only] Look for an annual registered agent subscription charge.
- **Fix**:
  1. Pull the Corporations Division record and confirm the agent name and Massachusetts address are current.
  2. File the appropriate Statement of Change electronically (no fee) if the agent or office has changed.
  3. For an LLC, confirm the agent is an individual resident of the Commonwealth, a domestic corporation, or a foreign corporation authorized to do business here.
- **Source**: https://malegislature.gov/Laws/GeneralLaws/PartI/TitleXXII/Chapter156D/Section5.01 (verified 2026-08-14)
- **Note**: Corporate requirement also stated verbatim at https://www.sec.state.ma.us/divisions/corporations/filing-by-subject/corporations/corporations-domestic.htm: 'Each corporation must continuously maintain a registered office and a registered agent in the commonwealth.' LLC resident agent requirement from M.G.L. c.156C s.5: the agent 'must be an individual resident of the commonwealth, a domestic corporation, or a foreign corporation authorized to do business in the commonwealth.'

### Massachusetts Foreign Qualification `ma-foreign-qualification`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An entity formed outside Massachusetts that transacts business here must register with the Corporations Division before it starts. Corporations file a Foreign Corporation Certificate of Registration; LLCs file an Application for Registration. Both must be accompanied by a certificate of good standing from the home state that is less than 90 days old, and neither can be filed fully online.
- **Deadline**: For a foreign LLC, the application for registration must be submitted to the state secretary within ten days after it commences doing business in the commonwealth. For a foreign corporation, before transacting business in Massachusetts. In both cases the accompanying home-state certificate of legal existence, good standing or authority must be less than ninety (90) days old.
- **Cost**: Foreign corporation Certificate of Registration: $400.00 by mail or hand delivery, or $375.00 plus a $15.00 expedite fee by fax. Foreign LLC Application for Registration: $500.00 by mail, or $500.00 plus a $20.00 expedite fee by fax. Neither can be filed electronically.
- **Rule out first**:
  - The entity has Massachusetts customers and even sales tax nexus but no office, employees or property here, so foreign qualification was never triggered. (common) Check: Separate the tax nexus question from the transacting-business question; economic nexus for sales tax is a lower bar than qualification.
  - The entity registered under a different name because its home-state name was unavailable in Massachusetts, so a name search misses it. (occasional) Check: Search the Corporations Division by Individual Name (an officer or manager) or by the registered agent, which Massachusetts supports for free.
  - Massachusetts workers are all fully remote employees of an out-of-state parent and the company registered as an employer with DOR and DUA but concluded it was not transacting business. (occasional) Check: Confirm whether the activity meets the transacting-business standard; having Massachusetts employees generally does.
- **If it genuinely was missed**: A registered foreign entity that falls out of compliance can have its authority administratively revoked; reinstatement costs $100.00 and a foreign corporation must file annual reports for the last ten fiscal years first.
- **How to prove it**:
  - [tier 1, settles it] Search the Corporations Division; a registered foreign entity shows 'Entity type: Foreign ...', a 'Date of Registration in Massachusetts', and 'Organized under the laws of' with the home state. https://corp.sec.state.ma.us/corpweb/corpsearch/CorpSearch.aspx
  - [tier 4, settles it] Ask for the filed Certificate of Registration or Application for Registration and the home-state good standing certificate that accompanied it.
  - [tier 5, corroborating only] Look for a $400 or $500 payment to the Commonwealth of Massachusetts near the date Massachusetts operations began.
- **Fix**:
  1. Order a certificate of good standing from the home state dated within 90 days.
  2. File the Foreign Corporation Certificate of Registration ($400) or the foreign LLC Application for Registration ($500) by mail or fax.
  3. Calendar the resulting annual report obligation: corporations 2.5 months after fiscal year end, LLCs on the anniversary of registration.
  4. Appoint a Massachusetts registered or resident agent as part of the filing.
- **Source**: https://malegislature.gov/Laws/GeneralLaws/PartI/TitleXXII/Chapter156C/Section48 (verified 2026-08-14)
- **Note**: Foreign LLC registration is statutory and quoted verbatim from M.G.L. c.156C s.48 on malegislature.gov: 'Every foreign limited liability company doing business in the commonwealth shall submit to the state secretary, within ten days after it commences doing business in the commonwealth, an application for registration' and 'The fee for the filing of the application of registration and each annual report shall be five hundred dollars payable to the state secretary and due at the time of filing.' IMPORTANT SOURCING CAVEAT: the FOREIGN CORPORATION $400.00 fee (and the $375 fax alternative), the 90-day certificate rule, and the cannot-file-electronically restriction come from the Secretary of the Commonwealth Corporations Division fee schedule at sec.state.ma.us, the official state source but a .us domain, NOT .gov. No .gov-domain page states the corporate figure.

### Massachusetts Corporate Excise (C corporations) `ma-corporate-excise`
Applies to: c-corp, benefit-corp | category: tax
Massachusetts taxes corporations with a two-part excise: 8.0% of net income plus $2.60 per $1,000 of Massachusetts tangible property or net worth. If those two measures come to less than the floor, you still owe a minimum excise of $456, so a Massachusetts corporation with zero revenue still writes a check. Filing and payment must be electronic.
- **Deadline**: C corporation returns are due on the 15th day of the fourth month after the end of the corporation's taxable year (April 15 for a calendar-year corporation). Extensions may be available.
- **Cost**: Net income measure 8.0%. Non-income measure $2.60 per $1,000 of taxable Massachusetts tangible personal property or taxable net worth. Minimum excise $456.
- **Rule out first**:
  - The company paid exactly $456 and it looks like a token or erroneous payment; it is the statutory minimum excise for a loss-making year. (common) Check: Match the $456 to the minimum excise line on the filed Form 355.
  - The entity is an LLC taxed as a partnership or disregarded, so it owes no corporate excise in its own right and there is correctly no Form 355. (common) Check: Check the federal classification; Massachusetts follows it. Look for Form 3 instead.
  - No estimated payments appear because the corporation reasonably estimated its excise at $1,000 or less, below the estimated payment trigger. (occasional) Check: Compare prior-year excise to the $1,000 estimated payment threshold.
- **If it genuinely was missed**: Late payment penalty is 1% of the unpaid tax per month or fraction, up to 25%; late filing penalty is 1% of the balance due per month or fraction, up to 25%. Interest runs at the federal short-term rate plus 4%, compounded daily.
- **How to prove it**:
  - [tier 2, settles it] Log into MassTaxConnect and confirm the corporate excise registration is active and Form 355 has been filed for every year since nexus began. https://mtc.dor.state.ma.us/
  - [tier 4, settles it] Pull the filed Form 355 for each open year and confirm the excise paid is at least $456 per year.
  - [tier 5, corroborating only] Look for a MA DOR payment of at least $456 around the 15th day of the fourth month after year end.
- **Fix**:
  1. Register the corporation with DOR through MassTaxConnect (EIN, start date, addresses, officer details).
  2. File Form 355 electronically for every open year, paying at least the $456 minimum excise per year.
  3. Set up estimated payments if the excise is expected to exceed $1,000 for the year.
  4. Ask DOR about penalty abatement where the failure has a reasonable cause.
- **Source**: https://www.mass.gov/info-details/massachusetts-tax-rates (verified 2026-08-14)
- **Note**: Rates read verbatim from the DOR Massachusetts Tax Rates table (page updated December 30, 2025): 'General Business and manufacturing corporations / Net income / Tangible property or net worth / Minimum $456 / 8.0% / $2.60 per $1,000'. Deadline and estimated payment threshold quoted verbatim from https://www.mass.gov/info-details/massachusetts-dor-corporate-excise-tax-guide. Penalty and interest rates from https://www.mass.gov/guides/withholding-taxes-on-wages. Note: mass.gov returns HTTP 403 to automated fetchers; these pages were read through a real browser session.

### Massachusetts Corporate Excise for S corporations `ma-scorp-excise`
Applies to: s-corp | category: tax
A Massachusetts S corporation does not escape the corporate excise. It always owes the non-income measure ($2.60 per $1,000 of tangible property or net worth) and the $456 minimum, and once receipts reach $6 million it owes an entity-level income tax on top. The receipts brackets set the rate, they are not an exemption below $6 million.
- **Deadline**: S corporation returns and payment in full are due on or before the 15th day of the third month after the close of the taxable year. An automatic six-month extension is available to S corporations meeting certain payment requirements.
- **Cost**: Non-income measure $2.60 per $1,000 of taxable Massachusetts tangible personal property or taxable net worth. Minimum excise $456. Income measure: 2.00% of net income subject to tax where gross receipts are $6 million or more but less than $9 million; 3.00% where gross receipts are $9 million or more; 8.0% on certain built-in gains taxable federally under IRC section 1374 and on passive investment income taxable federally under IRC section 1375.
- **Rule out first**:
  - No entity-level income tax was paid because gross receipts were under $6 million, which is correct; only the non-income measure and the $456 minimum apply. (common) Check: Confirm gross receipts against the $6 million bracket on the filed Form 355S.
  - The S corporation filed in the third month rather than the fourth, so a check keyed to the C corporation deadline flags it as early or misfiled. (occasional) Check: S corporations are due one month earlier than C corporations; verify against the S corporation deadline.
- **If it genuinely was missed**: Late payment and late filing penalties of 1% per month each, capped at 25%; interest at the federal short-term rate plus 4%, compounded daily.
- **How to prove it**:
  - [tier 2, settles it] Log into MassTaxConnect and confirm Form 355S is filed for each year and the excise paid is at least $456. https://mtc.dor.state.ma.us/
  - [tier 4, settles it] Pull Form 355S with Schedule S and confirm the receipts bracket applied matches actual gross receipts.
  - [tier 5, corroborating only] Look for a MA DOR payment on or near the 15th day of the third month after year end.
- **Fix**:
  1. File Form 355S electronically for each open year with Schedule S and Schedules SK-1.
  2. Pay at least the $456 minimum excise for every year with Massachusetts nexus.
  3. Recompute the income measure if gross receipts crossed $6 million or $9 million in any year.
- **Source**: https://www.mass.gov/info-details/s-corporations (verified 2026-08-14)
- **Note**: Quoted verbatim: 'An S corporation with gross receipts that are $6 million or more but less than $9 million is subject to the income measure of the corporate excise at a rate of 2.00% on net income subject to tax.'; 'An S corporation with gross receipts that are $9 million or more is subject to the income measure of the corporate excise at a rate of 3.00% on net income subject to tax.'; 'In addition, S corporations, like traditional corporations, are subject to a minimum excise of $456.'; 'An S corporation is subject to the non-income measure of the corporate excise at a rate of $2.60 per $1,000'. Corroborated on the DOR Massachusetts Tax Rates table.

### Massachusetts Form 3 Partnership Return `ma-partnership-form3`
Applies to: partnership, llc | category: tax
A partnership does not pay Massachusetts income tax itself, but it must file an annual information return, Form 3, reporting its income and issuing Schedule 3K-1 to each partner. No tax is paid with it, which is exactly why it gets forgotten, and penalties still apply for failing to file. A multi-member LLC taxed as a partnership files this too.
- **Deadline**: Annually by the 15th day of the third month after the close of the partnership's taxable year (March 15 for a calendar-year partnership).
- **Rule out first**:
  - No payment trace exists because Form 3 carries no tax; the return can be perfectly compliant with zero dollars moving. (common) Check: Look for the filed return in MassTaxConnect, never for a payment.
  - A single-member LLC is disregarded and files no Form 3 at all; its activity belongs on the member's own return. (common) Check: Confirm the federal classification; Massachusetts follows it.
  - The partnership was dormant with no activity and no federal Form 1065 requirement, which is an explicit carve-out. (occasional) Check: Confirm no federal Form 1065 was required for the year.
- **If it genuinely was missed**: No tax payment accompanies Form 3, but the partnership is subject to penalties for failure to file or late filing of the return.
- **How to prove it**:
  - [tier 2, settles it] In MassTaxConnect, confirm a partnership registration and a filed Form 3 for each year. https://mtc.dor.state.ma.us/
  - [tier 4, settles it] Pull the filed Form 3 and the Schedules 3K-1 issued to partners, and tie them to the federal Form 1065 K-1s.
- **Fix**:
  1. Determine whether the partnership has a Massachusetts place of business or more than $100 of Massachusetts-source federal gross income.
  2. File the outstanding Form 3 returns with Schedules 3K-1 for each partner.
  3. Submit copies of the Schedules 3K-1 to DOR with the Form 3.
  4. Request penalty abatement for late-filed returns where reasonable cause exists.
- **Source**: https://www.mass.gov/info-details/partnerships (verified 2026-08-14)
- **Note**: Trigger and deadline quoted verbatim from the DOR partnerships page. Entity types listed cover multi-member LLCs taxed as partnerships; single-member LLCs are excluded because they are disregarded.

### Massachusetts Payroll Withholding Registration (MassTaxConnect) `ma-payroll-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Any employer with employees performing services in Massachusetts must register with DOR through MassTaxConnect and withhold state income tax from wages at 5.00%. Your filing frequency depends on how much you expect to withhold across all employees in a year. Once registered you must file every period even if you withheld nothing.
- **Deadline**: Filing frequency by projected annual withholding: $100 or less, annually by January 31 of the following year. $101 to $1,200, quarterly by the last day of the month following the quarter end. $1,201 to $25,000, monthly by the 15th of the following month, except March, June, September and December which are due the last day of the following month. More than $25,000, quarterly, but when withholding reaches $500 or more by the 7th, 15th, 22nd or last day of a month, pay it over within 3 business days. Annual reconciliation and W-2s: W-2 to each employee by January 31; employers with 50 or more employees file machine-readable W-2s with DOR by the last day of March.
- **Cost**: The withholding rate is 5.00% of wages. For tax year 2026 there is an additional 4% surtax on income exceeding $1,107,750.
- **Rule out first**:
  - A period shows a filed return with zero tax because the employer must file whether or not it withheld anything that period. (common) Check: Confirm the return exists in MassTaxConnect rather than looking for a payment.
  - There are no Massachusetts withholding filings because the only person paid is the owner of a sole proprietorship or a partner, who is not an employee for withholding purposes. (common) Check: Check whether anyone receives a W-2; owners generally make individual estimated payments instead.
  - Deposits look irregular because the employer crossed the $25,000 threshold and moved onto the 3-business-day accelerated rule mid-year. (occasional) Check: Compare projected annual withholding to the frequency table and check for a DOR frequency change notice.
- **If it genuinely was missed**: Late payment penalty 1% of the unpaid tax per month or fraction, up to 25%. Late filing penalty 1% of the balance due per month or fraction, up to 25%. Interest at the federal short-term rate plus 4%, compounded daily. Businesses with more than $25,000 in annual withholding liabilities that fail to make timely deposits are liable for a 5% penalty.
- **How to prove it**:
  - [tier 2, settles it] Log into MassTaxConnect and confirm the withholding registration is active and Form M-941 is filed for every period since registration. https://mtc.dor.state.ma.us/
  - [tier 3, corroborating only] In the payroll provider, confirm the Massachusetts withholding account number is present and the deposit schedule matches the assigned frequency.
  - [tier 4, settles it] Pull a Massachusetts employee pay stub and confirm the state withholding line, then tie the annual total to Form M-3 and the W-2s.
- **Fix**:
  1. Register for withholding in MassTaxConnect (new registrations must file and pay electronically regardless of liability size).
  2. Determine the correct filing frequency from projected annual withholding and file all missing M-941 periods, including zero periods.
  3. File the annual reconciliation and issue and file W-2s (machine-readable if 50 or more employees).
  4. Report new hires, rehires after 30 days off payroll, and contractors earning $600 or more within 2 weeks of the first day of work.
- **Source**: https://www.mass.gov/guides/withholding-taxes-on-wages (verified 2026-08-14)
- **Note**: Frequencies, thresholds, penalties and new hire reporting quoted verbatim from the DOR withholding guide (page updated April 23, 2026). The 5.00% rate and the 2026 surtax threshold of $1,107,750 are from https://www.mass.gov/info-details/massachusetts-tax-rates.

### Massachusetts Unemployment Insurance (DUA) and EMAC `ma-unemployment-insurance`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
Most private employers in Massachusetts must contribute to unemployment insurance once they hit a low threshold: one employee for 13 weeks in a year, or $1,500 in wages in any quarter. Out-of-state employers hit it at just $200 of Massachusetts gross wages in a quarter, which catches remote-hire companies. Separately, once you are past your first three years and have six or more employees, you also owe the Employer Medical Assistance Contribution.
- **Deadline**: Quarterly employment and wage detail reports and contributions: Q1 by 3 p.m. on April 30, Q2 by July 31, Q3 by October 31, Q4 by January 31. DUA sends annual rate notices by January 31; a rate review must be requested before June 20.
- **Cost**: 2026 contribution rates: new employers registered less than 3 years, 2.42%; new construction industry employers, 6.08%; established employers registered 3 or more years pay a rate calculated by DUA annually. EMAC applies to the first $15,000 of each employee's wages per calendar year at 0% in years 1 to 3, 0.12% in year 4, 0.24% in year 5, and 0.34% in year 6 and above.
- **Rule out first**:
  - No EMAC appears because the employer has fewer than 6 employees in the quarter or is within its first three years of unemployment liability, both of which are express exemptions. (common) Check: Check headcount per quarter and the date the employer first became subject to unemployment contributions.
  - The employer is reimbursable (common for nonprofits), so it reimburses DUA for actual benefits rather than paying quarterly contributions. (occasional) Check: Check the DUA account's method of payment.
  - Wages paid are exempt categories: a child under 18 working for a parent, a spouse, or a parent working for their child. (occasional) Check: Check the DUA exempt-wage list against the actual relationships on payroll.
  - The contribution looks small because the employer deferred up to 34% of Quarter 1 and Quarter 2 contributions under the DUA deferral option. (rare) Check: Check the account for an active deferral election.
- **If it genuinely was missed**: Late payments are subject to a 12% interest rate until fully paid.
- **How to prove it**:
  - [tier 2, settles it] Log into Unemployment Services for Employers and confirm an active account, filed quarterly wage detail for every quarter, and the current contribution rate. https://www.mass.gov/info-details/employer-contributions-to-unemployment
  - [tier 4, settles it] Pull the DUA annual rate notice and reconcile the quarterly wage detail to the payroll register.
  - [tier 5, corroborating only] Look for quarterly MA DUA contribution payments near April 30, July 31, October 31 and January 31.
- **Fix**:
  1. Register with DUA through Unemployment Services for Employers as soon as the 13-week or $1,500 threshold is met.
  2. File all missing quarterly employment and wage detail reports and pay contributions plus 12% interest.
  3. Confirm the EMAC year-count and rate, and true up any underpaid EMAC.
  4. Review the annual rate notice each January and request a rate review before June 20 if it looks wrong.
- **Source**: https://www.mass.gov/info-details/employer-contributions-to-unemployment (verified 2026-08-14)
- **Note**: Triggers, 2026 rates, deadlines and the 12% late interest quoted verbatim from the DUA employer contributions page. EMAC wage base and rate ladder quoted verbatim from https://www.mass.gov/info-details/employer-medical-assistance-contribution-emac. The COVID-19 Recovery Assessment remains live for experience-rated employers per https://www.mass.gov/info-details/covid-19-recovery-assessment-rates, but the 2026 percentage is published only in a downloadable PDF and behind employer login and is therefore NOT stated here.

### Massachusetts Paid Family and Medical Leave (PFML) contributions `ma-pfml`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
Massachusetts funds paid family and medical leave through a payroll contribution remitted to the Department of Family and Medical Leave. The rate depends on whether you have 25 or more covered individuals: at 25 or more you owe an employer share, below 25 you only remit what you withhold from workers. The split between family and medical leave changes on January 1, 2027 under new legislation.
- **Deadline**: Contributions are reported and remitted quarterly. Contribution rates are set annually by October 1.
- **Cost**: Employers with 25 or more covered individuals: total contribution 0.88% of eligible wages. Family leave portion 0.18% of eligible wages, up to 100% of which can be withheld from the worker. Medical leave portion 0.70%, of which up to 40% (0.28%) can be withheld from the worker and the employer contributes the remaining 60% (0.42%). Employers with fewer than 25 covered individuals: effective contribution rate 0.46% of eligible wages, with no employer share of the medical leave contribution.
- **Rule out first**:
  - The contribution is 0.46% rather than 0.88% because the employer has fewer than 25 covered individuals and owes no employer share of medical leave. (common) Check: Count covered individuals against the 25 threshold before treating the lower rate as an underpayment.
  - The employer runs a DFML-approved private plan exemption, so no state contribution is remitted. (occasional) Check: Ask for the DFML private plan exemption approval.
  - Contributions stop partway through the year because individual contributions are capped by the Social Security taxable maximum. (common) Check: Compare year-to-date eligible wages to the federal Social Security wage base for the year.
- **How to prove it**:
  - [tier 2, settles it] In MassTaxConnect, confirm the PFML account is registered and quarterly contributions are filed for every quarter with Massachusetts wages. https://mtc.dor.state.ma.us/
  - [tier 3, corroborating only] In the payroll provider, confirm PFML is enabled and the correct rate tier (25+ or under 25) is applied.
  - [tier 4, settles it] Check a Massachusetts pay stub for the PFML withholding line and the W-2 Box 14 (or 1099-MISC Box 16) labelled 'MAPFML'.
- **Fix**:
  1. Count covered individuals to determine the correct rate tier.
  2. Enable PFML withholding in payroll at the correct rate and confirm the MAPFML label on W-2 Box 14.
  3. File and pay any missing quarterly PFML contributions through MassTaxConnect.
  4. Plan for the January 1, 2027 change: Chapter 101 of the Acts of 2026 shifts employer contributions from medical leave to family leave, and the 2027 total rate is not yet set.
- **Source**: https://www.mass.gov/info-details/paid-family-and-medical-leave-employer-contribution-rates-and-calculator (verified 2026-08-14)
- **Note**: Rates and the 25-covered-individual threshold quoted verbatim from the DFML rates page (last updated July 10, 2026), including: 'Employers are only required to send an employer contribution if they have 25 or more covered individuals in their workforce.' and 'Employers with fewer than 25 covered individuals must send an effective contribution rate of 0.46% of eligible wages.' The 2027 change is quoted verbatim from the same page. CAVEAT added 2026-08-14: Chapter 101 of the Acts of 2026 is a real session law (https://malegislature.gov/Laws/SessionLaws/Acts/2026/Chapter101, approved June 12, 2026) and its sections 25 and 26 do make the family/medical swap in G.L. c.175M s.6, but the act contains NO effective-date clause for those two sections. Its effective-date provisions name other sections only, and section 43(a) merely directs guidance on the impact 'in calendar year 2027'. So 'January 1, 2027' is DFML's rate-year framing, not statutory text; do not cite it as an effective-date clause. The wage cap is stated by DFML only as 'capped by the Social Security taxable maximum'; no dollar figure is given on any DFML page, so none is stated here.

### Massachusetts Workers' Compensation Insurance `ma-workers-comp`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
Massachusetts requires workers' compensation for every employee from the first hour worked, with no headcount minimum and no hours minimum except for domestic employees, who must work at least 16 hours a week to be covered. Family members count, so a company whose only staff are relatives still needs a policy. The enforcement is fast and expensive: the Department of Industrial Accidents issues stop work orders with fines that accrue every single day including weekends.
- **Deadline**: Coverage must be in force before any employee performs work. There is no grace period.
- **Cost**: Premium is set by the carrier based on classification and payroll; Massachusetts is not a monopolistic state and coverage is bought on the private market.
- **Rule out first**:
  - No policy exists in the company's name because the only workers are LLC members, LLP partners, or a sole proprietor, who are not required to cover themselves. (common) Check: Confirm there is no non-member employee; the self-exemption does not extend to employees who are not members or partners.
  - A corporate officer is not on the policy because they filed for the exemption available to officers owning at least 25% of the corporation. (common) Check: Ask for the filed officer exemption; note this is a request-based exemption, unlike the automatic LLC member one.
  - Coverage exists but under a PEO's master policy, so no direct carrier relationship shows in the company's records. (occasional) Check: Ask the PEO for a certificate of insurance naming the client company.
  - Massachusetts employees are covered under an out-of-state policy that lists Massachusetts in section 3A. (common) Check: Read section 3A of the policy information page, or request Form 154 from the carrier.
- **If it genuinely was missed**: The DIA Office of Investigations issues a stop work order to uninsured employers. Minimum fines are $100 per day including weekends and holidays, beginning on the date the stop work order was issued, accruing until insurance starts AND the fine is paid. If the order is not appealed the business must close immediately until coverage is proved and fines paid; if it is appealed the fines rise to $250 per day and the business may remain open. Employers issued stop work orders may face criminal charges including up to 1 year in prison and/or a fine of up to $1,500 on conviction, and are subject to debarment from public contracts for 3 years.
- **How to prove it**:
  - [tier 1, settles it] Check the DIA's insurance coverage verification for a current policy on file for the employer. https://www.mass.gov/info-details/workers-compensation-insurance-requirements
  - [tier 2, corroborating only] Confirm no open stop work order exists against the employer with the DIA Office of Investigations.
  - [tier 4, settles it] Ask for the certificate of insurance and confirm Massachusetts appears in section 3A of the policy information page; for 'all states' language, get Form 154 verification from the carrier.
  - [tier 5, corroborating only] Look for a workers' compensation premium payment to a private carrier or a pay-as-you-go deduction inside the payroll provider's invoice.
- **Fix**:
  1. Buy a Massachusetts workers' compensation policy from a licensed carrier before any employee starts.
  2. For an existing out-of-state policy, have the carrier add Massachusetts to section 3A of the information page.
  3. For corporate officers who want out, file the exemption request; confirm the officer owns at least 25%.
  4. If a stop work order has issued, decide quickly whether to appeal: not appealing means closing, appealing raises the fine to $250 per day but keeps the business open.
  5. Post the required notice of coverage conspicuously at the worksite.
- **Source**: https://www.mass.gov/info-details/workers-compensation-insurance-requirements (verified 2026-08-14)
- **Note**: Quoted verbatim: 'All employers operating in Massachusetts are required to carry workers' compensation insurance for their employees and themselves if they are an employee of their company.'; 'The requirement applies no matter the number of hours worked or the number of employees.'; 'Minimum fines are $100 per day, including weekends and holidays'; 'If you appeal your SWO, then the fines go up to $250 per day'. Member/officer rules quoted verbatim from https://www.mass.gov/info-details/who-is-covered-by-workers-compensation-insurance: LLC members, LLP partners and sole proprietors 'aren't required to carry workers' compensation insurance for themselves', while 'Corporate officers who own at least 25% interest in the corporation can request an exemption'. CORRECTED 2026-08-14: the requirements page carries one carve-out to the no-hours-minimum rule, quoted verbatim, 'The only exception is for domestic employees who must work at least 16 hours a week', which an earlier pass omitted. mass.gov returns HTTP 403 to automated fetchers; these pages were read through a real browser session.

### Massachusetts Sales and Use Tax Registration and Economic Nexus `ma-sales-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
Massachusetts charges 6.25% sales tax with no local add-on, so the rate is the same everywhere in the state. Remote sellers must register once they exceed $100,000 of Massachusetts sales in a calendar year; there is no transaction-count trigger. SaaS founders should note that standardized software is taxable whether downloaded or accessed on a remote server.
- **Deadline**: Filing frequency by annual sales/use tax collected: $100 or less, annually by the 30th day following the year; $101 to $1,200, quarterly by the 30th day following the quarter; $1,201 or more, monthly by the 30th day following the month. Returns are due for every period even when no tax is due. Taxpayers with over $150,000 in cumulative tax liability in the prior year must make advance payments.
- **Cost**: The Massachusetts sales tax is 6.25% of the sales price or rental charge of tangible personal property and telecommunications services. Use tax is also 6.25%. There is no local sales tax add-on for general tangible personal property.
- **Rule out first**:
  - Massachusetts sales stayed under $100,000 in the calendar year and there is no physical presence, so there is genuinely no registration duty. (common) Check: Pull Massachusetts-delivered gross revenue for the current and prior calendar year.
  - A marketplace facilitator collects and remits on the seller's behalf, so the seller's own returns show little or no Massachusetts tax. (common) Check: Confirm the marketplace's collection responsibility and the channel split of Massachusetts revenue.
  - Revenue is digital products other than software (music, video, reading material delivered electronically), which are not subject to Massachusetts tax. (occasional) Check: Classify the product: standardized software is taxable however delivered, other digital products delivered electronically are not.
  - Zero returns are filed with no payment, which is required behaviour, not neglect. (common) Check: Look for the filed return in MassTaxConnect rather than for a payment.
- **If it genuinely was missed**: Late payment and late filing penalties of 1% per month each, capped at 25%. Interest at the federal short-term rate plus 4%, compounded daily. A 20% underpayment penalty applies where the underpayment exceeds 10% of the tax required to be shown on the return or $1,000, whichever is greater.
- **How to prove it**:
  - [tier 2, settles it] Log into MassTaxConnect and confirm the sales/use tax registration and a filed ST-9 (or STS for services) for every period. https://mtc.dor.state.ma.us/
  - [tier 3, corroborating only] In the tax engine or billing system, confirm Massachusetts is registered and the flat 6.25% is applied, and check whether standardized software revenue is being taxed.
  - [tier 4, settles it] Ask for the Sales and Use Tax Registration Certificate (Form ST-1), which must be displayed at each business location, and reconcile Massachusetts revenue to the filed returns.
- **Fix**:
  1. Measure Massachusetts-delivered sales against $100,000 for the current and prior calendar year.
  2. Register with DOR through MassTaxConnect and display Form ST-1 at each location.
  3. File all outstanding ST-9 returns electronically, including zero returns.
  4. Review whether standardized software or remote-access software revenue should have been taxed, since this is the most common Massachusetts miss for software companies.
- **Source**: https://www.mass.gov/guides/sales-and-use-tax (verified 2026-08-14)
- **Note**: Economic nexus quoted verbatim: a vendor includes one who 'Makes remote sales to Massachusetts customers that exceed $100,000 in a calendar year'. The vendor definition contains no transaction-count prong, so Massachusetts is a dollar-only economic nexus state. Rate corroborated on https://www.mass.gov/info-details/massachusetts-tax-rates ('Sales and use tax ... 6.25%'). Software treatment quoted verbatim from the same guide. Page updated May 7, 2026.


## IL (10)

### Illinois Annual Report (Secretary of State) `il-annual-report`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
Every Illinois corporation, LLC, LP and nonprofit, plus every foreign entity qualified here, files an annual report with the Secretary of State. The filing window is narrow: 60 days ending on the last day of the month before your anniversary month, so there is no long grace period. For corporations the annual report is also the vehicle that reports paid-in capital and computes franchise tax.
- **Deadline**: The annual report, with all fees and taxes, must be delivered to the Secretary of State within 60 days immediately preceding the first day of the anniversary month (the month of incorporation, organization or qualification). Mailing before the first day of the anniversary month, properly addressed with postage prepaid, counts as compliance. The same 60-day rule applies to corporations, LLCs and nonprofits.
- **Cost**: Corporation (domestic or foreign), $75. LLC (domestic or foreign), $75, plus $50 for each series with a certificate of designation in effect. Not-for-profit corporation, $10. Limited partnership, $100. Expedited service is an additional $50 for corporations, LLCs and LPs, and $25 for nonprofits.
- **Rule out first**:
  - Nothing was filed this calendar quarter because the anniversary month is months away; Illinois keys the deadline to the formation month, not to a fixed date. (common) Check: Read the Date of Formation/Registration on the File Detail Report and derive the anniversary month.
  - The corporation shows $0 franchise tax on the report and it looks like an omission, but the first $10,000 of franchise tax liability is exempt, so most corporations correctly owe nothing. (common) Check: Compute 0.1% of Illinois-allocated paid-in capital and compare to the $10,000 exemption.
  - A registered agent service filed and paid, so there is no charge in the company's own records. (common) Check: Check the File Detail Report status rather than the bank feed.
  - The entity is a general partnership, which has no Secretary of State annual report obligation at all. (occasional) Check: Confirm the entity form; only corporations, LLCs, LPs, LLPs and nonprofits file.
- **If it genuinely was missed**: LLC: a penalty of $100 plus $100 for each year or fraction beginning with the second year of delinquency, if not cured before the first day of the second month after the anniversary month. Nonprofit: $3. Corporation: a penalty of 10% of the amount of any delinquent franchise tax due for the report, plus interest of 2% for each month or part month delinquent, or $1, whichever is greater. Administrative dissolution follows 90 days after a Notice of Delinquency for corporations and nonprofits, and 120 days for LLCs. Reinstatement is $200 for a corporation or LLC and $25 for a nonprofit. A dissolved corporation's name is locked up for 3 years.
- **How to prove it**:
  - [tier 1, settles it] Run a free Business Entity Search and open the File Detail Report, which shows the entity's active/inactive status, formation date and jurisdiction. https://apps.ilsos.gov/businessentitysearch/
  - [tier 3, settles it] Purchase a Certificate of Good Standing ($25 corporation or LLC, $5 nonprofit) for a definitive standing answer. https://www.ilsos.gov/departments/business-services/business-searches.html
  - [tier 5, corroborating only] Look for a $75 (or $10, or $100) payment to Illinois Secretary of State in the 60 days before the anniversary month.
- **Fix**:
  1. Look up the formation date to fix the anniversary month, then set a reminder 60 days before the first of that month.
  2. File the annual report online with the Secretary of State and pay the fee for the entity type.
  3. For an LLC already delinquent, expect $100 plus $100 per additional year of delinquency on top of the $75.
  4. If administratively dissolved, file the reinstatement application ($200 corporation or LLC, $25 nonprofit) together with all missed annual reports.
- **Source**: https://www.ilga.gov/legislation/ilcs/fulltext?DocName=080500050K14.10 (verified 2026-08-14)
- **Note**: Deadline quoted verbatim from 805 ILCS 5/14.10: 'shall be delivered to the Secretary of State within 60 days immediately preceding the first day of the anniversary month'. Identical LLC rule at 805 ILCS 180/50-1(b) and nonprofit rule at 805 ILCS 105/114.10. Fees from 805 ILCS 5/15.10(o) ('Filing an annual report ... of a domestic or foreign corporation, $75'), 805 ILCS 180/50-10(b)(11) (LLC $75 plus $50 per series), 805 ILCS 105/115.10(m) (nonprofit $10), and the SOS LP fee table ($100). LLC penalty from 805 ILCS 180/50-15(b)(1); corporate penalty from 805 ILCS 5/16.05(a) and (f); nonprofit penalty from 805 ILCS 105/116.05(a). Dissolution timing from 805 ILCS 5/12.40(b), 805 ILCS 180/35-30(b) and 805 ILCS 105/112.40(b). NOT VERIFIED: whether the Secretary of State assesses any separate flat-dollar late fee on a corporate annual report; the statute expresses the corporate penalty only as a percentage of delinquent franchise tax.

### Illinois Franchise Tax (still in force, with a $10,000 liability exemption) `il-franchise-tax`
Applies to: c-corp, s-corp, benefit-corp | category: tax
Illinois legislated a franchise tax phase-out and then reversed it, so the tax still exists in 2026. What changed is the exemption: on and after January 1, 2025 the first $10,000 of franchise tax liability is exempt. Since the rate is 0.1% of Illinois-allocated paid-in capital, that means a corporation with under $10 million of Illinois paid-in capital computes a real liability and then owes nothing. You still file the annual report and still report paid-in capital.
- **Deadline**: The annual franchise tax is payable each year with the annual report, within the 60 days immediately preceding the first day of the anniversary month. An initial franchise tax is due at the time of filing the first report of issuance of shares (domestic) or the application for authority (foreign), and an additional franchise tax on increases in paid-in capital.
- **Cost**: Rate: 1/10 of 1% of paid-in capital represented in Illinois. Statutory floor $25 and ceiling $2,000,000 per annum before the exemption. Exemption schedule: on or after January 1, 2020 and prior to January 1, 2021 the first $30 in liability is exempt; on or after January 1, 2021 and prior to January 1, 2024 the first $1,000; on or after January 1, 2024 and before January 1, 2025 the first $5,000; on and after January 1, 2025 the first $10,000 in liability is exempt.
- **Rule out first**:
  - The corporation paid only the $75 report fee and no franchise tax, which is correct for any corporation whose Illinois paid-in capital is under roughly $10 million, because the first $10,000 of liability is exempt. (common) Check: Multiply Illinois-allocated paid-in capital by 0.1% and compare to $10,000.
  - An LLC shows no franchise tax at all, which is correct; Illinois franchise tax applies only to corporations. (common) Check: Confirm the entity form; the LLC Act imposes no franchise tax.
  - A stale checklist expects a $1,000 exemption and flags an underpayment; the $1,000 figure was correct only for 2021 through 2023. (common) Check: Read the current exemption schedule in 805 ILCS 5/15.35, which reaches $10,000 on and after January 1, 2025.
  - The corporation elected to pay franchise tax on its entire paid-in capital rather than allocating, producing a higher figure than expected. (occasional) Check: Check item (h) of the annual report, where a corporation may elect the entire paid-in capital basis.
- **If it genuinely was missed**: A penalty of 10% of the amount of any delinquent franchise tax due for the report, plus interest of 2% for each month or part of a month it is delinquent, or $1, whichever is greater.
- **How to prove it**:
  - [tier 1, corroborating only] Confirm the corporation is in good standing, which requires the annual report and any franchise tax to have been paid. https://apps.ilsos.gov/businessentitysearch/
  - [tier 4, settles it] Read the paid-in capital figure and franchise tax computation on the filed corporate annual report (Form BCA 14.05).
  - [tier 5, corroborating only] Look for an Illinois Secretary of State payment materially larger than the $75 annual report fee, which would indicate real franchise tax.
- **Fix**:
  1. Determine Illinois-allocated paid-in capital as of the close of the fiscal year on or before the last day of the third month prior to the anniversary month.
  2. Apply 0.1%, then subtract the $10,000 exemption; pay only the excess.
  3. File the annual report with the franchise tax computation inside the 60-day window.
  4. If delinquent, expect the 10% penalty on delinquent franchise tax plus 2% per month interest, which is small or nil where the tax itself is fully exempted.
- **Source**: https://www.ilga.gov/legislation/ilcs/fulltext?DocName=080500050K15.35 (verified 2026-08-14)
- **Note**: Exemption schedule quoted verbatim from 805 ILCS 5/15.35: 'On or after January 1, 2024, and before January 1, 2025, the first $5,000 in liability is exempt from the tax imposed under this Section. On and after January 1, 2025, the first $10,000 in liability is exempt from the tax imposed under this Section.' (Source: P.A. 102-16, 103-8, 103-592.) The parallel foreign-corporation provision is 805 ILCS 5/15.65. Rate, floor and ceiling quoted verbatim from 805 ILCS 5/15.45: 'computed at the rate of 1/10 of 1% ... but in no event shall the amount of the annual franchise tax be less than $25 nor more than $2,000,000 per annum.' Both the statutory text and an independent second research pass confirmed the tax survives with no repealer. The $10,000 exemption was re-read directly from the live statute on 2026-08-14. URL NOTE (applies to every ILCS citation in this file): ilga.gov retired the 'fulltext.asp?DocName=' path, which now returns HTTP 404. The live path is 'fulltext?DocName=' without the .asp, and all five Illinois source_url values here were corrected to it on 2026-08-14. NOT VERIFIED: a .gov page narrating in prose that the earlier phase-out was itself repealed; the conclusion rests on the current statutory text and its public act citations.

### Illinois Registered Agent and Registered Office `il-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
Every Illinois corporation, LLC and foreign entity qualified here must continuously maintain a registered office and a registered agent in Illinois. The agent must be an Illinois resident individual or an entity authorized to transact business in Illinois, with a business office identical to the registered office. Losing your agent is an independent ground for administrative dissolution, separate from missing the annual report.
- **Deadline**: Continuous. If a registered agent resigns, the entity has 60 days from the Secretary of State's notification to appoint and maintain a replacement.
- **Cost**: $25 to file a statement of change of registered office or registered agent for a corporation or an LLC; $5 for a nonprofit.
- **Rule out first**:
  - The agent is a founder at the company's own Illinois office, so there is no agent invoice; an individual resident of Illinois is a valid agent. (common) Check: Read the agent name on the File Detail Report.
  - The agent recently resigned and the record looks broken, but the entity is inside its 60-day replacement window. (occasional) Check: Check the date of the Secretary of State's notification against the 60-day cure period.
  - The registered office differs from the principal place of business and looks wrong; Illinois expressly allows the registered office to be a different address. (common) Check: Confirm the agent's business office is identical with the registered office, which is the actual statutory requirement.
- **If it genuinely was missed**: Failure to maintain a registered agent is an independent ground for administrative dissolution (805 ILCS 5/12.35(e) for corporations, 805 ILCS 180/35-25(3) for LLCs) and makes an LLC delinquent and not in good standing under 805 ILCS 180/50-15(a)(2).
- **How to prove it**:
  - [tier 1, settles it] Open the File Detail Report in the free Business Entity Search; it shows the registered agent name and the registered office address. You can also search the database BY registered agent. https://apps.ilsos.gov/businessentitysearch/
  - [tier 3, corroborating only] If a commercial agent is used, confirm the Illinois appointment is active in that provider's dashboard.
  - [tier 5, corroborating only] Look for an annual registered agent subscription charge.
- **Fix**:
  1. Pull the File Detail Report and confirm the agent name and Illinois registered office address.
  2. File the statement of change of registered agent or office ($25, or $5 for a nonprofit) if either is stale.
  3. If an agent has resigned, appoint a replacement within 60 days of the Secretary of State's notification to avoid delinquency.
- **Source**: https://www.ilga.gov/legislation/ilcs/fulltext?DocName=080500050K5.05 (verified 2026-08-14)
- **Note**: Corporate requirement quoted verbatim from 805 ILCS 5/5.05: 'Each domestic corporation and each foreign corporation having authority to transact business in this State shall have and continuously maintain in this State: (a) A registered office ... (b) A registered agent'. LLC requirement quoted verbatim from 805 ILCS 180/1-35(a): 'Each limited liability company and foreign limited liability company shall continuously maintain in this State a registered agent and registered office'. Fees from 805 ILCS 5/15.10(h), 805 ILCS 180/50-10(b)(15) and 805 ILCS 105/115.10(g).

### Illinois Foreign Qualification `il-foreign-qualification`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An entity formed outside Illinois that transacts business here must apply to the Secretary of State for authority. Corporations file Form BCA 13.15 and LLCs file Form LLC 45.5, each $150. A foreign corporation also owes an initial franchise tax when it files, though the $10,000 liability exemption usually zeroes that out.
- **Deadline**: Before transacting business in Illinois.
- **Cost**: Foreign corporation Application for Authority to Transact Business (BCA 13.15): $150, plus $100 for expedited service. Foreign LLC Application for Admission to Transact Business (LLC 45.5): $150, or $400 for a series LLC, plus $100 expedited. Foreign nonprofit application for authority: $50. Foreign LP Application for Certificate of Authority: $150. Amended authority $25; withdrawal $25.
- **Rule out first**:
  - The company has Illinois customers and collects Illinois sales tax under the $100,000 economic nexus test but has no Illinois office, employees or inventory, so qualification was never triggered. (common) Check: Separate the tax nexus question from the transacting-business question.
  - A search by trading name misses the entity because it qualified under its exact home-state legal name or an assumed name. (occasional) Check: Search the Business Entity Search by registered agent, president or file number, all of which Illinois supports for free.
  - No franchise tax was paid with the application, which is normal: the initial franchise tax is fully covered by the $10,000 liability exemption for most companies. (common) Check: Compute 0.1% of Illinois-allocated paid-in capital against the $10,000 exemption.
- **If it genuinely was missed**: Failure to maintain the annual report or a registered agent leads to administrative revocation on the same timetable as domestic entities.
- **How to prove it**:
  - [tier 1, settles it] Search the free Business Entity Search; a qualified foreign entity appears with an Illinois file number and a Jurisdiction field showing the home state. https://apps.ilsos.gov/businessentitysearch/
  - [tier 4, settles it] Ask for the filed Application for Authority (BCA 13.15) or Application for Admission (LLC 45.5) and the Secretary of State's acceptance.
  - [tier 5, corroborating only] Look for a $150 payment to Illinois Secretary of State near the date Illinois operations began.
- **Fix**:
  1. Confirm whether Illinois activity amounts to transacting business.
  2. File Form BCA 13.15 (corporation) or LLC 45.5 (LLC) with the $150 fee, naming an Illinois registered agent.
  3. Compute and pay any initial franchise tax, applying the $10,000 exemption.
  4. Calendar the annual report to the 60-day window before the qualification anniversary month.
- **Source**: https://www.ilga.gov/legislation/ilcs/fulltext?DocName=080500050K15.10 (verified 2026-08-14)
- **Note**: Corporate fee quoted verbatim from 805 ILCS 5/15.10(j): 'Filing an application of a foreign corporation for authority to transact business in this State, $150.' LLC fee quoted verbatim from 805 ILCS 180/50-10(b)(1), which prices 'application for admission (foreign)' at $150 and $400 for a series LLC. Nonprofit $50 from 805 ILCS 105/115.10(h). Initial foreign franchise tax from 805 ILCS 5/15.65(a). Expedited fees and the LP figure from the Secretary of State published fee tables at ilsos.gov.

### Illinois Corporate Income Tax and Personal Property Replacement Income Tax `il-income-and-replacement-tax`
Applies to: c-corp, s-corp, llc, partnership, benefit-corp | category: tax
Illinois taxes C corporations at 7% income tax plus 2.5% Personal Property Replacement Tax, so the effective entity-level rate is 9.5%. Pass-through entities escape the income tax but still owe Replacement Tax at 1.5%, which surprises founders who assume an S corp or LLC pays nothing at the entity level in Illinois.
- **Deadline**: IL-1120 (C corporation): on or before the 15th day of the 4th month following the close of the tax year, or the 15th day of the 3rd month if the year ends June 30; automatic seven-month extension (eight months for a June 30 year end). IL-1120-ST (S corporation): on or before the 15th day of the 3rd month following the close of the taxable year; automatic seven-month extension. IL-1065 (partnership): on or before the 15th day of the 4th month following the close of the taxable year; automatic six-month extension.
- **Cost**: Corporate income tax: 7 percent of net income (effective July 1, 2017). Personal Property Replacement Tax: 2.5 percent of net income for corporations other than S corporations; 1.5 percent of net income for partnerships, trusts and S corporations.
- **Rule out first**:
  - An S corporation or partnership paid Illinois tax despite being a pass-through, which is correct: Replacement Tax at 1.5% is an entity-level tax. (common) Check: Match the payment to the Replacement Tax line on IL-1120-ST or IL-1065.
  - A corporation with a loss still filed a return, which is required: qualification to do business plus a federal filing obligation triggers IL-1120 regardless of net income or loss. (common) Check: Read the filing requirement, which does not depend on profitability.
  - The return was filed months after the deadline but no penalty applies because Illinois grants an automatic extension (seven months for corporations, six for partnerships) with no application. (common) Check: Check whether the filing date falls inside the automatic extension window.
  - A single-member LLC filed nothing at the entity level, which reflects disregarded-entity treatment flowing to the owner's return. (occasional) Check: Confirm the federal classification. Note the Illinois rate page addresses partnerships, trusts and S corporations but does not expressly address disregarded entities.
- **How to prove it**:
  - [tier 2, settles it] Log into MyTax Illinois and confirm the income tax account is open and IL-1120, IL-1120-ST or IL-1065 is filed for every year with Illinois activity. https://mytax.illinois.gov/
  - [tier 4, settles it] Pull the filed Illinois return and confirm the Replacement Tax line is present, since it is the line most often omitted for pass-through entities.
  - [tier 5, corroborating only] Look for Illinois Department of Revenue payments around the return deadline.
- **Fix**:
  1. Identify the correct return for the entity form: IL-1120, IL-1120-ST or IL-1065.
  2. File all open years, remembering the automatic extension lengths before assuming a return is late.
  3. Confirm the Replacement Tax line is completed, especially for S corporations and partnerships.
  4. Evaluate the pass-through entity tax election, available for tax years ending on or after December 31, 2021.
- **Source**: https://tax.illinois.gov/research/taxrates/income.html (verified 2026-08-14)
- **Note**: Rates quoted verbatim from the IDOR tax rate page: 'Corporations - 7 percent of net income'; 'Personal Property Replacement Tax / Corporations - (other than S corporations) / 2.5 percent of net income / Partnerships, trusts, and S corporations / 1.5 percent of net income'. Deadlines and automatic extensions quoted verbatim from IDOR answers pages for IL-1120, IL-1120-ST and IL-1065. NOT VERIFIED: whether a single-member LLC treated as a disregarded entity owes Replacement Tax in its own right; the IDOR rate page does not address disregarded entities.

### Illinois Withholding Income Tax Registration and IL-941 `il-payroll-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
If you pay Illinois wages you register with the Department of Revenue using Form REG-1 through MyTax Illinois and withhold 4.95%. The IL-941 return is always quarterly and must be filed electronically; only your payment schedule changes, from monthly to semi-weekly once you cross $12,000 of withholding in the look-back period. Unlike the federal system, Illinois has no annual reconciliation return.
- **Deadline**: Form IL-941 is due quarterly, by the last day of the month that follows the end of the quarter. Monthly IL-501 payments are due by the 15th day of the month following the month in which the tax was withheld. Semi-weekly IL-501 payments are due by Wednesday for amounts withheld on the preceding Wednesday, Thursday or Friday, and by Friday for amounts withheld on the preceding Saturday, Sunday, Monday or Tuesday.
- **Cost**: The withholding rate is 4.95 percent of net income (effective July 1, 2017).
- **Rule out first**:
  - There is no annual reconciliation filing and it looks like a gap; Illinois deliberately does not have one, unlike the federal system. (common) Check: Confirm the four quarterly IL-941 returns exist; that is the complete annual set.
  - Payment frequency changed mid-year from monthly to semi-weekly, making deposits look erratic. (occasional) Check: Check whether withholding exceeded $12,000 in a quarter, which forces the switch in the following quarter.
  - A registration submitted on paper appears missing for weeks; IDOR states paper Form REG-1 processing takes six to eight weeks versus one to two business days through MyTax Illinois. (occasional) Check: Check the submission channel and date before concluding registration failed.
- **How to prove it**:
  - [tier 2, settles it] Log into MyTax Illinois and confirm the withholding account is registered and every IL-941 quarter is filed. https://mytax.illinois.gov/
  - [tier 3, corroborating only] In the payroll provider, confirm the Illinois withholding account number is present and the deposit schedule matches the assigned monthly or semi-weekly frequency.
  - [tier 4, settles it] Pull an Illinois pay stub and confirm the 4.95% state withholding line, then tie the quarterly totals to the filed IL-941s.
- **Fix**:
  1. Register through MyTax Illinois using Register a New Business (Form REG-1), which processes in one to two business days.
  2. Determine the payment schedule from the look-back period against the $12,000 threshold.
  3. File all missing IL-941 quarters electronically, which is mandatory.
  4. If assigned to semi-weekly, set up electronic payments, which are required at that tier.
  5. Register with IDES at the same time through MyTax Illinois if you have employees.
- **Source**: https://tax.illinois.gov/research/publications/pubs/withholding-income-tax-payment-and-filing-requirements.html (verified 2026-08-14)
- **Note**: Quoted verbatim from IDOR Publication 131: 'All Forms IL-941 must be filed electronically. Your Form IL-941 return is due quarterly.'; 'Unlike the federal government, Illinois does not have an annual reconciliation return.'; the $12,000 look-back threshold and the definition 'The look-back period is the one-year period ending on June 30 of the immediately preceding calendar year.' Registration language quoted verbatim from https://tax.illinois.gov/businesses/registration.html. The 4.95% rate is from https://tax.illinois.gov/research/taxrates/income.html.

### Illinois Unemployment Insurance (IDES) registration and contributions `il-unemployment-insurance`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
You must register a new business with the Illinois Department of Employment Security within 30 days of start-up, and you become liable for contributions once you pay $1,500 in wages in a single calendar quarter or employ someone for 20 weeks in a year. Nonprofits have a different and higher trigger. Contributions are only owed on the first $14,250 of each worker's 2026 wages.
- **Deadline**: Register with IDES within 30 days of start-up. Unemployment insurance contribution reports are filed each quarter. A granted quarterly extension gives an additional 30 days; a monthly extension gives an additional 15 days.
- **Cost**: 2026: most employers who became liable on or after January 1, 2024 pay the entry rate of 3.350%, which includes the 0.550% Fund Building Rate. New employers in the Administrative Support & Waste Management sector (NAICS 56) pay 3.450%. The minimum rate for 2026 is 0.750%. Only the first $14,250 of wages paid to a worker in calendar year 2026 are subject to contributions.
- **Rule out first**:
  - Contributions stop early in the year for each employee because only the first $14,250 of 2026 wages is subject to contributions. (common) Check: Compare year-to-date wages per employee to the $14,250 taxable wage base.
  - A nonprofit has employees but no IDES liability, which is correct until it employs four or more persons during each of 20 weeks in a calendar year. (occasional) Check: Count weeks with four or more employees against the nonprofit trigger, which is higher than the for-profit one.
  - A new business has no IDES account yet and is inside its 30-day registration window. (occasional) Check: Compare the start-up date to the 30-day registration deadline.
  - The rate looks high at 3.350% versus an established competitor's rate; that is the standard entry rate for new employers, including the 0.550% Fund Building Rate. (common) Check: Check the employer's liability date; experience rating replaces the entry rate over time.
- **How to prove it**:
  - [tier 2, settles it] Log into MyTax Illinois and confirm the IDES account exists and quarterly contribution and wage reports are filed for every quarter. https://ides.illinois.gov/employer-resources/taxes-reporting.html
  - [tier 4, settles it] Pull the IDES rate determination notice and the quarterly reports, and reconcile reported wages to the payroll register.
  - [tier 5, corroborating only] Look for quarterly IDES contribution payments after each quarter end.
- **Fix**:
  1. Register with IDES through MyTax Illinois within 30 days of start-up using the REG-UI-1 Report to Determine Liability.
  2. File all missing quarterly contribution and wage reports and pay contributions on wages up to the $14,250 base.
  3. Request a quarterly filing extension (30 extra days) where a report cannot be completed on time.
  4. Report new employees to the state New Hire Directory within 20 days of the employee's first day on the payroll.
- **Source**: https://ides.illinois.gov/employer-resources/taxes-reporting.html (verified 2026-08-14)
- **Note**: Triggers quoted verbatim from the IDES taxes and reporting page, including the nonprofit variant: 'Non-profit organizations are liable for the year when they have employed four or more persons during each of 20 weeks in a given calendar year.' The 30-day registration deadline is quoted verbatim from https://ides.illinois.gov/faqs/employer.html. 2026 entry rate, Fund Building Rate, minimum rate and the $14,250 taxable wage base are quoted verbatim from the IDES EA-50 Report for 2026 at https://ides.illinois.gov/content/dam/soi/en/web/ides/ides_forms_and_publications/EA-50_2026.pdf.

### Illinois Workers' Compensation Insurance `il-workers-comp`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
One employee, even part-time, means you must carry workers' compensation insurance in Illinois, and coverage attaches from the moment of hire with no waiting period. Owners can opt out of covering themselves, but that has to be done in writing to the carrier. The penalties are among the harshest in the country: up to $500 for every day of noncompliance with a $10,000 minimum, and personal criminal exposure for officers.
- **Deadline**: Coverage must be in place from the moment an employee is hired. There is no waiting period.
- **Cost**: Premium is set by private carriers; Illinois is not a monopolistic state fund.
- **Rule out first**:
  - No policy exists because the only people working are the sole proprietor, partners, corporate officers or LLC members, all of whom may exempt themselves. (common) Check: Confirm nobody outside that group is an employee; the exemption covers only the owners themselves.
  - The owners opted out but there is no opt-out form on file anywhere; the Commission does not have an opt-out form and does not require individuals to use one. (common) Check: Look for the written notice to the insurance carrier under Section 3(17)(b), not for a state form.
  - Coverage sits under a PEO master policy, so no direct carrier relationship shows in company records. (occasional) Check: Get a certificate of insurance from the PEO naming the client company.
  - A family member on payroll is uninsured, which is permitted only where they are a corporate officer or the business is a qualifying agricultural enterprise. (occasional) Check: Confirm officer status or the agricultural test (under 400 working days of labor per quarter in the preceding calendar year).
- **If it genuinely was missed**: An employer that knowingly and willfully fails to obtain insurance may be fined up to $500 for every day of noncompliance, with a minimum fine of $10,000. Corporate officers can be held personally liable if the company fails to pay the penalty. Corporate officers who negligently fail to obtain insurance are guilty of a Class A misdemeanor; if they knowingly fail to obtain insurance, they are guilty of a Class 4 felony. An employer that knowingly fails to insure loses its protections under the Act, so an injured employee may sue in civil court where benefits are unlimited and the burden falls on the employer to prove it was not negligent. The Commission may issue a work-stop order requiring the employer to stop all business operations until it provides proof of insurance.
- **How to prove it**:
  - [tier 1, settles it] Search the IWCC insurance coverage database to confirm a current policy is on file for the employer. https://iwcc.illinois.gov/about/insurance.html
  - [tier 3, corroborating only] Check the payroll or PEO platform for an active Illinois workers' compensation policy or pay-as-you-go arrangement.
  - [tier 4, settles it] Ask for the certificate of insurance from an Illinois-licensed carrier, and for any owner opt-out, the written notice sent to the carrier under Section 3(17)(b).
  - [tier 5, corroborating only] Look for workers' compensation premium payments to a private carrier.
- **Fix**:
  1. Buy a policy from an Illinois-licensed carrier before the first employee's start date; coverage attaches from the moment of hire.
  2. For owners who want to opt out, send written notice to the carrier following Section 3(17)(b); do not expect a Commission form.
  3. If in construction or trucking at construction sites, assume coverage is mandatory and check the Employee Classification Act.
  4. If already uninsured, insure immediately: fines run up to $500 per day with a $10,000 minimum and officers face personal criminal liability.
- **Source**: https://iwcc.illinois.gov/about/insurance.html (verified 2026-08-14)
- **Note**: All quotes verbatim from the IWCC insurance page, including: 'If you have one employee, even a part-time employee, you must obtain workers' compensation insurance.'; 'From the moment they are hired, employees are covered by the Workers' Compensation Act and must be insured.'; 'An employer that knowingly and willfully fails to obtain insurance may be fined up to $500 for every day of noncompliance, with a minimum fine of $10,000.'; and the Class A misdemeanor / Class 4 felony provisions. IWCC cites Section 4(d) of the Act. NOT VERIFIED: the specific imprisonment terms and fine caps attaching to a Class A misdemeanor or Class 4 felony; IWCC names the classifications but not the sentences, so none are stated here.

### Illinois Retailers' Occupation Tax Registration and Economic Nexus `il-sales-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
Illinois charges 6.25% state sales tax on general merchandise, with local rates stacking on top. The important 2026 change: the 200-transaction economic nexus prong was repealed effective January 1, 2026, so the only test now is $100,000 or more in cumulative gross receipts from Illinois purchasers in a 12-month lookback period. Illinois's own overview page has not been updated and still shows the old 200-transaction test.
- **Deadline**: A remote retailer determines on a quarterly basis, ending the last day of March, June, September and December, whether it met the threshold for the preceding 12-month period; if so it collects and files for one year.
- **Cost**: Illinois' general state retailers' occupation and use tax rates are 6.25 percent on general merchandise, including items required to be titled or registered by an agency of Illinois state government, and 1 percent on drugs and medical appliances. Local retailers' occupation tax stacks on top of the state rate.
- **Rule out first**:
  - The seller crossed 200 Illinois transactions but did not register, which is correct from January 1, 2026 onward because the transaction prong was repealed. (common) Check: Check the period: for periods before 2026 the 200-transaction test applied, and prior exposure may still exist.
  - IDOR's own Sales & Use Taxes overview page still lists the 200-transaction test, so a source check appears to contradict the registration decision. (common) Check: Rely on Informational Bulletin FY 2026-12 (December 2025, citing P.A. 104-0006), which supersedes the stale overview page.
  - Illinois receipts stayed under $100,000 in the 12-month lookback and there is no physical presence, so there is genuinely no duty. (common) Check: Run the quarterly lookback test on the last day of March, June, September and December.
  - A marketplace facilitator collects on the seller's behalf, so the seller's own returns show little Illinois tax. (common) Check: Confirm the marketplace's collection responsibility and the channel split.
- **If it genuinely was missed**: For destination-based sales where a taxpayer fails to provide sufficient information to determine the proper location, IDOR will assess tax on the gross receipts of such sales to undetermined tax locations at the rate of 15%.
- **How to prove it**:
  - [tier 2, settles it] Log into MyTax Illinois and confirm the ROT registration and the electronically issued Certificate of Registration, plus filed returns for every period. https://mytax.illinois.gov/
  - [tier 3, corroborating only] In the tax engine, confirm Illinois is registered and that destination-based local rates are being calculated, not just the 6.25% state rate.
  - [tier 4, settles it] Reconcile Illinois-sourced revenue to the filed ST-1 returns, and check whether destination-based local rates were applied for remote sales.
- **Fix**:
  1. Run the 12-month lookback test against $100,000 as of the most recent quarter end.
  2. Register through MyTax Illinois using Register a New Business (Form REG-1) with Schedule REG-1-L for site locations.
  3. Configure destination-based local rates for remote sales; the local rate follows where the goods are shipped or possession is taken.
  4. Review pre-2026 periods separately, since the 200-transaction prong applied then and may have created earlier exposure.
  5. Make sure customer location data is captured, because sales to undetermined locations are taxed at a flat 15%.
- **Source**: https://tax.illinois.gov/research/publications/bulletins/fy-2026-12.html (verified 2026-08-14)
- **Note**: Quoted verbatim from Informational Bulletin FY 2026-12: 'On or after January 1, 2026, the only threshold used to determine if a remote retailer or marketplace facilitator is engaged in the occupation of selling TPP at retail in Illinois and is subject to State and local ROT is whether the retailer makes $100,000 or more in cumulative gross receipts of sales of TPP to purchasers in Illinois during the lookback period. The 200-transaction threshold no longer applies.' and the 15% undetermined-location rule. Statutory cite P.A. 104-0006, 35 ILCS 120/2-12. Rates quoted verbatim from https://tax.illinois.gov/questionsandanswers/answer.139.html. STALE PAGE WARNING: https://tax.illinois.gov/research/taxinformation/sales/rot.html still states the 200-transaction test; the bulletin is later and controls.

### Illinois Benefit Corporation Annual Benefit Report `il-benefit-corp-report`
Applies to: benefit-corp | category: information-report
An Illinois benefit corporation carries every ordinary corporate obligation and one extra: an annual benefit report assessing its performance against a third-party standard. It goes to shareholders and onto your website, not to the Secretary of State, which is why it is so often missed. It must also name every holder of 5% or more of the shares.
- **Deadline**: Sent annually to each shareholder within 120 days following the end of the fiscal year of the benefit corporation, or at the same time the benefit corporation delivers any other annual report to its shareholders.
- **Rule out first**:
  - Nothing appears in the Secretary of State's records, which is expected: the benefit report goes to shareholders and the website, not to the state. (common) Check: Look on the company website and ask shareholders, not the entity registry.
  - No report is posted online because the company has no website, in which case it must instead provide a copy free of charge to any person who requests it. (occasional) Check: Request a copy directly; the statute provides this alternative.
  - The posted report omits director compensation and financial details, which the statute expressly permits for the public version. (occasional) Check: Compare the posted version to the shareholder version before treating omissions as a defect.
- **How to prove it**:
  - [tier 1, corroborating only] Confirm benefit corporation status on the Secretary of State entity record; the benefit report itself is not filed with the state. https://apps.ilsos.gov/businessentitysearch/
  - [tier 3, settles it] Check the public portion of the company's website, where all benefit reports must be posted (compensation and proprietary information may be omitted from the posted version).
  - [tier 4, settles it] Ask for the most recent annual benefit report and confirm it includes the third-party standard assessment and the 5% shareholder list.
- **Fix**:
  1. Select a third-party standard and assess the corporation's performance against it.
  2. Prepare the benefit report including the name of each holder of 5% or more of the outstanding shares.
  3. Send it to every shareholder within 120 days after fiscal year end.
  4. Post it on the public portion of the website, redacting director compensation and proprietary financial information if desired.
- **Source**: https://www.ilga.gov/legislation/ilcs/fulltext?DocName=080500400K5.01 (verified 2026-08-14)
- **Note**: Quoted verbatim from 805 ILCS 40/5.01: '(b) The benefit corporation shall send a benefit report annually to each shareholder: (1) within 120 days following the end of the fiscal year of the benefit corporation; or (2) at the same time that the benefit corporation delivers any other annual report to its shareholders.' and '(c) A benefit corporation shall post all of its benefit reports on the public portion of its Internet website, if any'. The 5% shareholder disclosure is 805 ILCS 40/5.01(a)(5).


## NJ (11)

### New Jersey Annual Report (Division of Revenue and Enterprise Services) `nj-annual-report`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
Every New Jersey entity, and every out-of-state entity authorized here, files an annual report with the Division of Revenue and Enterprise Services. It is keyed to your formation month, not to a fixed calendar date, so each company has its own deadline. Miss it two years running and the state voids your charter or revokes your authority to do business.
- **Deadline**: Due every year on the last day of the month in which the business formation was completed (the anniversary month). The responsibility to file falls on the business even if it receives no notification from the State.
- **Cost**: $75.00 for a for-profit corporation, LLC, limited partnership and LLP. $30.00 for a non-profit corporation. Portal convenience fees are $3.00 by credit card or $0.50 by e-check. Expediting is not available on the annual report.
- **Rule out first**:
  - The free name search shows the entity but no status, so it looks unverified; New Jersey deliberately does not expose standing for free. (common) Check: Buy the $5.00 status report, or check Corp Watch on the business account.
  - The deadline is the last day of the formation month, so a company formed in September looks overdue when checked in June but is not. (common) Check: Read the formation date and compute the anniversary month.
  - A registered agent service filed and paid the report, so no charge appears in company records. (common) Check: Check the status report or the agent's invoice for a pass-through fee.
  - The entity is a general partnership, which makes no public record filing and therefore owes no annual report at all. (occasional) Check: Confirm the entity form; only statutory entities file.
- **If it genuinely was missed**: Businesses that fail to file annual reports for two consecutive years may have their charter voided or authority to do business in New Jersey revoked, the Business Registration Certificate may be invalidated, and access to state services including funding opportunities and licenses may be lost. Reinstatement: for-profit corporation $95.00 ($75.00 reinstatement plus $20.00 tax clearance filing), plus all delinquent annual reports; non-profit $150.00 domestic and $200.00 foreign; LP, LLP and LLC $75.00. Foreign corporations pay a separate $25.00 tax clearance fee directly to the Division of Taxation.
- **How to prove it**:
  - [tier 1, corroborating only] Search the free Business Entity Name Search to confirm the entity exists and read its 10-digit Entity ID, city, entity type and Incorporated Date, which is what sets the anniversary month. Note the free search returns entities 'regardless of status', so it does not by itself prove good standing. https://www.njportal.com/DOR/BusinessNameSearch/
  - [tier 2, settles it] Sign up for the free Corp Watch and Annual Report Filing Due alerts on the business account, which report filings posted and reports coming due. https://www.nj.gov/treasury/revenue/freetools.shtml
  - [tier 3, settles it] Buy a $5.00 status report (plus $1.25 online convenience fee) through the state Business Records Service, which is the cheapest authoritative read on standing. https://www.njportal.com/DOR/businessrecords/
  - [tier 5, corroborating only] Look for a $75 (or $30) payment to NJ Division of Revenue in the anniversary month.
- **Fix**:
  1. Find the formation month and set the deadline to the last day of that month each year.
  2. File the annual report online through the state annual report portal and pay $75 (or $30 for a nonprofit).
  3. If revoked, use the online reinstatement service, which begins with the annual report filing, and pay all delinquent annual reports plus the reinstatement fee.
  4. Check whether tax clearance is required: foreign profit corporations, domestic limited partnerships, and domestic and foreign LLCs revoked for more than two years must file for it ($20.00 application).
  5. Turn on the free Corp Watch and Annual Report Filing Due alerts so this never recurs.
- **Source**: https://www.nj.gov/treasury/revenue/fees.shtml (verified 2026-08-14)
- **Note**: Fees quoted verbatim from the DORES Registry Fee Schedules ('Annual Report - corporate and LP (Expediting is not available on this item.) | $75.00'; non-profit 'Annual Report | $30.00'; LLC and LLP 'Annual Report | $75.00') and corroborated on the state annual report portal FAQ. Anniversary-month rule quoted verbatim from https://business.nj.gov/pages/filings-and-accounting: 'The report is due every year on the last day of the month, in the month in which you completed your business formation'. Two-year revocation quoted verbatim from https://www.nj.gov/treasury/revenue/reinstate.shtml. Reinstatement fees from https://www.nj.gov/treasury/revenue/reinstatefees.shtml.

### New Jersey Registered Agent `nj-registered-agent`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: registered-agent
Every entity that makes a public record filing in New Jersey must name one registered agent with a New Jersey street address. A PO Box is allowed only if the street address is listed as well. The agent receives official papers and legal documents on the company's behalf.
- **Deadline**: Continuous, named at formation or authorization and kept current. Changes can be made inside the annual report or as a standalone filing.
- **Cost**: $25.00 to change the registered office or agent or both (this also covers resignation of the agent). Filed inside the annual report there is no additional service fee; filed standalone there is a $3.00 credit card or $1.00 e-check service fee on top.
- **Rule out first**:
  - The agent detail is not visible for free, so it looks unverifiable; New Jersey puts agent data behind the paid status report. (common) Check: Buy the $5.00 status report rather than concluding from the free name search.
  - A founder is the agent at the company's own New Jersey address, so there is no agent invoice anywhere. (common) Check: Read the agent name on the status report; an individual is permitted.
  - The record shows a PO Box and looks non-compliant, but a street address is also listed, which New Jersey permits. (occasional) Check: Check whether the registered office includes a New Jersey street address alongside the box.
- **How to prove it**:
  - [tier 3, settles it] Buy the $5.00 status report through the Business Records Service, which returns the current registered agent and office. https://www.njportal.com/DOR/businessrecords/
  - [tier 4, settles it] Read the entity's public record filing (certificate of formation or certificate of authority) for the agent named at formation, then check for any later change filing.
  - [tier 5, corroborating only] Look for an annual registered agent service subscription charge.
- **Fix**:
  1. Pull the status report and confirm the registered agent and New Jersey street address are current.
  2. File the change of registered office or agent ($25.00), ideally bundled into the annual report to avoid the extra service fee.
  3. If the agent has resigned, appoint a replacement promptly; the same $25.00 filing covers resignation.
- **Source**: https://www.nj.gov/treasury/revenue/pdf/NJ_Public_Records_Filing.pdf (verified 2026-08-14)
- **Note**: Quoted verbatim: 'a. Registered Agent - Enter one agent only. The agent may be an individual or a corporation duly registered, and in good standing with the State Treasurer. b. Registered Office - Provide a New Jersey street address. A PO Box may be used only if the street address is listed as well.' Fee from https://www.nj.gov/treasury/revenue/fees.shtml: 'Change of Registered Office or Agent or Both (Also, includes resignation of agent) | $25.00'. The general partnership carve-out is quoted from https://www.nj.gov/treasury/taxation/partnotice.shtml: 'General partnerships are not subject to Public Record filing'.

### New Jersey Foreign Qualification `nj-foreign-qualification`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: entity
An entity formed outside New Jersey that conducts business here must be authorized by the Division of Revenue and Enterprise Services. Corporations file a Certificate of Authority and LLCs file a Certificate of Registration, both $100. Out-of-state corporations (but not LLCs) must supply a certificate of good standing from the home state, and the name must match the home-state name exactly.
- **Deadline**: Before conducting business in New Jersey. Form NJ-REG must then be submitted within 60 days of the public record filing.
- **Cost**: $100.00 for a certificate of authority for a foreign corporation or limited partnership. $100.00 for a certificate of authority for a foreign non-profit. $100.00 for a certificate of registration for a foreign LLC. $100.00 for a certificate of registration for a foreign LLP. Foreign corporate name registration and renewal are $50.00 each.
- **Rule out first**:
  - The company has New Jersey customers and sales tax nexus but no office, employees or property here, so authorization was never triggered. (common) Check: Separate economic nexus for sales tax from the conducting-business standard for authorization.
  - The entity is registered but the free name search returns nothing because the New Jersey name differs slightly from the trading name. (occasional) Check: Search by keyword and by Entity ID; New Jersey requires the registered name to match the home-state name exactly, which may differ from the brand.
  - An LLC has no home-state good standing certificate on file and looks incomplete, but New Jersey only requires one for foreign corporations. (occasional) Check: Confirm the entity type; the certificate requirement is corporation-only.
- **If it genuinely was missed**: Same as domestic: failure to file annual reports for two consecutive years can result in revocation of the authority to do business. Foreign non-profit reinstatement is $200.00 and foreign LLC cancellation is $125.00.
- **How to prove it**:
  - [tier 1, corroborating only] Search the free Business Entity Name Search for the company; an authorized foreign entity appears with a New Jersey 10-digit Entity ID. https://www.njportal.com/DOR/BusinessNameSearch/
  - [tier 3, settles it] Buy the $5.00 status report or a standing certificate to confirm the entity is authorized and in good standing. https://www.njportal.com/DOR/businessrecords/
  - [tier 4, settles it] Ask for the filed Certificate of Authority or Certificate of Registration and the home-state good standing certificate that accompanied it.
- **Fix**:
  1. Confirm whether the New Jersey activity amounts to conducting business.
  2. For a corporation, order a home-state certificate of good standing; LLCs and other entities do not need one.
  3. File the Certificate of Authority or Certificate of Registration and pay $100.00, using the exact home-state name.
  4. Submit Form NJ-REG within 60 days of the public record filing.
  5. Calendar the annual report on the last day of the anniversary month of authorization.
- **Source**: https://www.nj.gov/treasury/revenue/fees.shtml (verified 2026-08-14)
- **Note**: Fees quoted verbatim from the DORES Registry Fee Schedules: 'Certificate of authority for a foreign corporation or limited partnership | $100.00'; 'Certificate of registration for a foreign LLC | $100.00'. Process and the corporation-only good standing requirement quoted verbatim from https://www.nj.gov/njfilm/assets/pdf/registering-to-do-business-in-NJ.pdf: 'Out of State (Foreign) Corporations only, need a Certificate of Good Standing ... This is not required for LLC's or other legal entities.' and 'For foreign businesses, the business name must match the business name in your home state exactly.' CBT nexus language from https://www.nj.gov/treasury/taxation/cbt/index.shtml.

### New Jersey Corporation Business Tax (C corporations) and the minimum tax `nj-corporation-business-tax`
Applies to: c-corp, benefit-corp | category: tax
New Jersey taxes corporations on net income at up to 9%, but the part that surprises founders is the minimum tax: even with no profit you owe between $500 and $2,000 depending on your New Jersey gross receipts. The minimum cannot be prorated and zero returns are generally not permitted. New Jersey's deadline is also one month later than the federal one.
- **Deadline**: Returns and payments, except estimated payments, are due the 15th day of the month following the month the federal corporate income tax return is originally due. For a calendar-year corporation with a December 31, 2025 year end, the return is due May 15, 2026. Estimated payments are due on or before the 15th day of the 4th, 6th, 9th and 12th month of the tax year, except that taxpayers with gross receipts greater than or equal to $50,000,000 make three installments instead, on the 15th day of the 4th, 6th and 12th months.
- **Cost**: Rates: 9% of taxable net income over $100,000; 7.5% where over $50,000 and up to $100,000; 6.5% where $50,000 or less. Minimum tax by New Jersey gross receipts: less than $100,000 = $500; $100,000 to under $250,000 = $750; $250,000 to under $500,000 = $1,000; $500,000 to under $1,000,000 = $1,500; $1,000,000 or more = $2,000. A separate filer that is a member of an affiliated or controlled group with total payroll of $5,000,000 or more pays the $2,000 minimum regardless of its own gross receipts. Each nexus member of a combined group is subject to the $2,000 minimum tax.
- **Rule out first**:
  - A $500 payment looks like a stray fee but is the statutory minimum tax for a loss-making corporation with under $100,000 of New Jersey gross receipts. (common) Check: Tie the payment to line 2b of the filed CBT-100.
  - Nothing was filed in April and it looks late, but New Jersey's deadline is a month after the federal one, so May 15 is on time for a calendar-year filer. (common) Check: Apply the 15th-day-of-the-month-following rule before calling a return late.
  - The entity is an LLC or partnership taxed as a partnership, so it owes no CBT minimum and correctly files NJ-1065 instead. (common) Check: Check the federal classification; disregarded entities and partnerships are not members of a combined group for the $2,000 minimum.
  - The minimum tax jumped to $2,000 with no change in the company's own receipts because it joined an affiliated group with $5,000,000 or more of total payroll. (occasional) Check: Check the affiliated or controlled group's total payroll, which is group-wide and not New Jersey-only.
- **How to prove it**:
  - [tier 2, settles it] Log into the New Jersey Tax Portal and confirm a CBT registration and a filed CBT-100 (or CBT-100U) for every privilege period since nexus began. https://www.nj.gov/treasury/taxation/cbt/index.shtml
  - [tier 4, settles it] Pull the filed CBT-100 and check Schedule J line 6 (New Jersey gross receipts) against the minimum tax bracket actually paid on line 2b.
  - [tier 5, corroborating only] Look for a NJ Division of Taxation payment of at least $500 around mid-May for a calendar-year filer.
- **Fix**:
  1. Register for CBT and confirm every privilege period since New Jersey nexus began has a filed return.
  2. Compute New Jersey gross receipts on Schedule J to pick the correct minimum tax bracket for each year.
  3. File the outstanding CBT-100 returns and pay at least the minimum for each year; the minimum cannot be prorated.
  4. If the corporation is part of a combined group, confirm each nexus member is carrying its own $2,000 minimum.
- **Source**: https://www.nj.gov/treasury/taxation/pdf/current/cbt/cbt100ins.pdf (verified 2026-08-14)
- **Note**: Rates, minimum tax table, affiliated group rule and deadline quoted verbatim from the 2025 CBT-100 instructions. Combined group $2,000 per nexus member quoted verbatim from the 2025 CBT-100U instructions, which also state that disregarded entities and partnerships are not subject to the $2,000 minimum as combined group members. The instruction PDFs were preferred over https://www.nj.gov/treasury/taxation/corp_over.shtml, which carries its own warning: 'This page has not been updated to reflect all the legislative changes that have impacted the Corporation Business Tax Act in recent years'.

### New Jersey Corporation Business Tax for S corporations `nj-cbt-s-corporation`
Applies to: s-corp | category: tax
A New Jersey S corporation still owes an entity-level minimum tax, scaled to New Jersey gross receipts, from $375 up to $1,500. It files Form CBT-100S. S corporations are exempt from the Corporate Transit Fee, which is the one break they get.
- **Deadline**: Same as C corporations: the 15th day of the month following the month the federal return is originally due (May 15, 2026 for a December 31, 2025 year end).
- **Cost**: Minimum tax by New Jersey gross receipts: less than $100,000 = $375; $100,000 to under $250,000 = $562; $250,000 to under $500,000 = $750; $500,000 to under $1,000,000 = $1,125; $1,000,000 or more = $1,500. If the taxpayer is a member of an affiliated or controlled group with total payroll of $5,000,000 or more, the minimum tax is $2,000 regardless of its own gross receipts. Rate ladder on taxable income mirrors the C corporation: 9% over $100,000, 7.5% over $50,000 up to $100,000, 6.5% at $50,000 or less.
- **Rule out first**:
  - The payment is $375 rather than $500 and looks short; the S corporation minimum schedule is genuinely lower than the C corporation one. (common) Check: Confirm the New Jersey S election, then compare against the CBT-100S minimum table, not the CBT-100 one.
  - No Corporate Transit Fee appears even though income exceeds $10 million; New Jersey S corporations are expressly exempt from it. (occasional) Check: Confirm S status; the exemption is stated in the CBT-100S instructions.
- **How to prove it**:
  - [tier 2, settles it] In the New Jersey Tax Portal, confirm a CBT-100S is filed for each privilege period. https://www.nj.gov/treasury/taxation/cbt/index.shtml
  - [tier 4, settles it] Pull the filed CBT-100S and check the minimum tax on line 2b against Schedule J line 6 gross receipts.
  - [tier 5, corroborating only] Look for a NJ Division of Taxation payment of at least $375 for a calendar-year S corporation.
- **Fix**:
  1. Confirm the New Jersey S election is on file, since New Jersey S status is not automatic from the federal election.
  2. File CBT-100S for every open privilege period and pay at least the applicable minimum.
  3. Check whether the affiliated group payroll test pushes the minimum to $2,000.
- **Source**: https://www.nj.gov/treasury/taxation/pdf/current/cbt/cbt100sins.pdf (verified 2026-08-14)
- **Note**: Minimum tax table and the affiliated group rule quoted verbatim from the 2025 CBT-100S instructions. DISCREPANCY: the older overview page https://www.nj.gov/treasury/taxation/corp_over.shtml states the second tier as $562.50 while the current 2025 CBT-100S instructions print $562; that overview page self-warns it is not current, so the instruction figure is used here. Confirm on the live return before relying on the exact cents.

### New Jersey Corporate Transit Fee `nj-corporate-transit-fee`
Applies to: c-corp, benefit-corp | category: tax
New Jersey layers a 2.5% Corporate Transit Fee on top of the CBT for large corporations. It only bites once taxable net income exceeds $10 million, so most startups never see it, but it is worth knowing it exists and has a scheduled end date. The $10 million is a CLIFF, not an exemption: once you cross it the 2.5% applies to the entire taxable net income, not just the excess, so a corporation at $10.1 million owes roughly $252,000 rather than $2,500. S corporations, public utilities and P.L. 86-272 filers are exempt.
- **Deadline**: Reported on the CBT return (page 1, line 5) for privilege periods beginning on and after January 1, 2024 through December 31, 2028.
- **Cost**: 2.5% of taxable net income (Schedule A, Part III, line 2a, 2b or 2c as applicable), applied to the entire amount on that line rather than to the excess over $10 million.
- **Rule out first**:
  - Line 5 is zero because taxable net income is at or below $10 million, which is true for the overwhelming majority of companies. (common) Check: Compare taxable net income on Schedule A Part III to the $10 million threshold.
  - A large, profitable company shows zero because it is a New Jersey S corporation or a P.L. 86-272 filer, both expressly outside the fee. (occasional) Check: Check the entity's S election or P.L. 86-272 protected status.
  - No fee appears for a privilege period beginning before January 1, 2024, which predates the fee entirely. (occasional) Check: Check the privilege period start date against the January 1, 2024 effective date.
- **How to prove it**:
  - [tier 2, settles it] In the New Jersey Tax Portal, review the CBT liability breakdown for the privilege period. https://www.nj.gov/treasury/taxation/cbt/index.shtml
  - [tier 4, settles it] Read line 5 on page 1 of the filed CBT-100 and tie it to taxable net income on Schedule A, Part III.
- **Fix**:
  1. Compute taxable net income for each privilege period beginning on or after January 1, 2024.
  2. If it exceeds $10 million, apply 2.5% to the entire taxable net income (not just the excess) and file an amended CBT return for any period where the fee was omitted.
  3. Confirm no exemption applies (S corporation, public utility, P.L. 86-272) before paying.
- **Source**: https://www.nj.gov/treasury/taxation/pdf/current/cbt/cbt100ins.pdf (verified 2026-08-14)
- **Note**: Quoted verbatim from the 2025 CBT-100 instructions, Line 5: 'For privilege periods beginning on and after January 1, 2024, through December 31, 2028, any corporation with a taxable net income on Schedule A, Part III, line 2a, 2b, or 2c (whichever is applicable) over $10 million is subject to the Corporate Transit Fee.' and 'Multiply the amount ... by 2.5% and enter the result.' and 'Public utilities and New Jersey S corporations ... are exempt from the Corporate Transit Fee.' RESOLVED 2026-08-14: the older separate CBT surtax under N.J.S.A. 54:10A-5.41 (distinct from the 5.41a Transit Fee) is EXPIRED and does not apply for 2026. The Division of Taxation surtax page (https://www.nj.gov/treasury/taxation/cbt/surtax.shtml) states the 2.5% temporary surtax applied to taxpayers with New Jersey allocated taxable net income over $1 million 'for tax periods beginning on or after January 1, 2018 through December 31, 2023'. The 2025 CBT-100 instructions contain zero occurrences of the word 'surtax', confirming it is off the return.

### New Jersey Partnership Filing Fee ($150 per owner) `nj-partnership-filing-fee`
Applies to: partnership, llc | category: tax
New Jersey charges partnerships and LLCs taxed as partnerships a filing fee of $150 for every owner, on top of filing the NJ-1065. It only applies once you have more than two owners, and it is capped at $250,000. You also have to prepay 50% of next year's fee at the same time, which catches people out on cash flow.
- **Deadline**: Due on or before the 15th day of the fourth month after the close of each privilege period (April 15 for a calendar-year business). An installment payment equal to 50% of the current year's filing fee is required at the same time. Extensions use Form PART-200-T.
- **Cost**: $150 for each owner of an interest in the entity, up to a maximum of $250,000.
- **Rule out first**:
  - No fee was paid because the entity has exactly two owners or fewer; the fee only triggers at more than two owners. (common) Check: Count owners at any point during the year, including entities and trusts.
  - A single-member LLC paid nothing, which is correct: it is a disregarded entity with one owner, so it is neither classified as a partnership nor over the two-owner threshold. (common) Check: Confirm the federal classification as a disregarded entity.
  - The payment is about 50% larger than expected because the required installment prepayment of next year's fee is bundled with it. (common) Check: Split the payment into the current-year fee and the 50% installment on the filed NJ-1065.
  - A partnership with New Jersey partners paid nothing because all its operations and facilities are outside New Jersey and it has no New Jersey source income, expenses or loss. (occasional) Check: Confirm the entity has zero New Jersey source items and no in-state facilities.
  - A final-year return shows the fee but no prepayment; when 'Final Return' is checked, no prepayment of next year's fee is required. (occasional) Check: Check whether the Final Return box is marked on the NJ-1065.
- **How to prove it**:
  - [tier 2, settles it] In the New Jersey Tax Portal, confirm the NJ-1065 is filed and the filing fee plus the 50% installment were paid for each privilege period.
  - [tier 4, settles it] Count the K-1s issued for the year and multiply by $150, then compare to the fee actually paid on the NJ-1065.
  - [tier 5, corroborating only] Look for a NJ Division of Taxation payment near April 15 sized at roughly 1.5 times $150 times the owner count (fee plus 50% prepayment).
- **Fix**:
  1. Count owners for each year, remembering that entity and trust owners count and dual general/limited partners count twice.
  2. File the outstanding NJ-1065 returns and pay $150 per owner (capped at $250,000) plus the 50% installment.
  3. Check separately whether NJ-CBT-1065 is required to pay tax on behalf of nonresident partners.
  4. Use Form PART-200-T to extend where the fee is due but the return is not ready.
- **Source**: https://www.nj.gov/treasury/taxation/pdf/current/part/1065i.pdf (verified 2026-08-14)
- **Note**: Quoted verbatim from the 2025 NJ-1065 instructions: 'Any entity classified as a partnership for federal income tax purposes, other than an investment club, that has any income or loss derived from New Jersey sources and that has more than two owners is required to make a payment of a filing fee of $150 for each owner of an interest in the entity up to a maximum of $250,000.' Owner-counting rules and the double count for dual-interest partners from https://www.nj.gov/treasury/taxation/partnotice.shtml. Exemptions and the 'Nonprofit owners are not exempt from the fee' rule from TB-55(R) at https://www.nj.gov/treasury/taxation/pdf/pubs/tb/tb55.pdf. The single-member LLC exclusion is derived from the operative conditions (partnership classification plus more than two owners), not from an express exemption sentence.

### New Jersey Business Registration (NJ-REG) and Payroll Withholding `nj-payroll-withholding`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: payroll
New Jersey uses one form, NJ-REG, to register your business for tax and employer purposes, and it has a hard deadline: at least 15 business days before you start doing business. There is no fee for NJ-REG itself. Once registered as an employer you file the NJ-927 quarterly return and the WR-30 wage report together.
- **Deadline**: Register at least 15 business days prior to commencing business or opening an additional place of business. If collecting sales tax, submit NJ-REG at least fifteen days prior to the first sale. NJ-REG must be submitted within 60 days of filing a new business entity. NJ-927 and WR-30 are due on or before the 30th day of the month following the end of the quarter. Form NJ-500 monthly remittance is required for the first and/or second month of a quarter in which MORE THAN $500 of tax was withheld, due by the 15th of the month following the month it was collected; the third month of a quarter is always paid with the quarterly return. Annual reconciliation NJ-W-3 is due on or before February 15.
- **Cost**: There is no fee for filing NJ-REG. Separate fees apply to the business entity public record filing.
- **Rule out first**:
  - There is no NJ-500 monthly remittance because the monthly liability never exceeded $500, which is the trigger; quarterly filing alone is correct. (common) Check: Compare first and second month withholding to the more-than-$500 threshold before treating a missing NJ-500 as a gap; a month at exactly $500 does not trigger it, and the third month never does.
  - A dormant entity is registered with NJ-REG but has no payroll filings, which is right: NJ-REG is required of dormant corporations, payroll filings are not. (occasional) Check: Confirm there are no wages paid; NJ-REG registration and employer registration are different things.
  - Deposits look unusually frequent because the employer crossed $10,000 of prior-year withholding and became a weekly payer. (occasional) Check: Check prior-year employer withholding against the $10,000 weekly payer threshold.
- **How to prove it**:
  - [tier 2, settles it] Log into the New Jersey Tax Portal and confirm the withholding account is registered and NJ-927 and WR-30 are filed for every quarter. https://www.nj.gov/treasury/taxation/businesses/payroll/payroll-filing.shtml
  - [tier 3, corroborating only] In the payroll provider, confirm the New Jersey withholding ID and employer registration numbers are present and the deposit schedule matches.
  - [tier 4, settles it] Ask for the Business Registration Certificate issued after NJ-REG, and pull a New Jersey pay stub showing state withholding.
- **Fix**:
  1. File NJ-REG (no fee) and, for a new entity, do it within 60 days of the public record filing.
  2. Register for payroll tax purposes before filing NJ-927, NJ-W-3 or WR-30, which requires prior registration.
  3. File all missing NJ-927 and WR-30 quarters by the 30th of the month following each quarter end.
  4. Determine whether the business is a weekly payer ($10,000 prior-year threshold) and switch to NJ-927-W if so.
  5. File the NJ-W-3 annual reconciliation by February 15.
- **Source**: https://www.nj.gov/treasury/taxation/njit31.shtml (verified 2026-08-14)
- **Note**: NJ-927/WR-30 deadlines, weekly payer definition, NJ-500 and NJ-W-3 rules quoted verbatim from the Division of Taxation employer withholding page. CORRECTED 2026-08-14: the NJ-500 trigger is MORE THAN $500, not '$500 or more'. NJ-WT (September 2025), the authoritative withholding instruction, states verbatim: 'If you collected more than $500 in tax withheld for the first and/or second months of the quarter, you are required to make monthly payments using Form NJ-500 for those months. The third month of the quarter is always paid with the quarterly return.' CONFLICT: the Business Registration Packet says '$500 or more'. NJ-WT controls and is followed here. The 15-business-day registration deadline, the no-fee statement, the universality language and the 60-day rule are quoted verbatim from the NJ-REG instructions at https://www.nj.gov/treasury/revenue/pdf/Legacy-Reg-Form-0825.pdf.

### New Jersey Unemployment, Workforce Development, Temporary Disability and Family Leave contributions `nj-unemployment-insurance`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: unemployment
New Jersey bundles four employer programs together: unemployment insurance, workforce development, temporary disability and family leave insurance. You register for all of them through NJ-REG and report them all on the same quarterly NJ-927 and WR-30. You become an employer once you have at least one worker and pay $1,000 or more in wages in a calendar year, which is a very low bar.
- **Deadline**: Quarterly wage reporting on Form WR-30 and contributions on Form NJ-927, due on or before the 30th day of the month following the end of the quarter.
- **Cost**: 2026 taxable wage bases: $44,800 for unemployment compensation (workers and employers) and for employer TDI, up from $43,300 in 2025. $171,100 for Temporary Disability and Family Leave Insurance for workers only, up from $165,400 in 2025. The contribution rate for state and local government entities that elect to contribute rather than reimburse decreases to 0.5 percent of taxable wages for calendar year 2026.
- **Rule out first**:
  - Contributions stop mid-year for a well-paid employee because the unemployment taxable wage base caps at $44,800 for 2026. (common) Check: Compare year-to-date wages per employee to the $44,800 UI base and the $171,100 TDI/FLI worker base.
  - No employer registration exists because total wages have not reached $1,000 in the calendar year. (occasional) Check: Total calendar-year wages against the $1,000 threshold.
  - The company pays only contractors, so no employer contributions appear; this is benign only if the workers pass all three prongs of the ABC test. (common) Check: Run the ABC test, which is stricter than the IRS test and presumes employee status.
  - A nonprofit reimburses the trust fund for benefits paid rather than making contributions, so no contribution payments appear. (occasional) Check: Check whether the employer elected reimbursement rather than contribution.
- **How to prove it**:
  - [tier 2, settles it] Log into the New Jersey employer services portal and confirm WR-30 and NJ-927 are filed for every quarter and the rate notice is current. https://www.nj.gov/labor/ea/employer-services/who-qualifies/
  - [tier 4, settles it] Pull the WR-30 wage reports and reconcile the reported wages to the payroll register; check TDI and FLI withholding on employee pay stubs.
  - [tier 5, corroborating only] Look for quarterly NJ Department of Labor contribution payments near the 30th of the month after each quarter end.
- **Fix**:
  1. File NJ-REG to register with the Division of Revenue, which opens the labor accounts.
  2. File all missing WR-30 wage reports and NJ-927 contribution returns.
  3. Confirm TDI and FLI worker withholding is switched on in payroll at the correct wage base.
  4. Keep the business information current by amending Form NJ-REG-C as needed.
- **Source**: https://www.nj.gov/labor/ea/employer-services/who-qualifies/ (verified 2026-08-14)
- **Note**: Employer trigger and the four-program bundling quoted verbatim from the NJDOL who-qualifies page: 'Once your established business employs one or more individuals and pays wages of $1,000 or more in a calendar year, you are considered an employer.' 2026 wage bases quoted verbatim from the NJDOL press release of December 29, 2025 at https://www.nj.gov/labor/lwdhome/press/2025/20251229_newbenefitrates2026.shtml. NOT VERIFIED: the private-employer UI contribution rate schedule for FY2026-27; private rates are experience-rated and issued on individual rate notices, and no published rate table was fetched, so no employer rate percentage is stated.

### New Jersey Workers' Compensation Insurance `nj-workers-comp`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: workers-comp
New Jersey requires all employers to carry workers' compensation or be approved to self-insure, bought from any of more than 400 private carriers (New Jersey is not a monopolistic state fund). The critical distinction: corporate officers COUNT as employees, so a one-officer corporation needs a policy, while LLC members and partners do not count. Penalties reach $5,000 per ten-day period and can attach to officers personally.
- **Deadline**: Coverage must be in place while any covered individual performs services. Every New Jersey annual report filing asks for workers' compensation policy data.
- **Cost**: Premium is set by the private carrier; there is no state fund charge.
- **Rule out first**:
  - A member-managed LLC with no staff other than its members carries no policy, which is correct because LLC members are expressly excluded from the count. (common) Check: Confirm nobody outside the membership performs services for financial consideration.
  - The annual report says workers' compensation is not required, which the portal expressly allows a company to answer; that is not evidence of a missing policy. (common) Check: Test the answer against the entity form: an officer-only corporation IS required, a member-only LLC is not.
  - Coverage sits with a PEO under a master policy, so no direct carrier relationship shows. (occasional) Check: Get a certificate of insurance from the PEO naming the client company.
  - An out-of-state employer's existing policy already covers New Jersey work through its multi-state endorsement. (occasional) Check: Read the policy information page for New Jersey and confirm with the carrier.
- **If it genuinely was missed**: Failing to insure is a disorderly persons offense and, if determined to be willful, a crime of the fourth degree. Penalties can be assessed up to $5,000 for the first ten days and up to $5,000 for each additional ten-day period of failure to insure thereafter. In the case of a corporation, liability for failure to insure can extend to the corporate officers individually. Penalties assessed for failure to insure are not dischargeable in bankruptcy. Where a work-related injury or death has occurred, the employer, including individual corporate officers, partners, or members of an LLC, is directly liable for medical expenses, temporary disability, and permanent disability or dependency benefits, and awards can become liens against the employer and its officers.
- **How to prove it**:
  - [tier 1, settles it] The Office of Special Compensation Funds cross-matches its database with the Compensation Rating and Inspection Bureau (NJ CRIB) to identify uninsured employers; a CRIB coverage lookup confirms a policy on file. https://www.nj.gov/labor/workerscompensation/employer-requirements/index.shtml
  - [tier 4, settles it] Ask for the certificate of insurance from a carrier authorized to write workers' compensation in New Jersey, or the Department of Banking and Insurance self-insurance approval.
  - [tier 4, corroborating only] Read the workers' compensation section of the company's most recent New Jersey annual report filing, which requires policy data or an express 'not required' answer.
  - [tier 5, corroborating only] Look for a workers' compensation premium payment to a private carrier or a pay-as-you-go deduction in the payroll invoice.
- **Fix**:
  1. Determine whether anyone performing services counts: for a corporation, officers do; for an LLC or partnership, members and partners do not.
  2. Buy a policy from a carrier authorized in New Jersey, or apply to the Commissioner of Banking and Insurance for self-insurance approval.
  3. Post the prescribed notice of coverage conspicuously at the worksite, which is a separate statutory duty.
  4. If already uninsured, insure immediately: penalties accrue per ten-day period and are not dischargeable in bankruptcy.
  5. Answer the workers' compensation section of the annual report accurately, since it feeds the state's uninsured-employer cross-match.
- **Source**: https://www.nj.gov/labor/workerscompensation/employer-requirements/index.shtml (verified 2026-08-14)
- **Note**: All rules and penalties quoted verbatim from the NJDOL employer requirements page, including: 'New Jersey law requires that all New Jersey employers, not covered by Federal programs, have Workers' Compensation coverage or be approved for self-insurance.'; the corporation rule 'including corporate officers'; the partnership/LLC rule 'excluding partners or members of the LLC'; and 'penalties for such failure can be assessed up to $5,000 for the first ten days and up to $5,000 for each additional ten-day period'. Note the penalty is per TEN-DAY PERIOD, not per day, which differs from several other states.

### New Jersey Sales and Use Tax Registration and Economic Nexus `nj-sales-tax`
Applies to: c-corp, s-corp, llc, llc-single-member, partnership, benefit-corp, nonprofit | category: sales-tax
New Jersey charges 6.625% sales tax and still uses BOTH an economic nexus test: gross revenue EXCEEDING $100,000 (strictly more, so exactly $100,000 does not trip it) OR 200 or more separate transactions. Many states have dropped the transaction count, so a low-price high-volume seller can trip New Jersey while staying clear elsewhere. You must register at least 15 days before your first sale.
- **Deadline**: Monthly payments and quarterly returns are due by 11:59 p.m. on the 20th day of the month after the end of the filing period. Quarterly ST-50 returns are due April 20, July 20, October 20 and January 20. A return must be filed for each quarter even if no tax is due and no sales were made.
- **Cost**: The New Jersey sales tax rate is 6.625% on sales of most tangible personal property, specified digital products, and certain services unless specifically exempt.
- **Rule out first**:
  - New Jersey receipts are well under $100,000 so registration looks unnecessary, but the 200-transaction prong may still have been crossed. (common) Check: Count separate transactions delivered into New Jersey for the current and prior calendar year, not just dollars.
  - All New Jersey sales run through a marketplace facilitator, which must collect regardless of the seller's own thresholds. (common) Check: Confirm the channel split and the marketplace's collection.
  - A registered business files zero returns every quarter, which is required behaviour where there are no sales. (common) Check: Look for the filed return rather than a payment.
  - The business was placed on a non-reporting basis by filing Form C-6205-ST, so no quarterly returns appear. (occasional) Check: Check for an approved Form C-6205-ST on the account.
- **How to prove it**:
  - [tier 2, settles it] Log into the New Jersey Tax Portal and confirm the sales tax registration and a filed ST-50 for every quarter.
  - [tier 3, corroborating only] In the tax engine or billing system, check whether New Jersey is registered and whether BOTH the $100,000 and the 200-transaction counters are being tracked.
  - [tier 4, settles it] Ask for the Certificate of Authority for sales tax showing the 12-digit identification number, and reconcile New Jersey revenue to the filed returns.
- **Fix**:
  1. Measure New Jersey-delivered gross revenue AND separate transaction count for the current and prior calendar year.
  2. Submit NJ-REG at least fifteen days before the first sale to obtain the Certificate of Authority.
  3. File all outstanding ST-50 returns electronically through the New Jersey Tax Portal, including zero returns, and pay electronically.
  4. If sales have genuinely stopped, file Form C-6205-ST to be placed on a non-reporting basis rather than leaving returns unfiled.
- **Source**: https://www.nj.gov/treasury/taxation/remotesellers.shtml (verified 2026-08-14)
- **Note**: Economic nexus quoted verbatim: 'The remote seller's gross revenue from sales ... delivered into New Jersey during the current or prior calendar year, exceeds $100,000; or The remote seller sold ... in 200 or more separate transactions during the current or prior calendar year.' Rate quoted verbatim from https://www.nj.gov/treasury/taxation/businesses/salestax/index.shtml: 'New Jersey assesses a 6.625% Sales Tax'. Registration requirement, filing deadlines, the monthly payment trigger and the zero-return rule quoted verbatim from https://www.nj.gov/treasury/taxation/su_12.shtml. The 15-day pre-sale registration deadline is from the NJ-REG instructions.


## States not covered

Do not invent rules for these. Report them as uncovered and link the state's own pages.

What typically comes into play:
- Foreign qualification with the Secretary of State, if the company is transacting business there
- A registered agent in that state, which is normally required once qualified
- State income or franchise tax registration and filing
- Payroll withholding and unemployment insurance registration, if the company is the legal employer of someone working there
- Sales tax registration, if the company sells something taxable to customers there

