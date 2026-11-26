# Game Server VPS USA: How Much RAM Does Your Server Need, Which US Location Wins on Ping, and What Does a DDoS-Protected Plan Really Cost? (Full SixtyNet Plan Table)

A US-hosted game server from SixtyNet starts at **$200 a year** for 2 cores, 2 GB RAM and 40 GB NVMe in Los Angeles, and the plan most modded Minecraft, Rust and FiveM groups end up on is LAX-MICRO at **$400 a year** (4 cores, 4 GB, 10 TB traffic, DDoS protection on the plan). Both prices are annual, both are in US dollars, and Los Angeles is the only US location the provider runs. If your whole community plays from the East Coast, that last fact matters more than any spec below, and a New York or Chicago host will beat this one on ping.

What follows is the full plan list with the per-month math, a rule for matching RAM to each game, the latency you can expect coast to coast, and an honest look at where SixtyNet sits against the rest of the US market — including the fact that the same 4 GB of RAM costs anywhere from $5 to $33 a month depending on who you buy it from.

> **Quick pick:** LAX-MICRO — 4 vCPU, 4 GB RAM, 80 GB NVMe, 10 TB traffic on a 4 Gbps port, DDoS protection included, $400/year (about $33/month). The sensible fit for a modded Minecraft server, a small Rust or CS2 server, or a FiveM build with a light resource load.
> 👉 [Check LAX-MICRO's current annual price](https://sixtynet.net/aff.php?aff=39)

If you are running vanilla Minecraft for a handful of friends, drop to LAX-STARTER at $200/year and put the difference into a backup drive.

## Every SixtyNet plan, and what the annual price works out to per month

SixtyNet publishes its prices as yearly figures with a struck-through list price beside them. The 17% you see is the annual rate against that list price, not a coupon code, so there is nothing to stack at checkout.

| Plan | vCPU / RAM | Storage | Traffic / port | Price (USD, annual) | Order |
| --- | --- | --- | --- | --- | --- |
| LAX-STARTER | 2 / 2 GB | 40 GB NVMe | 5 TB, 2 Gbps | $200 (list $240) | [Order LAX-STARTER](https://sixtynet.net/aff.php?aff=39) |
| LAX-MICRO | 4 / 4 GB | 80 GB NVMe | 10 TB, 4 Gbps | $400 (list $480) | [Order LAX-MICRO](https://sixtynet.net/aff.php?aff=39) |
| LAX-MEDIUM | 8 / 8 GB | 160 GB NVMe | 20 TB, 10 Gbps | $800 (list $960) | [Order LAX-MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| LAX-LARGE | 8 / 16 GB | 320 GB NVMe | 40 TB, 10 Gbps | $1,600 (list $1,920) | [Order LAX-LARGE](https://sixtynet.net/aff.php?aff=39) |
| Los Angeles China Unicom-Premium | Network/BGP plan, not a VPS | — | 100M base, 3x burst, 95th percentile billing | $2,500 (list $3,000) | [See this plan](https://sixtynet.net/aff.php?aff=39) |

The four LAX plans are the ones built for game servers: every one of them lists DDoS protection on the feature line, and the ports are open, which you need the moment you want a Dynamap, a web admin panel or a status page on 80/443. The China Unicom-Premium entry at the bottom is a BGP and transit product sitting on the same page, priced for carriers and resellers rather than for anyone running a Minecraft world.

Three other product lines appear on that page and none of them is the right buy for a public game server:

- **Residential IP plans (Los Angeles),** in 2C/2G, 4C/4G, 8C/8G and 16C/16G sizes with 5 TB to 40 TB of traffic. Ports 80 and 443 are closed on these for IP risk-control reasons, and the listing does not carry a DDoS line. Pricing isn't displayed on the plan listing itself.
- **Residential IP with AS9929 China-optimized routing,** in 2C/2G and 4C/4G sizes. Same port restriction, and refunds on this line are issued as account balance only.
- **A 4-core / 4 GB storage-heavy plan** with 300 GB plus 200 GB free RAID 10 disk, 10 TB traffic and DDoS protection. Worth a look if you are hosting ARK with a pile of maps, since the entry LAX disk of 40 GB runs out fast.

## Which plan fits Minecraft, CS2, Rust, FiveM, or ARK

RAM is the wrong single number to shop on, but it is the fastest filter. These ranges are the ones hosts in this bracket generally quote, and they line up with what each game actually consumes at idle and under load.

| Game | RAM rule of thumb | SixtyNet plan |
| --- | --- | --- |
| Minecraft Java, vanilla or Paper, small group | 2–4 GB | LAX-STARTER, or LAX-MICRO once plugins go in |
| Minecraft modpack, or a couple dozen concurrent players | 6–8 GB and up | LAX-MEDIUM |
| CS2 | 1–2 GB, but wants clock speed | LAX-MICRO |
| Rust | 2–4 GB, CPU-bound once entities pile up | LAX-MICRO, LAX-MEDIUM on a busy wipe |
| ARK | 4–8 GB plus serious disk for mods and maps | LAX-MEDIUM or the RAID 10 storage plan |
| FiveM | 4–8 GB, CPU-heavy per running resource | LAX-MEDIUM |

Two things the table hides. Minecraft, CS2 and Rust all live and die on single-thread performance, so a plan with more cores and the same RAM will not rescue a server that is ticking badly. And disk is the quiet limiter: 40 GB on LAX-STARTER is fine for a vanilla world, tight for a modpack with backups, and nowhere near enough for ARK.

## Los Angeles is the only US location, and that decides your ping

SixtyNet's US footprint is Los Angeles. Not "US and EU" — one city. That works beautifully for a West Coast player base and acceptably for a mixed one, and it is the wrong choice for a community concentrated in New York, Chicago or Atlanta.

For calibration, hosts publishing their own US latency figures put East Coast-to-East Coast connections at roughly 2–15 ms and coast-to-coast traffic at 60–70 ms. So a Los Angeles game server is going to feel like 60–70 ms to an East Coast player, which is fine for Minecraft survival and noticeable in CS2 or Rust firefights. If you want one number to decide on: count where most of your regulars live, not where you live.

## The DDoS line is where the plan tiers actually split

"Includes DDoS protection" is not a given in this market, and the difference is spelled out on the product pages rather than the homepages. One well-known US VPS seller states plainly that its VPS plans do not include DDoS protection and points people running public servers at dedicated machines instead. Others put mitigation on every plan. Both models exist at similar prices, so read the plan line.

On SixtyNet, DDoS protection is listed on all four LAX plans and on the RAID 10 storage plan. It is absent from the residential IP listings, which is the trap: the residential line looks like the cheap way into the same hardware, and it is the wrong one for a server that strangers can hammer. Closed 80/443 ports are the second reason. A public Minecraft server listens on 25565 and will run fine, but the moment you bolt on a web map, a billing panel or a status page, you are fighting the port policy.

If your server is friends-only and never listed publicly, this whole section is optional. The day you post the IP in a Discord with a few hundred members, it stops being optional.

## What the first year really costs, and what year two might

The monthly equivalents are the numbers worth carrying in your head:

- LAX-STARTER, $200/year — about **$16.70/month**
- LAX-MICRO, $400/year — about **$33.30/month**
- LAX-MEDIUM, $800/year — about **$66.70/month**
- LAX-LARGE, $1,600/year — about **$133.30/month**

Two costs hide behind those figures.

The first is cash flow. Every price on the page is annual, so LAX-MICRO means $400 leaving your account before the server has ticked once. Against a $8/month competitor, that is four years of prepayment compressed into one invoice, and you are taking on the risk that your community is gone in six weeks.

The second is renewal. The listing shows a list price and a discounted annual price, and what you pay in year two is not stated on the page. Ask support before you commit, because hosting discounts that exist only on the first invoice are common enough that the question is worth the ticket. The same pattern shows up on the dedicated side of the market, where one provider charges an installation fee equal to a full month's rent and waives it only on a twelve-month commitment. The sticker is rarely the invoice.

Refunds are the other thing to nail down early. A recent third-party writeup on SixtyNet reports a **3-day** money-back window, which is short by the standards of this market (7 days is common). Build and stress-test your server inside the first 48 hours, not on day five. That same writeup notes that card payments were suspended for fraud screening when it was published, so confirm your payment method before you count on a card going through.

👉 [See what the LAX-MICRO plan costs for a full year](https://sixtynet.net/aff.php?aff=39)

## How the same 4 GB compares across the US market

Published prices for a 4 GB-class server, pulled from each provider's own product pages:

| Provider | US location | 4 GB-class price | DDoS on VPS plans |
| --- | --- | --- | --- |
| SixtyNet (LAX-MICRO) | Los Angeles | $400/year (~$33/mo), 4 vCPU | Listed on LAX plans |
| Netvaz | Dallas | $5/mo (2 vCPU); $8/mo for 4 vCPU / 8 GB | Stated as included on all plans |
| VPS.DO | LA, New York, Chicago, Miami | $8/mo (2 vCPU); $20/mo for 4 vCPU / 8 GB | Explicitly **not** included |
| vShield | New York | from $12.99/mo | Stated as included |
| WinterNode | Chicago | Ryzen/NVMe, price not published on the VPS page | Stated as included |
| OVHcloud (dedicated, not VPS) | Multiple | from $331/mo | Game-specific filtering |

Two cautions on that table. The low figures come from providers' own marketing pages with no independent verification, and the spread is wide enough (Netvaz quoting 16 vCPU / 32 GB at $30/mo against another host quoting 12 vCPU / 32 GB at $80/mo) that the only safe move is to price your exact configuration at checkout. And OVHcloud is in the list to mark a boundary rather than as an alternative: $331/month for a dedicated game machine with 8 cores and 64 GB only makes sense for a hosting business or a tournament operator, not for a friend group.

Read against those numbers, SixtyNet is not the value pick for a purely US audience. What the $400 buys is a Los Angeles box with a premium network port and mitigation included, priced for traffic that crosses the Pacific. If all your players are in Ohio, you are paying for routing you will never use.

## Who should not buy SixtyNet

- **Vanilla Minecraft with three friends.** LAX-STARTER is $200/year and you can run the same thing for $4–8/month elsewhere if you accept no DDoS protection. For a private, unlisted server that trade is reasonable.
- **An all-East-Coast community.** One US location, and it is on the wrong coast for you. New York or Chicago hosts will cut 50-plus milliseconds off every player's ping.
- **Anyone who wants a managed game panel.** These are unmanaged VPS instances with root access and a control panel for rebuilds and reboots. Mod installs, plugin updates and crash debugging are yours.
- **A community split across the US and Europe.** Los Angeles to Europe is a long hop, and SixtyNet does not sell a European location to pair with it.

## Before you pay: four things to confirm

1. **The renewal rate.** The page shows a discounted annual figure next to a list price. Year two is the number that decides whether this is affordable.
2. **Which line you are on.** LAX plans carry DDoS protection and open ports; the residential and AS9929 residential lines do not open 80/443 and refund to account balance only.
3. **The refund window.** Three days, per a third-party review. Test on day one.
4. **The payment method.** Card processing has reportedly been suspended at times; know what you are paying with before you reach the checkout page.

Matching the plan to the situation:

- Vanilla Minecraft, small group, US West — **LAX-STARTER**, $200/year.
- Modded Minecraft, a small Rust or CS2 server, or a light FiveM build — **LAX-MICRO**, $400/year.
- ARK, a busy Rust wipe, or several instances on one box — **LAX-MEDIUM**, $800/year, and check the RAID 10 storage plan if disk is the worry.
- Players mostly east of the Mississippi — none of the above; buy in New York or Chicago.

👉 [Start with LAX-MICRO and confirm the annual price and the DDoS line before you pay](https://sixtynet.net/aff.php?aff=39)
