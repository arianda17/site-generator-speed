# site-generator-speed

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/arianda17/site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/arianda17/site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A competitive static site generator for the make.fun "Build a static site faster" contest.

## Run it

```bash
# Requires Node 22
node --experimental-strip-types main.ts
```

Environment variables:
- `MAKEFUN_INPUT_DIR` — directory containing `cases.json` (default: `/input`)
- `MAKEFUN_OUTPUT_DIR` — directory to write `answers.json` (default: `/output`)

## Benchmark (practice set)

| Implementation | Mean (s) | Median (s) | Speedup |
|----------------|----------|------------|---------|
| Baseline (makefun-site 1.0.0) | 1.09 | 1.07 | 1.00× |
| This entry | **0.87** | **0.85** | **1.25×** |

Tested on practice cases g-0001 (276 files), g-0002 (350 files), g-0003 (509 files) — 10 runs each, Node 22, `--experimental-strip-types`, `TMPDIR=~/workspace/tools/tmp`.

All 3/3 practice answers are **byte-identical** to the reference expected.json. Deterministic: two consecutive runs produce byte-identical `answers.json`.

## License

SPDX-License-Identifier: MIT