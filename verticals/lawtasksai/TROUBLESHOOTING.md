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

Supported values are `claude-desktop`, `cursor`, `windsurf`, `codex`, and
`gemini`. Restart Claude Desktop, Cursor, Windsurf, Codex, or Gemini CLI after
the check passes because these applications normally load MCP configuration at
startup.

## No credits available

Visit:

```text
https://lawtasksai.com/#pricing
```

## Google Gemini clients

Use `antigravity` for Google Antigravity CLI with a personal Google account. Use `gemini` only for the legacy Gemini CLI when an API-key or enterprise configuration still supports it. Restart the selected client after installation.
