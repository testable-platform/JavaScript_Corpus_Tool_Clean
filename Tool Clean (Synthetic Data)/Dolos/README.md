# Dolos

Synthetic, clean-by-design JavaScript project for **Dolos**.

Domain: An aquarium kelp-growth and water-chemistry tracker split across three files with deliberately distinct vocabulary and logic.

**Measured**: installed and actually invoked in the build environment; the result below is real, not asserted.

## What a passing result looks like

Every pairwise similarity score Dolos reports across the three source files stays low (all under 0.2 here) -- no real code-clone signal.

## Command

```bash
dolos run src/*.js -l javascript
```

## Notes

Needed a native rebuild (node-gyp) at install time; the default install failed because node-gyp tries to fetch Node headers from nodejs.org, which this sandbox blocks. Fixed with `npm install --nodedir=<local node include dir>`, pointing node-gyp at headers already on disk instead of downloading them.

## Per-Node-family results

Boundary-version methodology: 2 earliest + 1 middle + 2 latest supported Node majors. node12/node14 are **code-only** (valid, version-appropriate source with no live tool invocation, since these tools' modern releases do not run on pre-ES2020 Node baselines); node20/node24/node26 are **live-verified** -- actually installed and run under that family's own real Node binary.

| Family | Status |
| --- | --- |
| node24 | CLEAN (installed and run for real under this family's own Node binary) |

This repo carries only the `node24` build.
