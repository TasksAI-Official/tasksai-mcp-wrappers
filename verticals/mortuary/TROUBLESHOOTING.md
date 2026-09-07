# MortuaryTasksAI Troubleshooting

The official source is https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/mortuary.

Node.js and npm are required. Use the exact manifest-declared source and package. Stop if the product, domain, repository, branch, path, or package differs.

If browser connection expires, rerun the installer and use https://mortuarytasksai.com/connect. Manual license-key entry is only a fallback and credentials must not be pasted into chat.

Run doctor with the same client used for installation:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install mortuary doctor --client claude-desktop'
```

Supported clients are `claude-desktop`, `cursor`, `windsurf`, and `codex`. Restart the selected client after doctor passes. Contact hello@mortuarytasksai.com without sending task records or generated files.
