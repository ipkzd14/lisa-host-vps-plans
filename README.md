# LisaHost US VPS: Dual-ISP Residential IP Plans Compared, Real Pricing in Yuan, and Which US Location Actually Fits Your Setup

If you've been digging through forums looking for "LisaHost US VPS," you've probably already noticed the problem: LisaHost doesn't sell one US VPS product. It sells about seven different ones, spread across Los Angeles, New York, and Chicago, each with its own network routing, IP type, and pricing structure. Some plans give you a "native" US IP, some give you a dual-ISP residential IP that's supposed to look like a real home connection, and some are just plain CN2-optimized VPS with no residential angle at all. That distinction matters a lot depending on whether you're trying to unlock US streaming catalogs, run a stable AI/API endpoint, or just host something lightweight that talks back to mainland China without lag.

This piece walks through what LisaHost actually has on the shelf right now, what each line costs, what independent testers have found when they actually ran benchmarks on these boxes, and where the catches are — because there are a few, mostly around refund terms and bandwidth caps that aren't obvious from the marketing copy.

## LisaHost isn't one US VPS, it's seven

LisaHost (丽萨主机), operated as LisaHost Incorporation, LLC with an operations base listed in Hong Kong's New Territories, runs its entire catalog through a standard WHMCS storefront. For US-based VPS specifically, the product groups break down like this:

**9929 Premium Network VPS (Los Angeles).** This is the flagship US line, running through China Telecom/China Unicom's 9929 route. You can buy it with either a plain non-native US IP or a "native" US IP, and there's also a dual-ISP residential variant. Entry-level monthly pricing starts at ¥68/month for 1 core, 1GB RAM, 10GB NVMe, 50Mbps, and 1,000GB of traffic. There's also an unlimited-traffic "Pro" tier at ¥1,288/month with 4 cores and 4GB RAM if you're running something that chews through bandwidth.

**AS4837 Mainland-Optimized VPS (Los Angeles).** Same city, different backbone — this one forces traffic through China Unicom's AS4837 route and comes with noticeably fatter bandwidth allowances (up to 1Gbps on the top monthly tier). Entry pricing is also ¥68/month for a 1C/1G/20GB setup with 300Mbps and 3,000GB of traffic, which is actually a better traffic-to-price ratio than the 9929 line at the same price point.

**New York and Chicago dual-ISP VPS.** These are newer additions and mirror the AS4837 pricing structure almost exactly — ¥68/month entry, dual-ISP residential native IP, scaling up to unlimited-traffic Pro tiers around ¥498/month. If your use case cares about geographic diversity (not everything you're doing should look like it's coming from LA), these are the practical alternative.

**CERA CN2 GIA line (Los Angeles).** This is the odd one out — it's not residential-IP focused at all. It's a CN2 GIA route with built-in DDoS protection (50G by default, upgradable to 100G), and LisaHost sells a genuinely cheap ¥2 one-day trial capped at 1GB of traffic, one per customer, no refund. The regular basic plan is currently discounted to ¥50/month (listed as down from ¥75) for 1 core, 1GB RAM, and 500GB of traffic with the DDoS shield included.

**Residential static home-broadband VDS.** This is where LisaHost gets genuinely unusual for a VPS provider — these are IPs from actual home ISPs rather than a datacenter. The listings name specific carriers: Atlas Networks in Seattle, Astound Broadband (formerly WaveBroadband/RCN) in Los Angeles, and T-Mobile/Frontier in California. Pricing runs ¥169/month for the base tier up to ¥899/month for higher bandwidth/unlimited-traffic configurations, and it comes with free IPv6.

**Shared NAT residential IP.** The most niche and most expensive option — an OpenVZ-based setup in New York starting at ¥599/month for a shared IP with only 2 TCP/UDP NAT ports and a hard 10Mbps peak. LisaHost's own product description literally calls it "meteorite scarce, collector's item" pricing, which is marketing-speak for "this is a specialty product, not a general-purpose VPS." It carries no refund at all.

## The annual pricing table: what LisaHost's "从199元/年起" deal actually includes

LisaHost runs a dedicated annual-plans page that bundles discounted yearly billing across most of the US lines above. If your main goal is finding the cheapest way into a US IP, this page is the one to actually look at — monthly pricing on these same specs would cost noticeably more over a year.

| Plan | Location / Network | CPU / RAM / Storage | Bandwidth / Traffic | Price | Billing | Order Link |
| --- | --- | --- | --- | --- | --- | --- |
| 9929 Premium Network – Non-Native IP | Los Angeles, 9929 route | 1 core / 1GB / 10GB SSD | 50Mbps / 200GB monthly | ¥199/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=13) |
| 9929 Premium Network – Native IP | Los Angeles, 9929 route | 1 core / 1GB / 10GB SSD | 50Mbps / 400GB monthly | ¥299/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=66) |
| AS4837 Mainland-Optimized, Dual-ISP Native IP | Los Angeles, AS4837 route | 1 core / 1GB / 10GB NVMe | 100Mbps / 600GB monthly | ¥399/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=52) |
| New York Dual-ISP Residential Native VPS | New York | 1 core / 1GB / 10GB NVMe | 100Mbps / 600GB monthly | ¥399/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=155) |
| Chicago Dual-ISP Residential Native VPS | Chicago | 1 core / 1GB / 10GB NVMe | 100Mbps / 600GB monthly | ¥399/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=161) |
| 9929 Premium Network, Dual-ISP Residential Native IP | Los Angeles, 9929 route | 1 core / 1GB / 10GB NVMe | 50Mbps / 600GB monthly | ¥499/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=61) |
| Home Broadband Static Residential VDS (Astound Broadband) | Los Angeles | 1 core / 1GB / 10GB NVMe | 100Mbps / 1,000GB monthly | ¥899/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=214) |
| Home Broadband Static Residential VDS (Atlas Networks) | Seattle | 1 core / 1GB / 10GB NVMe | 100Mbps / 1,000GB monthly | ¥899/year | Annual | [ Check current price](https://lisahost.com/aff.php?aff=7175&pid=141) |

A few things worth noticing in that table. First, the cheapest entry point (¥199/year, roughly ¥16/month) doesn't get you a native US IP — that's reserved for the ¥299/year tier and up. Second, every plan in this annual hub is capped at 1 core and 1GB RAM regardless of price; what you're actually paying more for as you move up the list is traffic allowance, network route, and IP type, not raw compute. If you need more CPU or memory, you have to go back to the monthly product pages instead.

## Monthly billing: for when you don't want a year-long commitment

Not everyone wants to commit annually before they know if a route actually performs well from their location. Each US line also sells month-to-month, generally at the same ¥68/month entry point across the 9929, AS4837, New York, and Chicago lines, scaling up through "进阶版" (Advanced) and "豪华版" (Premium) tiers to unlimited-traffic "Pro" configurations. The AS4837 line's unlimited Pro tier, for example, runs ¥998/month for 8 cores, 8GB RAM, and 500Mbps with no traffic cap — a big jump from the entry tier, but relevant if you're running something continuous like a media server or a proxy relay that genuinely needs unmetered throughput.

The residential static broadband VDS line (Seattle/LA/California) also sells monthly, starting at ¥169/month for the base config and going up to ¥899/month for 4 cores, 4GB RAM, and unlimited traffic on 300Mbps.

> Refund terms differ by product line. Standard 9929/AS4837/New York/Chicago VPS carry a 48-hour no-questions-asked refund. The residential static broadband VDS and shared NAT lines do not — they're marked "特殊产品" (special product), meaning refunds, when offered at all, come back only as site account credit, not cash.

## What "dual-ISP native/residential IP" actually gets you

LisaHost markets most of its US lines around unlocking geo-restricted services — Netflix, Hulu, Disney+, HBO Max, ESPN, Amazon Prime Video — plus stable access to ChatGPT and similar AI tools, and cleaner IP reputation for things like TikTok account management, Meta/WhatsApp marketing, or Amazon/Etsy/Temu-related work. That's the sales pitch. Independent testing gives a more grounded picture.

A hardware and routing test on the AS4837 line found the underlying hardware runs on E5-2680v4 CPUs with NVMe storage delivering around 517MB/s I/O, BBR enabled, and IP addresses registered to Cogent based out of Los Angeles. Return-path routing for China Telecom, China Unicom, and China Mobile traffic mostly funnels back through the AS4837 route, which the tester described as "not a premium route, but decent for a plain direct-connect line — cheap and usable." That's a fair summary: this isn't CN2 GIA-tier latency, but it's not bargain-bin either.

A separate review of the 9929 dual-ISP residential lite plan reached a similar conclusion from a different angle — it categorized the box as better suited to "a fixed AI egress point and light remote development" than to performance-heavy workloads, noting the residential IP genuinely tested as carrying dual-ISP characteristics across multiple IP-reputation databases, but explicitly warned against treating "residential IP" as some kind of permanent immunity from account risk controls. Its recommendation was to test important accounts on a monthly plan first and watch for at least a week before committing to anything long-term.

That's a reasonable way to frame expectations here: the dual-ISP/residential IP angle is real and does test out as advertised on IP-reputation tools, but it's a tool for reducing friction, not a guarantee against platform enforcement.

## Coupon code: what's actually circulating

Several independent deal-tracking sites currently list a sitewide LisaHost coupon code, **TS-CBP205DQJE**, described as a reusable 10% discount that stacks with the existing annual/multi-year billing discounts already baked into the pricing above. Multiple unrelated sources report the same code and the same 10% figure, which is a reasonable level of cross-confirmation for a promo code, but LisaHost's own public announcements page doesn't list it directly — it only shows a terms-of-service notice and a network-status alert as of this writing. If you're going to use it, apply it at checkout and confirm the discount actually reflects on your order total before paying, since promo codes on any hosting storefront can lapse without an update to third-party listings.

## Who this setup actually makes sense for

If your goal is a cheap, single-core VPS that gives you a US-based IP for account management, AI tool access, or light remote work, the ¥199–¥499/year annual tier is hard to argue with on price — you're looking at roughly ¥16 to ¥42 a month depending on which IP type and traffic allowance you pick. If you need real CPU headroom or you're running anything latency-sensitive like gaming or high-throughput proxying, none of these annual plans will satisfy you, since they're all capped at 1 core/1GB regardless of price; you'd need to move to the monthly "豪华版" or unlimited-traffic "Pro" tiers instead. And if your actual interest is a genuine US home-broadband IP rather than a datacenter IP with residential characteristics, the static residential VDS line (Seattle/LA/California) is the more accurate fit — but expect to pay a real premium for it, and go in understanding refunds on that line work differently than the standard VPS refund policy.

## How to actually order

1. Pick your line based on what matters more to you — network route (9929 vs AS4837 vs NY/Chicago), IP type (native vs dual-ISP residential vs plain), or specific location.
2. Decide on monthly vs annual. Annual is meaningfully cheaper per month but locks you into the 1-core/1GB spec ceiling on the discounted hub plans.
3. Enter the promo code at checkout if it's still active, and check the total before submitting payment.
4. For standard 9929/AS4837/NY/Chicago lines, you get 48 hours to test and request a refund if it doesn't work for your use case — use that window on anything account-sensitive before renewing.

👉 [Browse LisaHost's current US VPS lineup and annual pricing](https://bit.ly/lisaHost)

## Quick FAQ

**Is the "native US IP" the same as the residential IP?** No. LisaHost sells these as separate tiers even within the same product line — non-native IP is the cheapest, native (but datacenter) IP is a step up, and dual-ISP residential IP is a further step up in both price and the claimed IP-reputation quality.

**Can I upgrade from a monthly plan to annual later?** The site treats these largely as separate products rather than automatic tier upgrades, so it's worth deciding on billing cycle before ordering rather than assuming a simple mid-term switch.

**Does the 48-hour refund apply to every US VPS plan?** No — it explicitly does not apply to the residential static home-broadband VDS lines or the shared NAT product, which are marked as special products with credit-only or no refunds.
