# NicOS Sync Protocol

Use this protocol when Nic gives a ChatGPT summary, a conversation recap, or new operating context that should update the repository.

## Purpose

Turn conversations into clean NicOS updates without confusing:

- discussion with execution
- one module with another
- projects with permanent knowledge
- new ideas with proven rules

## Step 1. Classify the update

Decide whether the summary belongs to:

- `modules/trading/`
- `modules/betting/`
- another module
- a project in `projects/active/`, `projects/completed/`, or `projects/archived/`
- the whole system

If a summary touches more than one domain, split the update instead of mixing everything together.

## Step 2. Update the right context file

Use the relevant context file first.

- Trading: `modules/trading/context/latest_chat_sync.md`
- Betting: `modules/betting/context/latest_betting_sync.md`
- Projects: the relevant project file inside `projects/`

If the summary changes the overall philosophy of the system, update:

- `README.md`
- `VISION.md`
- `system/principles.md`
- `system/project_lifecycle.md` when lifecycle rules change

## Step 3. Update the right operating documents

Examples:

- new trade setup -> trading watchlist
- repeated trading mistake -> trading rules or lessons
- new betting model detail -> betting models
- new betting discipline lesson -> betting rules or lessons
- active initiative update -> project file in `projects/active/`
- finished initiative takeaway -> project lessons plus the right permanent module

## Step 4. Keep execution logs strict

Execution logs should only contain real actions.

### Trading logging rule

Only add a row to `modules/trading/journal/trades.csv` if Nic explicitly says the trade was taken.

Do not log:

- watchlist ideas
- hypothetical entries
- planning notes
- unconfirmed trades

### Betting logging rule

Only add a row to `modules/betting/ledger/bets.csv` if Nic writes the bet in the exact format ending with `- bet!`

Do not log:

- casual discussion
- possible bets
- opinion-only chat
- model experiments without an actual bet

## Step 5. Update lessons only when they are useful

Lessons should capture:

- repeated mistakes
- repeated strengths
- clarified rules
- practical insights worth reusing

Keep them short, specific, and actionable.

## Step 6. Distill project knowledge back into modules

Projects are temporary workspaces.

Modules are the permanent knowledge layer.

When a project generates durable insight:

- move the lasting lesson into the right module
- keep the project focused on execution and context
- do not let project folders become permanent knowledge dumps

## Step 7. Preserve boundaries

- Trading logic stays in the trading module.
- Betting logic stays in the betting module.
- Investing content stays separate from trading.
- Project execution notes stay inside projects until they are distilled.

If a note belongs in a different module, move it there rather than forcing it into the wrong one.

## Final Rule

If there is doubt about whether an action really happened, treat it as not executed and do not log it.
