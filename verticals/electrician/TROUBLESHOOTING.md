# ElectricianTasksAI Troubleshooting

The official source is https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/electrician.

Node.js and npm are required. Use the exact manifest-declared source and package. Stop if the product, domain, repository, branch, path, or package differs.

If browser connection expires, rerun the installer and use https://electriciantasksai.com/connect. Manual license-key entry is only a fallback and credentials must not be pasted into chat.

Run doctor with the same client used for installation:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install electrician doctor --client claude-desktop'
```

Supported clients are `claude-desktop`, `cursor`, `windsurf`, `codex`, `gemini`, and `antigravity`. Restart the selected client after doctor passes. Contact hello@electriciantasksai.com without sending task records or generated files.

## Google Gemini clients

Use `antigravity` for the Google Antigravity desktop app or terminal client with a personal Google account. Use `gemini` only for the legacy Gemini CLI when an API-key or enterprise configuration still supports it. After installation, restart the selected client. For the Google Antigravity desktop app, fully quit and reopen the app; closing only the window can leave it running without loading the new TasksAI tools.
