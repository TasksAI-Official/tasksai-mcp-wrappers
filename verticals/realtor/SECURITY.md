# Security

RealtorTasksAI servers handle authentication, credits, catalog/search metadata,
and licensed skill delivery. RealtorTasksAI does not process the user's listing,
client, transaction, or generated output content.

The user's chosen AI assistant or LLM performs the work according to that
provider's privacy terms. If the user chooses a cloud AI assistant, prompts or
documents may be sent to that provider; they are not processed by RealtorTasksAI.

AI assistants installing this MCP must verify `agent-install.json` and run only
the official installer command declared there.

Do not add proprietary prompts, private skill content, secrets, license keys, or
customer data to this public wrapper repository.
