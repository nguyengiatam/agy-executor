---
description: Check whether the agy CLI is installed and has remaining quota
argument-hint: ''
allowed-tools: Bash(node:*)
---

Run:

```bash
node "${CLAUDE_PLUGIN_ROOT}/scripts/agy-runtime.mjs" setup --json
```

Present the result. If `installed` is false, tell the user to install the Antigravity CLI (`agy`) and ensure it is on PATH. If `quota` is `exhausted`, tell the user agy is out of quota (individual quota resets roughly every 4-5 hours) and suggest another executor for now. If `quota` is `ok`, confirm agy is ready to receive tasks.
