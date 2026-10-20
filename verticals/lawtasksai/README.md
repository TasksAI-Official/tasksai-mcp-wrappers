# LawTasksAI Install Manifest

This folder contains the public install manifest and product metadata for LawTasksAI.

LawTasksAI adds legal-administration, drafting-support, and law-office workflow materials to MCP-capable AI applications.

## Terminal install

```bash
npm exec --package=@tasksai/install --call 'tasksai-install lawtasksai --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/lawtasksai --client claude-desktop'
```

Supported client values are `claude-desktop`, `cursor`, `windsurf`, `codex`,
and `gemini`. Gemini users must also install Gemini CLI and sign in with their
chosen Google account. After installation, run:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install lawtasksai doctor --client claude-desktop'
```

## Source

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/lawtasksai
```

## Website

https://lawtasksai.com

## Privacy

LawTasksAI servers handle authentication, credits, catalog/search metadata, and licensed skill delivery. LawTasksAI does not process the user's task content or generated output files. The user's chosen AI assistant or LLM performs the task work according to that provider's privacy terms, and saved files are created locally by the MCP runtime.

## Support

support@lawtasksai.com

