---
name: canonical-memory-curator
description: Register durable CANA memory without silent overwrite, cross-project leakage, or unsupported truth
version: 0.1.0
metadata:
  rsi:
    authority: proposal-only
    project_scope: [CANA]
    maximum_autonomy: OBSERVE
    required_tools: [memory-registry, truthgraph, evidence-store]
    prohibited_actions: [delete-source, self-promote, widen-consumers, store-credentials]
---

# CANA Canonical Memory Curator

## Trigger
Use when a project fact, decision, preference, receipt-backed result, supersession, contradiction, or review date may deserve durable storage.

## Non-trigger
Do not use for casual remarks, temporary task instructions, unverified completion claims, secrets, raw credentials, another tenant's facts, or content whose project/scope is unknown.

## Inputs
- proposed memory object;
- project and scope;
- source and author;
- evidence references;
- confidence and verification date;
- review/expiration policy;
- allowed consumers.

## Procedure
1. Classify the item as observed, calculated, corroborated, inferred, disputed, stale, unknown, superseded, or temporary.
2. Reject secrets and raw credentials before any durable write.
3. Require stable object ID, claim key, project, scope, source, author, timestamps, confidence and sensitivity.
4. Canonicalize the payload and compare its hash with active records in the same project, scope and claim key.
5. Return `DUPLICATE` when the payload already exists; do not create a second active fact.
6. Return `CONTRADICTION` and mark both records disputed when active payloads differ; never silently choose one.
7. Use explicit supersession only when the replacement resolves the prior record and records both directions of the relationship.
8. Link every verified fact to TruthGraph and evidence references.
9. Set a review date for facts that can become stale.
10. Emit a receipt or candidate report; do not promote memory status by model preference.

## Verification
- no secret pattern detected;
- project/scope isolation passes;
- duplicate and contradiction checks executed;
- TruthGraph state matches available evidence;
- supersession links are bidirectional;
- stale-review policy is present when required;
- production memory was not self-modified.

## Failure modes
- preference extracted from one task and incorrectly treated as permanent;
- contradictory records both remain active;
- evidence reference points only to another unsupported claim;
- user correction is generalized outside its named project;
- obsolete provider-specific instruction survives a provider-neutral supersession.
