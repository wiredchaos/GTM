# AGENTROPOLIS Distribution Layer

Shared GTM and UGC infrastructure for the AGENTROPOLIS Intelligence Grid.

This repository owns the reusable, white-label distribution architecture used across districts, projects, applications, communities, creator systems, marketplaces, and service networks.

## Canonical Boundary

This repository is **shared Distribution Layer infrastructure**.

`AGENTROPOLIS-CITY-OF-AGENTS/AGENTROPOLIS-GTM` is the canonical GTM command district and owns GTM decision products such as Revenue War Room and SIGNAL.

```text
AGENTROPOLIS Intelligence Grid
  -> wiredchaos/GTM
       shared distribution primitives
  -> AGENTROPOLIS-GTM
       opportunity intelligence + governed GTM decisions
  -> district distribution packs
       domain-specific configuration
  -> external providers / channels
       execution surfaces
```

Do not fork Revenue War Room, Signal Court, Action Market, Credit Shield, or Reputation Shield into independent versions here. This layer provides the reusable distribution contracts those products consume.

## Core Purpose

AGENTROPOLIS uses one citywide Distribution Layer.

Every district connects through a district distribution pack. Districts configure the shared engines with their own identity, audience, offers, channels, campaigns, templates, KPIs, permissions, and approval rules.

Districts do not receive cloned GTM systems.

## Core Engines

### GTM Engine
- positioning and messaging
- SEO, AEO, and GEO
- AI-search visibility
- GitHub discoverability
- campaign orchestration
- community distribution
- publishing workflows
- analytics and attribution

### UGC Engine
- user-generated content intake
- creator and ambassador campaigns
- referrals
- reviews and testimonials
- case studies
- social-proof collection
- contributor consent
- moderation
- rewards and commission events

## Shared Services
- Campaign Manager
- Workflow Engine
- Publishing Queue
- Asset Library
- Template Registry
- Analytics
- Attribution
- Governance
- Approval Pipeline
- Audit Logging
- Permissions
- Connector Interface
- District Adapter Runtime
- Provider Adapter Contract

## Revenue War Room Interface

The Distribution Layer accepts only approved actions from the GTM command layer for consequential GTM execution.

```text
Revenue War Room
  -> approved GTM action envelope
  -> Distribution Layer
  -> district/channel adapter
  -> external execution surface
  -> execution event
  -> GTM Receipt / attribution
```

An action envelope should carry at minimum:
- mandate / actor identity
- action type
- target scope
- policy decision
- approval state
- provider/channel selection
- budget or credit ceiling when applicable
- correlation / receipt identifier

Distribution does not infer authority from a model response, social message, provider result, or untrusted content.

## Provider Neutrality

Apollo, Clay, CRMs, publishing platforms, social networks, email providers, web builders, and other external systems are integrations, not AGENTROPOLIS districts.

Provider-specific behavior belongs behind adapters. Shared schemas should remain portable wherever practical.

## Guardrails
- No blind public submissions
- No directory spam
- No fabricated authority claims or metrics
- No fabricated FOMO, revenue lift, savings, or confidence
- No raw credential ingestion
- No untrusted content directly triggering tool execution
- Human approval required for consequential public actions unless a district explicitly enables a narrower approved automation path
- Third-party systems may only appear as clearly labeled external integrations
- Third-party company names, trademarks, and brands must not be encoded as AGENTROPOLIS districts

## Architecture

See [`docs/AGENTROPOLIS_DISTRIBUTION_LAYER.md`](docs/AGENTROPOLIS_DISTRIBUTION_LAYER.md).

```text
AGENTROPOLIS Intelligence Grid
└── Distribution Layer
    ├── GTM Engine
    ├── UGC Engine
    ├── Shared Services
    ├── Provider Adapter Contract
    └── District Distribution Packs
```

## Immediate Build Targets
1. District pack schema
2. GTM campaign schema
3. UGC submission and consent schema
4. Approval workflow
5. Analytics and attribution model
6. Publishing queue
7. Audit event schema
8. AGENTROPOLIS connector interface
9. Approved-action envelope
10. Provider adapter contract
11. Counterfactual attribution interface for Revenue War Room

## Final Principle

Build distribution like infrastructure.

Configure it by district.

Govern it like a system capable of affecting every brand connected to the Grid.
