# Second-Half Goals Model

## Purpose

Estimate second-half goal probability using second-half scoring and conceding tendencies.

## Trigger

Use this model when Nic explicitly wants the second-half version or uses the prefix `2h:`.

## Main Inputs

For each team, use:

- second-half goals scored
- second-half goals conceded
- home and away splits where possible

## Simple Process

1. Estimate the home team's second-half output using:
   - home team's second-half goals scored at home
   - away team's second-half goals conceded away
2. Estimate the away team's second-half output using:
   - away team's second-half goals scored away
   - home team's second-half goals conceded at home
3. Combine both into total expected second-half goals.
4. Convert that expectation into probability for the relevant second-half market.

## Guardrails

- Do not use this model unless second-half data is the intended lens.
- Keep the market label clear so first-half and second-half logic are not mixed.
- If splits are missing, note the lower confidence level.

## Reminder

The purpose is structured estimation, not forced action.
