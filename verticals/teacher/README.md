# TeacherTasksAI Install Manifest

TeacherTasksAI adds classroom planning, communication, assessment,
documentation, and school-administration workflows to supported MCP clients.
It is an add-on for an AI assistant, not a student-information system, gradebook,
IEP platform, emergency service, or substitute for authorized educator judgment.

## Official source

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/teacher
```

Official website: https://teachertasksai.com

The official product ID is `teacher`, the MCP tool prefix is `teachertasksai`,
and the installer package is `@tasksai/install`.

## AI-assistant install prompt

Use an AI assistant with permission to run setup on your computer. A cloud or
remote command environment cannot configure a desktop app on your computer.
Account approval and a restart may still be needed.

> Please set up TeacherTasksAI from
> https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/teacher.
> Follow AGENT-SETUP.md and prepare any required software automatically.

Instructions for the assistant: [AGENT-SETUP.md](AGENT-SETUP.md).

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install@0.1.46 --call 'tasksai-install teacher --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/teacher --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` for another
supported client. Node.js and npm are required for this Terminal route. An
assistant with local command access can use the verified native launcher in
[AGENT-SETUP.md](AGENT-SETUP.md) when Node is missing.

## Verify the installation

The installer runs doctor after writing the selected client configuration. It
can also be rerun for the same client:

```bash
npm exec --package=@tasksai/install@0.1.46 --call 'tasksai-install teacher doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client,
start a new conversation if needed, and try:

> Help me create a one-page classroom procedures handout for a fictional Grade
> 7 mathematics class, then save the finished draft as a local Word document.

The local workspace lets the customer reopen projects and create reviewable Word
documents, with Excel added only when the selected task genuinely needs a table,
tracker, or calculation.

## Privacy boundary

TeacherTasksAI receives authentication, account and credit state, catalog
metadata, licensed workflow delivery requests, and content-free activation
events. It does not receive student details, prompt text, generated drafts,
document contents, or local file paths.

The selected AI assistant or LLM is a separate processing layer and may process
information supplied to it under that provider and account's terms. Use
de-identified or fictional student information whenever possible and follow
applicable school, district, FERPA, and provider requirements. Finished files
are saved locally by the MCP runtime.

## Support

Use https://teachertasksai.com/support or email support@teachertasksai.com.
