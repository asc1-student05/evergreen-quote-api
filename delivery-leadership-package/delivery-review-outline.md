# Delivery Review: Evergreen Quote API

**Presenter:** Delivery Lead 
**Presentation:** Friday delivery review  
**Target:** 5 minutes, followed by 3 minutes of questions

## Slide 1 — Delivery goal and outcome

**Goal:** Deliver an assembled Evergreen Quote API with REST and GraphQL backed by MongoDB, tested, containerized, demonstrated on a local Kubernetes cluster, and merged to `main` through a reviewed pull request with green CI.

**Outcome: YES — based on the completed delivery work and the corrected green CI run.**

**Why:** The team fixed the CI failure, and I made a GO decision based on the corrected green signal. The delivery included the API assembly, automated tests, container work, and Kubernetes demonstration. The project was managed through the delivery board and pull request linked below.

> Before presenting, confirm that PR #16 is actually merged and that the Kubernetes demo was completed. If either is not true, change the outcome to “Partially” and say exactly what remains.

## Slide 2 — What shipped

- **Repository:** [Evergreen Quote API](https://github.com/asc1-student05/evergreen-quote-api)
- **Pull request:** [PR #16](https://github.com/asc1-student05/evergreen-quote-api/pull/16)
- **CI outcome:** The team fixed the CI issue; the corrected run was green. **Successful Actions run:** (https://github.com/asc1-student05/evergreen-quote-api/actions/runs/43255734973/job/131313308404)
- **Merge status:** Merged Succesfully, https://github.com/asc1-student05/evergreen-quote-api/pull/16
- **Demo / Screenshots** & **GraphQL / Kubernetes proof:** 
Briefly state what you personally verified. I have screenshots saved seperately.

**What the API does:** It serves quotes through REST and GraphQL, stores them in MongoDB, validates quote requests, and calculates premiums using the shared rate table.

## Slide 3 — Two important decisions

### Decision 1: Defer renters coverage

I recommended **not adding renters coverage this week** and putting it into a later planning round.

**Why it mattered:** Renters was not just a dropdown option. It required API/schema changes, an approved rate from the sponsor, seed data, tests, GraphQL changes, and a website update. Deferring it protected the agreed delivery goal and avoided taking on unplanned work without a pricing decision.

### Decision 2: GO after CI was fixed

During the Wednesday incident exercise, the supplied CI log showed a failing test run on `main`. The team fixed the CI issue, and the corrected run was green. I chose **GO** based on the corrected green CI signal.

**Why it mattered:** The decision used the actual recovery signal rather than treating the earlier red run as the final state. I also kept the customer-deployment question open for the release/engineering owner to confirm, because the failing run itself did not produce a build.

## Slide 4 — Risks and the two injects

### Main risk

**Risk:** Customers could be affected by a change that is not represented by the failing CI run.  
**Response:** Ask the release/engineering owner to confirm what version is deployed and how the customer-facing behavior reached users. Keep the investigation with the appropriate technical owner rather than trying to change the validator myself.

### Tuesday Inject #1 — Scope request and base-image CVE

- A partner requested renters quotes by Thursday and described them as “one more dropdown option.”
- At the same time, Platform reported a moderate CVE in the pinned `node:22-alpine` base image. The patched tag was expected next week, and the API was not internet-exposed this week.
- **My renters decision:** Defer it to a later round; record the work and dependencies on the project board.
- **Base-image decision:** [State your actual ship/hold recommendation and any approval or condition. Do not claim approval unless you received it.]
- **What I needed:** A sponsor-approved renters rate for future planning and a clear platform/security decision on the current base image.

### Wednesday Inject #2 — Customer incident and simulated CI log

- Support reported quote requests failing with an age minimum of 110.
- The supplied log showed the test step failed because the change set the age **minimum** to 110, rejecting normal ages. Checkout, setup, MongoDB startup, and dependency installation passed; the tests caught the problem. That failing run produced no build.
- The simulated log was evidence for the exercise; it was separate from the learner’s own green branch.
- The team then fixed the CI issue, and the corrected run was green. I chose **GO** based on that corrected result.
- I did not assume the red run caused the customer-facing issue. I routed the question of what was actually deployed to the appropriate owner.

## Slide 5 — What I would do differently next time

- Confirm deployment ownership and how releases are gated by CI before an incident, so the team can quickly identify the version customers are using.
- Ask for sponsor decisions—especially pricing and scope—early, with a named owner and a clear response deadline.
- Keep separate records of CI results for the feature branch, `main`, and the corrected run so the release decision is based on the right evidence.

## Q&A preparation

**Why didn’t you add renters coverage?**  
Because it required changes across the API, pricing, data, tests, GraphQL, and website. The rate also needed a sponsor decision. Deferring it protected the agreed work for this delivery.

**Why did you choose GO after seeing a red CI run?**  
The red run was the earlier signal. The team fixed the issue, and the corrected CI run was green. I chose GO based on the corrected result—not the old red run. The PR still needed to meet its actual review and merge checks.

**Did the red run cause customers’ quote errors?**  
I did not assume that. The red run produced no build, so I asked the release/engineering owner to confirm what version was serving customers and how the behavior reached them.

**What evidence supports the delivery outcome?**  
The repository, project board, PR, corrected green CI run, and a verified service demonstration. I will show the links and evidence I confirmed before the presentation.

**What would you do if PR #16 was not merged?**  
I would report the outcome as partially complete, explain what remained, and give the specific condition and owner needed to complete the merge. I would not describe an open PR as merged.

## Presenter’s final checks

- [ ] Confirm PR #16’s current status; state “merged” only if GitHub shows it is merged.
- [ ] Add the successful corrected CI run link, if available.
- [ ] Confirm the local Kubernetes demo and API responses you personally verified.
- [ ] Fill in the actual base-image decision and any platform/security approval.
- [ ] Update the outcome if any part of the stated delivery goal was not completed.
- [ ] Remove or complete all remaining bracketed prompts before presenting.
