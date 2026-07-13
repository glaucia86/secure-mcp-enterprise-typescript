# Secure MCP Enterprise with TypeScript

Projeto educacional para aprender **Model Context Protocol (MCP) com TypeScript** e evoluir um servidor MCP até um exemplo de segurança de nível enterprise, tomando como referência o relatório da NSA **[Model Context Protocol (MCP): Security Design Considerations for AI-Driven Automation](https://www.nsa.gov/Portals/75/documents/Cybersecurity/CSI_MCP_SECURITY.pdf)**.

> [!IMPORTANT]
> Este projeto é independente, educacional e não representa certificação, homologação ou conformidade oficial da NSA. O relatório apresenta riscos e recomendações; as decisões arquiteturais e implementações deste repositório são interpretações técnicas explicitamente documentadas.

## Objetivos

- Explicar os fundamentos do MCP antes de adicionar controles enterprise.
- Construir um MCP Server funcional usando TypeScript e o SDK oficial.
- Implementar um cenário corporativo fictício chamado **Enterprise Risk Knowledge MCP Server**.
- Relacionar recomendações da NSA a decisões, código e testes.
- Demonstrar falhas e proteções com testes de segurança reproduzíveis.
- Produzir um tutorial completo em português, desenvolvido junto com o código.

## Cenário do tutorial

O servidor fornecerá acesso controlado a políticas e casos fictícios de risco corporativo. As capacidades serão introduzidas progressivamente:

- `public.get_policy_summary`: consulta conteúdo público.
- `risk.search_cases`: pesquisa casos conforme o escopo do usuário.
- `risk.get_case_details`: consulta detalhes restritos.
- `risk.export_case_report`: exportação sensível sujeita a autorização e aprovação.

Nenhum dado real, pessoal, financeiro ou interno será utilizado.

## Método

Cada parte do tutorial seguirá o mesmo encadeamento:

1. Fundamento ou recomendação.
2. Risco que precisa ser tratado.
3. Decisão arquitetural.
4. Implementação TypeScript.
5. Teste e evidência.
6. Atualização do tutorial e da matriz de controles.

## Conteúdo

- [Índice do tutorial](./tutorial/README.md)
- [Parte 1 — Fundação, escopo e critérios](./tutorial/01-foundations.md)
- [Matriz de controles de segurança](./docs/security-controls-matrix.md)

## Fontes primárias

- [NSA — MCP Security Design Considerations](https://www.nsa.gov/Portals/75/documents/Cybersecurity/CSI_MCP_SECURITY.pdf)
- [MCP Specification](https://modelcontextprotocol.io/specification/)
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
- [Building an MCP Server](https://modelcontextprotocol.io/docs/develop/build-server)

## Status

**Parte 1 concluída:** fundação documental pronta para revisão. Ainda não existe implementação do MCP Server.

## Autora

**Glaucia Lemos**
