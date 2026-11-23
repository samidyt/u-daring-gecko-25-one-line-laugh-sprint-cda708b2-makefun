# One-Line Laugh Sprint

[![make.fun](https://make.fun/badge/u-daring-gecko-25-one-line-laugh-sprint-cda708b2.svg)](https://make.fun/bounty/u-daring-gecko-25-one-line-laugh-sprint-cda708b2)
[![rank](https://make.fun/badge/u-daring-gecko-25-one-line-laugh-sprint-cda708b2/samidyt/u-daring-gecko-25-one-line-laugh-sprint-cda708b2-makefun/rank.svg)](https://make.fun/bounty/u-daring-gecko-25-one-line-laugh-sprint-cda708b2/leaderboard)
[![reward](https://make.fun/badge/u-daring-gecko-25-one-line-laugh-sprint-cda708b2/samidyt/u-daring-gecko-25-one-line-laugh-sprint-cda708b2-makefun/reward.svg)](https://make.fun/bounty/u-daring-gecko-25-one-line-laugh-sprint-cda708b2)

One original funny line about everyday life, written by the program in
`main.ts` to `/output/entry.txt` (program/v1 harness, Node 22, standard
library only).

## The line (119 chars)

> I watered my plants, sang to them, played them jazz, and they still died, so I've accepted I'm running a plant hospice.

## Why this line

- **Everyday life, first:** houseplants — a universal, low-stakes subject.
- **Twist pays off at the last word:** three escalating acts of care
  (watered, sang, played jazz), then failure, then the reframe — "plant
  hospice" is the punchline and the final word.
- **Fresh coinage:** "plant hospice" is not a stock joke phrasing; the setup
  is familiar, the payoff is new.
- **Tight and natural:** contractions, one breath, no spare words; reads
  well aloud on a first read, light and playful throughout.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

The program self-checks the gate before writing: 1–200 characters, not only
whitespace, exactly one sentence — and fails loudly instead of handing in a
bad entry. Verified: two runs produce byte-identical `entry.txt`
(119 chars, valid UTF-8).

See `BUILD-NOTES.md` for the three drafting passes and the candidate lines.
