# Troubleshooting

## Installer cannot verify the repository

Stop installation and confirm that the source repository is:

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/lawtasksai
```

## Browser login times out

Run the installer again, or use the license-key fallback when prompted.

## Tools do not appear

Run the doctor check with the client selected during installation:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install lawtasksai doctor --client claude-desktop'
```

Supported values are `claude-desktop`, `cursor`, `windsurf`, `codex`, `gemini`,
and `antigravity`. Restart Claude Desktop, Cursor, Windsurf, Codex, or Gemini CLI
after the check passes. For Google Antigravity, fully quit and reopen the app.
These applications normally load MCP configuration at startup.

## No credits available

Visit:

```text
https://lawtasksai.com/#pricing
```

## Google Gemini clients

Use `antigravity` for the Google Antigravity desktop app or terminal client with a personal Google account. Use `gemini` only for the legacy Gemini CLI when an API-key or enterprise configuration still supports it. After installation, restart the selected client. For the Google Antigravity desktop app, fully quit and reopen the app; closing only the window can leave it running without loading the new TasksAI tools.
