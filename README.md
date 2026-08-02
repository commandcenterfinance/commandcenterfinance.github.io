# CommandCenterFinance brand site

One-page brand site for the [CommandCenterFinance Etsy shop](https://www.etsy.com/shop/CommandCenterFinance), built for AI/answer-engine discoverability (AEO):

- `index.html` — semantic one-pager with `Organization`, `Product`, and `FAQPage` JSON-LD schema
- `llms.txt` — catalog summary for AI crawlers ([llmstxt.org](https://llmstxt.org) format)
- `robots.txt` — explicitly allows GPTBot, ClaudeBot, PerplexityBot, and other AI crawlers
- `sitemap.xml`, `.nojekyll`

## Deploy (GitHub Pages)

1. Create GitHub account/org **commandcenterfinance** (the site URLs assume `commandcenterfinance.github.io`).
2. Create a public repo named **commandcenterfinance.github.io**.
3. Push this folder to it (`main` branch). Pages auto-publishes root sites named `<user>.github.io` — no settings needed.
4. Verify https://commandcenterfinance.github.io/ and https://commandcenterfinance.github.io/llms.txt load.

If a different username is used, update the absolute URLs in `index.html` (canonical, og:url, JSON-LD), `llms.txt`, `robots.txt`, and `sitemap.xml`.

## Maintenance

- When a "coming soon" product goes live on Etsy: swap its card's `<span class="soon">` for a Buy link, add a `Product` schema block, and update `llms.txt`.
- When the launch sale ends (Aug 31, 2026): update the price line in the live product card and the `priceValidUntil`/`price` in the JSON-LD.
- Add real customer quotes only once reviews exist — never fabricate ratings/reviews in schema.
