# RealtorTasksAI Troubleshooting

## The installer cannot verify the source

Stop installation. The official source must be exactly:

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/realtor
```

The manifest must identify product `realtor`, domain `realtortasksai.com`, and
package `@tasksai/install`. Do not approve a substituted repository, package,
domain, or arbitrary command.

## Node.js or npm is missing

Install the current Node.js LTS release from https://nodejs.org/. npm is
included. Then rerun the official install prompt or command from `README.md`.

## Browser account connection does not finish

Confirm the browser is on `https://realtortasksai.com/connect` and that the
displayed code matches the installer. Rerun the installer if the code expires.
Use manual license-key entry only when the official installer offers it as the
fallback; do not paste a license key into chat or MCP client configuration.

## Doctor reports a missing client configuration

Run doctor with the same client selected during installation. For example:

```bash
npm exec --package=@tasksai/install@0.1.41 --call 'tasksai-install realtor doctor --client claude-desktop'
```

Supported client values are `claude-desktop`, `cursor`, `windsurf`, and
`codex`. A passing check prints `TasksAI doctor passed.`

## The installer cannot write a required path

Allow the selected AI assistant or Terminal to write the product install
directory and that client's MCP configuration path declared in
`agent-install.json`. In a restricted environment, `--install-dir` or
`TASKSAI_INSTALL_DIR` may point to an exact alternate RealtorTasksAI install
directory, but the selected client configuration must still be writable.

## Tools do not appear after doctor passes

Restart Claude Desktop, Cursor, Windsurf, or Codex after installation. Start a
new conversation or reload the workspace if the client caches MCP tools. Then
ask: `Check my RealtorTasksAI credit balance.`

## A finished file is not visible

Ask the assistant to use `realtortasksai_save_document`. By default, files are
saved under `~/Documents/TasksAI/RealtorTasksAI/`. If
`TASKSAI_OUTPUT_DIR` is set, check that configured folder. Local output does not
appear on the RealtorTasksAI website.

## No credits are available

Visit https://realtortasksai.com/#pricing. If the balance appears incorrect,
contact hello@realtortasksai.com without sending listing, client, or transaction
content.
