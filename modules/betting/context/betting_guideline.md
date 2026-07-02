# Betting Guideline

This file is the source of truth for the Betting module.

If any other betting file conflicts with this document, this document wins.

## Source

- Supplied by Nic in prior Codex conversation context during the betting module setup
- Confirmed against the current local betting files on `2026-07-02`
- Distilled here without adding new betting rules

## Guideline

### Context

- Nic uses sports betting mainly for soccer.
- Nic prefers reasoned picks over gut bets.

### First-Half Goal Model

- Estimate first-half goal probability using both teams' first-half goals scored and conceded.
- Use home and away splits where possible.
- Combine those inputs into expected goals and convert that into probability.

### Second-Half Model

- Use second-half goals scored and conceded.
- This can be triggered by the prefix `2h:`.

### Cup-Game Rule

- Only apply a cup or single-leg boost when Nic explicitly says the fixture is a cup.
- Otherwise use the league model by default.

### Betting Decision Model

- Compare estimated probability against implied odds.
- Require at least `+3%` edge.
- Use medium-risk staking: `0.5x Kelly`.

### Ledger Rule

- Only log a bet when Nic writes the bet in the exact format ending with `- bet!`
- Do not log casual discussion as a bet.
