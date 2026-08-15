# Company compliance check

A free skill and MCP server that works out what your US company actually has to file with federal and state governments, then goes looking through your own documents for evidence you have done it.

Your documents never leave your machine. The server only ever receives structured facts like entity type and which states you operate in.

## Why this exists

On 2026-08-11 FinCEN permanently ended beneficial ownership reporting for US companies and started deleting the data it had collected. Almost every compliance checklist on the internet, and most AI assistants, still tell founders to file it.

That is the problem in one example. The rules move, and anything with the rules baked in goes stale silently. This keeps the rules on a server so they can be corrected in one place, and every single item links to the government's own page with the date it was last checked.

## Install

Two pieces. The server carries the rules and is the part that matters. The skill teaches your assistant how to search your own documents for evidence, and is optional.

**The server** is `https://medianfi.com/mcp`. No signup, no API key, no account.

| Where you are | How to add it | Skill |
|---|---|---|
| Claude desktop or claude.ai | Settings > Connectors > Add custom connector, paste the URL, Add | Download this repo as a ZIP and upload it under Customize > Skills |
| Claude Code | `claude mcp add --transport http --scope user median https://medianfi.com/mcp` | `npx skills add https://github.com/median-labs/median-compliance-skill` |
| ChatGPT | Settings > Connectors > Add | Not supported, the server alone still works |

**Add the server before you start the session you plan to use it in.** A connector added mid-session does not appear until the client reloads, and an assistant that cannot reach the rules will answer from its own training data instead, which is the failure this whole project exists to prevent. If the `claude` command is not on your PATH you are on the desktop app: use its settings UI, and do not hand-edit `~/.claude.json`.

Then ask, naming the company:

> Check whether Acme Robotics Inc is up to date on its filings.

Name it even if it is the only company you own. Your assistant can see every entity whose paperwork has ever passed through your machine, and naming one keeps the answer about that one.

## What it does

1. Reads what it can find about your company first, then asks you to correct it, rather than making you fill in a form.
2. Settles the questions that change the answer before deriving anything. The big one is who your legal employer is: if you are on an employer of record, the state payroll registrations sit under their entity and you are supposed to have none of your own.
3. Works out what applies to your entity type and footprint.
4. Hunts for evidence in your files, email and connected tools, strongest source first.
5. Where it cannot find something, it tells you the likely innocent explanation before asking you a question about it.
6. Gives you a report with the deadline, the cost, the exact fix and the government link for each item.

## What it will not do

It will not tell you that you are compliant. It is a checklist and a document finder, not legal or tax advice, and not a substitute for your attorney or accountant. It does not file anything, and it never logs in to a government site as you.

It also will not tell you something is missing just because it could not find a receipt. A missing document usually means a bundled fee, a personal card, a lawyer's inbox, or a registry that does not publish that field. Every item carries the innocent explanations, and unresolved stays unresolved rather than turning into a false alarm.

## Coverage

**156 obligations across 13 jurisdictions**: US federal plus California, Colorado, Delaware, Florida, Georgia, Illinois, Massachusetts, New Jersey, New York, Pennsylvania, Texas and Washington. Entity types: C corporation, S corporation, LLC, single-member LLC (including foreign-owned), partnership, benefit corporation and nonprofit. Categories: entity filings, registered agents, income and franchise tax, payroll, unemployment, workers compensation, sales tax and information returns.

Every other state is reported as not covered, with a link to that state's Secretary of State and tax authority. That is deliberate. An invented rule is worse than an honest gap.

Every rule carries the government page it came from and the date it was last checked. Where a fee or deadline could not be confirmed at the source, the obligation still appears but the number is withheld rather than guessed.

## A few things it knows that most sources get wrong

- **BOI reporting is over for US-formed companies** as of the 2026-08-11 final rule. If you get an invoice to file or renew one, you do not need it.
- **The corporate and pass-through extended deadlines are different, and get swapped constantly.** A calendar-year C corporation extends to October 15. A partnership or S corporation extends to September 15. Reading the statute alone gets the C corporation answer wrong, because Treasury grants a flat six months by regulation.
- **Delaware franchise tax is often calculated the expensive way.** You are allowed to recalculate using the assumed par value capital method, which for a startup with lots of authorized shares and few assets can turn a five-figure bill into a few hundred dollars.
- **A virtual mailbox in a state is not the same as doing business there.** Where your people are is what decides foreign qualification.
- **New York sales tax economic nexus needs both tests**, over $500,000 in receipts AND over 100 transactions. New York is one of only two states using AND rather than OR.
- **New Jersey's Corporate Transit Fee is a cliff, not a band.** Once taxable net income crosses $10 million the 2.5% applies to the entire amount, not the excess, so $10.1 million owes roughly $252,000 rather than $2,500.
- **New Jersey still has the 200-transaction sales tax prong.** Several sites claim it was repealed in 2024. It was not, and the repeal bills introduced in January 2026 are not enacted.
- **Georgia's corporate rate is 4.99% for 2026** under HB 463, signed May 2026. The Department of Revenue's own corporate page is stale at 5.19%.
- **State registries publish more for free than almost anyone assumes.** Delaware gives you the registered agent, Colorado gives you good-standing certificates, Pennsylvania gives you officers and governors, all at no charge. A tool that sends you to a paid lookup for those is wrong.

## Maintenance, and how to tell us a rule is wrong

**Maintained by Jacob Sheldon at Median.** Rules are re-verified against their government sources on a monthly cycle, first Monday, and any rule older than 90 days is rechecked or withdrawn.

Every report states the **oldest** verification date across the rules it used, as "Sources verified through YYYY-MM-DD". That is deliberately the oldest and not the newest, so one freshly checked rule cannot make a stale report look current. Treat anything near that horizon as needing a look at the source before you act.

**If you find a rule that is wrong, [open an issue](https://github.com/median-labs/median-compliance-skill/issues) with the obligation id and the government page that contradicts it.** Wrong rules get fixed or pulled, not argued with. The dataset already carries corrections from about a third of what single-source research first produced, so this is expected rather than embarrassing.

Rules move fast enough that this matters: FinCEN ended BOI reporting by final rule three days before this shipped, and most checklists online still say to file.

## Privacy, and what gets sent

Your documents never leave your machine. The assistant reads your files, email and accounts locally, and sends the server only structured facts: entity type, state and date of formation, two-letter state codes, a revenue band rather than any figure, the payroll and incorporation arrangement, and yes or no answers to threshold questions.

It never sends documents, EINs, addresses, people's names, bank details or dollar amounts. No field accepts them.

Median logs those structural facts, what came back, and a company name **if your assistant chooses to send one**. That field is optional and the answer is identical without it, so leave it out if you would rather Median not know you ran this. Use is subject to [Median's terms](https://medianfi.com/terms) and [privacy policy](https://medianfi.com/privacy).

The public endpoint is rate limited. A normal session needs a handful of calls; if you are getting 429s, something is looping.

## Who made this

[Median](https://medianfi.com), the finance team for owner-led businesses and US startups. We keep books current and file taxes. We built this because our own customers kept asking the same question and there was no good free answer.

We do not do compliance filings, so most of what this finds routes you to the government's own page rather than to us. Where an item is something we genuinely do, it says so.

## License

MIT. Fork it, change it, ship it.

Which also means: provided as is, without warranty of any kind, and the authors are not liable for anything that follows from using it. This is a reference tool. Confirm anything you act on at the government's own page, which every item links to, and talk to an accountant or attorney licensed where you operate before making a decision that costs money.
