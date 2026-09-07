# MortuaryTasksAI Install Manifest

MortuaryTasksAI adds licensed administrative workflows for morticians, funeral directors, and mortuary staff to supported MCP-capable AI applications.

## Official source

https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/mortuary

Official website: https://mortuarytasksai.com

The official product ID is `mortuary`, the tool prefix is `mortuarytasksai`, and the installer package is `@tasksai/install`.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install mortuary --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/mortuary --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` for another supported client.

## Verify and start

```bash
npm exec --package=@tasksai/install --call 'tasksai-install mortuary doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client, then try:

> Help me prepare a monthly financial statement summary for a fictional funeral home. Ask for revenue categories, operating expenses, payroll, accounts receivable, cash balance, and notable variances, then save the finished summary as a local Word document.

Finished files are saved locally under `~/Documents/TasksAI/MortuaryTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Privacy

MortuaryTasksAI services handle authentication, account and credit state, catalog metadata, licensed workflow delivery, and content-free activation events. MortuaryTasksAI does not receive decedent or family details, health records, authorization documents, case files, or generated drafts. The selected AI assistant or LLM performs the task under that provider's privacy terms, and the local MCP runtime saves finished files on the user's machine.

Review every draft, source, date, figure, and applicable professional requirement before relying on or submitting an output.

## Support

Use https://mortuarytasksai.com/support or email hello@mortuarytasksai.com.
