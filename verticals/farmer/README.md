# FarmerTasksAI Install Manifest

FarmerTasksAI turns farm notes into structured crop records, equipment logs,
checklists, and draft applications inside supported MCP clients. It is a
document and workflow assistant, not a farm-management, accounting, sensor, or
regulatory-submission system.

## Official source

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/farmer
```

Official website: https://farmertasksai.com

The official product ID is `farmer`, the MCP tool prefix is `farmertasksai`,
and the installer package is `@tasksai/install`.

## AI-assistant install prompt

Copy this prompt into Claude Desktop, Cursor, Windsurf, or Codex:

> Set up FarmerTasksAI from the official source at
> https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/farmer.
> Verify that `agent-install.json` identifies product `farmer`, domain
> `farmertasksai.com`, repository `TasksAI-Official/tasksai-mcp-wrappers`, and
> package `@tasksai/install`. Ask which supported MCP client to configure if it
> is not clear. Run only the manifest-declared installer command, use browser
> account connection when available, run doctor for the same client, and tell
> me when to restart the client. After setup, help me create the first-file
> example declared in the manifest.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install farmer --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/farmer --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` when installing
for a different supported client. Node.js and npm are required.

## Verify the installation

The installer runs doctor after writing the selected client configuration. It
can also be rerun explicitly for the same client:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install farmer doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client,
start a new conversation if needed, and try:

> Help me create a crop production record from my notes. Ask me for the crop,
> field, acreage, planting date, variety, inputs, and observations, then
> organize the result as a table and save it as a local Word document.

Finished files are saved locally under `~/Documents/TasksAI/FarmerTasksAI/`
unless `TASKSAI_OUTPUT_DIR` is configured.

## Supported clients

- Claude Desktop (`claude-desktop`)
- Cursor (`cursor`)
- Windsurf (`windsurf`)
- Codex (`codex`)

## Privacy boundary

FarmerTasksAI receives authentication, account and credit state, catalog
metadata, licensed workflow delivery requests, and content-free activation
events. It does not receive farm notes, field or livestock records, prompt
text, generated drafts, or local file paths.

The selected AI assistant or LLM performs the task under that provider's
privacy terms. A cloud AI provider may process information supplied to it. The
local MCP runtime saves finished documents on the user's machine.

FarmerTasksAI creates structured drafts. Review official forms, dates, figures,
program requirements, and compliance records before relying on or submitting
them.

## Support

Use https://farmertasksai.com/support or email hello@farmertasksai.com.
