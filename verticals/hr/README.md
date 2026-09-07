# HRTasksAI Install Manifest

HRTasksAI adds licensed administrative workflows for HR managers and human resources professionals to supported MCP-capable AI applications.

## Official source

https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/hr

Official website: https://hrtasksai.com

The official product ID is `hr`, the tool prefix is `hrtasksai`, and the installer package is `@tasksai/install`.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install hr --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/hr --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` for another supported client.

## Verify and start

```bash
npm exec --package=@tasksai/install --call 'tasksai-install hr doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client, then try:

> Help me write a job posting for an office manager. Ask for responsibilities, qualifications, schedule, location, compensation range, and application instructions, then save the finished posting as a local Word document.

Finished files are saved locally under `~/Documents/TasksAI/HRTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Privacy

HRTasksAI services handle authentication, account and credit state, catalog metadata, licensed workflow delivery, and content-free activation events. HRTasksAI does not receive applicant or employee details, personnel records, investigation notes, or generated drafts. The selected AI assistant or LLM performs the task under that provider's privacy terms, and the local MCP runtime saves finished files on the user's machine.

Review every draft, source, date, figure, and applicable professional requirement before relying on or submitting an output.

## Support

Use https://hrtasksai.com/support or email hello@hrtasksai.com.
