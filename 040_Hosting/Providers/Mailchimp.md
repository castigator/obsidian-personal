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
- **9 Nov 2026: sending paused for the whole account.** Free plan, 271 of 250 contacts, pushed over by the bot sign-ups below. This blocks the Pebmarsh Mailing List too. Fix: archive the bots (archived contacts don't count). The alerts go back to May 2026: 82 sign-ups, of which 74 look like bots. Kept as genuine or to check: Kate Stubbs, Dionne Bartlett, Stephen Elmes, John Fennelly, Kay Reed, Claire Lock, Paul Press.
- **Export review (9 Nov 2026), after Rupert archived 48 bots from July onwards:** the audience still had 212 subscribed, 2 unsubscribed and 1 cleaned. About 105 are genuine: the December 2024 pop-up sign-ups (village people) plus a few later ones. 110 are bots: the bots started in **January 2026**, not May, and nearly all came in through the Embed Form. Rule used: Embed Form and signed up from June 2025 onwards, except Sarah Jarman, Stephen Elmes and Simon Aslett (UK, plausibly real); also all the unsubscribed and cleaned contacts. One pop-up sign-up looks dubious: chw@inpectorerobur.org ("Charles Whilems", Jul 2025).
- **To fix: bot sign-ups to Courtyard Stores (found 9 Nov 2026).** The "did not receive a welcome email" alerts are a Mailchimp upsell, not a failure (the audience has no welcome automation). Each one reports a new subscriber, and about 50 since July 2026 are mostly bots: made-up names (Lesch, Rogahn, Kuphal, Cruickshank), dotted Gmail variants (jp.aper00 / jpap.er00), "apple order" / "order samsung", .top/.help domains, and mostly German residential IPs. Classic subscription bombing: real people's addresses are signed up to bury other mail. They post straight to the list-manage endpoint, so the site's honeypot doesn't stop them. Because the alerts arrive, double opt-in must be off. Risk: campaigns to these addresses draw spam complaints, and a suspension would hit the whole account, including the Pebmarsh Mailing List. Fix (Rupert, in Mailchimp): turn on double opt-in and reCAPTCHA for the Courtyard Stores audience, then archive the bot contacts (genuine ones such as Kate Stubbs kept).
- **Find it in Mailchimp:** profile icon → Account & billing → Domains.
