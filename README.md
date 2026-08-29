# Sharkeylicious — Brenda Sharkey

Digital business card. Live at **https://cards.sharkitectdigital.com/brenda-sharkey-668/**

**vCard / NFC target:** https://cards.sharkitectdigital.com/brenda-sharkey-668/vcard.vcf

Handcrafted chocolate, sweetened only with Stevia, Monkfruit, Allulose and Erythritol.
Company website: **https://sharkeylicious.com** (EN + ES).

## Files

| File | What it is |
|---|---|
| `index.html` | The card. Self-contained except Google Fonts (Fraunces + Outfit). |
| `vcard.vcf` | vCard 3.0 with embedded logo photo. **The QR and NFC chip both point here.** |
| `qr-code.svg` | On-page QR shown in the modal. |
| `logo.png` / `logo.webp` | Card mark and favicon. |
| `icon-192/512.png`, `apple-touch-icon.png` | Home-screen icons. |
| `manifest.json` | Add-to-home-screen support. |
| `.gitattributes` | `*.vcf -text` — **required.** vCard 3.0 mandates CRLF; without this git can normalize to LF and some phones reject the file. |

## Build notes

- **Card design standard held:** exactly one button (`Save My Contact`) and it opens the QR
  modal. No `saveContact()` JS download, no separate `qr-btn`, no `.vcf` anchor button.
- **Palette:** neutral white and grey text on chocolate. Gold carries the button, the QR,
  the divider ornament and the top hairline — colour goes on the accents, not the copy.
- **Button text is chocolate on gold, not white.** Gold is a light brand colour; white on
  gold fails contrast and reads washed.
- **Contact rows** show the real value in each: phone, email, then `sharkeylicious.com`.
  The website row was added 2026-08-29 once the site went live, matching the row pattern
  set by `lion-painting-remodeling`.
- **vCard carries a bare `URL:`** because sharkeylicious.com is a genuine company website.
  Per the design standard, a bare `URL:` renders as "homepage" in the saved contact and is
  reserved for real websites — social profiles use `X-SOCIALPROFILE` instead.

## Related

- Site source: `projects/clients/sharkeylicious/site/` in the Workforce HQ workspace
- Brand source of truth: `projects/clients/sharkeylicious/brand/brand-brief.md`
