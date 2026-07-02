# Latest Betting Sync

This is the latest working betting summary.

Source of truth: `betting_guideline.md`

If this file conflicts with the guideline, the guideline wins.

## Sync Status

- Sync date: `2026-07-02`
- Status: betting guideline confirmed

## Current Operating Context

- Main sport: soccer
- Decision style: reasoned picks over gut bets
- Betting should stay separate from trading.

## Confirmed Guideline Summary

### First-half goal model

- Estimate first-half goal probability using both teams' first-half goals scored and conceded.
- Use home and away splits where possible.
- Combine those inputs into expected first-half goals.
- Convert expected goals into a probability.

### Second-half model

- Use second-half goals scored and conceded.
- This can be triggered by the prefix `2h:`.

### Betting decision model

- Compare estimated probability against implied odds.
- Require at least `+3%` edge.
- Use medium-risk staking: `0.5x Kelly`.

### Cup-game rule

- Only apply a cup or single-leg boost when Nic explicitly says the fixture is a cup.
- Otherwise use the league model by default.

### Ledger rule

- Only log a bet when Nic writes the bet in the exact format ending with `- bet!`
- Do not log casual discussion as a bet.

## Next Useful Actions

- Use `betting_guideline.md` as the source of truth during future betting syncs.
- Keep betting templates aligned with the confirmed guideline.
- Only update `ledger/bets.csv` when the confirmed logging rule is satisfied.
