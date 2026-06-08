# 📡 WISP Tycoon v2

> **Build a rural broadband empire from the ground up.**

A browser-based idle strategy game simulating the real economics of running a Wireless Internet Service Provider across the United States. Every mechanic is grounded in actual WISP industry dynamics — FCC compliance audits, USDA ReConnect grants, CBRS spectrum deployment, pole attachment disputes, union organizing, and competitive pressure from real incumbent types.

**[▶ Play Now](https://ericbalverson.github.io/wisptycoon)**

---

## 🎮 Game Modes

### Sprint
Pick one state. Survive one simulated year. Hit your MRR target before the clock runs out. Target scales by state — Rhode Island plays very differently from Texas.

| Difficulty | Target |
|---|---|
| Easy | $150,000 MRR |
| Normal | $300,000 MRR |
| Hard | $500,000 MRR |

### Campaign
Four tiers of progression with no hard time limit. The game ends when you choose to **Retire** (locks in your leaderboard score), go bankrupt, get outcompeted, or accept an acquisition offer.

| Tier | States | Easy | Normal | Hard | Feel |
|---|---|---|---|---|---|
| 📡 Local WISP | 1 | $200k | $400k | $750k | Scrappy startup, every dollar counts |
| 🗺 Regional WISP | 2 | $750k | $1.5M | $2.5M | Building systems, not just calling customers |
| 🏗 Multi-State ISP | 4 | $2.5M | $5M | $8M | You're an institution now |
| 🌎 National ISP | 8 | $8M | $15M | $25M | Can you hold it together at this scale? |

Each tier has a distinct visual accent (green → teal → amber → gold) and unlocks new challenges, staff roles, and overhead requirements.

---

## 🗺️ All 50 States + DC

Every state is playable with real county geometry, 2020 Census population weights, and distinct market characteristics.

- **ARPU** ranges from $46/mo (Mississippi) to $75/mo (Hawaii, DC)
- **County costs** weighted by population — Los Angeles County vs rural Montana
- **State expansion costs** reflect real market difficulty

### Competitor Profiles
Every state has a named incumbent with a realistic pre-existing footprint:

| Profile | Starting Coverage | Example States |
|---|---|---|
| Cable Giant | 35–45% | CA, NJ, FL, PA |
| Telco Incumbent | 32–40% | NY, IL, OH |
| Fiber Provider | 22–35% | TX, WA |
| Regional WISP | 20–25% | GA, TN, NC |
| Small WISP | 4–15% | MT, ND, WY, AK |

Entering a market with ≥25% incumbent coverage gives you **challenger bonuses** (ARPU boost, reputation boost, grant multiplier) and a **90-day outcompeted grace period**.

---

## ⚙️ Core Mechanics

### Customer Acquisition

| Action | How It Works | Best For |
|---|---|---|
| **Cold Call** | Manual, no cooldown, committed subs | Early grind |
| **Run Promo** | Cheap, fast, soft subs with +30% churn for 60s | Quick count before grants |
| **Bulk Campaign** | Scales with county footprint (~7 subs × counties), 3min CD | Mid-game area plays |
| **Referral Drive** | ~3%+ of subs convert neighbors, $5/conversion | Late-game compound growth |

### Revenue
```
MRR = Subscribers × State-Weighted ARPU × County Bonus × Income Multiplier × Market Synergy
```
Adjacent state pairs earn +2% market synergy bonus. Rewards contiguous expansion.

### Overhead — Scales With Your Footprint

**Per-state field overhead** (dynamic, recalculates as you expand):
- $1,500/mo base per state (local NOC presence, regional admin)
- +$75/mo per county you own in that state (field technicians)
- Delaware at 3 counties: ~$1,725/mo. Texas at 50 counties: ~$5,250/mo

**Tier advancement overhead bumps** (explained in activity log when triggered):

| Advance | Bump | Roles Added |
|---|---|---|
| Local → Regional | +$8,000/mo | Regional VP of Operations, Legal Counsel, Compliance Manager |
| Regional → Multi-State | +$15,000/mo | EVP Operations, Regional CFO, Infrastructure Director |
| Multi-State → National | +$25,000/mo | National NOC, DC Government Affairs, Chief Legal Officer |

### Expansion Requirements (Campaign)
Beyond the MRR target, each tier requires structural proof:

- **→ Regional**: 2 *adjacent* states + own ≥40% of home state counties + Field Manager + Regional Director hired
- **→ Multi-State**: 4 states + Regional Director + State Ops Manager hired
- **→ National**: 8 states + Compliance Officer hired

The goal bar tells you exactly what's blocking advancement at any time.

### Staff — 17 Roles

**Field & Ops:** Help Desk Rep, RF Engineer, Network Ops Tech, Field Manager, RF Manager, Operations Director

**Sales & Marketing:** Account Manager, Marketing Director, CMO

**Executive:** CTO, CFO, COO, CEO

**Multi-State (required for expansion):** Regional Director, State Ops Manager (up to 5), Regional Sales Manager, Compliance Officer

When hiring, the activity log shows what changed and why overhead increased.

### Grants — 61 Programs

- **5 federal** (all states): USDA ReConnect, FCC RDOF, NTIA BEAD, E-Rate, USDA Distance Learning
- **5 regional**: ARC (13 Appalachian states), Delta Regional Authority, Northern Border, Southeast Crescent, Gulf Coast
- **51 state-specific**: Named real programs per state (ConnectAR, CA Advanced Services Fund, NC GREAT, Denali Commission, etc.)

Grants **stack** correctly — each new grant accounts for counties already committed to prior grants. The system tracks `baseCounties` at acceptance time and stacks targets cumulatively.

---

## 🚨 Events — 45+ Total

### Generic Events
Competitor moves in, FCC audit, backhoe cut, DDoS attack, tower failure, grid outage, key employee poached, viral moment, school district contract, anchor client, referral wave, tower lease renegotiation, economic hardship, permit denial

### State-Specific Events
Weather events gated to realistic geographies: hurricanes (Gulf/Atlantic), blizzards (Northern tier), wildfires (Pacific), tornadoes (Tornado Alley), ice storms, heatwaves

Regulatory: CPUC audit (CA), PUC rate hearings (TX), tourism boom (mountain states), precision ag contracts (farm belt), tribal broadband opportunities, Alaska supply chain, Hawaii cable

### Late-Game Events (2+ states, significant MRR)

| Event | Trigger | What's at Stake |
|---|---|---|
| FCC Investigation | 2 states, $500k | Hire counsel or face fine + rep loss |
| Acquisition Offer | 3 states, $1M | Accept (alternate win), reject, or counter |
| Municipal Franchise Demand | 2 states, $600k | $15k to secure rights-of-way |
| Lobbyist Hire | 3 states, $800k | Influence broadband legislation |
| CBRS Spectrum Auction | 2 states, $600k | Bid on PAL for ARPU + capacity boost |
| Class Action Lawsuit | 3 states, $1.5M | Settle, fight, or offer service credits |
| Union Organizing | 3 states, $1.2M | Negotiate or risk overhead spike |
| Cybersecurity Breach | 2 states, $500k | Respond transparently or risk AG investigation |
| Competitor Merger | 3 states, $2M | Rivals consolidate — counter or find your own partner |
| Pole Attachment Dispute | 2 states, $300k | 40% rate hike from utility — fight or pay |
| Emergency BEAD Grant | 2 states, $500k | Competitive bid for $35-75k |
| Tower Condemnation | 2 states, $400k | Eminent domain forces relocation |

### Expansion Events (fires when 2+ states active)
CEO/COO travel costs, Regional Director conflict, multi-state FCC filing, PUC rate hearing, regional hiring crisis, board expansion report, competitor poaches your Regional Director, local newspaper profile

---

## 🏅 Achievements — All with Real Mechanical Effects

| Badge | Trigger | Effect |
|---|---|---|
| 📡 First Contact | First subscriber | Cold call cost -$2 |
| 💰 Debt Free | No loans at run end | Credit APR 18% → 14% |
| 📊 Balanced Books | Never overdrawn | Salary overhead -5% |
| 🗺 Statewide | Own all home state counties | Income multiplier +5% |
| 📜 Grant Magnet | 4 grants fulfilled | Rep +8, grant windows +1 month |
| 🏆 Six Figures | $100k MRR | ARPU +$3 |
| ⚡ Early Bird | $50k MRR before month 6 | Board patience +25% |
| ⭐ Community Hero | Rep = 100 | Referral rate 3%→5%, churn -10% |
| 🤖 Growth Hacker | 500 subs, never cold called | Auto-sub upgrades +20% |
| 🦊 Outfoxed | More counties than rival (10+) | Competitor expansion speed -20% |
| 👔 Full House | All C-suite hired | Income +10%, churn -10% |
| 🚀 Speed Runner | Win Sprint on Hard | Noted for prestige |

---

## 🗼 Coverage Map

- Real SVG county geometry for all 3,143 US counties with correct aspect ratio projection
- Tower placement mirrors real WISP deployment: hub at centroid (blue), coverage towers at cardinal directions (light blue), outer/backhaul towers at diagonals (teal)
- County shading scales with tower density
- Competitor territory in red, contested counties in amber
- At Regional tier, Counties tab becomes **State Operations** view — whole-state health, competitor coverage bars, estimated MRR per state, and **Buy All Counties** button

---

## 🏁 Winning

**Campaign** has no automatic win — reach National tier and a **Retire** button appears. You choose when to lock in your score. Higher MRR at retirement = better leaderboard rank. Every run is genuinely different.

**Alternate endings:**
- **Acquired** — accept the acquisition offer event
- **Retired** — click Retire at National tier
- **Bankrupt** — cash drops below -$150,000
- **Outcompeted** — competitor dominates your home state while you've lost your foothold

---

## 💾 Technical

- Single HTML file — no server, no install, no account required
- Auto-saves every 60 real seconds (speed-invariant)
- Save/load persists full game state including activity log
- Mobile-responsive — hamburger menu on small screens
- JS obfuscated and copyright-protected

---

## ⚖️ License

Copyright © 2026 Eric Alverson. All rights reserved.
Proprietary and confidential. Unauthorized copying, modification, or distribution is prohibited.
