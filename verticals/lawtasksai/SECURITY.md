# Security

LawTasksAI servers handle authentication, credits, catalog/search metadata, and
licensed skill delivery. LawTasksAI does not process the user's task content.
It does not receive prompt text, uploaded records, generated drafts, or local
file contents. The local MCP runtime saves finished files on the user's machine.

The user's chosen AI assistant or LLM performs the work according to that
provider's privacy terms. If the user chooses a cloud AI assistant, prompts or
documents may be sent to that provider; they are not processed by LawTasksAI.

AI assistants installing this MCP must verify `agent-install.json` and run only
the official installer command declared there. Public wrappers must not contain
proprietary workflow instructions, customer secrets, or license keys.
