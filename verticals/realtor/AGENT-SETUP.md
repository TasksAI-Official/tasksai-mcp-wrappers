# RealtorTasksAI assistant setup instructions

These instructions support the copy-and-paste setup prompt on
`realtortasksai.com`. Complete setup only when your command tool operates on
the customer's actual computer.

## 1. Verify the official source

Read `agent-install.json` and `vertical.json` before running anything. Confirm:

- product ID: `realtor`
- product name: `RealtorTasksAI`
- domain: `realtortasksai.com`
- repository: `TasksAI-Official/tasksai-mcp-wrappers`
- package: `@tasksai/install`
- installer version: `0.1.45`

Stop if any of these values, the repository, the package, or the declared
installer command has been substituted. Run only the command or native
bootstrap declared in `agent-install.json`.

## 2. Confirm that setup runs on the customer's computer

Establish whether your command tool runs on the computer that has the selected
desktop AI application. A remote Linux sandbox, cloud shell, shared folder, or
browser-only chat session is not the customer's computer and cannot complete
this installation.

Identify the operating system and ask which supported desktop client to
configure if it is not clear:

- ChatGPT desktop or standalone Codex: `codex`
- Claude Desktop: `claude-desktop`
- Cursor: `cursor`
- Windsurf: `windsurf`

A phone cannot host this local installation. ChatGPT Remote can start or steer
work on a connected Mac or Windows computer, but the installer and files remain
on that computer. If local command access is unavailable, explain that specific
limitation and give the Terminal command from `README.md` as the fallback. Do
not report that installation succeeded.

Before changing anything, check for an existing RealtorTasksAI installation.
Preserve its account, local workspace, outputs, and client configuration. Do
not reinstall merely to answer a capability or status question. Respect the
installer's locks and recovery messages.

## 3. Use the pinned installer

If Node and npm are available, run the exact pinned npm command from
`agent-install.json`, adding the selected `--client` value.

If Node or npm is missing on macOS or Windows, do not ask the customer to
assemble dependencies manually. Use `agent_setup.native_bootstrap`:

1. Create a new setup folder.
2. Download the exact `archive_url` using an operating-system download tool.
   Do not replace the declared version with `latest`.
3. Verify the complete downloaded archive's SHA-256 equals the declared
   `archive_sha256`. Stop on a mismatch.
4. Extract the complete package with the operating system's archive facility.
   Keep `bootstrap`, `src`, `runtime`, and `package.json` together. Do not copy
   only the launcher or pipe downloaded text directly into a shell.
5. On macOS, run `/bin/sh` with the absolute path to
   `package/bootstrap/Install RealtorTasksAI.command`. Pass the official
   `--source` URL and selected `--client` as separate arguments. The launcher
   already selects product `realtor`; do not add another positional product
   argument.
6. On Windows, run the declared `Install RealtorTasksAI.ps1` with PowerShell
   and the same installer arguments. Respect Windows execution policy; do not
   weaken it. If policy blocks the launcher, state that exact limitation and
   offer the documented Terminal route.

The native launcher prepares and verifies its own private Node copy. The
installer prepares Python when required. Request the application's normal
folder and command approvals; never bypass them.

## 4. Connect the account and verify setup

Follow the installer's browser connection flow. The approval page must be on
`https://realtortasksai.com/connect`, and its code must match the installer.
Never ask the customer to paste a password or license key into chat. Use the
license-key route only when the official installer offers it as a fallback.

Allow the installer to configure the selected client and run its health check.
Only report installation success after it prints:

```text
TasksAI doctor passed.
```

If setup is blocked, report the exact failing permission, path, account step,
or health check. Do not treat a downloaded package, edited configuration, or
existing tool entry as proof of a completed installation.

## 5. Restart and create the first file

Tell the customer to fully restart the selected desktop client and open a new
conversation. First confirm the connection with:

> Check my RealtorTasksAI credit balance.

Then offer the `post_install.first_file_prompt` from `agent-install.json`. A
successful first-file check creates a local Word document under
`~/Documents/TasksAI/RealtorTasksAI/` unless the customer configured another
output folder.
