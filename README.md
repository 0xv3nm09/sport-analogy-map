# sport-analogy-map

An open, human-reviewed map of "Like X, except Y" comparisons that explain
cricket moments to fans of American football, baseball, basketball and soccer.
Built for [Same Game](https://amazonappdev2026.devpost.com/) (Fire TV track,
Build Ship Shape hackathon) and open to any fan to improve.

## The rule

Every entry is `like` (what it resembles in your sport) plus `except` (where
the analogy breaks — analogies teach better when the break is pointed out;
Gentner & Smith 2013). Entries list `numbers_in_text` so the Same Game
validator can allow those numbers in generated lines, and `reviewed_by`
names the fans who approved the entry. **An entry with an empty
`reviewed_by` is a draft and is never served as reviewed.**

## Contribute

1. Pick a moment type from [`schema/comparison.schema.json`](schema/comparison.schema.json)
   (see a sport file's `_remaining_moment_types` for gaps).
2. Open a pull request adding or editing an entry in `cricket/<sport>.json`.
3. A fan of that sport reviews it; approvals add their handle to `reviewed_by`.

Factual ground truth (scores, runs needed) never comes from this repo — code
computes it from ball data. This repo only holds the analogies.
