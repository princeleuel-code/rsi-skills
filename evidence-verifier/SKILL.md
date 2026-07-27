---
name: evidence-verifier
description: Prevent plans, attempts, generated artifacts, and unsupported statements from becoming verified truth
version: 0.1.0
metadata:
  rsi:
    authority: proposal-only
    project_scope: [CANA, Hermes, ORBIT_OMEGA, ORDERWEEDDC]
    maximum_autonomy: OBSERVE
    required_tools: [truthgraph, receipt-ledger, evidence-store]
    prohibited_actions: [invent-evidence, rewrite-receipt, self-promote]
---

# Evidence Verifier

## Trigger
Use before any mission, capability, deployment, provider, ranking, revenue, inventory, compliance, test, integration, or launch claim is marked complete or verified.

## Procedure
1. Identify the exact claim and its current state: planned, attempted, partial, completed-unverified, verified, failed, rolled back, or superseded.
2. Define the evidence required for that claim class.
3. Inspect direct receipts rather than trusting summaries produced by the acting agent.
4. Validate hashes, signatures, scope, timestamps, idempotency, source identity and chain continuity where applicable.
5. Separate source-supported facts, calculations and inferences.
6. Reject circular evidence in which one unsupported claim cites another.
7. Reject stale evidence when the claim requires current state.
8. Return missing, contradictory and independently unverifiable evidence as explicit gaps.
9. Permit `VERIFIED` only when every mandatory receipt and postcondition is satisfied.
10. Preserve failed and partial states; do not soften them for presentation.

## ORDERWEEDDC protected claims
Never verify rankings, traffic, revenue, customers, reviews, inventory, pricing, delivery availability, licensing, merchant authorization, legal approval, ad eligibility, medical claims, provider connectivity or test results without direct appropriate evidence.

## Verification
The output must name the claim, required evidence, observed evidence, missing evidence, result state and supporting receipt references.
