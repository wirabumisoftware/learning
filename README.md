# Wirabumi Software Learning Coach

This repository contains the content modules for the Wirabumi Software Learning Coach AI Agent used in VS Code.

The coach is designed as a modular learning system:
- a master entry point
- role routing rules
- role-specific playbooks
- coaching style guidance
- output quality rules
- optional product context

## Video Walkthrough

If you want to see the import flow in action, use this video:

https://www.youtube.com/watch?v=rbpodFuqXwE

## What Is In This Repo

This repository is not a software application. It is a content bundle for a custom VS Code AI agent.

At a high level, the repository is organized around these content types:

- Master agent entry logic
- Role routing rules
- Role-specific playbooks
- Coaching style guidance
- Output quality rules
- Optional product context files

The exact files and folders may evolve over time, but the repository is intended to keep those learning modules together so the agent can route users, apply the right playbook, and stay within defined coaching and product boundaries.

## Importing The Agent Into VS Code

### Option 1: User-Level Agent

Use this option if you want the agent available across your own VS Code environment.

1. Open the VS Code user prompts folder.
2. Create a file named `Wirabumi Software Learning Coach.agent.md`.
3. Paste your agent definition into that file.
4. Keep this repository available in your workspace so the supporting playbooks and context files can be referenced.
5. Reload VS Code if the agent does not appear immediately.

Typical Windows user prompts location:

```text
%APPDATA%\Code\User\prompts\
```

### Option 2: Workspace-Level Agent

Use this option if you want to share the agent with a team inside a repository.

1. Create a `.github/agents/` folder in the target workspace.
2. Add `Wirabumi Software Learning Coach.agent.md` there.
3. Copy this repository's module folders into the same workspace, or keep this repository opened alongside the target workspace.
4. Reload the VS Code window if needed.

## Recommended Setup

For this repository, the clean setup is:

1. Use `Wirabumi Software Learning Coach.agent.md` as the agent entry point.
2. Keep this repository as the source of the learning modules.
3. Treat `master/ai-coach-master.prompt.md` as the master reference for the coaching logic.
4. Keep the playbooks, routing rules, style rules, quality rules, and product context files together.

## How The Agent Works

The expected flow is:

1. Route the user to the correct training stream and role.
2. Activate the matching playbook.
3. Apply coaching style guidance.
4. Enforce the output quality bar.
5. Use product context only when that context is actually loaded.

## Available Learning Tracks

- Computer Science: Computer Science Student
- Customer: Operator
- Partner: Configuration & Data Migration

## Important Notes

- Product-specific guidance should only be given when a product context file is loaded.
- The current `products/metasfresh-erp.context.md` file is a placeholder, not a full product implementation.
- This repo currently includes the modular source content. The custom agent file itself should be stored in the VS Code prompts or agents location.

## Minimal Import Checklist

- You have GitHub Copilot Chat available in VS Code.
- You created `Wirabumi Software Learning Coach.agent.md` in the correct location.
- This repository is open in your workspace, or its module files were copied into the workspace.
- The agent can see the playbooks and support files.
- You can start a chat and route the learner by stream, role, objective, and product context.

## Suggested Next Step

Follow the video first, then use this repository as the content source behind the agent:

https://www.youtube.com/watch?v=rbpodFuqXwE