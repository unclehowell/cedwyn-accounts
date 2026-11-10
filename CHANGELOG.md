# Changelog — Counting House public accounts

## [0.4.0] - 2026-11-10

### Added
- Free-allowance check on every quote (“Free first?”): ✅ the free allowance the law gives came before the fee · ❌ not given · n/a not FOI, or a copy or statutory fee (free route noted) · ? not checked. Each line carries the regime, a short legal basis and a link to the provision on legislation.gov.uk (`free`, `free_regime`, `free_basis`, `free_route`, `free_url` in `quotes.beancount` and `data.json`). Count today: ✅ 8 · ❌ 2 · n/a 15 · ? 2.
- Three new lines: Llandough Community Council cost-limit refusal (11 Oct 2026, £450 / 18 h), Cabinet Office cost-limit reply (10 Nov 2026, £600 / 24 h), and a private copy-ordering website's title-register and title-plan prices (21 Sep 2026). Headline total quoted £681.19.

### Changed
- Cost-limit replies count with the quotes from bodies; estimates stay apart.

## [0.3.0] - 2026-11-10

### Added
- `ledger/quotes.beancount`: quotes and estimates received for copies, searches and records — 20 fee or paid-copy offers quoted by bodies and 4 of our own estimates, each with its price as written, VAT, date and source. Every line is "quote, not paid"; offers without a figure are flagged ! at £0.00. Kept apart from the cash accounts; never added to them.
- New tab “Quotes, not paid” (`#quotes`), built by `tools/build.py` into `data.json` (`quotes`).

### Unchanged
- Cash ledger, totals, the farm money memo and the held redress memo.

## [0.2.0] - 2026-10-25

### Added
- `ledger/farm.beancount`: the farm’s money, 1877–1987 — a memorandum ledger of money recorded between other parties about Great House Farm and its land (rents, the 1974 rent-free licence, estate and site sales, the 1962 legal charge, the 1969 takeover bid, court orders), each line with its catalogue ID. Lines with no figure on file are flagged GAP at £0.00. Kept apart from the cash accounts; never added to them.
- New tab “Farm money 1877–1987” (`#farm-money`), built by `tools/build.py` into `data.json` (`farm`). The courts’ view is stated first.

### Unchanged
- Cash ledger, totals and the held redress memo.

## [0.1.0] - 2026-10-24

### Improved
- Add a consistent, high-contrast `:focus-visible` treatment to keyboard-operable links, search, filters and controls.
- Announce the existing generated-at timestamp politely to assistive technology.

### Validated
- The page's displayed spend and “Built … from the plain-text ledger” metadata are embedded from `public/data.json`.
- Latest data snapshot: 2026-10-23 00:57 UTC, 26 ledger rows. No account values were altered or presented as newly reconciled.
