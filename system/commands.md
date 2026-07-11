# NicOS Command Language

These are the standard natural-language commands Nic can use with Codex inside NicOS.

Commands should keep the system predictable, practical, and distilled.

## Canonical Workspaces

- `🏠 Bobby | HQ`
- `📈 Bobby | Investments`
- `🍣 Bobby | Kitchen`
- `🌱 Bobby | Reflection`
- `⚽ Bobby | Betting`

These titles, emojis, capitalization, spacing, and wording are locked.

Do not rename a canonical Bobby workspace without Nic's explicit approval.

## `Sync to NicOS`

What it does:

- Distills a meaningful closed session into clean NicOS updates using `NICOS_SYNC_V1`
- Updates modules and projects without pasting raw transcripts
- Preserves the difference between durable knowledge and casual conversation

Files it may update:

- `projects/active/*/README.md`
- `modules/*/context/*.md`
- `modules/*/watchlist/*.md`
- `modules/*/rules/*.md`
- `modules/*/lessons/*.md`
- `modules/trading/journal/trades.csv` only if Nic explicitly says the trade was taken

Boundary:

- Content from `⚽ Bobby | Betting` must not be written into NicOS unless Nic later explicitly reverses this decision

## `Catch Up Sync`

What it does:

- Distills multiple meaningful conversations since the last successful sync
- Excludes duplicates, repeated material, and raw transcript content
- Applies only the durable updates that change NicOS in a useful way

Files it may update:

- `projects/active/*/README.md`
- `modules/*/context/*.md`
- `modules/*/watchlist/*.md`
- `modules/*/rules/*.md`
- `modules/*/lessons/*.md`
- `modules/*/reports/*.md`
- `modules/trading/journal/trades.csv` only if Nic explicitly says the trade was taken
- `DASHBOARD.md`, `projects/dashboard.md`, and `projects/project_index.md` only if the real system state changed

## `Close session and prepare NicOS sync`

What it does:

- Ends a meaningful session deliberately instead of leaving it half-open
- Prepares a clean distilled sync summary for a later `Sync to NicOS` or `Catch Up Sync`
- Keeps the repository unchanged until Nic chooses to apply the sync

Files it may update:

- None by default

## `Close without syncing`

What it does:

- Ends a session cleanly without creating repository changes
- Keeps casual conversation, emotional support, brainstorming, and repeated material out of NicOS when they do not create durable knowledge

Files it may update:

- None

## `NicOS Status`

What it does:

- Summarizes the current state of the whole system across system files, modules, and projects

Files it may update:

- None by default
- `DASHBOARD.md`, `projects/dashboard.md`, and `projects/project_index.md` if a status refresh is explicitly requested

## `Project Status`

What it does:

- Reports the status of one project or all active projects
- Highlights progress, open questions, risks, and next actions

Files it may update:

- `projects/active/*/README.md`
- `projects/dashboard.md`
- `projects/project_index.md`

## `Weekly Review`

What it does:

- Distills the most important weekly lessons, decisions, mistakes, and next steps

Files it may update:

- `projects/active/*/README.md`
- `modules/*/lessons/*.md`
- `modules/*/reports/*.md`
- `DASHBOARD.md` if the current focus changes

## `Monthly Review`

What it does:

- Creates a higher-level review of patterns, performance, and improvement areas across the month

Files it may update:

- `projects/active/*/README.md`
- `modules/*/reports/*.md`
- `modules/*/lessons/*.md`
- `DASHBOARD.md` if priorities change

## `Trading Status`

What it does:

- Summarizes the state of the trading module, including context, watchlist, rules, and journal discipline

Files it may update:

- None by default
- `modules/trading/context/latest_chat_sync.md`
- `modules/trading/watchlist/*.md`
- `modules/trading/lessons/*.md`
- `modules/trading/journal/trades.csv` only if Nic explicitly says the trade was taken

## `Kitchen Status`

What it does:

- Summarizes the state of restaurant and kitchen knowledge, decisions, and active experiments

Files it may update:

- None by default
- `modules/restaurant/*.md`
- `modules/restaurant/templates/*.md`
- `projects/active/japanese-restaurant-development/README.md`

## `Reflection Review`

What it does:

- Distills personal lessons, repeated patterns, and decision-quality insights into the reflection module

Files it may update:

- `modules/reflection/*.md`
- `modules/reflection/templates/*.md`
- `system/principles.md` only if the lesson changes NicOS broadly

## `Search NicOS`

What it does:

- Searches NicOS for a topic, file, lesson, rule, project, or prior decision

Files it may update:

- None

## `Show Recent Changes`

What it does:

- Shows recent repository changes, latest commits, and important modified files

Files it may update:

- None

## `NicOS Health Check`

What it does:

- Runs a periodic consistency review instead of requiring a full repository audit after every sync
- Checks dashboards, active projects, canonical source files, and stale duplication risks
- Refreshes status files only where the real system state has changed

Files it may update:

- `DASHBOARD.md`
- `projects/dashboard.md`
- `projects/project_index.md`
- `projects/active/*/README.md`
- `system/*.md` if a workflow rule has genuinely changed

## `Rebuild Dashboard`

What it does:

- Refreshes the top-level and project dashboards so they reflect the current real state of NicOS

Files it may update:

- `DASHBOARD.md`
- `projects/dashboard.md`
- `projects/project_index.md`
