# Monorepo Source Format

TasksAI public install manifests live under:

```text
verticals/<product>/
```

Each vertical folder should include:

```text
README.md
agent-install.json
vertical.json
examples.md
SECURITY.md
TROUBLESHOOTING.md
```

The preferred source URL shape is:

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/<product>
```

The corresponding raw manifest URL shape is:

```text
https://raw.githubusercontent.com/TasksAI-Official/tasksai-mcp-wrappers/main/verticals/<product>/agent-install.json
```

The shared installer should verify that the manifest product id, official domain, and source path match the requested product before installation.

