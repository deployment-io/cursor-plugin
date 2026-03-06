# Deployment.io — Cursor Plugin

Deploy and manage apps to your cloud directly from Cursor. This plugin connects Cursor's AI agent to [Deployment.io](https://deployment.io) via the Model Context Protocol (MCP).

## What it does

This plugin lets you manage your Deployment.io infrastructure through natural language:

- **List environments** — view all your environments with status, region, and classification
- **Create environments** — provision new environments on shared or custom AWS runners
- **Edit environments** — rename and reconfigure existing environments
- **Monitor jobs** — check deployment job status and logs
- **Approval workflows** — manage approval requests for production changes

## Setup

1. Install the plugin from the [Cursor Marketplace](https://cursor.com/marketplace)
2. Cursor will prompt you to authenticate with your Deployment.io account via OAuth
3. Start using natural language to manage your infrastructure

## Authentication

This plugin uses OAuth 2.0 with Dynamic Client Registration. When you first use a Deployment.io tool, Cursor will open a browser window to authenticate with your Deployment.io account. No API keys or tokens need to be configured manually.

## Available tools

| Tool | Description |
|------|-------------|
| `list_environments` | List all environments in your organization |
| `list_runners` | List available deployment runners and regions |
| `create_environment` | Create a new environment |
| `edit_environment` | Rename an environment |
| `get_job_status` | Check the status of a deployment job |
| `get_approval_status` | Check the status of an approval request |

## Security

- All actions respect your organization's RBAC permissions
- Production environments require human approval before changes
- Agent keys are scoped to specific permissions via OAuth consent
- Three-layer access control: OAuth scopes, RBAC entity permissions, classification-based approval gates

## Links

- [Documentation](https://deployment.io/docs/coding-agents/mcp-configuration/)
- [Available tools reference](https://deployment.io/docs/coding-agents/available-mcp-tools/)
- [Terms of Service](https://deployment.io/terms-of-service/)
- [Privacy Policy](https://deployment.io/privacy-policy/)

## License

MIT
