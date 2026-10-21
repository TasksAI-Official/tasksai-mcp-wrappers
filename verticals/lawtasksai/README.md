# LawTasksAI Install Manifest

This folder contains the public install manifest and product metadata for LawTasksAI.

LawTasksAI adds legal-administration, drafting-support, and law-office workflow materials to MCP-capable AI applications.

## Terminal install

```bash
npm exec --package=@tasksai/install --call 'tasksai-install lawtasksai --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/lawtasksai --client claude-desktop'
```

Supported client values are `claude-desktop`, `cursor`, `windsurf`, `codex`,
`gemini`, and `antigravity`. For personal Google accounts, install Google Antigravity CLI; use `gemini` only for a supported legacy account or API configuration. After installation, run:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install lawtasksai doctor --client claude-desktop'
```

## Source

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/lawtasksai
```

## Website

https://lawtasksai.com

## Google Gemini clients

Use `antigravity` for Google Antigravity CLI with a personal Google account. Use `gemini` only for the legacy Gemini CLI when an API-key or enterprise configuration still supports it. Antigravity uses `~/.gemini/config/mcp_config.json`; the legacy client uses `~/.gemini/settings.json`. Restart the selected client after installation.

## Privacy

LawTasksAI servers handle authentication, credits, catalog/search metadata, and licensed skill delivery. LawTasksAI does not process the user's task content or generated output files. The user's chosen AI assistant or LLM performs the task work according to that provider's privacy terms, and saved files are created locally by the MCP runtime.

## Support

support@lawtasksai.com

