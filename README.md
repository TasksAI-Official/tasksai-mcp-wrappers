# TasksAI Public MCP Install Manifests

This repository contains public installer manifests and product metadata for TasksAI vertical products.

TasksAI products add licensed, profession-specific workflows to MCP-capable AI applications such as Claude Desktop, Cursor, Windsurf, and Codex. This repository is the public installation catalog those AI applications can inspect before setup.

## What Is In This Repository

- Public `agent-install.json` files
- Public `vertical.json` product metadata
- Customer-facing setup notes
- Troubleshooting and support references

## What Is Not In This Repository

- Customer data
- License keys or secrets
- Payment data
- Proprietary workflow or prompt libraries
- The private TasksAI API implementation

The shared installer package is `@tasksai/install`. Product websites, account connection, credits, and licensed workflow delivery are handled by TasksAI services.

## Production Products

| Product | Folder | Website |
|---|---|---|
| FarmerTasksAI | `verticals/farmer` | https://farmertasksai.com |
| TeacherTasksAI | `verticals/teacher` | https://teachertasksai.com |
| RealtorTasksAI | `verticals/realtor` | https://realtortasksai.com |
| LawTasksAI | `verticals/lawtasksai` | https://lawtasksai.com |
| ElectricianTasksAI | `verticals/electrician` | https://electriciantasksai.com |
| HRTasksAI | `verticals/hr` | https://hrtasksai.com |
| InsuranceTasksAI | `verticals/insurance` | https://insurancetasksai.com |
| MortgageTasksAI | `verticals/mortgage` | https://mortgagetasksai.com |
| MortuaryTasksAI | `verticals/mortuary` | https://mortuarytasksai.com |
| RestaurantTasksAI | `verticals/restaurant` | https://restauranttasksai.com |

## Install Source Format

Each vertical folder has its own manifest:

```text
verticals/<product>/agent-install.json
```

The installer source for RealtorTasksAI, for example, is:

```text
https://github.com/TasksAI-Official/tasksai-mcp-wrappers/tree/main/verticals/realtor
```

The raw manifest URL is:

```text
https://raw.githubusercontent.com/TasksAI-Official/tasksai-mcp-wrappers/main/verticals/realtor/agent-install.json
```

## Support

For product support, use the support link or email listed in that product's `vertical.json`.
