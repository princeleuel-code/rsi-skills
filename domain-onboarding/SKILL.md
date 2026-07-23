---
name: domain-onboarding
description: Onboard a domain without granting unverified management authority
version: 0.1.0
metadata:
  rsi:
    authority: proposal-only
---


# RSI Domain Onboarding

## When to Use
When a business owner submits a domain for analysis or management.

## Procedure
1. Normalize and classify the domain.
2. Start in PUBLIC_ANALYSIS mode.
3. Discover only public facts until ownership is verified.
4. Offer DNS, HTML, CMS, GitHub, Search Console, analytics, ads, revenue, or signed-owner verification.
5. Create a tenant-scoped DomainTwin only after identifiers are established.
6. Begin authorized read-only observation after verification.
7. Require policy promotion for draft or production actions.

## Pitfalls
- A URL is not authorization.
- Search Console access is not automatically CMS or ads authority.
- Never reuse one tenant's memories or credentials for another.

## Verification
Produce an ownership receipt, connector inventory, authority matrix, and unresolved unknowns.
