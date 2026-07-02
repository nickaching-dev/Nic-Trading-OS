# Betting Decision Model

## Purpose

Decide whether a bet is worth taking based on estimated probability, market odds, and edge.

## Step 1. Estimate Probability

Use the relevant model to estimate the real probability of the outcome.

## Step 2. Convert Odds To Implied Probability

Use:

`implied probability = 1 / decimal odds`

Example:

- Odds: `2.00`
- Implied probability: `50%`

## Step 3. Calculate Edge

Use:

`edge = estimated probability - implied probability`

Example:

- Estimated probability: `56%`
- Implied probability: `50%`
- Edge: `+6%`

## Step 4. Apply The Threshold

- Require at least `+3%` edge
- If the edge is below `+3%`, skip the bet

## Step 5. Apply Staking

Use medium-risk staking:

- `0.5x Kelly`

If confidence is lower than usual because of weak data, reduce stake or skip the bet.

## Cup-Game Rule

- Only apply a cup or single-leg boost if Nic explicitly says the fixture is a cup
- Otherwise use the league model by default

## Final Check

If the reasoning is weak, the edge is thin, or the data is messy, no bet is a valid decision.
