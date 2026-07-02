# Latest Betting Sync

## Sync Status

- Sync date: `2026-07-02`
- Status: starter module context

## Current Operating Context

- Nic uses sports betting mainly for soccer.
- Nic prefers reasoned picks over gut bets.
- Betting should stay separate from trading.

## Model Summary

### First-half goal model

- Estimate first-half goal probability using both teams' first-half goals scored and conceded.
- Use home and away splits where possible.
- Combine those inputs into expected first-half goals.
- Convert expected goals into a probability.

### Second-half model

- Use second-half goals scored and conceded.
- This can be triggered by the prefix `2h:`.

## Betting Decision Rules

- Compare estimated probability against implied odds.
- Require at least `+3%` edge.
- Use medium-risk staking: `0.5x Kelly`.

## Cup-Game Rule

- Only apply a cup or single-leg boost when Nic explicitly says the fixture is a cup.
- Otherwise use the league model by default.

## Ledger Rule

- Only log a bet when Nic writes the bet in the exact format ending with `- bet!`
- Do not log casual discussion as a bet.

## Next Useful Actions

- Keep model notes simple and reviewable.
- Track only real bets in the ledger.
- Review whether the model edge and actual discipline match.
