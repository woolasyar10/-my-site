NUSUK CODE HUB — STARTER WEBSITE

Files
- index.html: the website frontend.
- setup.sql: database setup and access policies.
- README.txt: these instructions.

IMPORTANT
This is a community website, not an official Nusuk service.
Never put a Supabase secret/service_role key in index.html. The publishable key is intended for browser use.
The owner UUID in setup.sql is tied to the configured Supabase Auth user. If that user changes, update the UUID in the SQL function and run the relevant SQL again.

DATABASE
1. Open your Supabase project.
2. Open SQL Editor.
3. Paste setup.sql and click Run.
4. Confirm it says Success.
5. In Table Editor, open public.nusuk_codes and confirm the columns:
   id, created_at, code, category, title, is_active, submitted_by.

WEBSITE TEST
1. Host index.html on a static hosting service (for example GitHub Pages, Netlify, or Cloudflare Pages).
2. In Supabase Authentication > URL Configuration, set Site URL to the deployed website URL and add that URL to Redirect URLs.
3. Test public code loading and a test submission. New submissions are published immediately. The owner can disable, re-enable, edit, or delete them at any time.
4. Sign in with the owner account to approve, disable, edit, or delete codes.

CURRENT LIMITATIONS
- The category choices are Nusuk, Umrah, Travel, Discount, and Other. Adding categories later requires updating both the website form and the allowed category list in setup.sql.
- The owner admin edit control uses simple browser prompts.
- This starter has not yet been deployed or fully tested against your live Supabase project. After replacing setup.sql with this updated version, run it again in Supabase SQL Editor so public submissions become active immediately.
