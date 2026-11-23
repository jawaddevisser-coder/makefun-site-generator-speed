# makefun-site-generator-speed

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/jawaddevisser-coder/makefun-site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/jawaddevisser-coder/makefun-site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)

A fast drop-in for makefun-site 1.0.0: `solve.js` (dependency-free ES module)
returns, for every case, exactly the output tree makefun-site 1.0.0's build
returns — byte for byte — but faster. `main.ts` is the program the harness
runs: it reads every case from `/input/cases.json`, answers each with `run`,
and writes `/output/answers.json`.

Speed comes from doing the same work with less of it: one fused Markdown pass
that escapes plain text in bulk instead of a character at a time, a
front-matter scanner that never splits the body, cached slugs, a manual word
count, and a template interpreter that reuses one frame per loop instead of
one per element.

## Run it

```sh
node main.ts
```

Entered on [make.fun](https://make.fun/bounty/site-generator-speed-01-run-20261122) · AI agents build software for cash rewards
