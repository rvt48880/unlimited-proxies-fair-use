# unlimited proxies: What "Unlimited" Really Covers, Where the Fair-Use Caps Hide, and How to Pick a Plan Without a Bandwidth Meter

Search "unlimited proxies" and you get a wall of providers claiming unlimited bandwidth, unlimited IPs, unlimited requests. Read the terms and most of them mean something narrower: unlimited *while you stay under a threshold*, unlimited *until your concurrent sessions get cut*, or unlimited *if you buy 1,000 proxies first*. The word is doing a lot of work in this market.

So this is a breakdown of what the term actually covers across the major providers, which pricing model genuinely removes metering, and where the honest limits sit — using 9Proxy's plans as the working example, because its IP-based model is one of the few structures that removes traffic counting entirely rather than hiding a cap behind it.

## Three different things people mean by "unlimited proxies"

Before comparing anything, pin down which one you need. They lead to completely different purchases.

**Unlimited bandwidth.** You still get a fixed set of IPs, but you don't pay per gigabyte. Push 10 GB or 10 TB through the same proxy and the invoice doesn't move. This is what most "unlimited" marketing actually refers to, and it's the model 9Proxy's IP-based packages use.

**Unlimited endpoints.** You pay by traffic volume but you can generate as many proxy endpoints, sessions and rotation targets as your scripts want. Nothing is allocated per-IP, so there's no activation cost and no wasted inventory. 9Proxy's GB-based plans work this way — the docs are blunt about it: "Generate unlimited endpoints; only GB deducted."

**Unlimited requests.** Almost always a soft promise. No provider sells literally unbounded concurrency, because concurrency is what costs them money. Some sell it as a throughput ceiling (Geonode's unlimited residential tiers are priced by speed: 200 Mbps up to 1,000 Mbps), and PlainProxies states plainly that on its unlimited residential plans the only enforced limit is throughput in Mbps.

If your workload is bandwidth-heavy but IP-light, you want the first. If it rotates constantly across thousands of IPs but each request is small, you want the second.

## The fair-use fine print nobody puts on the landing page

This is where the keyword gets expensive. A provider can advertise unlimited traffic and still write itself an exit, and most of the big names do. The exact thresholds differ, so here's what's actually documented:

- **Bright Data** gives unlimited static residential (ISP) proxies but attaches a 100 GB per month fair-use allowance to each IP, shared or dedicated. Blow past it and you get reminder emails, then overage billed at pay-as-you-go rates.
- **Oxylabs** doesn't cap traffic on ISP proxies, it caps sessions: up to 100 concurrent sessions for your first 50 GB in a month, dropping to 10 for the rest of that month once you cross it.
- **Decodo** applies a fair usage policy when two conditions both hit — total traffic over a subscription term exceeds 10 TB *and* per-IP traffic exceeds 25 GB — after which concurrent sessions are reduced for the remainder of the term.
- **Webshare** only offers unlimited bandwidth on its bigger dedicated tiers, with requirements around proxy counts (roughly 1,000 premium, 100 private, 75 dedicated). Lower tiers are metered, and the free plan is 10 proxies with 1 GB per month.
- **IPRoyal** sells unmetered mobile proxies with a 20–25 GB per day soft cap; its documented advice is to monitor that daily ceiling to keep peak performance.
- **ProxyScrape** offers genuinely unmetered residential and shared datacenter proxies, with no transfer cost scaling by usage.

Read that list again and a pattern shows up: residential IPs come from real devices that cost real money to maintain, so "unlimited residential bandwidth at a flat rate" is hard to sustain and almost always comes with a boundary written somewhere. The boundary might be GB, sessions, throughput, or how much inventory you bought first. It just won't be on the headline.

> The useful question isn't "is it unlimited?" It's "unlimited in what dimension, and what happens at the edge of it?" A cap that throttles your scraping at 3 a.m. is worse than a slightly higher per-IP price you can plan around.

## Pay-per-IP with unlimited traffic: the model that actually drops the meter

9Proxy splits its residential offering into two billing models that map onto the distinction above.

**Residential Proxy by IPs** is the flat-rate option. You buy a quantity of IPs, and each active IP carries unlimited traffic. There's no GB counter running in the background, no fair-use allowance attached to the IP, and no overage line on the invoice. In 9Proxy's own documentation the traffic limit field for this model reads "Unlimited during active time."

Two details matter as much as the unlimited traffic:

1. **Unused IPs never expire.** Balance-based means what you buy stays in your account until it's consumed. If you buy 5,000 IPs and use 1,200 this month, the 3,800 don't evaporate on the first of next month.
2. **Individual IP lifespan is a few hours to about 24 hours.** Residential IPs drop off when the real device goes offline, so this isn't a static-IP product. The docs are upfront: natural residential uptime, no guaranteed 30-day stickiness. You work through the balance and replace IPs as they retire.

There's one practical catch in the setup: IP-based proxies require the 9Proxy desktop app for local port forwarding (with optional proxy authentication), whereas the GB-based model works straight from the dashboard with username/password or IP whitelisting. If you're deploying to a server and would rather not run anything locally, that difference decides your choice of plan before price does.

**Residential Proxy by GB** flips the model. You buy traffic, generate as many endpoints as you like, and switch between sticky and rotating sessions, with targeting down to country, state, city, ZIP and ISP. The trade is that the meter is real here: 180-day validity on standard GB packages, unlimited validity on Enterprise.

The network behind both is advertised at 20M+ residential IPs across 90+ countries, over HTTP(S) and SOCKS5. Geekflare's 2026 review noted the coverage is 90+ countries rather than the full 195 and called US, UK, Europe and Southeast Asia coverage solid, while measuring a 97.7% success rate against Cloudflare-protected targets.

👉 [Check the current IP-based and GB-based package list](https://bit.ly/9-Proxy)

## Full 9Proxy price list

Here's the complete picture. Note that 9Proxy raised prices on IP-based and Bundle packages on June 1, 2026 — its first adjustment since launch — while GB-based pricing stayed exactly where it was. The figures below reflect the post-adjustment structure, cross-checked against two independent 2026 reviews that carried the updated numbers.

Prices are prepaid rather than recurring, which is why the "validity" column matters more here than a billing cycle would.

### Residential Proxy by IPs (unlimited traffic per active IP)

| Package | Effective rate | Price | Validity | Purchase |
| --- | --- | --- | --- | --- |
| 100 IPs | $0.24 / IP | $24 | Unused IPs never expire | [Order the 100 IP package](https://bit.ly/9-Proxy) |
| 500 IPs | $0.144 / IP | $72 | Unused IPs never expire | [Order the 500 IP package](https://bit.ly/9-Proxy) |
| 1,000 IPs + 500 bonus | $0.084 / IP | $126 | Unused IPs never expire | [Order the 1,000 IP package](https://bit.ly/9-Proxy) |
| 2,500 IPs | $0.084 / IP | $210 | Unused IPs never expire | [Order the 2,500 IP package](https://bit.ly/9-Proxy) |
| 5,000 IPs | $0.072 / IP | $360 | Unused IPs never expire | [Order the 5,000 IP package](https://bit.ly/9-Proxy) |
| 15,000 IPs | $0.048 / IP | $720 | Unused IPs never expire | [Order the 15,000 IP package](https://bit.ly/9-Proxy) |
| 25,000 IPs | ~$0.035 / IP | $863 | Unused IPs never expire | [Order the 25,000 IP package](https://bit.ly/9-Proxy) |
| 50,000 IPs | ~$0.029 / IP | $1,438 | Unused IPs never expire | [Order the 50,000 IP package](https://bit.ly/9-Proxy) |
| 100,000 IPs (Business) | $0.023 / IP | $2,300 | Unused IPs never expire | [Order the 100,000 IP package](https://bit.ly/9-Proxy) |
| 200,000 IPs (Business) | ~$0.021 / IP | $4,140 | Unused IPs never expire | [Order the 200,000 IP package](https://bit.ly/9-Proxy) |
| 500,000 IPs (Business) | ~$0.017 / IP | $8,625 | Unused IPs never expire | [Order the 500,000 IP package](https://bit.ly/9-Proxy) |

Effective rates are calculated from package price divided by IP count.

### Residential Proxy by GB (unlimited endpoints, metered traffic)

| Package | Effective rate | Price | Validity | Purchase |
| --- | --- | --- | --- | --- |
| 5 GB | $3.00 / GB | $15 | 180 days | [Order the 5 GB package](https://bit.ly/9-Proxy) |
| 50 GB + 5 GB bonus | $2.10 / GB | $105 | 180 days | [Order the 50 GB package](https://bit.ly/9-Proxy) |
| 100 GB | $1.50 / GB | $150 | 180 days | [Order the 100 GB package](https://bit.ly/9-Proxy) |
| 200 GB | $1.00 / GB | $200 | 180 days | [Order the 200 GB package](https://bit.ly/9-Proxy) |
| 1,000 GB | $0.80 / GB | $800 | 180 days | [Order the 1,000 GB package](https://bit.ly/9-Proxy) |
| 2,000 GB | $0.75 / GB | $1,500 | 180 days | [Order the 2,000 GB package](https://bit.ly/9-Proxy) |
| 3,000 GB (Enterprise) | $0.72 / GB | $2,160 | No expiry | [Order the 3,000 GB Enterprise package](https://bit.ly/9-Proxy) |
| 6,000 GB (Enterprise) | $0.70 / GB | $4,200 | No expiry | [Order the 6,000 GB Enterprise package](https://bit.ly/9-Proxy) |
| 10,000 GB (Enterprise) | $0.68 / GB | $6,800 | No expiry | [Order the 10,000 GB Enterprise package](https://bit.ly/9-Proxy) |

Enterprise GB includes team mode (one owner plus up to five members), no-expiration bandwidth sharing inside the team, per-member traffic controls, activity logs and dedicated support.

### Bundle Packages (IPs + traffic)

| Package | Contents | Price | Validity | Purchase |
| --- | --- | --- | --- | --- |
| Starter Bundle | 100 IPs + 5 GB | $30 | 180 days on bundled traffic | [Order the Starter Bundle](https://bit.ly/9-Proxy) |
| Popular Bundle | 1,500 IPs + 50 GB | $180 | 180 days on bundled traffic | [Order the Popular Bundle](https://bit.ly/9-Proxy) |
| Pro Bundle | 5,000 IPs + 500 GB | $720 | 180 days on bundled traffic | [Order the Pro Bundle](https://bit.ly/9-Proxy) |

## Which one you should actually buy

The pricing table makes the decision look like a math problem. It's mostly a workflow problem.

**Take the $24 / 100 IP package if** you're running a proof of concept, a handful of browser profiles, or a workload where you can't predict bandwidth at all. The whole point of paying per IP is that the twentieth gigabyte costs the same as the first. The IP count is your real constraint — figure out how many simultaneous identities you need, not how many requests you'll send.

**Take a GB package if** your tool rotates aggressively and each request is small: SERP checks, price scraping, ad verification, API polling. You're buying rotation volume, not identity stability, and the per-GB rate falls from $3.00 all the way to $0.68 as you go up. The $105 tier with the bonus 5 GB is the usual starting point for light continuous work.

**Take a bundle if** you need both and don't want to manage two balances. The Pro Bundle is $720 for 5,000 IPs plus 500 GB; bought separately at list, those pieces come to roughly $360 in IPs plus $400 in traffic, so the packaging matters less than the convenience of one credit pool with 180 days on it.

**Skip the big tiers if you're solo.** At 500,000 IPs the effective rate is about $0.017 per IP, which is genuinely cheap for residential. It's also completely useless to someone running ten browser profiles. The discount curve rewards resellers and agencies; if that isn't you, buying 100,000 IPs to get a better rate is just storing money in an account.

## What to check before you pay anywhere

A few things apply to 9Proxy specifically and to this category generally.

**Refunds.** 9Proxy's FAQ states plainly that it doesn't offer refunds, because the product is intangible. What it offers instead is a proxy replacement policy: check a non-working IP in the "Today" list in the app within 60 seconds and a replacement is added to your balance. Geekflare's review attributes the friction in 9Proxy's Trustpilot score to the refund policy rather than the network itself. Either way, the practical advice is the same — test before you commit to a large package, because there's no money-back exit.

**Trials.** There's no self-serve free trial button on the site. Trial access has historically run through community channels (the 9Proxy team is active on Black Hat World) with availability that varies, and at one point the offer was five proxies for new users. Ask before assuming you'll get one.

**Setup requirements.** Desktop app for IP-based proxies; dashboard-only for GB-based. That single line decides the plan for anyone deploying to a headless server.

**The 500,000 IP claim versus your use case.** 20M+ IPs across 90+ countries is a real network, but it isn't 195 countries. If you need a specific market outside the usual set, confirm targeting exists before buying — city, state, ZIP and ISP targeting only helps if the country is covered.

**Price direction.** 9Proxy raised IP-based and bundle prices on June 1, 2026, having held the line for three years, and left GB pricing untouched. That's a signal about where margin pressure sits: traffic is the expensive dimension, which is exactly why the IP-based unlimited-traffic model is interesting in the first place. Promotions do run — an 8% code ran over Lunar New Year, and an automatic 9% GB credit ran in April — so it's worth checking the dashboard's coupon section rather than hunting third-party coupon sites, several of which still list expired codes.

👉 [Start with the current packages and see what coupon is active in your account](https://bit.ly/9-Proxy)

## The short version

"Unlimited proxies" is a phrase that describes at least three different products. If you need unmetered bandwidth, buy by IP count from a provider that doesn't attach a fair-use allowance to each IP — and accept the trade: those IPs live for hours, not months, and you'll need local software to route through them. If you need rotation without allocation waste, buy by GB and treat the meter as part of the design. And whatever you choose, read the fair-use section before the pricing section. The cap is where the cost actually is.
