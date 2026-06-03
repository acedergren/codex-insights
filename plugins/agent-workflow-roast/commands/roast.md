---
description: Generate an Agent Workflow Roast report in the current workspace
argument-hint: [--days 7] [--project name-or-path] [--no-memory] [--no-ai] [--output-dir .] [--site] [--export markdown|html|json|site]
allowed-tools: [Bash, Read]
---

# Agent Workflow Roast

The user invoked `/roast` with: `$ARGUMENTS`

Capture the folder where `/roast` was invoked before changing directories. Never paste raw `$ARGUMENTS` into a shell command.

Parse the supplied arguments into an argv JSON array first, using only the analyzer options shown in the argument hint. If the argument text is ambiguous, ask a short clarifying question. Run the local command wrapper from the plugin root with that folder as `AGENT_WORKFLOW_ROAST_OUTPUT_DIR`; the wrapper will pass parsed arguments to Node as argv without a shell:

```bash
AGENT_WORKFLOW_ROAST_OUTPUT_DIR="$INVOKED_DIR" node scripts/agent-workflow-roast-command.mjs <<'AGENT_WORKFLOW_ROAST_ARGV_JSON'
[]
AGENT_WORKFLOW_ROAST_ARGV_JSON
```

Replace `[]` with the parsed argv array when options are supplied, for example `["--days","7","--project","oci-self-service-portal","--no-ai","--no-open"]`.

When the user asks to present the result with Sites, pass `["--site"]` or add `--site` to their other options. The command prints a `agent-workflow-roast-site.tgz` archive containing a deployable `dist/server/index.js` Worker and Sites metadata, ready for the Sites `_create_project_version` archive parameter. Do not use the legacy playground for presentation.

Report the generated file path back to the user. Local HTML artifacts must be named `agent-workflow-roast.html` and land in the folder where the command was invoked, unless the user explicitly passes an output directory. Sites presentation artifacts must be named `agent-workflow-roast-site.tgz`.
