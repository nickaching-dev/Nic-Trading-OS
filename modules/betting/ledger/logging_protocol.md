# Betting Ledger Logging Protocol

## Core Rule

Only log a bet when Nic writes the bet in the exact format ending with `- bet!`

## What Counts As A Real Bet

Examples:

- `2026-07-02 | soccer | Team A vs Team B | FH over 0.5 | 1.72 | est 63% | 0.6u - bet!`
- `2h: Team C vs Team D | over 1.0 second half | 1.95 | est 56% | 0.5u - bet!`

## What Does Not Count

- `I like this`
- `maybe over 0.5 FH`
- `this looks bettable`
- `what do you think?`
- any note that does not end with `- bet!`

## Logging Discipline

- If the format is not explicit, do not log the bet.
- If the stake is unclear, do not guess.
- If the market is unclear, do not invent details.

## Final Rule

If there is doubt, leave `bets.csv` unchanged.
