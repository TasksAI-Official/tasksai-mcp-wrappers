# RestaurantTasksAI Install Manifest

RestaurantTasksAI adds licensed administrative workflows for restaurant owners, managers, and food service operators to supported MCP-capable AI applications.

## Official source

https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/restaurant

Official website: https://restauranttasksai.com

The official product ID is `restaurant`, the tool prefix is `restauranttasksai`, and the installer package is `@tasksai/install`.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install --call 'tasksai-install restaurant --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/restaurant --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` for another supported client.

## Verify and start

```bash
npm exec --package=@tasksai/install --call 'tasksai-install restaurant doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client, then try:

> Help me write a staff scheduling memo for a fictional restaurant. Ask for the schedule period, shift changes, coverage expectations, time-off reminders, manager contact, and acknowledgement deadline, then save the finished memo as a local Word document.

Finished files are saved locally under `~/Documents/TasksAI/RestaurantTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Privacy

RestaurantTasksAI services handle authentication, account and credit state, catalog metadata, licensed workflow delivery, and content-free activation events. RestaurantTasksAI does not receive employee details, customer records, vendor information, inspection records, or generated drafts. The selected AI assistant or LLM performs the task under that provider's privacy terms, and the local MCP runtime saves finished files on the user's machine.

Review every draft, source, date, figure, and applicable professional requirement before relying on or submitting an output.

## Support

Use https://restauranttasksai.com/support or email hello@restauranttasksai.com.
