# NicOS Sync Protocol

This document defines the standard `Sync to NicOS` workflow.

## Core Principles

1. Chats are for thinking.
2. NicOS stores distilled knowledge, not full transcripts.

The purpose of a sync is to convert useful conversation output into clean, structured knowledge that improves the system over time.

## Canonical Workspace Identities

The official Bobby workspace names are locked.

- `🏠 Bobby | HQ`
- `📈 Bobby | Investments`
- `🍣 Bobby | Kitchen`
- `🌱 Bobby | Reflection`
- `⚽ Bobby | Betting`

These titles, emojis, capitalization, spacing, and wording must not change without Nic's explicit approval.

`⚽ Bobby | Betting` is recorded only as a canonical external workspace title.

It remains outside NicOS and must not sync into the repository.

## What Every Sync Must Identify

Every sync should identify:

- Source workspace
- Date
- Module affected
- Project affected, if any
- Key decisions
- Lessons learned
- Rules added or changed
- Files to update
- Whether action is required

## Standard Format: `NICOS_SYNC_V1`

Use this Markdown/YAML-style structure when turning a conversation into a NicOS update.

```yaml
# NICOS_SYNC_V1
source_workspace: ""
date: ""
sync_type: "single_session"
# Optional when sync_type is "catch_up"
since_last_successful_sync: ""
scope: ""
module_affected:
  - ""
project_affected:
  - ""
key_decisions:
  - ""
lessons_learned:
  - ""
rules_added_or_changed:
  - ""
files_to_update:
  - ""
action_required: yes
action_summary:
  - ""
```

## How To Use The Format

### 1. Start with the source

Record where the thinking happened.

Examples:

- `📈 Bobby | Investments`
- `🍣 Bobby | Kitchen`
- `🌱 Bobby | Reflection`
- `🏠 Bobby | HQ`

### 2. Identify the module

Decide which permanent knowledge domain should receive the update.

Examples:

- `Trading`
- `Investing`
- `Restaurant`
- `Reflection`
- `Business`
- `Learning`

### 3. Identify the project if relevant

If the conversation belongs to an active initiative, name the related project.

If no project applies, leave it empty.

### 4. Distill the conversation

Do not paste full chat transcripts into NicOS.

Instead, extract:

- decisions
- lessons
- rules
- required file updates

### 5. Decide whether action is required

Use `action_required: yes` if something in NicOS should change.

Use `action_required: no` if the conversation was useful but does not yet require a system update.

## Sync Rules

### Distillation rule

NicOS should store distilled knowledge, not raw conversational volume.

### Session-closing rule

Meaningful sessions should be deliberately closed before they are synced.

Use `Close session and prepare NicOS sync.` when the conversation produced durable knowledge that should later be distilled into NicOS.

Use `Close without syncing` when the conversation should end cleanly without repository changes.

### Sync-selection rule

Casual conversation, emotional support, brainstorming, and repeated information should not be synced automatically.

NicOS should only store durable knowledge that improves future decision-making.

### Catch-up sync rule

A catch-up sync may cover multiple meaningful conversations since the previous successful sync.

It should exclude duplicates, repeated material, and raw transcript content.

### Health-check rule

NicOS should use weekly or periodic health checks instead of requiring a full repository audit after every individual sync.

Dashboards and status files should be refreshed when the real state changes, not as ceremony.

### Module boundary rule

Knowledge should go into the right permanent module.

Examples:

- trading ideas -> `modules/trading/`
- investing notes -> `modules/investing/`
- kitchen or restaurant insights -> `modules/restaurant/`
- self-review insights -> `modules/reflection/`

### Investments workspace boundary rule

`📈 Bobby | Investments` is for education, research, chart analysis, investing principles, and risk-management learning only.

Actual trades, positions, entries, exits, quantities, average prices, and P&L are managed separately in Nic's dedicated Codex trading room and must not be stored in NicOS from this workspace unless Nic explicitly requests it.

When syncing from `📈 Bobby | Investments`, keep updates limited to research, chart-learning, paper-trade review, watchlist planning, and durable rules.

### Single-source-of-truth rule

Each durable topic should have one canonical source of truth.

When the same topic touches multiple modules, one file should own the live record and other modules should reference it instead of maintaining conflicting duplicates.

### Boundary rule

Content from `⚽ Bobby | Betting` must not be written into NicOS unless Nic later explicitly reverses this decision.

The separate `⚽ Bobby | Betting` conversation may continue outside NicOS, but it must not sync into the repository.

### Workspace-lock rule

Renaming a canonical Bobby workspace requires explicit approval from Nic.

### Project boundary rule

Projects are temporary workspaces.

If the conversation belongs to a project, update the relevant project file first.

If the conversation creates long-term knowledge, also distill the lasting lesson into the right module.

### Execution logging rule

Execution logs should only contain real actions.

#### Trading

Only add a row to `modules/trading/journal/trades.csv` if Nic explicitly says the trade was taken.

If execution is unclear, do not log it.

## Example: Trading Sync

```yaml
# NICOS_SYNC_V1
source_workspace: "📈 Bobby | Investments"
date: "2026-07-02"
sync_type: "single_session"
module_affected:
  - "Trading"
project_affected:
  - "Trading Improvement 2026"
key_decisions:
  - "WOLF remains a watch, not an automatic entry."
  - "Wait for bullish confirmation near support."
lessons_learned:
  - "Planning a trade is not the same as taking a trade."
rules_added_or_changed:
  - "Do not log a trade or store live execution details from this workspace unless Nic explicitly asks for it."
files_to_update:
  - "modules/trading/context/latest_chat_sync.md"
  - "modules/trading/watchlist/WOLF.md"
  - "modules/trading/lessons/lessons_learned.md"
action_required: yes
action_summary:
  - "Refresh the WOLF watchlist."
  - "Update the latest trading sync."
  - "Do not touch the trade journal or store live execution details from this workspace."
```

## Example: Kitchen Sync

```yaml
# NICOS_SYNC_V1
source_workspace: "🍣 Bobby | Kitchen"
date: "2026-07-02"
sync_type: "single_session"
module_affected:
  - "Restaurant"
project_affected:
  - "Japanese Restaurant Development"
key_decisions:
  - "Concept clarity matters before expanding menu ideas."
lessons_learned:
  - "Operational unknowns should be written down early."
rules_added_or_changed:
  - "Separate brainstorming from actual business decisions."
files_to_update:
  - "projects/active/japanese-restaurant-development/README.md"
  - "modules/restaurant/README.md"
action_required: yes
action_summary:
  - "Update the restaurant development project."
  - "Capture any durable concept lesson in the restaurant module."
```

## Example: Reflection Sync

```yaml
# NICOS_SYNC_V1
source_workspace: "🌱 Bobby | Reflection"
date: "2026-07-02"
sync_type: "single_session"
module_affected:
  - "Reflection"
project_affected:
  - ""
key_decisions:
  - "Decision quality matters more than weekly activity."
lessons_learned:
  - "A skipped action can be a disciplined win."
rules_added_or_changed:
  - "Do not add complexity that does not improve judgment."
files_to_update:
  - "modules/reflection/README.md"
  - "system/principles.md"
action_required: yes
action_summary:
  - "Preserve the reflection lesson in the permanent module."
  - "Update system principles only if the lesson affects NicOS broadly."
```

## Final Rule

If there is doubt about whether something belongs in NicOS, prefer a smaller distilled update over a larger raw dump.
