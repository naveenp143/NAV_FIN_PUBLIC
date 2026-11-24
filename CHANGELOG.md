# NAV Books: release notes

Versions are the date of the build (year.month.day). Newest first.

## 2026.11.23

First version.

### Your books
- **Personal and Business books** are created on first run and kept separate. Switch with one click.
- **One encrypted database per year**, each in its own folder under `Documents\NAV Books`. Each
  person signs in with their own name and password.
- **Finish the year** locks it and starts the next year with the right starting balances.

### Getting your data in
- **Bank and card files:** CSV (with column matching), QFX and OFX. The bank's ending balance is
  compared with the app's.
- **QuickBooks:** the Journal report from QuickBooks Online or Desktop (Excel or CSV), with the
  Account List report for exact account types, or a Desktop IIF file.
- **Quicken:** QIF with accounts, categories, splits and transfers.
- **Connect your bank** through SimpleFIN Bridge. Plaid works if you have your own developer keys
  and an access token; Plaid's sign-in window is not built in yet.
- Everything is filed into the right year, and loading the same thing twice does not double it.

### Day to day
- **Sort into categories**, with rules the app remembers.
- **Check against your statement** each month, with a saved report of what matched and what is
  still outstanding.
- **Reports:** Profit & Loss, Profit & Loss by month, Balance Sheet, Tax Summary by Schedule C / A /
  B line, Cash Flow, Trial Balance, General Ledger. Print, save as PDF or export to Excel.
- **Help on everything:** a ? beside every button and field, and "Help me with this page".

### Audit trail
- Entries are never erased; mistakes are cancelled with a reversing entry.
- Unusual changes need an admin's password and a written reason.
- Every action is logged with user, time, computer details and before and after values, in a log
  that cannot be edited and shows if it was tampered with.

### Not yet
- Only tested on made-up sample files so far, not on real QuickBooks, Quicken or bank exports.
- No receipt attachments, invoices, payroll, investments tracking or multi-currency.
- Windows only.
