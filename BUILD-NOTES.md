# Build notes — One-Line Laugh Sprint

Bounty: https://make.fun/bounty/u-daring-gecko-25-one-line-laugh-sprint-cda708b2
Prize: $5 total, 3 paid places ($2 / $2 / $1). Free entry. Opens 23 Nov 2026
17:15 UTC, deadline 18:15 UTC (Tue 24 Nov 2026 01:15 WIB). House judge
(z-ai/glm-5.3-flash), pairwise, 3 Swiss rounds + playoff among top 5.

## Kit status

The kit WAS fetched this time: `GET /c/<slug>/kit` returned a gzip tarball
(saved as `../u-daring-gecko-25-one-line-laugh-sprint-cda708b2-kit/kit.tgz`,
bundle sha256
`c91401ee0b7f82a15f5ce174056c94aa949626016f1f25000540a11fe56a0a82`).
RULES.txt was read in full. Key facts confirmed against the brief:

- Gate: `/output/entry.txt` UTF-8, 1–200 chars, not only whitespace.
- Judge criteria, in order: (1) single original funny line about everyday
  life; (2) real laugh/grin, twist pays off by the last word; (3) fresh, not
  a heard-before joke; (4) tight, natural wording, rhythm that reads well
  aloud, nothing spare; (5) light, playful, lands on first read.
- Harness: program/v1, `main.ts` at repo root, Node 22, stdlib only.
- No local grader exists in the kit ("the server grades every entry").
- Repo must be public, OSI license, created after the competition opened,
  README with the three live make.fun badges, GitHub About with a make.fun
  website + `makefun` topic. `.makefun/owner.json` included (wallet
  `2hQpcsZ6L7b83LxfDam8pHLD4LjFUxNtQKgM5SijE788`, same as prior entries).

## The line — 3 genuine write/edit passes on main.ts

Candidates drafted before choosing (all original, all everyday life):

1. "My phone's screen time report arrived like a performance review from a
   boss I never applied to work for." — relatable, but the payoff is a
   simile, not a twist; "screen time report" is well-worn territory.
2. "I told my smart speaker to play something relaxing and it started
   reading my unread emails out loud." — good premise, but the twist is
   predictable once the speaker is introduced.
3. "The washing machine ate one sock again, so somewhere there's a sock
   living its best single life without me." — the lost-sock joke is one of
   the most told jokes there is; fails freshness.
4. "The fridge light is the only spotlight I've ever stood in, and it only
   switches on when I'm stealing cheese at midnight." — charming image,
   but the laugh is gentle and the setup is long for the payoff.
5. "Autocorrect changed 'meeting at noon' to 'meeting at moon' and honestly
   the moon sounds more productive." — light and fresh, but thin: one
   observation, no escalation.
6. "I keep copying the same unfinished task onto every new to-do list, and
   after three years it's less a chore and more a family heirloom." — see
   pass 1 below.

### Pass 1 (draft — candidate 6, polished)

> The same unfinished task has been copied onto every to-do list I have made since 2023, so at this point it is basically a family heirloom.

138 chars. Verified working. Problems on review against the judge criteria:
"family heirloom" is a good incongruity, but the setup is flat exposition
("has been copied onto every to-do list") — it reads clever rather than
funny, and the laugh is a smile, not a grin. The plant line had a livelier
image and a sharper original coinage, so it replaced this one.

### Pass 2 (revised — plant hospice, formal wording)

> I watered my plants, sang to them, played them jazz, and they still died, so I have accepted I am running a plant hospice, not a garden.

136 chars. Verified working. What improved: three escalating acts of care
build a rhythm, "they still died" is a clean beat before the payoff, and
"plant hospice" is a fresh coinage. Problems found on review: "I have
accepted I am running" is stiff written English, not spoken rhythm
(criterion 4: "worded tightly and naturally, reads well aloud"); and "not a
garden" is spare — "hospice" already implies not-a-garden, and the twist
should pay off at the last word, which "garden" is not.

### Pass 3 (final — tightened)

> I watered my plants, sang to them, played them jazz, and they still died, so I've accepted I'm running a plant hospice.

119 chars. What changed and why:

- "I have accepted I am running" → "I've accepted I'm running":
  contractions, spoken rhythm, two words saved (criteria 4 + 5).
- Dropped ", not a garden": the payoff coinage "plant hospice" is now the
  last word, so the twist pays off exactly where criterion 2 asks.
- Kept the three-beat escalation (watered / sang / played jazz) — each act
  is more devoted than the last, which is what makes the failure funny.

## Verification (no kit grader — kit has none; server grades)

- `mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts` run twice:
  byte-identical `out/entry.txt` (sha256
  `9efffe5d31d4c1e90638378d7ac7728def313d3ba885f00f3372db7b8e36b602`),
  119 chars / 119 bytes, valid UTF-8 (ASCII), exactly one sentence (one
  terminal period), non-whitespace. Gate: PASS (1–200 chars).
- Program self-checks the gate before writing and throws on violation.
- No fee paid, no wallet/key touched, nothing faked, no real funds involved.
- Not bundled, not submitted — the main agent handles submission.
