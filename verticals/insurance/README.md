# InsuranceTasksAI Install Manifest

InsuranceTasksAI adds licensed administrative workflows for insurance agents, brokers, and office staff to supported MCP-capable AI applications.

## Official source

https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/insurance

Official website: https://insurancetasksai.com

The official product ID is `insurance`, the tool prefix is `insurancetasksai`, and the installer package is `@tasksai/install`.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install insurance --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/insurance --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` for another supported client.

## Verify and start

```bash
npm exec --package=@tasksai/install --call 'tasksai-install insurance doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client, then try:

> Help me prepare a policy summary letter for a fictional small business. Ask for the coverage types, limits, deductibles, exclusions to highlight, renewal date, and contact details, then save the finished letter as a local Word document.

Finished files are saved locally under `~/Documents/TasksAI/InsuranceTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Privacy

InsuranceTasksAI services handle authentication, account and credit state, catalog metadata, licensed workflow delivery, and content-free activation events. InsuranceTasksAI does not receive policyholder details, claim records, underwriting data, coverage documents, or generated drafts. The selected AI assistant or LLM performs the task under that provider's privacy terms, and the local MCP runtime saves finished files on the user's machine.

Review every draft, source, date, figure, and applicable professional requirement before relying on or submitting an output.

## Support

Use https://insurancetasksai.com/support or email hello@insurancetasksai.com.
