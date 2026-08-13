# Company compliance check

A free skill and MCP server that works out what your US company actually has to file with federal and state governments, then goes looking through your own documents for evidence you have done it.

Your documents never leave your machine. The server only ever receives structured facts like entity type and which states you operate in.

## Why this exists

On 2026-08-11 FinCEN permanently ended beneficial ownership reporting for US companies and started deleting the data it had collected. Almost every compliance checklist on the internet, and most AI assistants, still tell founders to file it.

That is the problem in one example. The rules move, and anything with the rules baked in goes stale silently. This keeps the rules on a server so they can be corrected in one place, and every single item links to the government's own page with the date it was last checked.

## Install

Add the server. No signup, no API key, no account.

```
https://medianfi.com/mcp
```

In Claude, add it as a custom connector. In ChatGPT, add it as a connector. Then install this skill:

```bash
npx skills add https://github.com/jmsheldon/median-compliance-skill
```

Then just ask:

> Check whether my company is up to date on its filings.

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

Verified today: **US federal, Delaware, New York.** Entity types: C corporation, S corporation, LLC, single-member LLC (including foreign-owned), partnership, benefit corporation.

Every other state is reported as not covered yet, with a link to that state's Secretary of State and tax authority. That is deliberate. An invented rule is worse than an honest gap.

More states are being added. Rules that fail a two-source check are held back rather than shipped.

## A few things it knows that most sources get wrong

- **BOI reporting is over for US-formed companies** as of the 2026-08-11 final rule. If you get an invoice to file or renew one, you do not need it.
- **The 2025 C corporation extension runs to September 15, 2026, not October 15.** For a tax year ending December 31 that began before January 1, 2026, the statute gives 5 months rather than 6. Most sources say October and are wrong for this year.
- **Delaware franchise tax is often calculated the expensive way.** You are allowed to recalculate using the assumed par value capital method, which for a startup with lots of authorized shares and few assets can turn a five-figure bill into a few hundred dollars.
- **A virtual mailbox in a state is not the same as doing business there.** Where your people are is what decides foreign qualification.
- **New York sales tax economic nexus needs both tests**, over $500,000 in receipts AND over 100 transactions. New York is one of only two states using AND rather than OR.

## Who made this

[Median](https://medianfi.com), the finance team for owner-led businesses and US startups. We keep books current and file taxes. We built this because our own customers kept asking the same question and there was no good free answer.

We do not do compliance filings, so most of what this finds routes you to the government's own page rather than to us. Where an item is something we genuinely do, it says so.

## License

MIT. Fork it, change it, ship it.
