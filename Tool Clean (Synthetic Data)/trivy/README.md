# trivy

Synthetic, clean-by-design JavaScript project for **trivy**.

Domain: A cargo-yard loading-dock drop-off scheduler.

**Not installed here**: see Notes for why, and what was checked instead.

## What a passing result looks like

0 vulnerabilities, 0 secrets -- zero runtime dependencies and no credential-shaped strings anywhere in source.

## Command

```bash
trivy fs --scanners vuln,secret --exit-code 1 .
```

## Notes

The trivy binary is a GitHub release asset; this sandbox's egress allowlist returns 403 for it (same constraint as the Python sibling corpus).

## Per-Node-family results

Boundary-version methodology: 2 earliest + 1 middle + 2 latest supported Node majors. node12/node14 are **code-only** (valid, version-appropriate source with no live tool invocation, since these tools' modern releases do not run on pre-ES2020 Node baselines); node20/node24/node26 are **live-verified** -- actually installed and run under that family's own real Node binary.

| Family | Status |
| --- | --- |
| node14 | CODE-ONLY (valid source, no live tool run) |

This repo carries only the `node14` build.
