---
tags:
  - hosting
  - site
---

# Site - Ernis

"Ernis Returns", a 10-page comic by Dylan Thomas, Tom Scroggs-Paris and Tommy Hele for Comic Relief (Red Nose Day, March 2007; the PDF is dated 15 March 2007). Ernis is a cool chicken with a red crown, standing for President. Kept for sentimental value. Back to [[Hosting]].

- **URL:** https://ernis.pebmarsh.com
- **Hosting:** [[Cloudflare]] Workers static assets (the Worker is called `ernis`), **since 29 Oct 2026**. It's free and needs no maintenance.
- **Source:** GitLab `pebmarsh/ernis` (private), cloned on the Mac at `~/workspace/gitlab/private/pebmarsh/sites/ernis`.
  - `public/`: what's served. That's a new page in the original 2007 style (yellow Courier on blue, the old `ernis.css` unchanged), the "Ernis for President" badge, and `Ernis_Returns.pdf`.
  - `original/`: the files exactly as they were on [[DreamHost]].
  - Cloudflare deploys automatically on every push to `main`. Preview builds are on for other branches.
- **DNS:** the `ernis` record is managed by Cloudflare as a Worker custom domain. The old DreamHost A records for `ernis` and `www.ernis` were deleted on 29 Oct 2026.
- **Email:** none. The `bollox@` mailbox went with the DreamHost domain deletion; its mail DNS records were dropped on 28 Oct 2026.
- **History:** on DreamHost, visitors only ever saw DreamHost's 2010 "Coming Soon" placeholder; the 2007 page itself was gone. The "visits" were almost all DreamHost's own uptime checks.

## Removed from DreamHost (29 Oct 2026)

- Rupert deleted ernis.pebmarsh.com in the DreamHost panel ("Permanently Delete Domain"), which also removed the `bollox@` mailbox and DreamHost's certificate renewals for it.
- The leftover folder `~/www/pebmarsh/ernis.pebmarsh.com` was deleted after its 3 real files checksum-matched `pebmarsh/ernis/original`.
