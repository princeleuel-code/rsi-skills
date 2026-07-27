---
name: launch-gate-review
description: Keep ORDERWEEDDC fail-closed until every required capability, provider, receipt and protected baseline check passes
version: 0.1.0
metadata:
  rsi:
    authority: proposal-only
    project_scope: [ORDERWEEDDC]
    maximum_autonomy: OBSERVE
    required_tools: [truthgraph, receipt-ledger, provider-registry, test-reports, release-manifest]
    prohibited_actions: [open-launch-gate, deploy, connect-credentials, invent-pass, weaken-test]
---

# ORDERWEEDDC Launch Gate Review

## Trigger
Use before a release, provider certification, production deployment, domain cutover, capability promotion or statement that ORDERWEEDDC is ready to launch.

## Protected rules
Do not redesign the approved interface, replace the approved logo, weaken fail-closed behavior, create doorway clones, expose credentials, or copy protected competitor assets.

Never invent rankings, traffic, revenue, customers, reviews, ratings, inventory, pricing, delivery availability, licensing, merchant authorization, legal approval, ad eligibility, medical claims, test results or provider connectivity.

## Procedure
1. Resolve the exact protected release and baseline commit/hash set.
2. Verify branch, commit, release hashes, test counts, archive continuity, local guardrails, TruthGraph validity, secret findings and current launch-gate state.
3. Compare candidate changes against the protected baseline and identify every affected capability.
4. Require direct receipts for authentication, success, dependency failure, invalid credential, timeout, rate limit, malformed response, stale data, revocation, rollback and secret-isolation tests where applicable.
5. Verify the browser/frontend bundle contains no credential or reversible secret material.
6. Verify every production claim against external state rather than generated reports alone.
7. Reject any missing, stale, contradictory or circular receipt.
8. Report each gate as PASS, FAIL, BLOCKED or NOT RUN.
9. Keep the launch gate closed unless every mandatory gate is PASS and promotion authority signs the release.

## Verification output
- protected baseline identifiers;
- changed components;
- exact test counts and reports;
- provider/capability certification matrix;
- secret-scan report;
- rollback proof;
- missing receipts;
- final launch-gate state.

This skill can recommend only. It cannot open the launch gate.
