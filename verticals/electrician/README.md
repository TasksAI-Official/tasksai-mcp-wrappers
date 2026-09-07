# ElectricianTasksAI Install Manifest

ElectricianTasksAI adds licensed administrative workflows for electricians and electrical contractors to supported MCP-capable AI applications.

## Official source

https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/electrician

Official website: https://electriciantasksai.com

The official product ID is `electrician`, the tool prefix is `electriciantasksai`, and the installer package is `@tasksai/install`.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install electrician --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/electrician --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` for another supported client.

## Verify and start

```bash
npm exec --package=@tasksai/install --call 'tasksai-install electrician doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client, then try:

> Help me prepare an electrical service estimate for a 200-amp panel replacement. Ask for the labor, materials, exclusions, schedule, and customer assumptions, then save the finished estimate as a local Word document.

Finished files are saved locally under `~/Documents/TasksAI/ElectricianTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Privacy

ElectricianTasksAI services handle authentication, account and credit state, catalog metadata, licensed workflow delivery, and content-free activation events. ElectricianTasksAI does not receive customer details, estimates, permit records, job notes, or generated drafts. The selected AI assistant or LLM performs the task under that provider's privacy terms, and the local MCP runtime saves finished files on the user's machine.

Review every draft, source, date, figure, and applicable professional requirement before relying on or submitting an output.

## Support

Use https://electriciantasksai.com/support or email hello@electriciantasksai.com.
