# Matriz de controles de segurança

Esta matriz conecta as recomendações do relatório da NSA às decisões que serão implementadas e testadas no projeto. Ela evoluirá durante o tutorial.

> [!NOTE]
> Uma linha marcada como planejada não representa um controle implementado. A coluna de evidência somente será preenchida depois que o teste correspondente existir e passar.

| ID | Recomendação da NSA | Risco tratado | Decisão planejada | Código | Teste/evidência | Status |
|---|---|---|---|---|---|---|
| NSA-01 | Escolher projetos MCP suportados | Dependências abandonadas ou vulneráveis | Usar SDK oficial, inventariar versões e automatizar análise de dependências | A definir | A definir | Planejado |
| NSA-02 | Projetar fronteiras de confiança | Propagação indevida e vazamento entre zonas | Separar tools públicas, internas, restritas e sensíveis | A definir | A definir | Planejado |
| NSA-03 | Validar parâmetros e contexto | Injection, forwarding e DoS | Schemas estritos, limites, allowlists e rejeição de campos desconhecidos | A definir | A definir | Planejado |
| NSA-04 | Restringir e isolar execução | RCE, movimento lateral e escalada | Privilégio mínimo, sandbox e egress controlado | A definir | A definir | Planejado |
| NSA-05 | Assinar e verificar mensagens sensíveis | Tampering, replay e reexecução | Expiração, nonce, idempotência e assinatura no limite apropriado | A definir | A definir | Planejado |
| NSA-06 | Filtrar e monitorar outputs | Indirect prompt injection e tool poisoning | Tratar output como não confiável antes do próximo estágio | A definir | A definir | Planejado |
| NSA-07 | Instrumentar logs e detecção | Falta de responsabilização e resposta forense | Auditoria estruturada com identidade, parâmetros seguros e hashes | A definir | A definir | Planejado |
| NSA-08 | Rastrear e corrigir vulnerabilidades | Exposição a CVEs conhecidas | Inventário, política de atualização e verificação contínua | A definir | A definir | Planejado |
| NSA-09 | Localizar servidores MCP expostos | Serviços não autorizados ou sem autenticação | Documentar descoberta, binding seguro e controles de implantação | A definir | A definir | Planejado |

## Riscos adicionais destacados no relatório

Além das recomendações, o tutorial acompanhará explicitamente:

- controle de acesso fraco ou ausente;
- serialização e contexto inseguros;
- fluxos de aprovação inadequados;
- segurança de tokens e sessões;
- comportamento inconsistente entre componentes;
- logs insuficientes;
- negação de serviço e fatigue-based techniques;
- tool parameter injection;
- tool invocation path confusion;
- tool poisoning e propagação para sistemas downstream;
- vulnerabilidades na toolchain e supply chain.

## Regra de atualização

Cada parte do tutorial deverá atualizar pelo menos uma linha desta matriz quando introduzir ou verificar um controle.

## Fonte

- [NSA — MCP Security Design Considerations, maio de 2026](https://www.nsa.gov/Portals/75/documents/Cybersecurity/CSI_MCP_SECURITY.pdf)
