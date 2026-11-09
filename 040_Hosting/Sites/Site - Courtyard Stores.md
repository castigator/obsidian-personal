---
tags:
  - hosting
  - site
---

# Site - Courtyard Stores

**Static since 2 Nov 2026.** Back to [[Hosting]].

- **URL:** https://courtyardstores.pebmarsh.com. About 170 visits a month.
- **Type:** static site on a [[Cloudflare]] Worker (`courtyardstores`, static assets) since 2 Nov 2026, replacing WordPress: a home page (shopfront photo, logo, opening hours, about, Facebook/Instagram) and a Mailing List page.
  - Source: GitLab `pebmarsh/courtyardstores` (private), cloned at `sites/courtyardstores/`. Cloudflare deploys on every push.
  - The sign-up form posts straight to the Courtyard Stores audience in [[Mailchimp]] (us19 account).
  - Opening hours are in `public/index.html`.
- **DNS:** `courtyardstores` is a Worker custom domain. The DreamHost A records for it and `www.courtyardstores` (173.236.240.244) were deleted on 2 Nov 2026. MX, TXT and `mysql.courtyardstores` are unchanged.
- **Left out of the rebuild:** the WordPress footer's demo contact details (a US phone number and a cattery's email address), and four empty, unlinked pages (Special Offers, New In, Meet the Team, Blog).

## The old WordPress site

- WordPress 7.1.4, theme vertice (Kubio page builder), folder `~/www/pebmarsh/courtyardstores.pebmarsh.com` on [[DreamHost]], database `courtyardstores_pebmarsh` on `mysql.courtyardstores.pebmarsh.com`. No longer reachable through courtyardstores.pebmarsh.com.
- Plugins: EWWW Image Optimizer, Insert Headers and Footers, Kubio, UpdraftPlus, WP Super Cache.
- **Archived 2 Nov 2026:** `www-pebmarsh-courtyardstores.pebmarsh.com.tar.gz` in Drive "Hosting Archives" (see [[Hosting Archive]]).
- **Removed 2 Nov 2026:** set to DNS Only and the database deleted in the DreamHost panel; folder deleted from the server. DreamHost now shows its "Site not found" page for this name.

- **Email:** `facebook@`, `mailinglist@` and `team@` forward to rupertthomas@gmail.com; `noreply@` is discarded. See [[Hosting Email]].
- **Mailing list:** a Courtyard Stores audience in [[Mailchimp]]. Since July 2026 it has been getting bot sign-ups (the "welcome email" alerts are a Mailchimp upsell, not a failure); see [[Mailchimp]].
