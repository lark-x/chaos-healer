# chaos-healer

Autonomous Postgres chaos testing & self-healing PR verification harness.

**Status: early development.** There is no release yet — no demo, no action, no code
beyond this file. This repository is the public home for the project while v0.1 is
being built.

## Goal

Gate database-touching pull requests on behaviour, not on review opinions:

1. Spin up a disposable Postgres instance per run.
2. Inject realistic faults (connection loss, lock contention, replication lag,
   disk pressure, restarts) deterministically and reproducibly.
3. Run the candidate patch against those faults while checking a set of
   invariants (no lost commits, no duplicate side effects, bounded retry storms,
   correct rollback after failure).
4. Report a minimal failing scenario when an invariant breaks, so the author gets
   a repro instead of a stack trace.

## Roadmap

- `v0.1` (target date, not yet shipped): `docker compose up` one-command demo plus
  a reusable GitHub Action.
- Follow-up: fault profiles for common ORMs, saved-seed regression fixtures, and a
  report format that CI can post back to the PR.

Target dates are plans; they will be updated here as work progresses.

## Running it

Nothing to run yet. This section will be replaced with real instructions once the
first runnable milestone lands.