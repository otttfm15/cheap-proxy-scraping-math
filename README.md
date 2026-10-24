# cheap proxy for scraping: Real Cost Math for Amazon, Google & Protected Sites, Which Plans Are Worth It

Searching for a cheap proxy for scraping usually means one of two things: your requests keep getting blocked, or your current proxy bill has outgrown your project. Here's the short answer before anything else. If your targets are Amazon, Google, Bing, LinkedIn, or sites sitting behind Cloudflare and Datadome, the cheapest route usually isn't a raw proxy list — it's a scraping API that charges per successful request and handles rotation, CAPTCHAs, and rendering for you. ScraperAPI sits in that category, with a permanent free plan of 1,000 credits per month, a 7-day trial with 5,000 credits, and paid plans from $49/month.

If your targets are plain, unprotected pages, a straightforward datacenter proxy service will cost less — sometimes dramatically so. Both routes are covered below with real numbers, because "cheap" in this market hides more traps than almost any other product category.

> **Quick picks**
> - Just testing: ScraperAPI's free plan (1,000 credits/month, 5 concurrent requests) plus the 7-day trial with 5,000 credits. No credit card required. 👉 [Get ScraperAPI's plans and current prices](https://www.scraperapi.com/pricing?fp_ref=coupons)
> - Light-to-moderate scraping of protected sites: the Hobby plan, $49/month or $44.10/month billed annually
> - Heavy volume on Amazon, Google, or LinkedIn: Business or Scaling, where the per-credit cost drops sharply
> - Simple targets on a tight budget: datacenter proxies from providers like Webshare cost cents per IP — comparison below

## What "cheap" actually means when you're scraping

The sticker price per GB or per IP tells you almost nothing on its own. Two numbers matter more.

First, what one *successful* request really costs. When a raw proxy gets blocked, you pay for the failed request and pay again on the retry. On protected targets, effective costs can double or triple before you notice. This is why the webscraping.ai comparison worked out the break-even point: at $3/GB residential pricing, 10,000 pages a month (roughly 5 GB) runs about $15, while 100 datacenter proxies cost about $3 for the same volume — but only if the datacenter IPs actually survive against your target. Against sites with serious bot detection, they won't, and the "cheap" option quietly becomes the expensive one.

Second, whether you pay for failures at all. ScraperAPI only charges credits for requests that come back. Its own marketing pages state this directly: "No charges for failed requests." Combined with rotation across a pool of 40 million+ IPs, built-in CAPTCHA solving, and automatic retries, you're buying outcomes rather than raw IPs. For difficult targets that's usually cheaper in practice. For easy targets it's overkill.

The catch, and almost nobody explains this properly: credits are not equal across sites. That's the next section, because it changes which plan you should buy.

## ScraperAPI plans and prices: the full table

All paid plans include JS rendering, premium residential and mobile IPs, advanced anti-bot bypassing, structured data APIs, DataPipeline, and crawler access. Annual billing knocks 10% off every tier.

| Plan | Monthly / annual price | Credits per month | Concurrent threads | Buy |
| --- | --- | --- | --- | --- |
| Free | $0 | 1,000 | 5 | [Start free](https://www.scraperapi.com/signup?fp_ref=coupons) |
| Hobby | $49 / $44.10 | 100,000 | 20 | [Get Hobby](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Startup | $149 / $134.10 | 1,000,000 | 50 | [Get Startup](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Business | $299 / $269.10 | 3,000,000 | 100 | [Get Business](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Scaling | $475 / $427.50 | 5,000,000 | 200 | [Get Scaling](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Professional | $975 / $877.50 | 10,500,000 | 300 | [Get Professional](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Advanced | $1,975 / $1,777.50 | 21,500,000 | 500 | [Get Advanced](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Enterprise | Custom | 22,000,000+ | 500+ | [Talk to sales](https://www.scraperapi.com/pricing?fp_ref=coupons) |

Annual billing works out to the same 10% discount on every tier: Hobby drops from $588 to $529.20 a year, Startup from $1,788 to $1,609.20, Business from $3,588 to $3,229.20. If you already know you'll run past three months, paying annually saves real money.

Two quirks worth knowing before you pick. Hobby and Startup limit geo-targeting to US and EU only, and their analytics dashboard only keeps 30 days of history. Country-level targeting and unlimited analytics start at Business. And Scaling is the tier ScraperAPI itself labels "Most popular" — a useful hint about where their actual customer base sits.

## The credit math most comparisons skip

Here's the part that determines whether a plan is actually cheap for *your* project. ScraperAPI's official pricing page is blunt about it:

> A standard page costs 1 credit. Amazon costs 5, Google and Bing (including their subdomains) cost 25, and LinkedIn costs 30. Sites behind bot protection like Cloudflare, Datadome, or PerimeterX add 10 credits per request when we bypass them.

Run your target list against that table and the numbers change fast. On the Hobby plan's 100,000 credits, you get:

- **100,000 standard pages** — plain blogs, product listings without protection
- **20,000 Amazon pages**
- **4,000 Google or Bing searches**
- **About 3,300 LinkedIn requests**
- **Roughly 9,000 requests** against Cloudflare-protected sites (1 + 10 per bypass)

The same 100,000 credits stretch across very different realities, and the official page doesn't put this math next to the price tags. ScraperAPI does give you the tools to check before committing, though: the Domain Cost Estimator in your dashboard shows the exact credit cost for any URL, and you can set a `max_cost` parameter per scrape so a single heavy request can't blow through your budget. Use both before choosing a tier — five minutes of checking beats a month of watching credits evaporate.

This is also why the "$1/GB" headlines you see in proxy comparison posts can be misleading. A $1/GB residential proxy that fails against Google's anti-bot wall three times out of four effectively costs you $4 per successful scrape. A Google request on ScraperAPI costs a fixed 25 credits with rotation, CAPTCHA handling, and retries included, and you know the price in advance.

## When a raw proxy service is genuinely cheaper

No contest here: for easy targets, plain proxy providers win on price. If you're scraping pages with no meaningful bot detection, buying raw datacenter IPs costs cents. Verified entry prices from current comparisons:

| Provider | Type | Entry pricing |
| --- | --- | --- |
| Webshare | Datacenter | $0.0299/IP/month (100 IPs); residential from $3.50 for 1 GB |
| IPcook | Residential / datacenter | Residential from $0.50/GB on bulk plans, traffic never expires; datacenter $0.04/IP/day |
| DataImpulse | Rotating residential | From $1/GB (the company's own claim) |
| Decodo | Residential | Around $2/GB, the third-party-tested pick for hard targets |
| Oxylabs | ISP | $1.60/IP/month (10 IPs) |
| Bright Data | Residential | $4.00/GB at entry volume |

A few thousand requests a day against public listings or classifieds sites? One of those datacenter plans will cost less per month than a single coffee, and there's no reason to pay for an API layer you don't need. Several independent reviewers make the same split: datacenter for easy targets, residential for anything that fingerprints aggressively like banking portals.

The equation flips when blocking starts eating your hours. ScraperAPI is a different product category — you're paying for someone else to absorb the blocks, CAPTCHAs, and headless-browser overhead. Its Structured Data Endpoints go further and return parsed JSON for Amazon, Google, Walmart, eBay, and Redfin, so there's no parser to maintain at all. If your time has any value, retry loops against a rotating wall of blocks are the hidden cost that never shows up in a $/GB comparison.

## Hidden rules that change your real bill

The fine print is where ScraperAPI actually gets more consumer-friendly than most competitors, with one exception to watch. The details:

1. **Overage is free.** Exceed your concurrency limit and you get a 429 response asking you to back off and retry. In the company's words: "There's no extra charge for going over, the request is simply turned away rather than queued."
2. **Credits running out pauses, not bills.** Scraping stops when your credits hit zero, rather than silently charging you for the excess.
3. **You control what happens next.** Auto-upgrade (opt-in, available on Hobby through Professional) bumps you to the next tier automatically. Pay-as-you-go — only on Scaling, Professional, Advanced, and Enterprise — continues at a fixed per-credit rate up to a monthly spending cap you set yourself.
4. **Refund policy is explicit.** Seven days, no questions asked, handled through support. You can also cancel anytime from the dashboard without a cancellation fee.

That last point pairs nicely with the trial: you can sign up, burn through the 5,000 trial credits against your real target sites, and still walk away inside a week owing nothing if the results disappoint. 👉 [Try the 7-day trial with 5,000 free credits](https://www.scraperapi.com/signup?fp_ref=coupons)

## Discounts: what's confirmed and what to double-check at checkout

The only discount ScraperAPI itself advertises is the 10% off for annual billing, shown on the official pricing page.

Third-party coupon sites list additional 10%-off codes, including one that was still marked as verified in October 2026 and applies to your first month. Treat any code from an aggregator the same way you'd treat a proxy claim: test it at checkout before assuming it works. Some of these codes carry restrictions the coupon pages only mention in passing, and codes that circulate on third-party sites have a habit of dying without notice. The annual-billing discount, by contrast, is built into the official price table and needs no code at all.

One more practical note: the discount codes apply at the checkout page's promo field, so pick your plan first, then paste the code. Nothing here stacks into the 28% or 50% off figures you might see floating around coupon aggregators — those listings are exactly the kind the better coupon guides openly call unverified.

If you're ready to lock in a plan, the pricing page is where both the annual discount and any code get applied in one place. 👉 [Check ScraperAPI's current pricing with annual discount applied](https://www.scraperapi.com/pricing?fp_ref=coupons)

## Which plan fits which situation

- **You're scraping standard pages — blogs, directories, unprotected product listings.** Hobby at $49/month is genuinely solid. 100,000 credits at 1 credit per page is a lot of pages, and 20 concurrent threads covers most solo projects.
- **Your targets are Google, Amazon, LinkedIn, or Cloudflare-walled sites at real volume.** The credit multipliers eat a small plan quickly, so start at Startup ($149) or Business ($299). Business is also the first tier with country-level targeting and unlimited analytics history.
- **You need millions of requests monthly with predictable spending.** Scaling ($475) or above, where pay-as-you-go with a spending cap keeps overruns controlled instead of surprising.
- **Your targets are easy and your budget is minimal.** Skip the API category entirely — a Webshare or IPcook datacenter plan costs dollars per month at entry level. Just accept that you're managing blocks and retries yourself.

Before you click buy on any tier, do the one thing this article exists to convince you of: run your actual target URLs through the Domain Cost Estimator and multiply out your monthly volume at the real per-request cost. The gap between "100,000 credits" and "4,000 Google scrapes" is the difference between a plan that's cheap and one that isn't. 👉 [Compare ScraperAPI's plans and pick your tier](https://www.scraperapi.com/pricing?fp_ref=coupons)

## FAQ

**Is ScraperAPI cheaper than buying residential proxies directly?**
For protected targets, usually yes once you count retries; for easy targets, no. Residential proxies run from about $0.50–$4.00 per GB depending on provider and volume, but every blocked request costs you bandwidth. ScraperAPI charges a fixed credit cost per site type, doesn't bill failed requests, and bundles CAPTCHA solving and rendering — the tradeoff is paying for infrastructure you might not need on simple sites.

**Is there a free option?**
Yes. A permanent free plan gives 1,000 credits per month with 5 concurrent connections, and new accounts get 5,000 additional credits for the first 7 days, with no credit card required.

**Does ScraperAPI charge by bandwidth?**
No. All plans are billed by API requests (credits), not bandwidth. This matters because bandwidth-based residential proxy pricing is what makes retry-heavy projects expensive.

**What happens if I run out of credits mid-month?**
Scraping pauses until renewal by default. You can optionally enable auto-upgrade (moves you to the next tier) or, on Scaling and higher plans, pay-as-you-go at a fixed per-credit rate with a monthly spending cap you define.

**Can I get a refund?**
Yes — ScraperAPI offers a 7-day no-questions-asked refund policy. Contact support through the dashboard to process it, and you can cancel a subscription at any time without a fee.
