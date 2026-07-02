# First-Half Goals Model

## Purpose

Estimate the probability of a first-half goals market using simple team scoring and conceding data.

## Main Inputs

For each team, use:

- first-half goals scored
- first-half goals conceded
- home and away splits where possible

## Simple Process

1. Estimate the home team's first-half attacking output using:
   - home team first-half goals scored at home
   - away team first-half goals conceded away
2. Estimate the away team's first-half attacking output using:
   - away team first-half goals scored away
   - home team first-half goals conceded at home
3. Combine those two estimates into expected first-half goals for the match.
4. Convert expected goals into a probability for the market you care about.

## Practical Estimating Shortcut

One simple way to estimate expected first-half goals:

- Home FH expected goals = average of:
  - home team's FH goals scored at home
  - away team's FH goals conceded away
- Away FH expected goals = average of:
  - away team's FH goals scored away
  - home team's FH goals conceded at home
- Total FH expected goals = home FH expected goals + away FH expected goals

## Converting To Probability

Once total expected first-half goals is estimated, convert it into a market probability.

Examples:

- Over `0.5` first-half goals
- Over `1.5` first-half goals

If a calculator or script is available, use a Poisson-style conversion. If not, keep the estimate simple and note the assumptions.

## Guardrails

- Prefer relevant home and away splits over raw season totals.
- If the data is thin or messy, reduce confidence.
- Do not force a bet just because the model produces a number.

## Reminder

The model is a decision aid, not a certainty machine.
