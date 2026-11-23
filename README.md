# Family Picnic Fund

Deposit tracker for the family annual picnic fund: 200 taka per person per month, due by the 15th.

- **Website:** `index.html`, hosted on GitHub Pages. Two logins: **Admin** (everything) and **Cashier** (record payments, see records, download Excel, undo his own latest entry; cannot manage families or change who received the money).
- **Public dashboard:** `status.html`, no password. Shows totals (fund, each month's target, paid, due) and, behind a "See family details" button, each family's status for the month (Paid, Partly paid, Not paid). No per-family amounts or payment details.
- **Database:** Supabase project `family-picnic-fund` (Mumbai). Tables are locked; the site can only call password-checked functions; family management is admin only. Both passwords are stored only as bcrypt hashes in the database, never in this repo.
- **Excel:** "Download Excel" on the site gives a Summary sheet and every deposit. A weekly .xlsx backup is also saved to Google Drive.
- **Keep-alive:** a daily GitHub Action pings the database so the free Supabase project never pauses.

No money data is stored in this repo.
