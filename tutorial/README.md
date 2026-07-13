# Tutorial — Secure MCP Enterprise with TypeScript

Este tutorial será escrito ao mesmo tempo que o projeto for desenvolvido. Cada parte deverá deixar o repositório executável, testável ou documentalmente mais preciso.

## Princípio editorial

Não apresentaremos código sem explicar qual problema ele resolve. Também não atribuiremos à NSA decisões que são nossas. Cada controle será classificado como:

- **Recomendação explícita da NSA**;
- **Requisito ou comportamento do MCP**;
- **Decisão arquitetural do projeto**.

O texto deverá se aproximar da leitura de um livro técnico passo a passo. A narrativa contínua será o formato principal, conectando um conceito ao seguinte. Bullet points poderão ser utilizados quando facilitarem a leitura ou evitarem um parágrafo artificial, mas não deverão dominar o capítulo.

Diagramas Mermaid serão utilizados quando fluxos, sequências, componentes, fronteiras de confiança ou comparações forem mais fáceis de compreender visualmente. Os diagramas deverão permanecer simples e poderão ser redesenhados posteriormente no [tldraw](https://www.tldraw.com/) para publicação.

A linguagem será acessível para quem ainda não conhece MCP, sem remover a precisão técnica nem simplificar indevidamente as recomendações do guia da NSA. Sempre que possível, apresentaremos primeiro o problema em linguagem cotidiana e depois o termo técnico correspondente.

## Roteiro progressivo

| Parte | Tema | Entrega principal | Status |
|---:|---|---|---|
| [1](./01-foundations.md) | Fundação, escopo e critérios | README, cenário e matriz inicial | Concluída |
| [2](./02-mcp-fundamentals.md) | Fundamentos e arquitetura do MCP | Modelo mental de Host, Client, Server e primitivas | Em revisão |
| 3 | MCP Server mínimo em TypeScript | Servidor local executável | Planejada |
| 4 | Enterprise Risk Knowledge | Domínio, tools e dados fictícios | Planejada |
| 5 | Threat model e fronteiras de confiança | Atores, ativos, fluxos e fronteiras | Planejada |
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

## Como navegar pelo tutorial?

Você pode começar pela [Parte 1 — Fundação, escopo e critérios](./01-foundations.md) e seguir para a [Parte 2 — Fundamentos e arquitetura do MCP](./02-mcp-fundamentals.md). No início e no final de cada capítulo, você encontrará atalhos para a parte anterior, para este índice e para a próxima parte disponível.

A [matriz de controles de segurança](../docs/security-controls-matrix.md) acompanha a evolução do projeto e conecta recomendações, decisões, implementações e evidências. As partes planejadas ganharão links somente quando seus respectivos arquivos forem criados.
