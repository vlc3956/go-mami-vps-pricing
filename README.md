# best unmanaged vps: what $5.95 a month really buys, what the refund clause hides, and when a $29–$69 China-route box is the better call

Most people searching for the best unmanaged VPS should buy a $5–8/month box and close the tab. CloudsPress tracks 329 unmanaged hosts and puts the median entry sign-up price at **$5.95/month**, with a renewal median of **$7.99** across the 41 hosts that publish renewal pricing. That is the market.

There is a second group, though: people whose users, customers or teammates sit in mainland China. For them, RAM-per-dollar is the wrong metric and 8pm latency is the right one. GoMami Networks sells into that gap at **$29 to $999 per month**, and the interesting question is whether the premium holds up — plus a few clauses buried in its Terms of Service that most roundups never touch.

**Quick pick, by use case.** Serving mainland China and North America from a single box: **LAX.Pulse.Nano at $29/month**, the only line with premium routing in both directions. Serving Asian users only: **JPN.Pulse.Nano**, same $29, shorter path to northern and eastern China. Want the flagship: **HKG.Turin.Mini at $69**, 5 GHz single-core with a 2 Gbps port. 👉 [Check the LAX.Pulse.Nano plan and current price](https://gomami.io/aff.php?aff=415&pid=27)

---

## What "unmanaged" actually obligates you to do

Unmanaged means the provider hands you a virtual machine, network, storage, an OS template and root access, then walks away. You install the stack, harden SSH, patch the kernel, configure the firewall, run backups, and debug it at 2am.

GoMami's Terms of Service say so in unusually plain language. The company states its responsibilities "do not extend to programming, system administration, or managing individual customer systems," that it does **not** perform data backups for customer accounts, and that support does not extend to your own customers.

That last part matters, because several third-party write-ups about GoMami repeat a claim that daily automatic backups to AWS S3 are included on every plan. The official ToS says the opposite. If you buy, assume nothing is backed up unless you built the job yourself — and if a review site and a contract disagree, the contract wins.

## What the mainstream "best unmanaged VPS" lists are ranking

The big roundups score price density, data-centre count and automation tooling. On those axes GoMami appears in none of the major lists, and it wouldn't win a category if it did.

Here is the entry tier of the providers those lists do recommend. Price, term and renewal are comparable across all of them; specs appear only where the provider's own ordering page publishes them.

| Provider | Entry plan / verified specs | Price | Term & renewal |
| --- | --- | --- | --- |
| Contabo | Core VPS: 4 vCPU / 8 GB / 100 GB SSD, 200 Mbit/s port | €5.24/mo incl. VAT; site quotes "from $5.28" | 24-month term; advertised figure is already the effective monthly rate |
| Hostinger | KVM 1: 1 vCPU / 4 GB / 50 GB NVMe / 4 TB | $6.49/mo | 24-month, renews at $11.99 |
| IONOS | entry VPS, Linux and Windows | from $2/mo | not published in the pages checked |
| Namecheap | Spark | $3.88/mo | yearly billing |
| Hostwinds | unmanaged Linux | $4.99/mo | monthly |
| Kamatera | configurable, 24 locations | from $4/mo | hourly billing; 30-day trial worth up to $100 |
| One.com | Cloud Server S, Linux and Windows | from ~$4.99/mo | first-month promo, monthly renewal after |

Two things worth internalising. Entry prices are promotional: Hostinger's $6.49 becomes $11.99 at renewal, an 85% jump that lands in month 25. And none of these providers optimise for Chinese carrier routing — they sell generic bandwidth out of Frankfurt, Helsinki, Ashburn or Singapore.

Hetzner gets recommended constantly for European workloads, with 20 TB of traffic included on its shared cloud plans. Published prices for its current line-up disagree wildly between third-party trackers, so treat any exact figure you see quoted as needing a same-day check.

## Where GoMami sits: the one thing the $5 hosts can't replicate

GoMami's entire product is premium Chinese carrier routing. Hong Kong, Japan and Singapore run China Telecom 163/CN2, China Unicom 10099/9929 and China Mobile CMI/CMIN2 on the return path, with mainline direct forwarding. Los Angeles runs premium routing in **both** directions on all three carriers.

The company advertises RTT under 50ms to mainland China. DDoS protection is best-effort by default, with optional 600 Gbps scrubbing.

Hardware splits into three lines, and the naming is where buyers get lost:

- **Turin** — AMD EPYC 9575F, boost to 5.0 GHz, PCIe Gen5 U.2 SSDs, DDR5-6400. One of only two EPYC SKUs that cross 5 GHz. This is the line for single-thread-sensitive work: MySQL InnoDB queries, Redis, game server ticks.
- **Pulse** — AMD EPYC 7763 at 3.5 GHz (7773X/7K83 in Japan, 7663 in Singapore, EPYC 7K62 at 3.3 GHz in LA). Same routing quality, lower clocks, lower price. Most website workloads belong here.
- **Ryzen 9 9950X** — 5.7 GHz, promoted on the homepage. Highest single-core clock in the line-up, least documented product line.

## The full plan line-up

Prices are monthly list, USD. Traffic is outbound, one-directional. Figures reflect the plans published on GoMami's store pages at the time of writing.

### Hong Kong — HKG Turin (EPYC 9575F, 5.0 GHz)

| Plan | vCPU / RAM / NVMe | Traffic & port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| HKG.Turin.Mini | 2 / 4 GB / 100 GB | 1 TB, 2 Gbps | $69 | [HKG.Turin.Mini — $69/mo](https://gomami.io/aff.php?aff=415&pid=14) |
| HKG.Turin.Air | 4 / 8 GB / 140 GB | 2 TB, 2 Gbps | $129 | [HKG.Turin.Air — $129/mo](https://gomami.io/aff.php?aff=415&pid=15) |
| HKG.Turin.Pro | 6 / 16 GB / 180 GB | 5 TB, 5 Gbps | $299 | [HKG.Turin.Pro — $299/mo](https://gomami.io/aff.php?aff=415&pid=16) |
| HKG.Turin.Ultra | 12 / 32 GB / 220 GB | 10 TB, 5 Gbps | $599 | [HKG.Turin.Ultra — $599/mo](https://gomami.io/aff.php?aff=415&pid=22) |

Pro and Ultra are listed as Windows-ready.

### Hong Kong — HKG Pulse (EPYC 7763, 3.5 GHz)

| Plan | vCPU / RAM / NVMe | Traffic & port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| HKG.Pulse.Nano | 2 / 2 GB / 40 GB | 500 GB, 1 Gbps | $49 | [HKG.Pulse.Nano — $49/mo](https://gomami.io/aff.php?aff=415&pid=26) |
| HKG.Pulse.Mini | 2 / 4 GB / 60 GB | 1 TB, 1 Gbps | $59 | [HKG.Pulse.Mini — $59/mo](https://gomami.io/aff.php?aff=415&pid=4) |
| HKG.Pulse.Air | 4 / 8 GB / 80 GB | 2 TB, 1 Gbps | $119 | [HKG.Pulse.Air — $119/mo](https://gomami.io/aff.php?aff=415&pid=5) |
| HKG.Pulse.Pro | 8 / 16 GB / 100 GB | 5 TB, 3 Gbps | $269 | [HKG.Pulse.Pro — $269/mo](https://gomami.io/aff.php?aff=415&pid=6) |
| HKG.Pulse.Ultra | 12 / 32 GB / 300 GB | 10 TB, 3 Gbps | $499 | [HKG.Pulse.Ultra — $499/mo](https://gomami.io/aff.php?aff=415&pid=25) |

### Japan — JPN Pulse (EPYC 7773X / 7K83, 3.5 GHz)

| Plan | vCPU / RAM / NVMe | Traffic & port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| JPN.Pulse.Nano | 2 / 2 GB / 40 GB | 500 GB, 1 Gbps | $29 | [JPN.Pulse.Nano — $29/mo](https://gomami.io/aff.php?aff=415&pid=13) |
| JPN.Pulse.Mini | 2 / 4 GB / 60 GB | 1 TB, 1.5 Gbps | $49 | [JPN.Pulse.Mini — $49/mo](https://gomami.io/aff.php?aff=415&pid=10) |
| JPN.Pulse.Air | 4 / 8 GB / 80 GB | 2 TB, 1 Gbps | $89 | [JPN.Pulse.Air — $89/mo](https://gomami.io/aff.php?aff=415&pid=11) |
| JPN.Pulse.Pro | 8 / 16 GB / 100 GB | 5 TB, 3 Gbps | $169 | [JPN.Pulse.Pro — $169/mo](https://gomami.io/aff.php?aff=415&pid=12) |
| JPN.Pulse.Ultra | 12 / 32 GB / 300 GB | 10 TB, 3 Gbps | $338 | [JPN.Pulse.Ultra — $338/mo](https://gomami.io/aff.php?aff=415&pid=24) |

### Singapore — SIN Pulse (EPYC 7663, 3.5 GHz)

| Plan | vCPU / RAM / NVMe | Traffic | Price/mo | Order |
| --- | --- | --- | --- | --- |
| SIN.Pulse.Nano | 2 / 2 GB / 40 GB | 500 GB | $29 | [SIN.Pulse.Nano — $29/mo](https://gomami.io/aff.php?aff=415&pid=21) |
| SIN.Pulse.Mini | 2 / 4 GB / 60 GB | 1 TB | $49 | [SIN.Pulse.Mini — $49/mo](https://gomami.io/aff.php?aff=415&pid=17) |
| SIN.Pulse.Air | 4 / 8 GB / 80 GB | 2 TB | $89 | [SIN.Pulse.Air — $89/mo](https://gomami.io/aff.php?aff=415&pid=18) |
| SIN.Pulse.Pro | 8 / 16 GB / 100 GB | 5 TB | $169 | [SIN.Pulse.Pro — $169/mo](https://gomami.io/aff.php?aff=415&pid=19) |
| SIN.Pulse.Ultra | 12 / 32 GB / 300 GB | 10 TB | $338 | [SIN.Pulse.Ultra — $338/mo](https://gomami.io/aff.php?aff=415&pid=23) |

Port speeds on the Singapore line are quoted inconsistently between GoMami's own store page and third-party stock trackers, so confirm on the order page rather than planning around a number.

### Los Angeles — LAX Pulse (EPYC 7K62, 3.3 GHz, dual-direction premium routing)

| Plan | vCPU / RAM / NVMe | Traffic & port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| LAX.Pulse.Nano | 2 / 2 GB / 40 GB | 1 TB, 1 Gbps | $29 | [LAX.Pulse.Nano — $29/mo](https://gomami.io/aff.php?aff=415&pid=27) |
| LAX.Pulse.Mini | 2 / 4 GB / 60 GB | 2 TB, 1 Gbps | $59 | [LAX.Pulse.Mini — $59/mo](https://gomami.io/aff.php?aff=415&pid=28) |
| LAX.Pulse.Air | 4 / 8 GB / 80 GB | 4 TB, 2 Gbps | $129 | [LAX.Pulse.Air — $129/mo](https://gomami.io/aff.php?aff=415&pid=29) |
| LAX.Pulse.Pro | 6 / 16 GB / 100 GB | 8 TB, 3 Gbps | $259 | [LAX.Pulse.Pro — $259/mo](https://gomami.io/aff.php?aff=415&pid=30) |
| LAX.Pulse.Ultra | 12 / 32 GB / 300 GB | 15 TB, 5 Gbps | $599 | [LAX.Pulse.Ultra — $599/mo](https://gomami.io/aff.php?aff=415&pid=31) |
| LAX.Pulse.Titan | 12 / 32 GB / 600 GB | 30 TB, 10 Gbps | $999 | [LAX.Pulse.Titan — $999/mo](https://gomami.io/aff.php?aff=415&pid=32) |

### Hong Kong — HKG Forge (dedicated-server class, TYAN B8033, EPYC 7663, 56C/112T)

| Plan | Memory / NVMe | Traffic | Price/mo | Order |
| --- | --- | --- | --- | --- |
| HKG.Forge.Mini | 128 GB / 960 GB | 10 TB, $0.06/GB overage | $599 | [HKG.Forge.Mini — $599/mo](https://gomami.io/index.php?rp=/store/hkg-forge&aff=415) |
| HKG.Forge.Air | 256 GB / 4 TB | 20 TB, $0.06/GB overage | $899 | [HKG.Forge.Air — $899/mo](https://gomami.io/index.php?rp=/store/hkg-forge&aff=415) |

Forge includes a 2 Gbps port, extra IPv4 at $10 each up to four per server, and immediate activation with panel-driven reinstall.

### The plans promoted on the homepage

GoMami's homepage surfaces two hardware sets that don't map neatly onto the named lines above: three Ryzen 9 9950X configurations at 5.7 GHz and three EPYC 7763 configurations. The EPYC set is the confusing one, because it uses the same 7763 silicon as HKG.Pulse with different RAM and disk pairings at lower prices — 2 vCPU / 4 GB / 40 GB for $39, against $59 for the 60 GB HKG.Pulse.Mini.

The homepage doesn't state which location these deploy in, and GoMami's documentation doesn't describe them as a separate product family, so treat them as a distinct listing rather than a second brand of hardware. Confirm the PoP and the exact allocation on the checkout page before paying.

| Plan | vCPU / RAM / NVMe | Traffic & port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| Ryzen 9 9950X Mini | 2 / 4 GB / 40 GB | 1 TB, 2 Gbps | $59 | [Ryzen 9950X Mini — $59/mo](https://bit.ly/Gomami) |
| Ryzen 9 9950X Air | 4 / 8 GB / 60 GB | 2 TB, 2 Gbps | $99 | [Ryzen 9950X Air — $99/mo](https://bit.ly/Gomami) |
| Ryzen 9 9950X Pro | 6 / 16 GB / 80 GB | 5 TB, 5 Gbps | $199 | [Ryzen 9950X Pro — $199/mo](https://bit.ly/Gomami) |
| EPYC 7763 Mini | 2 / 4 GB / 40 GB | 1 TB, 1 Gbps | $39 | [EPYC 7763 Mini — $39/mo](https://bit.ly/Gomami) |
| EPYC 7763 Air | 4 / 8 GB / 60 GB | 2 TB, 1 Gbps | $79 | [EPYC 7763 Air — $79/mo](https://bit.ly/Gomami) |
| EPYC 7763 Pro | 8 / 16 GB / 80 GB | 5 TB, 3 Gbps | $169 | [EPYC 7763 Pro — $169/mo](https://bit.ly/Gomami) |

## The cost math nobody puts in the review

A $5.95/month VPS runs about **$71 in year one**. HKG.Turin.Mini at $69/month runs **$828** — roughly eleven times as much. Meanwhile the Contabo entry tier hands you 8 GB of RAM against Turin.Mini's 4 GB, so the cheap box also carries double the memory.

The honest question is whether the routing is worth about $757 a year to you. For an e-commerce checkout where a few hundred milliseconds shows up in conversion, that's a plausible yes. For a personal blog with three readers in Chengdu, it's a hard no.

Running out of traffic is straightforward: GoMami sells self-service packs at **$6 per 100 GB** up to **$1,200 for 20 TB**, roughly $0.06/GB across the range. Forge plans bill overage at the same per-gigabyte rate. Overage rules are not uniform across the line-up — self-service packs on Pulse and Turin, metered overage on Forge, and third-party accounts of what happens at the limit don't agree — so size the plan against your actual monthly volume and confirm the specific plan's rule before you commit.

Then there's the clause that should change how you test the thing.

**The refund window is 24 hours, and it is narrower than it sounds.** GoMami's ToS voids the money-back guarantee if you push **more than 10 GB of traffic on a VM within that 24-hour period**, if the service is hit by a DDoS attack, or if there's evidence of fraud or abuse. Payment processing fees are deducted from whatever comes back.

Here's the trap: the normal way to evaluate a VPS is to buy it, run iperf3, check streaming unlocks, hammer it with a load generator, then decide. Ten gigabytes disappears in under three minutes on a 500 Mbps link. Do that before requesting a refund and you've forfeited it. If you plan to test, test latency and small packets first, and save the throughput runs for after you've committed.

Two more operational details: upgrades and downgrades currently go through a support ticket rather than a self-service button, and invoices three days past due can see service interrupted.

## What independent testing shows

A December 2025 review of HKG.Turin.Mini, JPN.Pulse.Nano and SIN.Pulse.Mini on NodeSeek is the most detailed public test set available, and it confirms the marketing on some points while contradicting it on others.

On HKG.Turin.Mini, Geekbench 5 came in at **2259 single-core / 4262 multi-core**, SysBench single-thread at **6173**, and fio hit **8.03 GB/s** on 1M blocks with 4K read/write around 666 MB/s. The tester's read: top three among machines they'd tested, with disk throughput suggesting the NVMe isn't oversold.

Throughput from China: Shenzhen Telecom on a 500 Mbps line pulled **~475 Mbps**, Jinan Unicom hit **545–572 Mbps**, and a 1 Gbps China Construction Bank mobile line reached **933 Mbps**.

The mobile carrier caveat is the one to remember. Uploads from Guangdong, Wuhan and Ningbo Mobile were throttled to **33–50 Mbps** in the same tests while downloads ran fine — Ningbo managed 653 Mbps down. If your workload is outbound-heavy toward mobile users (live streaming, uploads, backups to a China endpoint), that asymmetry will show up. The tester's carrier summary: Telecom sees Hong Kong ≈ Japan > Singapore, Unicom sees Hong Kong > Japan > Singapore with Singapore uploads badly degraded, and Mobile sees Singapore > Japan ≈ Hong Kong.

Two practical annoyances surfaced as well: iperf3's default port 5201 is blocked and needs changing, and IPv6 was offline on the test box. GoMami's documentation doesn't say whether IPv6 is available on request, so don't plan around it.

For a website or API serving Chinese users out of Hong Kong, the picture holds up. 👉 [See the HKG.Turin.Mini specs and order it at $69/month](https://gomami.io/aff.php?aff=415&pid=14)

## Who should not buy GoMami

You want the lowest cost per gigabyte of RAM. Your audience is in Europe or North America. You need managed databases, object storage or Kubernetes alongside the VM — GoMami sells none of that, and DigitalOcean, Vultr and Linode do. You want a hands-off server with patching and backups included. You're on a hobby budget; the NodeSeek reviewer's own advice to price-sensitive individual buyers was, bluntly, to buy from someone else.

One exclusion matters more than price: the ToS bans Tor, open proxies and anonymous proxy services outright, along with TikTok-style botting (immediate termination, no refund) and spam. If the plan was to run a proxy node on a China-optimised box, the account won't survive.

If you ruled yourself out of the LAX recommendation because you have no North American users, the Japan node is the cheaper path to the same $29 entry point — same triple-carrier return routing, shorter path to northern and eastern China. 👉 [Start with JPN.Pulse.Nano at $29/month](https://gomami.io/aff.php?aff=415&pid=13)

## How to order, and the promo codes worth trying

Ordering runs through a standard WHMCS flow: pick a location and product line in the left sidebar, hit Order Now on the plan, choose the billing cycle on the Configure page, continue to cart, enter a promo code on the Review & Checkout page, then choose payment — credit card, Stripe Alipay or crypto, with account credit applicable.

Deployment usually completes in **1–5 minutes** after payment, with IP and credentials emailed. OS templates cover Ubuntu 22.04/24.04, Debian 11/12, CentOS Stream 9, AlmaLinux 8/9 and Windows Server 2019/2022; anything else goes through custom ISO. The control panel handles VNC, rescue mode, reverse DNS, ISO mounting and reinstall, and there's a REST API for automation.

Two codes have multiple independent sources behind them: **GOMAMI365** (20% recurring, tied to annual billing in some write-ups) and **Hi,LAX** (20% recurring on the LAX.Pulse line, launched with the Los Angeles node in June 2026, putting the Nano near $23.20). Codes circulating for Turin, Japan and Singapore appear only in a single third-party list and aren't confirmed anywhere official. Apply whatever you find at checkout and watch the total change before you pay — that's the only verification that counts.

## FAQ

**Does GoMami include backups?** No. The ToS states the company does not perform data backups and isn't liable for data loss. Third-party claims about daily S3 backups conflict with the official terms; build your own job.

**Is GoMami managed?** No. No system administration, no programming support, and support doesn't extend to your own customers.

**Can I try it before paying?** There's no documented free trial. The only exit route is the 24-hour refund window, voided by more than 10 GB of traffic or a DDoS attack.

**What happens when traffic runs out?** Buy a top-up pack from the client area — $6 per 100 GB, up to $1,200 for 20 TB. Forge plans bill overage at $0.06/GB.

**Can I upgrade later?** Yes, but plan changes go through a support ticket.

## Picking your plan

If you're serving a Chinese audience and mostly pushing data toward them — websites, APIs, dashboards, video — **HKG.Turin.Mini at $69** is the reference point: 5 GHz single-core, 2 Gbps port, 100 GB NVMe, flagship routing. Drop to **HKG.Pulse.Mini at $59** if your workload scales across cores and you can live without the clock speed; you lose CPU frequency and 40 GB of disk, not routing quality.

If you need China and North America from one box, **LAX.Pulse.Nano at $29** is the cheapest way in and the only line with premium routing in both directions. If your budget ceiling really is a few dollars a month, none of this is your category — take the $5.95 median and put the difference into a CDN.

Before you pay, do two things: confirm the promo code actually applies on the checkout page, and decide now whether you'll keep the server, because the 24-hour window closes fast once traffic starts flowing. 👉 [Compare all GoMami plans and current pricing](https://bit.ly/Gomami)
