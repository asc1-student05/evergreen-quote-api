# Delivery Review: Evergreen Quote

Five slides OR one page. Target: 5 minutes spoken, then 3 minutes of questions.

## Slide 1: Delivery goal & did we hit it?

- **Goal:** By Thursday EOD, assemble the Evergreen Quote API with REST and GraphQL backed by MongoDB, pass the test suite, containerize it, demonstrate it on a local Kubernetes cluster, and merge it to `main` through a reviewed PR with green CI.
- **Hit?** ☒ Yes  ☐ Partially  ☐ No
- **Why:** We met the goal: the API was assembled with REST and GraphQL backed by MongoDB, the tests passed after the CI issue was fixed, the service was containerized and demonstrated on the local Kubernetes cluster, and the reviewed PR was merged to `main` with green CI.

## Slide 2: What shipped

- A curl transcript or screenshot of the running Evergreen Quote API on `main`: the health route and one quote response.
- Link to the merged PR.
- Link to the green CI run (install from the lock file + tests against a throwaway database).

## Slide 3: Two key decisions

- **Decision 1:** _one line._  Why it mattered: _one line._
- **Decision 2:** _one line._  Why it mattered: _one line._
- (Both should be in `decision-memo.md`.)

## Slide 4: Risks & injects

- Top risk we tracked: _from risk-register.md._
- Inject #1 (Tue): _what landed, how we re-prioritized._
- Inject #2 (Wed): _what landed, what we did, the go/no-go call._

## Slide 5: What I'd do differently next round

- 
- 

## Q&A prep: likely questions

- _e.g., "Why didn't you ship X?"_
- _e.g., "The demo returned quotes all week; why does one red test matter?"_
