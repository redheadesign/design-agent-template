# GitHub Workflow

Use GitHub CLI to let the agent work with GitHub without sharing passwords or personal access tokens in chat.

## One-Time Login

If `gh` is not installed on Windows, install GitHub CLI first:

```bash
winget install --id GitHub.cli
```

Restart the terminal after installation so `gh` is available in `PATH`.

Run this locally when needed:

```bash
gh auth login
```

Choose GitHub.com, HTTPS, and browser authentication unless you already use another setup. After that, the agent can use the authenticated `gh` client to create repositories, open pull requests, inspect issues, and check CI.

## Create A Public Template Repo

From this folder:

```bash
git init
git add README.md docs .cursor/skills .cursor/rules .cursor/mcp.example.json .gitignore
git commit -m "Create design agent template"
gh repo create design-agent-template --public --source . --push
```

The agent can run these after you explicitly ask it to commit and publish.

## Important Safety Rule

Never commit `.cursor/mcp.json`. It is ignored because it can contain local MCP bearer tokens. Publish `.cursor/mcp.example.json` instead.

## Starting A New Project

Clone the template, copy the MCP example, add local tokens, then reload Cursor:

```bash
git clone https://github.com/YOUR_USER/design-agent-template.git my-new-design-project
cd my-new-design-project
copy .cursor\mcp.example.json .cursor\mcp.json
```

Replace `YOUR_LAZYWEB_TOKEN` in `.cursor/mcp.json` with your real local token.

Get a free Lazyweb token from:

```text
https://www.lazyweb.com/mcp-install
```

The token is for no-billing UI reference tools. Keep it out of public Git history and store it only in ignored local config.
