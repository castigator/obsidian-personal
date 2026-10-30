---
tags:
  - hosting
---

# Mailchimp

Mailing lists for the village and Courtyard Stores. Back to [[Hosting]].

- **Account:** "Pebmarsh.com", owner Rupert. Roger Cuthbert also sends campaigns.
- **Audiences:**
  - **Pebmarsh Mailing List:** about 240 recipients; campaigns as recently as May 2026, such as "Local Fund" and the charity football match.
  - **Courtyard Stores.**
  - 976 campaigns across all audiences.
- **Domain authentication:** pebmarsh.com was **authenticated on 28 Oct 2026**.
  - The DKIM records (`k2._domainkey` → `dkim2.mcsv.net`, `k3._domainkey` → `dkim3.mcsv.net`) had been entered wrongly in [[DreamHost]] (as `k2._domainkey.pebmarsh.com.pebmarsh.com`), so authentication had never worked before.
  - Mailchimp re-created the records in [[Cloudflare]] through a one-time authorisation; it can't make further changes.
- **To fix:** since mid-October 2026, repeated alerts say "Someone subscribed to Courtyard Stores but they did not receive a welcome email". Check the Courtyard Stores audience's welcome email or automation.
- **Find it in Mailchimp:** profile icon → Account & billing → Domains.
