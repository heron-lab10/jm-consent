# OAuth consent page for open-brain-mcp

Static login + consent page for Supabase's OAuth 2.1 server. Claude (or any MCP client) is sent here during the OAuth flow; the user signs in, approves, and is redirected back with an authorization code.

**Deploy to GitHub Pages:** create a repo whose root is the contents of `consent/`, then Settings → Pages → Deploy from branch `main`, folder `/ (root)`. The page is `consent.html` at the repo root; GitHub Pages also serves it without the extension at `https://<user>.github.io/<repo>/consent`.

**Supabase (Authentication → OAuth Server):** Site URL = `https://<user>.github.io/<repo>`, Authorization Path = `/consent`.

**Reuse for another Mind:** change `SUPABASE_URL` and `SUPABASE_ANON_KEY` at the top of the script in `consent.html`.

Test: open `…/consent?authorization_id=test` → login form renders; after sign-in it shows an error for the fake id (expected).
