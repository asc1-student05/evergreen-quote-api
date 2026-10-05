## Delivery Goal: Evergreen Quote

### Goal

Deliver the Evergreen Quote API by the end of the week with working REST and GraphQL endpoints, automated testing, containerization, CI/CD validation, and a successful Kubernetes deployment.

### "Done" looks like

- The API answers every documented route: list, fetch by id, create with a computed premium.
- The same data answers through GraphQL, with the explorer at /explorer.
- npm test passes; the safety net holds.
- The containerized API serves the same answers as the dev server, and the CI run on the merge commit is green.
- The cluster demo shows three API pods behind one Service.
- A reviewed PR is merged, branch deleted.
- delivery-leadership-package/ is complete and committed.

### Out of scope (this week)

- UI redesign or front-end enhancements.
- New business features beyond documented requirements.
- Performance optimization beyond successful deployment.
- Production monitoring and alerting implementation.
- Security enhancements not included in the lab requirements.