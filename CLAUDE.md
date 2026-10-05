# rivermind

Poker study tool. Parses PokerStars and GG hand histories, profiles
opponents, computes equity with Monte Carlo simulation, and explains
decisions in plain words. Stages and daily steps live in
`mayureshmandan/daily-dev` (issues labelled `stage`).

## Build and test

- `./mvnw verify` must pass before every commit. No local Maven install needed.
- Java 21. Tests use JUnit Jupiter.
- Test data is synthetic. Never commit real hand histories with real
  player names.

## Rules

1. One small step per day. A reviewer reads the diff in under 10 minutes.
2. Branch `day/YYYY-MM-DD-slug` (London date). Never push to main. Open a PR;
   Mayuresh merges it.
3. 1 to 4 commits per PR, in the order a person would make them: test,
   implementation, refactor. No filler commits. Never invent work to keep a
   streak going.
4. Commit messages: conventional prefix, lowercase, imperative, short.
   Example: `feat: add hand history parser`. Plain words, no emojis, no hype.
5. Build and tests pass before every commit. Never commit secrets.
6. Add `Co-Authored-By: Claude <noreply@anthropic.com>` only when Claude
   wrote most of that commit. Leave it off when Mayuresh wrote it.
7. Every PR body has: What changed / What this teaches (the concept in plain
   words, and why it matters at scale) / Try it yourself / Check (one
   question). Every PR adds a dated entry to `LEARNING.md`.

## Scope

A study and training tool only. It never reads from, attaches to, or
advises on a real-money poker client while a hand is being played. That
breaks the sites' terms.
