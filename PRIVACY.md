# Privacy Policy

Effective date: 2026-04-28

## Summary

Cashdera is designed as a local-first desktop application. Your GnuCash files and imported financial data stay on your device.

## Data Processed Locally

The application may read and process:

- selected `.gnucash`, XML, or supported GnuCash-related files;
- account names, transaction descriptions, memos, dates, amounts, and commodity/currency metadata from selected files;
- derived analytics such as monthly cashflow, category summaries, budgets, trends, and net worth values;
- local application settings such as theme, timezone, and current book selection.

The application stores local SQLite databases and settings in the operating-system application data directory for the app.

Deleting an import removes the local imported database and related local history for that book. It does not delete or modify your original GnuCash file.

## Telemetry

This version does not intentionally collect, transmit, or upload telemetry, analytics events, crash reports, usage metrics, GnuCash files, imported databases, or financial records to Ars M servers.

If telemetry, update checks, licensing activation, crash reporting, or cloud features are added later, this policy should be updated before release.

## Network Access

The current core analytics workflow does not require a server connection. The application is intended to work offline for importing and analyzing local data.

Third-party operating-system components used by the desktop runtime, such as Microsoft WebView2 on Windows, may be governed by their own privacy terms.

## File Access

The application accesses files only when you select them or when you re-import a previously selected book. File metadata may be used locally to detect whether a source book changed since the last import.

## Data Sharing

Ars M does not sell or share your local GnuCash data. Because this version does not intentionally upload your data, Ars M does not receive your imported financial records through the application.

## User Responsibility

You are responsible for maintaining backups of original GnuCash files and exported reports. The application is an analyzer and should not be treated as the only copy of your financial records.

## Contact

Privacy questions may be submitted through the issue tracker for the GitHub repository where this release is published.
