# Tutorial — Secure MCP Enterprise with TypeScript

Este tutorial será escrito ao mesmo tempo que o projeto for desenvolvido. Cada parte deverá deixar o repositório executável, testável ou documentalmente mais preciso.

## Princípio editorial

Não apresentaremos código sem explicar qual problema ele resolve. Também não atribuiremos à NSA decisões que são nossas. Cada controle será classificado como:

- **Recomendação explícita da NSA**;
- **Requisito ou comportamento do MCP**;
- **Decisão arquitetural do projeto**.

## Roteiro progressivo

| Parte | Tema | Entrega principal | Status |
|---:|---|---|---|
| 1 | Fundação, escopo e critérios | README, cenário e matriz inicial | Concluída |
| 2 | Fundamentos e arquitetura do MCP | Modelo mental de host, client, server e primitives | Concluída — aguardando revisão |
| 3 | MCP Server mínimo em TypeScript | Servidor local executável | Planejada |
| 4 | Enterprise Risk Knowledge | Domínio, tools e dados fictícios | Planejada |
| 5 | Threat model e trust boundaries | Atores, ativos, fluxos e fronteiras | Planejada |
| 6 | Validação de parâmetros | Schemas, limites e bloqueio de forwarding | Planejada |
| 7 | Identidade e autorização | Autenticação, RBAC/ABAC e least privilege | Planejada |
| 8 | Aprovação humana | Consentimento informado para ações sensíveis | Planejada |
| 9 | Sessões e replay protection | Expiração, idempotência e integridade | Planejada |
| 10 | Output filtering | Tratamento de saídas como dados não confiáveis | Planejada |
| 11 | Auditoria e detecção | Logs estruturados e trilha forense | Planejada |
| 12 | DoS e uso abusivo | Rate limiting, quotas e limites de complexidade | Planejada |
| 13 | Sandboxing e egress | Isolamento, privilégios e saída de rede | Planejada |
| 14 | Supply chain | Inventário, versões, patches e dependências | Planejada |
| 15 | Testes ofensivos | Cenários de abuso e evidências | Planejada |
| 16 | Consolidação | Artigo final e revisão de rastreabilidade | Planejada |

## Definição de concluído para cada parte

Uma parte somente estará concluída quando:

- a explicação estiver escrita em linguagem didática;
- as afirmações externas tiverem fonte;
- decisões próprias estiverem identificadas como decisões;
- o código relacionado compilar, quando houver código;
- os testes relacionados passarem, quando houver testes;
- a matriz de controles estiver atualizada;
- limitações e itens pendentes estiverem explícitos.

## Navegação

- [Parte 1 — Fundação, escopo e critérios](./01-foundations.md)
- [Parte 2 — Fundamentos e arquitetura do MCP](./02-mcp-fundamentals.md)
- [Matriz de controles](../docs/security-controls-matrix.md)
