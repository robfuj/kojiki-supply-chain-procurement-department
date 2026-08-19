# 10 — Supply Chain / Procurement

> Part of the **Kojiki Decision System**. This repo is the
> **Supply Chain / Procurement** line. It references the shared ontology in
> [`00-kojiki-ontology`](https://github.com/robfuj/kojiki-ontology) for the
> canonical schemas, taxonomy, decision-rights, and handoff standards.

## Primary question
> How do we acquire required resources at the right cost, quality, reliability, and risk?

## Purpose
Secure required goods/services and supplier capacity while optimizing total cost and risk.

## Sub-functions
Strategic Sourcing, Purchasing, Supplier Management, Vendor Risk, Contract Management, Inventory, Supply Chain Planning

## Typical roles
Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager

## Inputs
Requirements, supplier universe, prices, contracts, demand forecasts, quality data.

## Outputs
Supplier selections, purchase orders, contracts, inventory, supplier performance.

## Learning focus
Supplier reliability; price patterns; negotiation effectiveness; supply risk; quality; lead times.

## Operating tree
```text
NEED →
    SPECIFICATION →
    SUPPLIER UNIVERSE →
    QUALIFICATION →
    COMPARISON →
    RISK →
    NEGOTIATION →
    SELECTION →
    ONBOARDING →
    PERFORMANCE →
    RENEW / CHANGE / EXIT
```

## Decision states
```text
NEED-STATED → SPEC'D → SOURCING → QUALIFYING → COMPARING → NEGOTIATING → SELECTED → ONBOARDING → PERFORMING → RENEWED → EXITED
```

## Decision outputs
`Source · Negotiate · Award · Consolidate · Renew · Replace · Exit`

## Critical prompts (what this function thinks about)
> What do we actually need?
> Why do we need it?
> Can we build instead of buy?
> What specifications matter?
> Which suppliers can satisfy them?
> What differentiates suppliers?
> What is total cost of ownership?
> What dependencies are created?
> What contractual risks exist?
> What happens if the supplier fails?
> What alternatives exist?
> What leverage do we have?
> What should we negotiate?
> How will supplier performance be measured?
> Should we renew?
> Should we consolidate?
> Should we replace?

## Canonical record schema (docx Learning Ledger + Decision Object Fields)
Every decision in this line is recorded as:
- a **Decision Object** (docx S9) — see `schema/decision-object.json`
- a **Learning Ledger** entry (docx S7) — see `schema/learning-ledger.json`

and the agent must run the **Orientation Protocol** first (see `AGENT.md`).

## How this line runs on SYNAPSIS (the cognitive substrate)
Every decision in this line is decomposed through the shared SYNAPSIS transformation
chain ([`00-kojiki-ontology/synapsis`](https://github.com/robfuj/kojiki-ontology/synapsis)):
```
SOURCE → RECORD → EVIDENCE → INTERPRETATION → STRATEGY → INTERACTION → OUTPUT → OUTCOME → LEARNING
```
- **Three steps are dedicated niche bots**: `bots/evidence/` (this line's extraction
  specialist); the shared `synapsis/audit-bot/` (independent audit, org-wide) and
  `synapsis/learning-bot/` (cross-line memory). See `AGENT.md` for the full contract.
- The rest run inline inside this line's agent, each bounded to one authority.
- Meta-rule: *evidence ≠ interpretation ≠ belief ≠ doctrine.* Validate with
  `python3 synapsis/validate.py <record.json>` (in the ontology repo).

## How to use
1. Read `AGENT.md` — the first-run Orientation Protocol.
2. Read `SCHEMA.md` — how this line maps to the universal schema.
3. Read `data/10-supply-chain-procurement.json` — the machine-readable spec.
4. See `data/example.json` — one fully worked decision (Decision Object + Ledger).
5. Use `decision-graph.mmd` — agent-decodable operating tree + state model.
6. Validate new records: `python3 tools/validate.py data/<name>.json`
