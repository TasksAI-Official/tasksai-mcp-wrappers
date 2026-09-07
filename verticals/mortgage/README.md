# MortgageTasksAI Install Manifest

MortgageTasksAI adds licensed administrative workflows for mortgage brokers, loan officers, and processors to supported MCP-capable AI applications.

## Official source

https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/mortgage

Official website: https://mortgagetasksai.com

The official product ID is `mortgage`, the tool prefix is `mortgagetasksai`, and the installer package is `@tasksai/install`.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install mortgage --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/mortgage --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` for another supported client.

## Verify and start

```bash
npm exec --package=@tasksai/install --call 'tasksai-install mortgage doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client, then try:

> Help me write a preapproval congratulations letter for a fictional borrower using the Write a pre-approval congratulations letter workflow. Ask for the loan program, amount, expiration date, conditions, loan officer contact details, and next steps, then save the finished letter as a local Word document.

Finished files are saved locally under `~/Documents/TasksAI/MortgageTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Privacy

MortgageTasksAI services handle authentication, account and credit state, catalog metadata, licensed workflow delivery, and content-free activation events. MortgageTasksAI does not receive borrower details, credit or income records, loan documents, property records, or generated drafts. The selected AI assistant or LLM performs the task under that provider's privacy terms, and the local MCP runtime saves finished files on the user's machine.

Review every draft, source, date, figure, and applicable professional requirement before relying on or submitting an output.

## Support

Use https://mortgagetasksai.com/support or email hello@mortgagetasksai.com.
