## Decision Memo: Renters Coverage Request

**Date:** Monday (Project started on Friday)
**Author:** Jyoti Kumari
**Decision Area:** Day 2 Scope Tradeoff

### Context

The project sponsor requested that renters coverage be made quotable through the Evergreen Quote API by Thursday. Initial review showed that renters coverage impacts multiple areas of the solution including the quote schema, premium rate table, seed data, automated tests, GraphQL schema, and customer-facing dropdown selections. The delivery goal has not changed and key deployment activities remain scheduled later in the week.

### Options Considered

- **Option A: Add renters coverage this week**
  - Pros: Supports the partner request immediately and allows earlier adoption.
  - Cons: Requires updates across multiple components and introduces additional testing and delivery risk. A renters premium rate has not yet been approved.

- **Option B: Defer renters coverage to the next release**
  - Pros: Protects the committed delivery goal, minimizes risk, and allows sufficient time for design, implementation, and testing.
  - Cons: Partner onboarding is delayed until the next release cycle.

- **Option C: Perform analysis only and revisit after sponsor approval**
  - Pros: Improves understanding of the effort required.
  - Cons: Does not provide customer value this week and still creates uncertainty around delivery commitments.

### Recommendation

Recommend Option B: defer renters coverage from the current release and include it in a future delivery increment after premium rates and business requirements are finalized.

### Why

The primary goal this week is to deliver a stable, tested, and deployable Evergreen Quote API. Introducing new scope late in the delivery cycle increases schedule risk and may impact solution quality and release readiness.

### What Would Change My Mind

If the sponsor provides an approved renters premium rate and confirms by 11:00 AM Wednesday that renters coverage is the highest business priority, I would revisit this recommendation and reassess delivery impacts before proceeding.
