# Betting Module

This is the betting module inside NicOS.

Its purpose is to help Nic bet more rationally, track results honestly, and separate real edge from casual opinion.

## Scope

- Main sport: soccer
- Decision style: reasoned picks over gut bets
- Focus: model logic, edge, staking, discipline, and review

## Core rules

- Compare estimated probability against implied odds
- Require at least `+3%` edge
- Use medium-risk staking: `0.5x Kelly`
- Only apply a cup or single-leg boost when Nic explicitly says the fixture is a cup
- Only log a bet when Nic writes it in the exact format ending with `- bet!`

## Structure

- `context/`
- `models/`
- `ledger/`
- `rules/`
- `lessons/`
- `prompts/`
- `reports/`
- `templates/`

## Important separation

This module is separate from trading.

- Betting logic should not be stored in the trading module.
- Betting results should not be mixed into trading journals.
