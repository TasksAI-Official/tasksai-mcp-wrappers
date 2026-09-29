# TeacherTasksAI Install Manifest

TeacherTasksAI adds purpose-built lesson-planning, classroom-communication,
resource, and school-administration workflows to supported MCP clients. It is
an educator preparation tool, not a student information system or an authorized
IEP, Section 504, grading, discipline, health, safety, or legal decision maker.

## Official source

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/teacher
```

Official website: https://teachertasksai.com

The official product ID is `teacher`, the MCP tool prefix is `teachertasksai`,
and the installer package is `@tasksai/install`.

## AI-assistant install prompt

Copy this prompt into Codex, Cursor, or Windsurf running on the computer where
you want to use TeacherTasksAI. Ordinary browser or mobile Claude and ChatGPT
sessions cannot install local software. Claude Desktop uses the Terminal route
below.

> Please set up TeacherTasksAI from
> https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/teacher.
> Follow AGENT-SETUP.md and prepare any required software automatically.

The assistant instructions are in [AGENT-SETUP.md](AGENT-SETUP.md). They require
the assistant to verify that commands run on the customer's actual computer,
use only the pinned installer, complete browser account approval, run the health
check, and report success only after it passes.

## Terminal install

For Claude Desktop:

```bash
npm exec --package=@tasksai/install@0.1.46 --call 'tasksai-install teacher --source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/teacher --client claude-desktop'
```

Replace `claude-desktop` with `cursor`, `windsurf`, or `codex` when installing
for a different supported client. Node.js and npm are required.

## Verify the installation

The installer runs doctor after writing the selected client configuration. It
can also be rerun explicitly for the same client:

```bash
npm exec --package=@tasksai/install@0.1.46 --call 'tasksai-install teacher doctor --client claude-desktop'
```

A passing check prints `TasksAI doctor passed.` Restart the selected client,
start a new conversation if needed, and try:

> Help me create a one-day lesson plan. Ask for the grade band, subject,
> learning objective, available time and materials, and any required standards
> or school constraints. Mark anything not supplied for educator review, then
> save the finished plan as a local Word document.

Finished files are saved locally under
`~/Documents/TasksAI/TeacherTasksAI/` unless `TASKSAI_OUTPUT_DIR` is configured.

## Supported clients

- Claude Desktop (`claude-desktop`)
- Cursor (`cursor`)
- Windsurf (`windsurf`)
- Codex (`codex`)

## Privacy boundary

TeacherTasksAI receives authentication, account and credit state, catalog
metadata, licensed workflow delivery requests, and content-free activation
events. It does not receive student records, names, identifiers, classroom
notes, prompt text, generated drafts, document contents, or local file paths.

The selected AI assistant or LLM performs the task under that provider's
privacy terms. A cloud AI provider may process information supplied to it.
Prefer anonymized or de-identified classroom information and follow current
school and district rules. The local MCP runtime saves finished documents on
the user's machine.

## Support

Use https://teachertasksai.com/support or email support@teachertasksai.com.
