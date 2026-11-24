# Connecting your bank

NAV Books can fetch new transactions by itself. It does this through a provider account that you
own. The connection is read-only, and the access key is stored only inside your encrypted books.

## SimpleFIN Bridge (recommended)

1. Create an account at https://beta-bridge.simplefin.org (about $15 a year, paid to SimpleFIN).
2. There, connect your banks and credit cards.
3. Choose **Create setup token** (under Apps) and copy the long code.
4. In NAV Books: Connect my bank > SimpleFIN Bridge > paste the code > Connect.
5. Press **Choose accounts** and match each bank account to an account in your books.
6. Press **Sync now** whenever you want the latest transactions. Anything already in your books is
   skipped.

A setup token works once. If you need to connect again, create a new one.

## Plaid (advanced)

Plaid is aimed at developers. You need a Plaid developer account with production access, your client
id and secret, and an access token for each bank created with Plaid Link (for example with Plaid's
Quickstart). Enter those under Connect my bank > Plaid. Plaid's sign-in window is not built into NAV
Books yet.

## Not using either

Download a CSV, QFX or OFX file from your bank's website and use Bring in transactions. The result
is the same.
