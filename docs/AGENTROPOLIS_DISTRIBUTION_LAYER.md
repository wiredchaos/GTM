# AGENTROPOLIS Distribution Layer

AGENTROPOLIS uses one shared Distribution Layer across the Intelligence Grid.

This is infrastructure, not a standalone marketing website.

The Distribution Layer provides reusable go-to-market and user-generated-content capabilities to every district without duplicating core logic.

## Core Principle

One citywide distribution system.

Each district owns its own distribution pack.

Districts do not receive cloned GTM systems. They inherit shared engines and supply their own configuration, policies, audiences, channels, assets, and measurement rules.

## Core Engines

### GTM Engine

Responsible for:

- positioning
- messaging
- SEO
- AEO
- GEO
- AI-search visibility
- GitHub discoverability
- community distribution
- campaign orchestration
- channel planning
- publishing workflows
- analytics
- attribution
- approval workflows

### UGC Engine

Responsible for:

- user-generated content intake
- creator campaigns
- community submissions
- ambassador programs
- referral programs
- reviews
- testimonials
- case studies
- social-proof collection
- viral-content tracking
- reward and commission events
- moderation and consent workflows

## Shared Services

The Distribution Layer includes:

- campaign manager
- workflow engine
- publishing queue
- asset library
- analytics
- attribution
- governance
- audit logging
- permissions
- approval gates
- template registry
- event bus
- queue system
- connector interface
- district adapter runtime

## District Distribution Packs

Each district supplies a configuration pack containing:

- canonical identity
- audience definitions
- offers
- brand voice
- goals
- approved channels
- content templates
- campaign templates
- KPIs
- attribution rules
- approval rules
- permissions
- assets
- publishing preferences
- legal and reputation constraints

A district pack configures the shared engines. It does not duplicate them.

## Architecture

```text
AGENTROPOLIS Intelligence Grid
└── Distribution Layer
    ├── GTM Engine
    ├── UGC Engine
    ├── Campaign Manager
    ├── Workflow Engine
    ├── Publishing Queue
    ├── Asset Library
    ├── Analytics
    ├── Attribution
    ├── Governance
    ├── Audit Log
    ├── Approval Pipeline
    ├── Template Registry
    ├── Connector Interface
    └── District Distribution Packs
```

## Recommended Repository Structure

```text
/distribution
    /gtm
    /ugc
    /campaigns
    /analytics
    /attribution
    /governance
    /workflows
    /templates
    /publishing
    /connectors
    /districts
```

Each district folder should contain configuration and policy, not copied engine code.

Example:

```text
/distribution/districts/<district-slug>
    district.yaml
    audiences.yaml
    channels.yaml
    campaigns.yaml
    templates.yaml
    approvals.yaml
    metrics.yaml
    permissions.yaml
```

## Event Model

The Distribution Layer should be event-driven.

Representative events:

- `campaign.created`
- `campaign.approved`
- `asset.generated`
- `asset.approved`
- `content.submitted`
- `ugc.consent_verified`
- `publication.queued`
- `publication.completed`
- `conversion.recorded`
- `commission.calculated`
- `district.policy_blocked`
- `canonical.drift_detected`

Every event must include:

- event ID
- timestamp
- district ID
- actor or agent ID
- campaign ID when applicable
- source system
- approval state
- audit metadata

## Governance Requirements

The Distribution Layer must:

- require human approval for public publishing unless a district explicitly enables a narrower approved automation path
- prevent raw credential ingestion
- prevent untrusted content from directly triggering tool execution
- maintain immutable audit records for consequential actions
- support rollback planning
- enforce district-level permissions
- block false claims, fabricated metrics, and unauthorized partnerships
- separate drafting, approval, publishing, and measurement permissions
- preserve canonical naming across all distribution surfaces

## UGC Safety Requirements

UGC workflows must support:

- contributor consent
- usage-right tracking
- moderation state
- attribution state
- compensation or commission state
- removal requests
- prohibited-content rules
- evidence retention
- campaign-specific terms

No user-generated asset should be published merely because it was submitted.

## Implementation Constraints

- Build for AI agents first and humans second.
- Keep every component independently testable.
- Favor composable services over monolithic code.
- Make district configuration declarative.
- Keep the system white-label capable.
- Do not duplicate GTM or UGC logic across districts.
- Do not encode third-party company names, trademarks, products, or brands as AGENTROPOLIS districts.
- Third-party systems may only appear as explicitly labeled external integrations.

## Success Condition

A new district should be able to join the Distribution Layer by adding a validated district pack without modifying the shared GTM or UGC engine.

The system should make distribution reusable, measurable, governed, and machine-operable across the entire Intelligence Grid.
