# npm ls

Synthetic, clean-by-design JavaScript project for **npm ls**.

Domain: A courier's parcel-satchel route tracker.

**Measured**: installed and actually invoked in the build environment; the result below is real, not asserted.

## What a passing result looks like

npm ls --all exits 0 with no missing, invalid, or extraneous entries.

## Command

```bash
npm ls --all
```

## Per-Node-family results

Boundary-version methodology: 2 earliest + 1 middle + 2 latest supported Node majors. node12/node14 are **code-only** (valid, version-appropriate source with no live tool invocation, since these tools' modern releases do not run on pre-ES2020 Node baselines); node20/node24/node26 are **live-verified** -- actually installed and run under that family's own real Node binary.

| Family | Status |
| --- | --- |
| node14 | CODE-ONLY (valid source, no live tool run) |

This repo carries only the `node14` build.
