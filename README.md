# Awesome Azure MCP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of MCP (Model Context Protocol) servers, tools, and resources for Microsoft Azure and enterprise AI.

MCP is becoming the universal standard for connecting AI agents to systems and data. This list focuses on the Azure and Microsoft ecosystem.

## Contents

- [What is MCP?](#what-is-mcp)
- [Official MCP Servers](#official-mcp-servers)
- [Azure-Native MCP Servers](#azure-native-mcp-servers)
- [Microsoft 365 MCP Servers](#microsoft-365-mcp-servers)
- [Enterprise Integration](#enterprise-integration)
- [Development Tools](#development-tools)
- [Frameworks with MCP Support](#frameworks-with-mcp-support)
- [Architecture Patterns](#architecture-patterns)
- [Learning Resources](#learning-resources)

## What is MCP?

[Model Context Protocol (MCP)](https://modelcontextprotocol.io/) is an open standard that provides a universal way to connect AI models to external data sources, tools, and systems. Think of it as USB-C for AI — one protocol, any model, any tool.

**Why MCP matters for Azure:**
- Replaces bespoke API integrations with a single standard
- Works across Claude, GPT, Gemini, and open-source models
- Separates tool capabilities from model choice — swap models without rewriting integrations
- Aligns with Microsoft's own Agent Framework (MAF) direction

## Official MCP Servers

| Server | Maintainer | Description |
|---|---|---|
| [Microsoft Learn](https://github.com/mcp/microsoft/learn) | Microsoft | Search and fetch official Azure/MSFT documentation |
| [Playwright](https://github.com/mcp/microsoft/playwright-mcp) | Microsoft | Browser automation for testing and data extraction |
| [GitHub](https://github.com/mcp/github/github-mcp-server) | GitHub | Repository management, issues, PRs, Actions |

## Azure-Native MCP Servers

| Server | Purpose | Status |
|---|---|---|
| [Azure AI Foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/) | Model deployment, evaluation, and management | GA |
| [Copilot Studio](https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio) | Build and manage agents with low-code | GA |
| [Azure SQL MCP](https://devblogs.microsoft.com/azure-sql/) | Query Azure SQL databases | Community |
| [Cosmos DB MCP](https://learn.microsoft.com/en-us/azure/cosmos-db/) | NoSQL data access | Community |
| [Azure Blob Storage](https://azure.microsoft.com/en-us/products/storage/blobs/) | File and object storage | Community |

## Microsoft 365 MCP Servers

| Server | Purpose | Auth |
|---|---|---|
| [Google Drive](https://drivemcp.googleapis.com/) | File search, read, and management | OAuth |
| [Gmail](https://gmailmcp.googleapis.com/) | Email search, send, and management | OAuth |
| [Google Calendar](https://calendarmcp.googleapis.com/) | Event management and scheduling | OAuth |
| [SharePoint (via Graph)](https://learn.microsoft.com/en-us/graph/) | Document management and search | OAuth |

## Enterprise Integration

| Server | System | Use Case |
|---|---|---|
| [ServiceNow](https://www.servicenow.com/) | ITSM | Ticket creation, incident management |
| [SAP](https://www.sap.com/) | ERP | Business process automation |
| [Supabase](https://mcp.supabase.com/) | PostgreSQL | Database queries, migrations, edge functions |
| [Netlify](https://netlify-mcp.netlify.app/) | Hosting | Deploy and manage web applications |

## Development Tools

| Tool | Purpose |
|---|---|
| [Claude Code](https://docs.anthropic.com/en/docs/build-with-claude/claude-code) | CLI-based agentic coding with MCP support |
| [Cursor IDE](https://www.cursor.com/) | AI-first code editor with MCP integration |
| [Windsurf](https://www.windsurf.com/) | AI coding agent with MCP |

## Frameworks with MCP Support

| Framework | Language | MCP Support | Best For |
|---|---|---|---|
| [Microsoft Agent Framework (MAF)](https://github.com/microsoft/agent-framework) | C# / Python | Native | Enterprise, Azure-first |
| [LangGraph](https://langchain-ai.github.io/langgraph/) | Python | Via tools | Stateful, complex workflows |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | Python | Via tools | Fast prototyping |
| [CrewAI](https://www.crewai.com/) | Python | Via tools | Role-based multi-agent |
| [AutoGen](https://github.com/microsoft/autogen) | Python | Native | Research, multi-agent |

## Architecture Patterns

### MCP-First Architecture (Recommended)

```
┌─────────────────────────────────────────────┐
│  Layer 6: Applications / Agents             │
├─────────────────────────────────────────────┤
│  Layer 5: Skills / Domain IP                │  ← Invest here
├─────────────────────────────────────────────┤
│  Layer 4: Tools / Capabilities              │
├─────────────────────────────────────────────┤
│  Layer 3: MCP Interoperability              │  ← Standardise here
├─────────────────────────────────────────────┤
│  Layer 2: Foundation Models                 │  ← Replaceable
├─────────────────────────────────────────────┤
│  Layer 1: Compute / Cloud                   │  ← Commodity
└─────────────────────────────────────────────┘
```

**Key insight:** Models and frameworks change. Skills and domain IP endure. Build on open standards, own your IP, deliver lasting value.

### Investment Priority

1. **Skills / Domain IP** — Your methodologies, templates, knowledge bases
2. **MCP Layer** — Universal connectivity standard
3. **Tools / Capabilities** — Actions your agents can take
4. **Framework** — Choose one, keep it replaceable
5. **Models** — Use the best available, stay portable
6. **Compute** — Commodity, choose by price and compliance

## Learning Resources

- [MCP Specification](https://spec.modelcontextprotocol.io/) — The official protocol specification
- [MCP Registry](https://github.com/mcp) — Browse all available MCP servers
- [Building MCP Servers](https://modelcontextprotocol.io/quickstart/server) — Getting started guide
- [Azure AI Foundry Docs](https://learn.microsoft.com/en-us/azure/ai-foundry/) — MSFT's AI platform

## Contributing

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

If you know of an MCP server or tool that works with Azure/MSFT ecosystem, open a PR.

## Author

[Jeffrey Chu](https://github.com/jeffreychu-au) — Sydney-based Cloud & AI Solution Architect specialising in Azure, hybrid cloud, and agentic AI for regulated industries.

## Licence

MIT
