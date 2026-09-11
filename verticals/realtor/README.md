# RealtorTasksAI Install Manifest

RealtorTasksAI adds purpose-built listing, buyer follow-up, seller-update, and
transaction-administration workflows to supported MCP clients. It is an add-on
for an AI assistant, not a CRM, MLS, or transaction-management system.

## Official source

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/realtor
```

Official website: https://realtortasksai.com

The official product ID is `realtor`, the MCP tool prefix is
`realtortasksai`, and the installer package is `@tasksai/install`.

## AI-assistant install prompt

Copy this prompt into Claude Desktop, Cursor, Windsurf, or Codex:

> Set up RealtorTasksAI from the official source at
> https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/realtor.
> Verify that `agent-install.json` identifies product `realtor`, domain
> `realtortasksai.com`, repository `TasksAI-Official/tasksai-mcp-wrappers`, and
> package `@tasksai/install`. Ask which supported MCP client to configure if it
> is not clear. Run only the manifest-declared installer command, use browser
> account connection when available, run doctor for the same client, and tell
> me when to restart the client. After setup, help me create the first-file
> example declared in the manifest.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install@0.1.40 --call 'tasksai-install realtor --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/realtor --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` when installing
for a different supported client. Node.js and npm are required.

## Verify the installation

The installer runs doctor after writing the selected client configuration. It
can also be rerun explicitly for the same client:

```bash
npm exec --package=@tasksai/install@0.1.40 --call 'tasksai-install realtor doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client,
start a new conversation if needed, and try:

> Help me create an open-house buyer follow-up email from my showing notes. Ask
> me for the property, the buyer's stated priorities, and the next step, then
> save the finished draft as a local Word document.

Finished files are saved locally under
`~/Documents/TasksAI/RealtorTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Supported clients

- Claude Desktop (`claude-desktop`)
- Cursor (`cursor`)
- Windsurf (`windsurf`)
- Codex (`codex`)

## Privacy boundary

RealtorTasksAI receives authentication, account and credit state, catalog
metadata, licensed workflow delivery requests, and content-free activation
events. It does not receive listing details, addresses, client names, showing
notes, prompt text, generated drafts, or local file paths.

The selected AI assistant or LLM performs the task under that provider's
privacy terms. A cloud AI provider may process information supplied to it. The
local MCP runtime saves finished documents on the user's machine.

## Support

Use https://realtortasksai.com/support or email hello@realtortasksai.com.
