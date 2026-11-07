MARCIAL POPOCA WEBSITE – WHAT TO REPLACE BEFORE GOING LIVE

Search all files for "[" to find every placeholder:

1. [YOUR EMAIL]            – all pages (footer) + contact.html + privacy.html
2. [Booking calendar embed] – contact.html: booking link or Cal.com embed (see note)
3. [LinkedIn post embed 1-3] – results.html: post links or embeds (see note)
4. [2–4 weeks]             – services.html: diagnostic duration
5. [DATE] and retention    – privacy.html (have it checked; this is a draft)

NOTE ON EMBEDS
Third-party embeds can set cookies and may need a consent banner. Any embed also
has to be allowed in the Content-Security-Policy in _headers, or it will not load.

BEFORE SHARING THE SITE
Remove the "X-Robots-Tag: noindex" line from _headers so search engines can list it.
After adding a custom domain, set "workers_dev": false in wrangler.jsonc.

PUBLISHING
The site runs on Cloudflare Workers, connected to this GitHub repo.
Each push to main redeploys it. There is nothing to upload by hand.
New top-level files go live too unless they are listed in .assetsignore.
