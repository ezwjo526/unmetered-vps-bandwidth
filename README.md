# Unmetered VPS: Is Traffic Really Unlimited, Why the Same Price Buys 5 Mbps or 200 Mbps, and Which LightLayer Plan to Pick (Full Plan Table)

"Unmetered" on a VPS listing means the provider stops counting gigabytes. It says nothing about how fast those gigabytes travel. LightLayer's own catalogue makes the gap visible: the same 1 vCPU / 1 GB / 50 GB instance is sold with ports running from 5 Mbps to 200 Mbps depending on which location and route class you pick, and the annual prices for those variants sit within about $25 of each other.

Two numbers decide whether an unmetered VPS plan is worth its price. The port speed printed on the plan card, and the monthly cost per GB of RAM. Everything below works from those two, starting with LightLayer and then applying the same test to four other providers so you can see where the value actually sits.

> **Quick pick.** Start with the annual 1 vCPU / 1 GB / 50 GB plan in Los Angeles on the Global or Standard route. Those are the variants listed with 100–200 Mbps unmetered ports, at roughly $25–$40 per year. The Premium route costs more and can drop to 5–20 Mbps, so only pay for it if mainland-China routing is the actual requirement.
> 👉 [Check the current LightLayer plan list and port speeds](https://account.lightlayer.net/?affid=74)

LightLayer is a subsidiary brand of Megalayer, run by Hong Kong Lightlayer Technology Co., Ltd., and it has been selling since 2024. The hardware is KVM with AMD EPYC processors and NVMe storage, and the locations span Hong Kong, Taiwan, Japan, Thailand, Singapore, the Philippines, the United States, the United Kingdom and Germany. Payment goes through PayPal, credit card or Alipay. If you want a well-known logo on the invoice, this is not that brand; if you want a 1 GB box with an unmetered port for two dollars a month, it is.

## LightLayer's unmetered VPS plans, plan by plan

The monthly lineup is small. LightLayer sells one base configuration and then scales cores, RAM and disk upward through a configurator, so the tiers below are the published entry points rather than a fixed SKU list.

| Plan | vCPU / RAM / Storage | Port | Price | Order |
| --- | --- | --- | --- | --- |
| Startup (Los Angeles) | 1 core / 1 GB / 50 GB SSD | 100 Mbps unmetered | $4.00/mo | [Open the plan](https://account.lightlayer.net/?affid=74) |
| Pay As You Go | 2+ cores / 2 GB+ / scalable disk | 200 Mbps+ | from $5.60/mo | [Configure it](https://account.lightlayer.net/?affid=74) |
| Mid-tier | 4 cores / 4 GB / 80 GB SSD | 200 Mbps unmetered | about $11–18/mo | [Open the plan](https://account.lightlayer.net/?affid=74) |
| Business | 32 cores / 32 GB / scalable disk | 200 Mbps unmetered | $53.60/mo | [Open the plan](https://account.lightlayer.net/?affid=74) |

The annual specials are where most buyers end up, and they deserve their own table because the hardware never changes. Every row below is 1 vCPU / 1 GB / 50 GB SSD. The only variable is the network class.

| Location and route class | Port speed (as listed) | Price | Order |
| --- | --- | --- | --- |
| Taiwan, Premium | 5 Mbps | $24.99/yr | [Open the plan](https://account.lightlayer.net/?affid=74) |
| Manila | Unmetered, speed not listed | $24.99/yr | [Open the plan](https://account.lightlayer.net/?affid=74) |
| Los Angeles, Global | 100–200 Mbps unmetered | $29.99/yr | [Open the plan](https://account.lightlayer.net/?affid=74) |
| Los Angeles, Standard | 100 Mbps unmetered | $39.99/yr | [Open the plan](https://account.lightlayer.net/?affid=74) |
| Los Angeles, Premium | 20 Mbps | $49.99/yr | [Open the plan](https://account.lightlayer.net/?affid=74) |

Two warnings that will save you money. First, listings disagree on these annual prices: some trackers flatten all thirteen annual variants to a single $24.99, others split them by route class as above. The total on the order form is the only number that binds, so read it before you pay. Second, the plan card and the order configurator do not always reconcile. One documented case had a $4.00 card advertising 50 Mbps unmetered sitting above a selector that defaulted to 10 Mbps and priced 50 Mbps unmetered at $800 per month, with a $9.00 recurring total underneath. That is not a reason to avoid the host. It is a reason to slow down at the checkout screen.

👉 [Open the LightLayer order page and confirm the recurring total before paying](https://account.lightlayer.net/?affid=74)

## What unmetered VPS really means, and what it does not

OVHcloud's FAQ gives the cleanest definition available: with an unmetered VPS, "the volume of data transferred (traffic) is not measured and has no limit," you are not billed by consumption. In the same answer, it states that "the maximum speed (bandwidth) of your network connection is set by the specific plan you choose, ranging from 250 Mbps to 2 Gbps."

Read those two sentences together and the marketing language collapses into something usable. Unlimited refers to the counter. Capped refers to the pipe. A 200 Mbps unmetered port will move about 2 TB in a day if you saturate it continuously, and the host will never send you an overage invoice, but it will also never give you 201 Mbps.

The same provider also shows how quickly the word gets qualified. OVHcloud's Mumbai, Singapore and Sydney VPS locations carry a monthly quota on top of the unmetered label: 1 TB for VPS-1 and VPS-2, 3 TB for VPS-3 and VPS-4, 4 TB for VPS-5 and VPS-6, and beyond that the connection is throttled to 10 Mbps. That is a 20-fold speed drop on a plan sold as unmetered. The lesson travels to every provider: the headline claim lives on the product page, the quota lives in the footnote, and the footnote is the one that runs your server.

## Port speed and guaranteed bandwidth are different numbers

A provider can describe its network in two ways, and the difference matters more than any CPU spec on the page.

ZetServers writes it out in full: every VPS sits on a **25 Gbps unmetered port** with a **guaranteed rate from 1 to 8 Gbps depending on the plan**. sbservers uses the same structure, 25 Gbps ports with 1 Gbps guaranteed. The port number is the ceiling of the switch you are plugged into. The guaranteed rate is what the provider contracts to deliver to your instance when the network is busy. Two VPS on the same 25 Gbps port can have wildly different experiences if one has a 1 Gbps guarantee and the other has 8.

LightLayer's plan cards quote a port speed and stop there. No guaranteed-bandwidth figure is published alongside the 100 Mbps and 200 Mbps labels, which means you are buying a best-effort unmetered port. For a personal VPN node or a small site, that is fine. For anything where throughput has to hold during peak hours, it is an unknown you should price accordingly.

## The fine print that decides whether the cheap plan is cheap

LightLayer's annual price is genuinely low, and the terms behind it are stricter than most Western hosts. These come from the published terms of service rather than the sales page:

- **No refund window.** The terms state that refunds are not supported, explicitly including regular-priced and promotional products. Provider-side faults are the only exception, and the policy is written to cover those, not buyer's remorse.
- **Credits do not become money.** Account balances can be used for any LightLayer purchase but cannot be withdrawn. A goodwill credit is another server, not a refund.
- **No compensation for network faults.** The document titled a service level agreement carries no uptime figure and no credit schedule.
- **Abuse complaints suspend first.** A cloud instance is suspended without refund on the first complaint, with 6 hours to respond and 24 to resolve, and $20–$50 per incident per IP.
- **Reinstalls are metered.** One free system reinstall per server per month, then 30 yuan each time.
- **Blocked IPs stay blocked.** If an IP is flagged because of what you run on it, LightLayer does not replace it. The terms also reserve the right to reclaim resources, including IP, bandwidth and hardware, following upstream changes.
- **No IPv6** on the plans reviewed, and the Taiwan, Hong Kong and Singapore addresses are non-native IP.

There is one clause in your favour. Price changes are written to apply only to new orders, so renewals are not repriced. That is rarer than it should be, and it makes the annual plan more attractive than a first-year discount would.

Compare the money-back position with VerticHost, which offers a full refund within 7 days and states that renewals stay at the same price. If you need a trial period to feel safe, LightLayer is the wrong shape of purchase. If you are paying $25 for a year and treat it as spent, the terms are survivable.

## How to check real throughput before you commit

Do not use speedtest.net to judge a VPS port. Both ZetServers and sbservers say this outright, because most speedtest endpoints have under 1 Gbps available and will under-report a fast link or produce noise on a slow one. Use iperf3 against a well-connected target:


iperf3 -c ping.online.net -p 5201 -P 30


Thirty parallel streams, a public target in France, and a number you can compare across providers. Run it from the VPS itself, not from your laptop, or you will be measuring your home connection. On a 100 Mbps unmetered port, a clean result sits near 94 Mbps each way. If you see 10 Mbps on a plan sold as 100, that is the configurator problem described above, and it is worth a support ticket before the refund window you do not have expires.

## Which plan fits which job

**One small site, a dev box, or a proxy node.** The $4.00 monthly Los Angeles plan is the right size. 1 GB of RAM runs a WordPress install with a caching plugin, or a single-user VPN, or a Tailscale exit node. Pay monthly for the first cycle so you can leave after 30 days without having prepaid a year.

**Downloading, streaming, or moving backups.** Port speed is the only spec that matters. Take a Los Angeles Global or Standard annual plan at 100–200 Mbps rather than a Premium plan at 20 Mbps, and check the transfer maths: 200 Mbps sustained moves roughly 2 TB a day, which is more than most people need and far more than a 5 Mbps port will ever deliver.

**Serving mainland China.** The Premium route is the reason to be on LightLayer at all, and the port speed is the price you pay for it. A 5 Mbps Taiwan Premium plan is a routing product, not a bandwidth product; buy it for latency and accept the ceiling.

**Anything that needs an SLA, IPv6, Windows licensing, or a refund.** None of those are documented for LightLayer. Pick a different host rather than discovering the gap after payment.

## How LightLayer compares on price per GB

Strip out the marketing and compare what a gigabyte of RAM costs per month, alongside the network guarantee you get with it.

| Provider | Example plan | Port and guaranteed rate | Price |
| --- | --- | --- | --- |
| ZetServers | 1 vCPU / 4 GB / 50 GB NVMe | 25 Gbps port, 1 Gbps guaranteed | €29/mo |
| ZetServers | 2 vCPU / 8 GB / 100 GB NVMe | 25 Gbps port, 2 Gbps guaranteed | €59/mo |
| sbservers | 1 vCPU / 1 GB / 50 GB NVMe | 25 Gbps port, 1 Gbps guaranteed | £4/mo |
| sbservers | 2 vCPU / 4 GB / 100 GB NVMe | 25 Gbps port, 1 Gbps guaranteed | £8/mo |
| VerticHost | 2 vCores / 4 GB / 40 GB SSD | 100 Mbps–1 Gbps by location, no guarantee published | €19/mo |
| LightLayer | 1 vCPU / 1 GB / 50 GB SSD | 100–200 Mbps unmetered, no guarantee published | $24.99–$39.99/yr |

On RAM alone, sbservers at £8 for 4 GB works out to £2 per GB per month, VerticHost to about €4.75, and ZetServers to €7.25. LightLayer's annual 1 GB plan lands near $2 per GB per month, which is competitive with the cheapest of them despite the smaller per-instance ceiling.

The premium at ZetServers buys things LightLayer does not list: a guaranteed 1–8 Gbps rate, a self-owned AS 25198 backbone with 40-plus points of presence, 100 Gbps of L3/L4 DDoS protection included on every VPS with an upgrade path to 10 Tbps from €149 per month, and roughly 60-second provisioning across eight European locations. Whether that is worth seven times the RAM price depends entirely on whether you need a guarantee in writing.

Two traps when reading tables like this. Core count is not a proxy for memory: sbservers prices a 3 vCPU plan at 3 GB (£10) above a 2 vCPU plan at 4 GB (£8), so sorting by cores puts you on the worse machine. And "DDoS protected" needs reading word by word: ZetServers includes 100 Gbps of L3/L4 mitigation, while sbservers still lists its L3–L7 option as "coming soon," which means the feature does not exist yet regardless of the checkmark.

## FAQ

**Is unmetered the same as unlimited bandwidth?**
In practice the two phrases describe the same billing promise: traffic is not measured and there is no overage invoice. Neither promises a speed, and neither rules out a monthly quota buried in a footnote.

**Will LightLayer throttle me for using too much traffic?**
No traffic cap is published on the plans reviewed; the port speed is the limit. The risk sits in the acceptable-use terms rather than the bandwidth policy, where a single abuse complaint can suspend an instance without refund.

**Does the annual price go up at renewal?**
The terms state that price changes apply only to new orders, so an existing annual plan is not repriced. That protects you from the usual year-two doubling.

**Can I get my money back if I do not like it?**
No. Refunds are not supported under the published policy, and a credit returns as account balance that cannot be withdrawn. Assume the money is spent once you pay.

**Can I install Windows or upload my own ISO?**
Nothing verifiable confirms either one for LightLayer's cloud plans. Ask support before paying. ZetServers, by way of contrast, ships Linux and BSD templates plus custom ISO upload over a VNC console on every plan, with Windows available through your own licence.

**Can I upgrade later?**
The Pay As You Go tier exists precisely because configuration is adjustable at order time. Plan sizes rather than live resizing are what the published pages describe, so if growth is likely, start on the configurable tier rather than the fixed annual special.

## The decision, in four lines

Running a small site, a proxy node, or a dev environment and you want to spend almost nothing: the $4.00 monthly Los Angeles plan, paid monthly for the first cycle.

Moving real traffic and throughput matters: the Los Angeles Global or Standard annual plan at 100–200 Mbps unmetered, and if you need a guaranteed rate in writing, pay ZetServers or sbservers for it instead.

Serving mainland China: the Premium route, with the low port speed accepted as part of the deal.

Needing a refund window, IPv6, or Windows licensing: buy somewhere else.

Before you pay, confirm three things on the order form itself: the route class and port speed of the specific variant you selected, the recurring total rather than the headline card price, and the location, since Manila and Los Angeles are not interchangeable for latency.

👉 [Pick your LightLayer location and port class, then check the total at checkout](https://account.lightlayer.net/?affid=74)
