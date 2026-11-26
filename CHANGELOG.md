# Changelog — Counting House public accounts

## [Unreleased] - 2026-11-26

### Added
- Remedies & claims workbench for current-year (2026) FOI, EIR, SAR, complaint and disclosure-history leads.
- Legal-route inventory and internal nominal-code map, with separate statuses for evidence-only, proposed/disputed, agreed/awarded, paid/cleared and unclassified receipts.
- Browser-local entry register, JSON backup, CSV and Beancount memorandum exports, nominal-code report, and guarded draft schedules. Separate fields display source response/review, regulator/tribunal/Ombudsman, judicial-review and civil limitation dates. No invoices or messages are sent automatically.
- Import paths for Dartboard's FOI/EIR/SAR tracker, That Old Chestnut findings and the earlier current-costs event list. Imports are unpriced evidence leads, not findings of liability.
- Internal suspense code 4190 and a local receipt workflow for the Dŵr Cymru £20 cheque; personal cheque data is not preloaded into the public source.
- Rule catalogue distinguishes CPR 46.5 / PD46's £24/hour litigant-in-person litigation costs rule from FOIA s.12's authority-side £25/hour staff-time calculation. Neither is a general hourly charge for waiting for disclosure.
- Added PHSO discretionary redress bands, police complaint / IOPC boundary and urgent judicial-review route (promptly and no later than 3 months, subject to statutory exceptions).
- Existing current-costs chronology retained but its misleading £24/hour valuation removed; repeated chasers are not treated as separate monetary entitlements.

### Safeguards
- Historic ledger/redress.beancount, ledger/claimed.beancount gate and 1987/1989 reopening workflow are unchanged.
- The browser-local claim register is not emitted into public/data.json, the public CSV or the cash ledger. Proposed values are memorandum-only and do not create an accounts receivable.
- A payment-request draft requires a verified/accepted/awarded entitlement, a positive amount and supporting evidence. Nothing is sent from the app.

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
