# Brisbane Southside Data Centre Options: 2RU VM Server Colocation

**Requirement:** colocation for one 2RU VM host server enclosure, in a data centre on Brisbane's southside.
**Prepared:** 1 November 2026. All pricing, specs and availability below must be confirmed directly with each provider. Several public listings are dated.

---

## 1. Shortlist: southside facilities

| # | Facility | Address | Suburb / distance from CBD | Notes |
|---|----------|---------|------------------------------|-------|
| 1 | **iseek Woolloongabba** | 100 Ipswich Road, Woolloongabba QLD 4102 | Inner south, ~3 km | Linked to iseek's City and Airport sites by a 60 km dark-fibre ring, which suits DR or a second site. Directories also list DigiCo "Woolloongabba BNE", apparently at the same address, so check who the operator is now. |
| 2 | **Interactive Brisbane** | 19 McKechnie Drive, Eight Mile Plains QLD 4113 | Brisbane Technology Park, ~15 km (M1/Gateway) | ISO 9001 and ISO 27001 certified, high-security, enterprise-grade. Better suited to managed or enterprise contracts than very small colocation. |
| 3 | **Host Networks / Edge Centres EC11** | 1/53 Brandl Street, Eight Mile Plains QLD 4113 | Brisbane Technology Park, ~15 km | A smaller Brisbane provider offering colocation and hosting. Small amounts of rack space, such as 1–2RU, are usually easy to arrange. |
| 4 | **Servers Australia (ex-Oz Servers)** | 96 Lytton Road, East Brisbane QLD 4169 | Inner south-east, ~3 km | Has UPS, generator backup and FM200 fire suppression. Listed 2RU plan: about **$163.90 ex GST/month** (0.5 kW, A+B PDUs, 1 TB). It is unclear whether this site is still active or whether colocation has moved to 14 Finchley St, Milton (northside). **Confirm.** |
| 5 | **Polaris Data Centre** | 11 Mary Mackenroth Lane, Springfield Central QLD 4300 | South-west corridor, ~30 km | Tier III / Tier 3+ (N+2), about 7,000 m² of raised floor, built for a major bank. The strongest facility on the list, but the furthest away. Best for a DR or high-resilience requirement. |

Also in Woolloongabba: **Telstra (InfraCo), 820 Main Street.** This is mainly a carrier exchange, and retail 2RU colocation there is unlikely.

### Nearby non-southside options, for comparison
For context only, since these are not on the southside: NEXTDC B1 (CBD) and B2 (Fortitude Valley), Equinix BR1, and Intergrid BDC (Fortitude Valley). Resellers such as Intergrid, Fluccs, DP Unicom, Summit Internet and RackCorp sell 2RU in these buildings for roughly **$199–$290/month**.

---

## 2. Recommendation

1. **Primary pick (balance of cost, access and connectivity): iseek Woolloongabba.** It is inner-south and quick to reach for hands-on work. It is carrier-connected, and iseek's fibre ring opens a later path to a second site for DR.
2. **Budget pick: Servers Australia, East Brisbane**, if the Lytton Road site is still operating. It has the lowest listed 2RU price.
3. **Enterprise / compliance pick: Interactive, Eight Mile Plains** if ISO 27001 matters, or **Polaris, Springfield** if Tier III certification is mandatory.

---

## 3. Sizing the 2RU request (what to give providers)

Typical 2RU VM host (e.g. Dell R750/R760, HPE DL380 Gen11, Lenovo SR650):

| Item | Suggested spec to request |
|------|---------------------------|
| Rack space | 2RU, plus a 1RU blank or 1RU for a switch/firewall if needed (ask for a 3–4RU quote as well) |
| Power | Dual-PSU server, so request **A+B redundant feeds**. Budget **0.5–1.0 kW** (about 2–4 A @ 240 V). Check the vendor power calculator at real load. |
| Network | 2 × 1 GbE (or 10 GbE) uplinks, plus 1 port for iDRAC/iLO out-of-band management |
| IP addressing | /29 or /28 public IPv4 block, plus IPv6 |
| Bandwidth | Unmetered or 1–10 TB/month to start. Confirm the 95th-percentile billing model. |
| Access | 24/7 escorted or unescorted access, and remote hands (ask the hourly rate) |
| Rails | Bring the server's sliding rails, since shared racks may need fixed rails |
| Term | Usually 12 months, sometimes with a setup fee (about $0–$200) |

---

## 4. Questions to ask every provider

- Uptime Institute tier or equivalent design (N+1 / 2N), and the SLA percentage for power and network
- Generator autonomy (hours of fuel on site) and refuel contracts
- **Flood immunity.** This is important on the southside, given the 2011 and 2022 Brisbane floods. Ask for the floor level against the Q100 / 2011 flood line.
- Certifications: ISO 27001, SOC 2, PCI DSS, and IRAP if you handle government data
- Carrier neutrality: which carriers are on-net (Telstra, Optus, Vocus, TPG, Superloop, Aussie BB)?
- Cross-connect cost, if you will bring your own carrier link
- Access process, induction requirements and lead time for new staff
- Remote hands rates and response times
- Power overage charges and whether power is metered or allocated
- Contract term, notice period, price escalation and setup fees

---

## 5. Next steps

1. Confirm the server's real power draw (W), the rail type and the uplink needs.
2. Send an RFQ for **2RU, A+B power, 1 kW, 2 × 1 GbE, /29, 24/7 access** to iseek, Servers Australia, Interactive and Host Networks (and Polaris if Tier III is required).
3. Do site visits for the top two. Check physical security, cooling, flood position and parking/loading access.
4. Compare total 12-month cost: monthly fee × 12, plus setup, cross-connects and remote hands estimate.

---

### Sources
- iseek Woolloongabba and other facilities: https://baxtel.com/data-center/brisbane, https://www.datacentermap.com/australia/brisbane/
- Interactive Brisbane: https://www.interactive.com.au/services/data-centres/locations/brisbane/, https://colo.exchange/data-centers/interactive-interactive-brisbane
- Servers Australia / Oz Servers: https://www.datacentermap.com/australia/brisbane/oz-servers, https://www.serversaustralia.com.au/marketplace/buy-colocation, https://docs.serversaustralia.com.au/docs/colocation
- Polaris: https://cloudscene.com/data-center/australia/brisbane/polaris-data-center-polaris-data-centre, https://datacenterhawk.com/marketplace/providers/polaris-data-centre/11-mary-mackenroth-lane-springfield-central-qld-4300-australia/1078703
- 2RU price benchmarks: https://intergrid.au/colocation/brisbane/, https://www.fluccs.com.au/colocation/brisbane/, http://www.dpunicom.com/brisbane-colocation.html, https://summitinternet.com.au/datacentre/datacentre-colocation/
