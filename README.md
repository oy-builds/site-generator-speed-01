[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/oy-builds/site-generator-speed-01/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/oy-builds/site-generator-speed-01/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

# Site Generator Speed

A fast, dependency-free drop-in replacement for makefun-site 1.0.0: `solve.js`
exports `run(input)`, which returns makefun-site's exact output tree for a site
(every page's `index.html`, the index and tag pages, `build-report.txt` and each
static file, byte for byte), and `main.ts` is the harness driver that answers
every case in `/input/cases.json` into `/output/answers.json`.

The implementation is a single-pass build written for CPU time: run-based HTML
escaping instead of per-character escaping, a fused Markdown lexer/renderer, a
manual word counter for reading time, and per-build memoised slugs — with no
state carried from one case to the next.
