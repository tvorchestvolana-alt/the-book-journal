# THE BOOK JOURNAL — Cloud beta

Private book translation tracker with Supabase Auth + RLS-protected `journal_data` JSON storage.

Deploy `index.html`, `manifest.webmanifest`, `icon.svg` to the root of GitHub Pages.

Before deployment: run `01_secure_database.sql` in Supabase SQL Editor; create a user in Authentication > Users and disable public sign-ups.

Supabase Authentication > URL Configuration: Site URL = https://tvorchestvolana-alt.github.io/the-book-journal/ ; add this exact URL to Redirect URLs.

Only the publishable key is embedded in the public frontend. Never commit service_role/secret keys or user data.

First login can offer migration of legacy local browser data if the cloud account is empty. Export JSON from old version before updating.

Known limitations: one JSON document per user (1 MiB database limit); no private file upload yet; simple last-write-wins cloud saves; avoid simultaneous editing in multiple tabs.
