# ci-hygiene-demo
Live demo for the GitHub Actions chapter of the team handbook

## Pull-request hygiene notes

- Keep feature branches short-lived; open a PR early and keep it current with the base branch.
- When the default branch moves ahead, update the PR branch so it picks up the new base commit before review/merge.
- Prefer many small, well-named CI jobs over one large opaque job — see `ci-findings.md` for a real-world example from `microsoft/TypeScript`.
