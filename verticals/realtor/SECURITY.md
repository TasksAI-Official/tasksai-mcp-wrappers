# Security and Privacy Boundary

## What RealtorTasksAI receives

RealtorTasksAI services handle authentication, account and credit state,
catalog metadata, licensed workflow delivery, and content-free activation
events. Activation events may include an event name, workflow identifier, file
format, anonymous installation identifier, client type, and runtime version.

## What RealtorTasksAI does not receive

RealtorTasksAI services do not receive listing details, addresses, client
names, showing notes, prompt text, generated drafts, document contents, or
local file paths. Finished documents are created by the local MCP runtime.

The selected AI assistant or LLM is a separate processing layer. A cloud AI
provider may process information the user supplies under that provider's
privacy terms. Users should apply the provider and account controls appropriate
for their listing, client, and transaction information.

## Safe installation

AI assistants must verify `agent-install.json` and run only the official
`@tasksai/install` command declared there. Stop if the product ID, official
domain, GitHub repository, manifest path, or package does not match.

This public folder is limited to product metadata, installation guidance,
generic examples, security notes, and troubleshooting. Do not add proprietary
workflows or prompts, private service code, secrets, license keys, customer
data, or generated customer documents.
