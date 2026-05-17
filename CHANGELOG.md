# Changelog

All notable changes to Cashdera are documented in this file.

## [1.0.0] - 2026-05-16

### Release
- First stable public release.

### Notes
- 1.0.0 is the first stable tag promoted from the 0.2.0 public beta baseline.
- No intentional breaking API/UX changes were introduced in the promotion step.

### Added
- Dashboard now shows separate counters for Transactions and Postings.
- Dashboard now separates Overview and Money Flow into tabs; Money Flow loads on demand.
- Categories page now includes account-type tabs: Expenses, Income, Assets, Liabilities, Equity.
- After successful import or re-import, the app automatically switches to the imported book.
- Recent imports now includes Delete action to remove Cashdera local import data and cache.
- All analytics aggregation now uses exact decimal arithmetic, eliminating cumulative rounding errors across large transaction sets.
- React ErrorBoundary added to the full route tree; unhandled render crashes show a reload prompt instead of a blank screen.

### Changed
- Dashboard account count now excludes the technical Root Account container.
- Date Range starts inactive on app launch and only filters analytics after the user chooses a range.
- Categories hierarchy behavior improved: better expand/select logic and clearer rollups.
- Dashboard client cache is invalidated immediately on any import or book refresh, preventing stale data after re-import.

### Fixed
- XML namespace parsing for account entities fixed (`gnc:account` vs `split:account`) to prevent phantom account rows during import.
- Re-import result messages are tied to the active background job, preventing stale job completions from showing counts for the wrong file.
- Dashboard avoids false empty states when postings exist but transaction headers are unavailable, using posting-backed transaction counts as a fallback.

### Security and Privacy
- Deleting an import removes only Cashdera local data; the original source `.gnucash` file is not modified or deleted.

## [0.2.0] - 2026-05-09

### Added
- Dashboard now shows separate counters for Transactions and Postings.
- Dashboard now separates Overview and Money Flow into tabs; Money Flow loads on demand.
- Categories page now includes account-type tabs: Expenses, Income, Assets, Liabilities, Equity.
- After successful import or re-import, the app automatically switches to the imported book.
- Recent imports now includes Delete action to remove Cashdera local import data and cache.
- All analytics aggregation now uses exact decimal arithmetic, eliminating cumulative rounding errors across large transaction sets.
- React ErrorBoundary added to the full route tree; unhandled render crashes show a reload prompt instead of a blank screen.

### Changed
- Dashboard account count now excludes the technical Root Account container.
- Date Range starts inactive on app launch and only filters analytics after the user chooses a range.
- Categories hierarchy behavior improved: better expand/select logic and clearer rollups.
- Dashboard client cache is invalidated immediately on any import or book refresh, preventing stale data after re-import.

### Fixed
- XML namespace parsing for account entities fixed (`gnc:account` vs `split:account`) to prevent phantom account rows during import.
- Re-import result messages are tied to the active background job, preventing stale job completions from showing counts for the wrong file.
- Dashboard avoids false empty states when postings exist but transaction headers are unavailable, using posting-backed transaction counts as a fallback.

### Security and Privacy
- Deleting an import removes only Cashdera local data; the original source `.gnucash` file is not modified or deleted.

## [0.1.0] - Initial Public Beta

### Added
- Local-first Windows desktop analytics for GnuCash files.
- Import and analysis pipeline for `.gnucash` books.
- Core pages: Dashboard, Transactions, Reports, Trends, Categories, Net Worth, Compare.
- CSV exports and PDF summary export.
- Offline-first architecture with local SQLite cache.
