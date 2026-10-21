# Mocha

Synthetic, clean-by-design JavaScript project for **Mocha**.

Domain: A library call-number shelving system.

**Measured**: installed and actually invoked in the build environment; the result below is real, not asserted.

## What a passing result looks like

Every test passes: mocha exits 0.

## Command

```bash
mocha 'test/**/*.test.js'
```

## Per-Node-family results

Boundary-version methodology: 2 earliest + 1 middle + 2 latest supported Node majors. node12/node14 are **code-only** (valid, version-appropriate source with no live tool invocation, since these tools' modern releases do not run on pre-ES2020 Node baselines); node20/node24/node26 are **live-verified** -- actually installed and run under that family's own real Node binary.

| Family | Status |
| --- | --- |
| node12 | CODE-ONLY (valid source, no live tool run) |

This repo carries only the `node12` build.
