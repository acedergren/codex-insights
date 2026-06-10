# Release Notes

## v0.2.3

Agent Workflow Roast now has sharper prompt-quality and token-effectiveness signals. The report counts clarity markers from user prompt rows only, and token effectiveness now says when it is using measured local token-count coverage instead of pure text-volume estimates.

### Highlights

- Added prompt-quality scoring from visible goal, scope, acceptance, verification, and boundary markers.
- Added measured-token-aware token effectiveness wording in Coaching Targets.
- Passed aggregate prompt/token stats into optional synthesis while keeping raw session prompts out of the payload.
- Kept deterministic `--no-ai` reports useful when synthesis is disabled.

### Install

```bash
codex plugin marketplace add acedergren/agent-workflow-roast --ref v0.2.3
codex plugin add agent-workflow-roast@agent-workflow-roast
```

If you already added the marketplace:

```bash
codex plugin marketplace upgrade agent-workflow-roast
codex plugin add agent-workflow-roast@agent-workflow-roast
```

### Verification

- `npm test`
- `npm run validate:plugin`
- `git diff --check`
