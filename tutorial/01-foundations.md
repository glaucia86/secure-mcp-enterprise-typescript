# Parte 1 — Fundação, escopo e critérios do projeto

## O que construiremos

Construiremos progressivamente um **MCP Server em TypeScript** chamado **Enterprise Risk Knowledge MCP Server**. Ele simulará o acesso a políticas e casos corporativos de risco com diferentes níveis de sensibilidade.

O objetivo não é apresentar uma arquitetura universal. O objetivo é criar um laboratório reproduzível no qual seja possível observar como decisões inseguras surgem e como controles enterprise podem reduzir esses riscos.

## Por que começar pela fundação

O relatório da NSA destaca que a postura de segurança do MCP depende fortemente da disciplina da implementação. Autenticação, autorização, validação, isolamento, observabilidade e ciclo de vida não podem ser presumidos apenas porque uma integração utiliza MCP.

Por isso, começar diretamente pelo SDK produziria um servidor funcional sem responder às perguntas mais importantes:

- Quem pode invocar cada tool?
- Quais dados cada tool pode acessar?
- Em qual fronteira um dado deixa de ser confiável?
- O que exige aprovação humana?
- Como detectar repetição, abuso ou comportamento inesperado?
- Que evidência mostrará que um controle funciona?

## Público-alvo

Este tutorial é destinado a pessoas desenvolvedoras que:

- conhecem JavaScript ou TypeScript;
- entendem APIs e aplicações backend;
- querem aprender MCP desde os fundamentos;
- precisam avaliar MCP em ambientes corporativos ou regulados;
- desejam conectar segurança arquitetural à implementação.

Não é necessário conhecimento prévio de MCP. Conceitos de segurança serão apresentados no momento em que se tornarem necessários.

## O que significa enterprise neste projeto

Neste tutorial, **enterprise** não significa adicionar várias ferramentas ou tornar o código excessivamente complexo. Significa considerar explicitamente:

- identidade e autorização granular;
- separação entre zonas e classificações de dados;
- privilégio mínimo;
- aprovação para operações de maior impacto;
- rastreabilidade e resposta a incidentes;
- limites de recursos e resiliência;
- gestão de dependências e vulnerabilidades;
- testes de abuso, além do caminho feliz.

## Cenário fictício

A empresa fictícia **Northstar Financial Services** mantém políticas corporativas e casos internos de risco. O MCP Server disponibilizará quatro capacidades progressivas:

| Tool | Classificação inicial | Propósito | Risco principal |
|---|---|---|---|
| `public.get_policy_summary` | Pública | Resumir políticas públicas | Conteúdo malformado ou envenenado |
| `risk.search_cases` | Interna | Pesquisar casos permitidos | Enumeração e vazamento entre escopos |
| `risk.get_case_details` | Restrita | Consultar detalhes de um caso | Broken access control |
| `risk.export_case_report` | Sensível | Exportar relatório | Exfiltração e ação sem consentimento |

Os nomes, usuários, políticas e casos serão inteiramente fictícios.

## Limites da afirmação

Este projeto:

- usa o documento da NSA como fonte primária de riscos e recomendações;
- cria uma interpretação técnica dessas recomendações em TypeScript;
- mantém rastreabilidade entre fonte, decisão, implementação e teste;
- não afirma que a NSA revisou, aprovou ou certificou a solução;
- não substitui threat modeling, revisão jurídica, AppSec ou arquitetura de uma organização real.

## Pergunta central

> Como evoluir um MCP Server simples em TypeScript para um exemplo corporativo no qual confiança, identidade, dados, execução e evidências de segurança sejam tratados explicitamente?

## Hipóteses iniciais

Estas hipóteses serão confirmadas ou corrigidas durante o tutorial:

1. O protocolo e o SDK não substituem os controles da aplicação e da infraestrutura.
2. Toda entrada de usuário, cliente, tool ou componente anterior atravessa uma fronteira de confiança.
3. Uma saída de tool pode se tornar entrada perigosa para o próximo componente.
4. Capacidade técnica não implica autorização para executar.
5. Operações repetidas precisam considerar idempotência e replay.
6. Um controle sem teste ou evidência é apenas uma intenção.

## Critérios de sucesso

Ao final, o leitor deverá conseguir:

- explicar a arquitetura básica do MCP;
- executar e inspecionar um MCP Server em TypeScript;
- reconhecer os riscos principais descritos pela NSA;
- implementar e testar controles proporcionais ao risco;
- distinguir protocolo, SDK, aplicação, gateway e infraestrutura;
- adaptar a matriz de rastreabilidade a outro domínio.

## Estratégia incremental

Começaremos com os fundamentos e um servidor mínimo. Em seguida, adicionaremos o domínio fictício e apenas depois introduziremos as proteções em fatias verticais. Cada fatia deverá atravessar explicação, código, teste e documentação.

## Entregas desta parte

- escopo e finalidade definidos;
- cenário fictício escolhido;
- significado de enterprise delimitado;
- disclaimers registrados;
- índice progressivo criado;
- matriz inicial de controles criada;
- implementação adiada conscientemente para a Parte 3.

## Próxima parte

Na [Parte 2](./README.md), estudaremos o modelo mental do MCP: host, client, server, tools, resources, prompts, mensagens e transportes. Ainda não adicionaremos controles enterprise antes de compreender o protocolo.

## Referências

- [NSA — Model Context Protocol (MCP): Security Design Considerations for AI-Driven Automation](https://www.nsa.gov/Portals/75/documents/Cybersecurity/CSI_MCP_SECURITY.pdf)
- [MCP Specification](https://modelcontextprotocol.io/specification/)
- [MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
