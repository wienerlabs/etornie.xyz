# etornie.xyz

Marketing site for **Etornie** — the intellectual property OS for the on-chain era. Static HTML / Tailwind landing pages for [etornie.xyz](https://etornie.xyz), separate from the production app at `app.etornie.com` and the platform repo.

> Built by [Wiener Labs](https://wienerlabs.com) for Etornie AG · Ruessenstrasse 5, 6340 Baar, Switzerland · `info@etornie.com`

## Pages

| Path             | Purpose |
|------------------|---------|
| `/`              | Landing — hero mockup (Destek Patent client case), 5 feature sections, pricing, use-case testimonials |
| `/platform.html` | Platform overview — Cases, Documents, AI Agents, Deadlines, Solana, API |
| `/solana.html`   | Solana layer — wallet sign-in, ZK attestations, RWA tokenization, x402+zk pay-per-query, roadmap |
| `/attorney.html` | For attorneys — 195 jurisdictions, deadline tracking, EtornieGPT, multilingual UI |
| `/pricing.html`  | Firm tier ($499/mo per counsel) and Enterprise (Custom), pricing FAQ |
| `/docs.html`     | Developer docs — quickstart, JWT + wallet auth, Cases / AI / Agent / Webhook reference |
| `/privacy.html`  | Privacy Policy (GDPR + Swiss FADP) |
| `/terms.html`    | Terms of Service (Swiss governing law, Zug jurisdiction) |
| `/dpa.html`      | Data Processing Addendum (Article 28 GDPR) |

> The three legal pages carry a **Draft — pending legal review** banner. They are working templates; final terms must be issued by Etornie AG's counsel before any contract execution.

## Stack

- Static HTML + [Tailwind CSS](https://tailwindcss.com) via CDN (production build pending)
- [Geist](https://vercel.com/font) typography + [Inter](https://rsms.me/inter/)
- [Iconify](https://iconify.design) — Solar icon set + simple-icons brand marks
- [Unicorn Studio](https://unicorn.studio) hero background scene
- In-house SVG brand mark (`logo.svg`)

## Local preview

The site is plain static files; any HTTP server will do.

```bash
# from the repo root
python3 -m http.server 5182
# → http://localhost:5182
```

Or via Bun:

```bash
bunx serve -p 5182
```

No build step. Edit the HTML, refresh the browser.

## Assets

- `logo.svg` — Etornie brand mark (blue field, white vertical bar + asterisk rays)
- `destek-patent-white.png` — Destek Patent's transparent logo, sourced from [destekpatent.com](https://destekpatent.com) for the client-card mockup. Replace or remove before public launch unless usage is cleared with Destek Patent.

## Roadmap

- Tailwind production build (PostCSS) — drop the CDN warning
- Migrate to Next.js with a shared layout — DRY the navbar/footer that is currently inlined in 9 pages
- Customers and Brand-kit pages
- Final legal review of `privacy.html`, `terms.html`, `dpa.html`
- Vercel deploy + CNAME for `etornie.xyz`
- Wire `Sign up` / `Log in` CTAs to live `app.etornie.com`

## Related repos

- `etornie-solana` — FastAPI + Next.js platform (the actual product behind `app.etornie.com`); landing site here (`etornie.xyz`) is a separate, marketing-only deploy.

## License

See [LICENSE](LICENSE). Proprietary; all rights reserved.

---

Built by [@wienerlabs](https://github.com/wienerlabs) for Etornie AG.
