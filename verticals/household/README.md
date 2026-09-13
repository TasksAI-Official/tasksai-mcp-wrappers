# HouseholdTasksAI Install Manifest

Status: pre-launch. This metadata is prepared for integration testing; public signup and skill release are pending.

HouseholdTasksAI prepares household schedules, bill calendars, repair-estimate comparisons, insurance-quote comparisons, and medical-appointment notes. The initial catalog contains five draft workflows. It does not diagnose, decide insurance coverage, pay bills, or book services.

## Official source

https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/household

Website: https://householdtasksai.com

Product ID: `household`. Tool prefix: `householdtasksai`. Installer: `@tasksai/install`.

## Install after release

```bash
npm exec --package=@tasksai/install --call 'tasksai-install household --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/household --client claude-desktop'
```

Supported clients: Claude Desktop, Cursor, Windsurf, and Codex. Client values: `claude-desktop`, `cursor`, `windsurf`, `codex`. Select the intended client, use browser account connection, run doctor for the same client, and restart that client.

```bash
npm exec --package=@tasksai/install --call 'tasksai-install household doctor --client claude-desktop'
```

## First document

Help me make a weekly household schedule. Ask for the week, time zone, commitments, travel time, and responsibilities. Flag conflicts and missing information, then save the schedule as a local Word document.

## Privacy and support

HouseholdTasksAI servers handle authentication, account and credit state, catalog metadata, licensed workflow delivery, and content-free activation events. HouseholdTasksAI does not receive household notes, health records, prompt text, generated drafts, or local file paths. The user's chosen AI assistant processes supplied information under its own privacy terms. Finished files are saved locally.

Review outputs before use. For support, contact hello@householdtasksai.com.

## Infrastructure release

The shared installer support is published as `@tasksai/install@0.1.44` (npm tag `household`). This manifest pins that version. The public website is coming soon and the backend remains inactive: customer signup, checkout, and new connections are disabled. Publishing the infrastructure does not publish any skills or enable customer access.
