# Sync To Trading Module

Use this workflow when Nic gives a ChatGPT conversation summary and wants the repository updated.

## Purpose

Turn a conversation summary into clean updates inside the NicOS trading module without mixing up:

- context
- watchlist ideas
- checklist rules
- lessons learned
- actual executed trades

## Files This Workflow Can Update

- `modules/trading/context/latest_chat_sync.md`
- `modules/trading/watchlist/[TICKER].md`
- `modules/trading/rules/swing_trade_checklist.md`
- `modules/trading/lessons/lessons_learned.md`
- `modules/trading/journal/trades.csv` only if an actual trade was taken

## Core Rule

Do not add trades to the journal unless Nic explicitly says the trade was taken.

If the summary only discusses:

- a plan
- a watchlist update
- a possible setup
- a hypothetical entry
- a trade idea

then do **not** add anything to `modules/trading/journal/trades.csv`.

## Step-By-Step Sync Flow

### 1. Read the summary and classify the information

Ask:

- Is this new operating context?
- Is this a watchlist update?
- Is this a new rule or checklist improvement?
- Is this a lesson learned?
- Was a real trade actually taken?

### 2. Update `modules/trading/context/latest_chat_sync.md`

Update this file when the summary changes:

- current focus
- current operating rules
- current chart interpretation
- current highlighted setups

Keep it concise and practical.

### 3. Update `modules/trading/watchlist/[TICKER].md`

If the summary includes a specific ticker:

- create `modules/trading/watchlist/[TICKER].md` if it does not exist
- update support, resistance, targets, invalidation, and setup notes
- keep the writeup practical and beginner-friendly
- separate `watch` ideas from `entered` trades

### 4. Update `modules/trading/rules/swing_trade_checklist.md`

Only update the checklist if the summary reveals a repeated process lesson such as:

- entering too early
- not waiting for confirmation
- unclear stop placement
- chasing price
- poor risk-to-reward discipline

Do not rewrite the whole checklist unless needed. Add or refine rules carefully.

### 5. Update `modules/trading/lessons/lessons_learned.md`

Add or revise lessons when the summary reveals:

- a mistake
- a pattern
- a rule Nic wants to reinforce
- a useful insight worth repeating

Keep lessons short and actionable.

### 6. Update `modules/trading/journal/trades.csv` only if the trade was actually taken

Only update `modules/trading/journal/trades.csv` if Nic explicitly confirms the trade happened.

Examples of valid confirmation:

- "I took the trade"
- "I entered WOLF"
- "I bought 50 shares"
- "This trade was executed"

Examples that are **not** enough:

- "I am watching this"
- "I might enter"
- "This looks good"
- "I planned this trade"
- "What do you think of this setup?"

If execution is unclear, do not log the trade.

## Output Discipline

When syncing:

- preserve the structure of the repo
- keep wording calm and simple
- do not invent fills, entries, exits, or results
- do not turn ideas into trade history
- prefer a missing journal row over a guessed journal row

## Quick Decision Rule

If there is any doubt about whether the trade happened, treat it as **not taken** and leave `modules/trading/journal/trades.csv` unchanged.
