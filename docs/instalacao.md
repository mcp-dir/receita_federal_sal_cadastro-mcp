# Instalação detalhada

Receita Federal Sistema de Acréscimos Legais (SAL): Dados Cadastrais é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_receita_federal_sal_cadastro`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_receita_federal_sal_cadastro` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_receita_federal_sal_cadastro` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_receita_federal_sal_cadastro` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.receita_federal_sal_cadastro` (ou `servers.receita_federal_sal_cadastro` no VS Code) do config do cliente e reinicie.
