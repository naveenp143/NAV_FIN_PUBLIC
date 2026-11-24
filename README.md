# NAV Books

Bookkeeping for your household and your small business that runs on your own Windows PC. Bring in
your bank and card activity, sort it into categories, check it against your statements each month,
and print the year-end reports your tax preparer asks for. Your books stay on your computer in an
encrypted database. There is no account and nothing is uploaded.

## Download

Get the latest version from **[Releases](../../releases/latest)**: `NAV-Books-Setup.exe`
(Windows 10 or 11, 64-bit).

- [Download page with step-by-step install](https://naveenp143.github.io/NAV_FIN_PUBLIC/)
- [Release notes](CHANGELOG.md)

## Install on Windows

1. Double-click `NAV-Books-Setup.exe`.
   If Windows says "Windows protected your PC": More info > Run anyway.
2. Click Next until it finishes.
3. Open it from the Start menu or the Desktop: **NAV Books**.

Nothing else has to be installed: the installer carries its own Python, the encrypted SQL database
engine and every library it needs. It installs for you only, with no administrator rights. To remove
it: Settings > Apps > Installed apps > NAV Books > Uninstall. Your books are not deleted.

## Updating

Download the newest installer and run it again. Your books and settings are left alone.

## What it does

- **Two sets of books, ready from the start.** Personal and Business are created on first run and
  kept separate. Switch between them with one click. Add more books if you need them.
- **Bring in your data.** Bank and card files (CSV, QFX, OFX), everything from QuickBooks (Journal
  report as Excel or CSV, or IIF), everything from Quicken (QIF). Transactions are filed into the
  right year and duplicates are skipped.
- **Connect your bank** (optional) through SimpleFIN Bridge or Plaid, using your own account there.
  See [Connecting your bank](BANK_SYNC.md).
- **Sort into categories**, with rules the app learns so it sorts repeat payees for you.
- **Check against your statement** every month (reconciliation), with a saved report.
- **Reports:** Profit & Loss (and month by month), Balance Sheet, Tax Summary by Schedule C / A / B
  line, Cash Flow, Trial Balance, General Ledger. Print, save as PDF, or export to Excel.
- **Finish the year:** locks the year and starts the next one in its own folder with the right
  starting balances.
- **Help on everything.** Every button and field has a ? that explains it in plain words, and every
  page has a "Help me with this page" button.

## Where your books are kept

```
Documents\NAV Books\
    Personal\2025\books_2025.db
    Personal\2026\books_2026.db
    Business\2026\books_2026.db
    Backups\
    workspace.json
```

Each year is its own database file, encrypted with SQLCipher (AES-256). Each person signs in with
their own name and password. **There is no password recovery.** If every admin forgets their
password, the books cannot be opened. Use Settings > Back up now regularly and keep a copy off the
computer; backups stay encrypted.

## Built to stand up to an audit

- **Nothing is erased.** A mistaken entry is cancelled with a reversing entry and both stay visible.
  The database itself refuses deletes and amount edits.
- **Admin entry for anything unusual.** Cancelling an entry that was already matched to a statement,
  changing a finished year, or reopening one needs an admin's password and a written reason.
- **Activity log.** Every entry, change, cancellation, import, sign-in and approval is recorded with
  the user, date and time, the approving admin, the before and after values, a location label, and
  the computer's details captured automatically (device name and ID, Windows edition and build,
  processor, memory, Windows account, network address).
- **Tamper evident.** Log entries are chained with SHA-256 hashes. The Activity log page verifies the
  chain and shows if anything was altered. The full log exports to CSV.

The app keeps a careful record, but it does not replace your receipts and source documents, and it
is not tax advice. Keep your receipts and check the Tax Summary with your tax preparer.

## If something goes wrong

Open an [issue](../../issues) and say what you were doing and what the message said. Never attach
your books or passwords.
