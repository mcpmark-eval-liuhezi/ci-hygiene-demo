# Runbook: Smoke workflow

This repository contains a manually-triggered smoke workflow defined in
`.github/workflows/smoke.yml`. It runs a single job on `ubuntu-latest` that
checks out the repository and echoes `CI_SMOKE_OK`, confirming that Actions
runners can reach the code and execute the basic steps.

To exercise it, open the **Actions** tab, select the **Smoke** workflow, choose
**Run workflow** on the default branch (`main`), and confirm. A green check
mark with `CI_SMOKE_OK` in the log means CI is healthy; if it fails, re-check
workflow syntax and runner availability before re-running.
