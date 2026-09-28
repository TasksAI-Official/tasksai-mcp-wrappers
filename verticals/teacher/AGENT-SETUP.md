# Agent setup instructions

## Start with the customer's computer

Read `agent-install.json` and `vertical.json` and verify the official product,
repository, domain, package version, and archive hash. Establish whether the
command tool runs on the customer's actual computer. Do not install into a
remote sandbox and report that a local desktop client is configured.

Ask which supported client to configure when it is not clear. Request the
application's normal folder and command approvals; do not bypass restrictions,
paste credentials into chat, or promise that a single prompt eliminates account
approval or restart. Existing TeacherTasksAI tools prove an existing connection,
not that the current session can install or update local software.

If TeacherTasksAI is already installed, preserve its account and saved projects.
Close active TasksAI connections before an authorized update when required.
Never bypass installer locks.

## Prepare required software automatically

If Node and npm are available, use the exact pinned npm command in the manifest
with the selected `--client`. If they are missing on Mac or Windows, use
`agent_setup.native_bootstrap`:

1. Download the exact `archive_url` to a new setup folder using the operating
   system's download facility. Do not replace the pinned version with `latest`.
2. Verify the complete archive SHA-256 before extracting or running anything.
   Stop on mismatch.
3. Extract the complete package. Keep `bootstrap`, `src`, `runtime`, and
   `package.json` together. Do not copy a launcher alone or pipe downloaded text
   into a shell.
4. On macOS, invoke `/bin/sh` with the absolute path to
   `package/bootstrap/Install TeacherTasksAI.command`. Pass
   `--source https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/teacher`
   and the selected `--client` as separate arguments. The launcher selects
   product `teacher`; do not add another product argument.
5. On Windows, invoke `package/bootstrap/Install TeacherTasksAI.ps1` with
   PowerShell and the same installer arguments. Respect execution policy; do not
   weaken it. If blocked, report that exact limitation.

The native launcher downloads and verifies a private Node copy. The installer
prepares Python when needed. Do not claim the website exposes a finished
downloadable setup package while `customer_download_journey_validated` is false.

## Account approval and completion

Follow the installer's browser account-approval flow. Do not change the installed
account without instruction. Allow the installer to configure the selected AI
client and run health checks. Only report success after doctor passes for the
same client. Tell the customer when a restart is required, then offer the
manifest's first-file prompt.

If the assistant cannot execute on the customer host or obtain ordinary required
permissions, report the exact blocked step and offer the documented Terminal
route as a fallback.
