---
name: receita_federal_sal_cadastro-mcp
description: Skill da REST API do Receita Federal Sistema de Acréscimos Legais (SAL): Dados Cadastrais na MCP.AI: 1 endpoint em /api/receita_federal_sal_cadastro. Receita Federal Sistema de Acréscimos Legais (SAL): Dados Cadastrais, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Receita Federal Sistema de Acréscimos Legais (SAL): Dados Cadastrais — REST API skill

Você tem acesso à **Receita Federal Sistema de Acréscimos Legais (SAL): Dados Cadastrais** REST API na MCP.AI.

> Receita Federal Sistema de Acréscimos Legais (SAL): Dados Cadastrais, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/receita_federal_sal_cadastro
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/receita_federal_sal_cadastro/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"pis":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/receita_federal_sal_cadastro/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `receita_federal_sal_cadastro_consultar`

Receita Federal Sistema de Acréscimos Legais (SAL): Dados Cadastrais, consulta em fonte oficial. _(POST /api/receita_federal_sal_cadastro/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `pis` | string | Sim | Parâmetro de consulta "pis". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_receita_federal_sal_cadastro` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
