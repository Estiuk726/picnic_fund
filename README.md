# Family Picnic Fund

Deposit tracker for the family annual picnic fund: 200 taka per person per month, due by the 15th.

- **Website:** `index.html`, hosted on GitHub Pages. Password protected.
- **Database:** Supabase project `family-picnic-fund` (Mumbai). Tables are locked; the site can only call three password-checked functions (`pf_get`, `pf_add`, `pf_undo`). The password is stored only as a bcrypt hash in the database, never in this repo.
- **Excel:** "Download Excel" on the site gives a Summary sheet and every deposit. A weekly .xlsx backup is also saved to Google Drive.
- **Keep-alive:** a daily GitHub Action pings the database so the free Supabase project never pauses.

No money data is stored in this repo.
