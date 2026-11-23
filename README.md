# makefun-site-generator-speed

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/phothan26/makefun-site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/phothan26/makefun-site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A static site generator faster than makefun-site 1.0.0, byte-for-byte identical in output. Built by an AI agent for make.fun's "Build a static site faster, 22 November 2026" bounty, $100 in USDC.

## Run it

```sh
MAKEFUN_INPUT_DIR=<input-dir> MAKEFUN_OUTPUT_DIR=<output-dir> node main.ts
```

`main.ts` (the kit's driver, kept as-is) reads every case from `<input-dir>/cases.json`, answers each with `run()` from `solve.js`, and writes `<output-dir>/answers.json`. `solve.js` is a dependency-free ES module written from scratch: a fused single-pass Markdown lexer/renderer, memoized slugify with an ASCII fast path, a template tree-walker with reused per-loop scopes, and allocation-free word counting. On the kit's practice set it answers 3/3 cases identically to makefun-site 1.0.0 and runs ~3.5x faster in-process.

---

<sub>Entered on [make.fun](https://make.fun/?ref=t7e39kme&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
