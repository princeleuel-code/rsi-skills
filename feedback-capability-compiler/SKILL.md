---
name: feedback-capability-compiler
description: Convert repeated durable corrections into tested candidate capability patches without direct production self-modification
version: 0.1.0
metadata:
  rsi:
    authority: proposal-only
    project_scope: [CANA]
    maximum_autonomy: DRAFT
    required_tools: [session-feedback, skill-registry, evaluation-court, promotion-court]
    prohibited_actions: [modify-production-skill, self-promote, cross-project-generalize, retain-sensitive-fixture]
---

# Feedback-to-Capability Compiler

## Trigger
Use after completed sessions contain explicit corrections, rejection reasons, accepted revisions, or repeated requests to close the same operational loop.

## Procedure
1. Extract explicit corrections and preserve source session and mission identifiers.
2. Separate task-specific feedback from durable candidate behavior.
3. Remove credentials, customer-sensitive facts and unnecessary personal data from replay fixtures.
4. Cluster by project, skill and concrete failure code.
5. Require repetition across distinct sessions and minimum confidence before creating a candidate.
6. Link the failure to the responsible skill, policy, router, prompt or tool contract.
7. Generate a proposal-only patch and regression case.
8. Replay baseline and candidate against representative historical tasks.
9. Compare factual correctness, task completion, instruction adherence, style, evidence quality, safety, latency, cost, unnecessary tool calls and user correction count.
10. Reject safety regression, any material quality regression, increased corrections, unjustified tool expansion or authority widening.
11. Produce an independently reviewable report.
12. Hand eligible candidates to shadow and canary gates; never promote directly.

## Verification
- at least two distinct source sessions unless a human explicitly designates a correction as durable;
- project scope remains narrow;
- sensitive details removed;
- new regression test exists;
- baseline/candidate scorecard exists;
- candidate state remains `PROPOSED`;
- rollback version is identified.
