# CI Findings: microsoft/TypeScript

## Organization and Repository Examined

- **Organization login (exact):** `microsoft` — https://github.com/microsoft
- **Repository:** `microsoft/TypeScript` — the TypeScript compiler, maintained publicly by Microsoft.
- **Main continuous-integration workflow:** `CI`, defined in `.github/workflows/ci.yml` (workflow ID 73).

## Recent Runs of the CI Workflow

Listing the workflow runs for `.github/workflows/ci.yml` returned **4,489 runs in total** (`total_count: 4489`). The most recent runs in the listing, newest first, were all `pull_request` events:

| Run # | Run ID | Title (display_title) | Status | Conclusion |
|---|---|---|---|---|
| 39044 | 39781668137 | Reuse this-independent interface member instantiations | completed | action_required |
| 39043 | 39773238950 | Emit the files of each checker in a deterministic order | completed | action_required |
| 39042 | 39769933610 | Clarify error when content mapper extension ends in a built-in extension | completed | action_required |
| 39041 | 39758106517 | [experiment] Skip incompatible discriminants when inferring | completed | success |

The `action_required` runs are fork pull requests whose workflows are parked awaiting maintainer approval, so they report **zero jobs**. The most recent run that had actually finished executing jobs (a full `success`) was:

- **Run #39041** (run ID `39758106517`), branch `fix-go/contextual-inference-discriminants`, head SHA `dfd496d6031cbc4da440fd18ab982c09c63aff3e`, run attempt 2, event `pull_request`, conclusion `success`.
- Run URL: https://github.com/microsoft/TypeScript/actions/runs/39758106517

## Jobs in the Most Recent Finished Run (Run #39041)

The run contained **24 jobs**, and every single one completed with conclusion `success`. The job names and outcomes, exactly as the API returned them:

| Job Name | Conclusion |
|---|---|
| package-feed-proxy | success |
| build | success |
| test extra (windows-latest) | success |
| test (ubuntu-latest) | success |
| release-build | success |
| test (race mode) | success |
| extension | success |
| test (windows-latest) | success |
| misc | success |
| test (windows arm64) | success |
| generate | success |
| lint (windows-latest) | success |
| codegen | success |
| test (concurrent test programs) | success |
| format | success |
| go-test | success |
| lint (ubuntu-latest) | success |
| test extra (ubuntu-latest) | success |
| tidy | success |
| test (noembed) | success |
| test (linux arm64) | success |
| lint (noembed) | success |
| smoke | success |
| required | success |

**Summary:** 24/24 jobs succeeded, giving the run an overall conclusion of `success`.

## Takeaways for Our Runbook

1. **Cite the exact org login** (`microsoft`, not `Microsoft`) when referencing upstream examples.
2. **Read run listings carefully** — `action_required` conclusions on fork PRs mean the workflow is waiting on maintainer approval, not that jobs failed; those runs legitimately have no jobs.
3. **A "finished" run** (`status: completed`) is the one whose jobs can be inspected and broken down.
4. TypeScript's CI matrix shows healthy CI hygiene: small, focused, well-named jobs across platforms (ubuntu, windows, arm64, noembed, race mode), plus a final `required` job that aggregates required checks.
