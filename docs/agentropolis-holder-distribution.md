# AGENTROPOLIS Holder Distribution Layer

## Purpose

AGENTROPOLIS is the evergreen backend distribution engine for holder-powered commerce, services, content, referrals, and GTM campaigns.

NFT project holders can become distribution participants. They can list services, goods, digital products, creator offers, consulting, local businesses, Web3 tools, and campaigns.

Gameplay or campaign triggers can route traffic, leads, referrals, and visibility to approved holder offers.

## Correct Project Map

### Marketplace / Mint Infrastructure

SolOnChain marketplace:

- Website: https://solonchain.io/
- BullBears NFT collection: https://solonchain.io/marketplace/collection/bullbears
- Vault Runners NFT mint: https://solonchain.io/mint/vault-runners

Other project websites / mint surfaces:

- Sol Asylum 5150 NFT: https://solasylum.help/ and https://launchmynft.io/mint/doc
- Sol Gods NFT: https://solgodsnfts.com/

## Supported NFT Communities

Initial SolOnChain-aligned communities:

1. BullBears NFT
2. Vault Runners NFT
3. Sol Asylum 5150 NFT
4. Sol Gods NFT

## Repository Split

- `wiredchaos/GTM` = evergreen GTM / AGENTROPOLIS distribution OS
- `wiredchaos/mutant-arcade-hub` = SolOnChain-specific gameplay wrapper

## Core Model

NFT holders unlock access to the distribution layer.

The distribution layer allows eligible holders to publish approved offers, sites, listings, landing pages, campaigns, and referral objects.

Non-holders can still participate by paying a per-site, per-listing, or per-campaign fee.

GTM receives commission from paid placements, upgrades, referrals, lead generation, campaign boosts, and completed service transactions.

## Holder Access Rules

Project-level rules should be configurable.

Possible holder access model:

- Verified holder gets a project-defined number of free sites/listings
- Additional sites/listings require a fee
- Non-holders pay from the first site/listing
- Featured placements and boosts are paid upgrades
- Gameplay can unlock temporary or permanent boosts

## Listing Types

Holders can submit:

- Services
- Goods
- Digital products
- Creator assets
- Consulting offers
- Local business listings
- Web3 tools
- Community campaigns
- Event promotions
- Affiliate/referral offers

## Gameplay Trigger Layer

Gameplay can trigger distribution through:

- Quests
- Raffles
- Staking milestones
- Burns
- Referrals
- Leaderboard wins
- Collection missions
- Social actions
- Marketplace activity
- Daily challenges
- Mutant Monday events

## Revenue Model

GTM earns from:

- Non-holder listing fees
- Holder upgrades after free allocation
- Campaign boosts
- Referral commissions
- Service transaction commissions
- Featured placements
- Analytics upgrades
- Sponsored quests
- Lead-generation fees

## Agent Roles

AGENTROPOLIS should include:

- Strategy Agent
- SEO Agent
- AEO Agent
- GEO Agent
- Listing Intake Agent
- Holder Verification Agent
- Campaign Agent
- Referral Agent
- Analytics Agent
- Commission Agent
- Drift Monitor Agent
- Red Team Agent

## Approval Workflow

No listing goes public automatically.

Each listing requires:

- Verified wallet or approved account
- Clear offer
- Real contact, checkout, or booking path
- Accurate category
- No fake claims
- No prohibited goods
- No duplicate spam pages
- Canonical description
- Review status
- Audit log

## Anti-Spam Controls

Reject or quarantine:

- Duplicate listings
- Thin AI-generated pages
- Fake testimonials
- Unverifiable income claims
- Misleading pricing
- Unsafe or prohibited products
- Keyword-stuffed landing pages
- Mass-created doorway pages
- Spam backlink patterns

## Data Objects

### Holder

```json
{
  "wallet": "",
  "project": "",
  "collection_id": "",
  "verification_status": "pending|verified|rejected",
  "free_site_allowance": 0,
  "used_free_sites": 0,
  "paid_sites": 0,
  "role": "holder|non_holder|admin|partner",
  "created_at": "",
  "updated_at": ""
}
```

### Listing

```json
{
  "listing_id": "",
  "owner_wallet": "",
  "project": "",
  "type": "service|goods|digital_product|consulting|local_business|web3_tool|campaign",
  "title": "",
  "canonical_description": "",
  "category": "",
  "status": "draft|review|approved|rejected|paused",
  "site_url": "",
  "contact_url": "",
  "checkout_url": "",
  "seo_keywords": [],
  "aeo_questions": [],
  "geo_queries": [],
  "created_at": "",
  "updated_at": ""
}
```

### Campaign Trigger

```json
{
  "trigger_id": "",
  "source": "mutant_arcade_hub|manual|partner|quest",
  "project": "",
  "event_type": "quest|raffle|leaderboard|burn|referral|social|marketplace_activity",
  "eligible_listing_ids": [],
  "boost_type": "traffic|featured|email|social|seo|referral_multiplier",
  "start_at": "",
  "end_at": "",
  "status": "draft|active|complete|paused"
}
```

## Positioning Statement

AGENTROPOLIS turns verified NFT holders into a commerce and distribution network.

NFT ownership becomes access.

Gameplay becomes traffic.

Distribution becomes utility.

## Immediate Next 5 Actions

1. Owner: Product Lead
   Asset needed: final holder rules by project
   Expected impact: defines eligibility and monetization
   Difficulty: medium
   Risk: low
   Timeline: 1 day

2. Owner: Engineering
   Asset needed: wallet verification design
   Expected impact: unlocks holder-specific access
   Difficulty: medium
   Risk: medium
   Timeline: 3 to 5 days

3. Owner: GTM Agent
   Asset needed: holder listing intake schema
   Expected impact: enables structured service/goods submissions
   Difficulty: low
   Risk: low
   Timeline: 1 day

4. Owner: Mutant Arcade Hub
   Asset needed: gameplay trigger events
   Expected impact: connects gameplay to distribution boosts
   Difficulty: medium
   Risk: medium
   Timeline: 3 to 7 days

5. Owner: Red Team Agent
   Asset needed: listing moderation policy
   Expected impact: prevents spam and trust degradation
   Difficulty: medium
   Risk: low
   Timeline: 2 days
