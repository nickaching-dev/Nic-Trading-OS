# Betting Module

This is the betting module inside NicOS.

Its purpose is to help Nic bet more rationally, track results honestly, and separate real edge from casual opinion.

## Status

- Module status: active
- Source of truth: `context/betting_guideline.md`
- Latest working summary: `context/latest_betting_sync.md`

If any betting file conflicts with the betting guideline, the guideline wins.

## Scope

- Main sport: soccer
- Decision style: reasoned picks over gut bets
- Focus: model logic, edge, staking, discipline, and review

## Working Rule

Use `context/betting_guideline.md` for the current betting rules.

This keeps models, templates, and future syncs aligned with one confirmed source.

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
