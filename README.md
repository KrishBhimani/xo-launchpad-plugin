# XO Launchpad plugin for Claude Code

Manage your XO Launchpad apps from Claude Code: list apps, check status, events and releases, read logs, and
start, stop or restart apps.

You sign in with your XO account in the browser (OAuth). There's no API key to copy, and Claude only gets a
temporary token that works on the Launchpad MCP server alone. Reading is granted at sign-in. Start, stop and
restart ask once for extra permission the first time you use them.

## Install

In a terminal:

```
claude plugin marketplace add KrishBhimani/xo-launchpad-plugin
claude plugin install launchpad@xo-launchpad --scope user
```

Or inside Claude Code: `/plugin marketplace add KrishBhimani/xo-launchpad-plugin`, then
`/plugin install launchpad@xo-launchpad`.

If Claude Code is already running, type `/reload-plugins` to load it without restarting.

## Sign in

The first time, sign in with your XO account: type `/mcp`, select **plugin:launchpad:launchpad**, then
**Authenticate**, and approve **Read Launchpad apps** in the browser.

## Try it

- "Who am I on Launchpad?"
- "List my Launchpad apps."
- "Show the status and recent logs of my-app."
- "Restart my-app." (asks you once for permission to manage apps)

## What's inside

Only configuration: `plugins/launchpad/.mcp.json` points Claude Code at the Launchpad MCP server
(`https://launchpad-mcp-xo-xpf8o5s.apps.hello-xo.nl/mcp`). No code runs on your machine, and no keys are stored
here.
