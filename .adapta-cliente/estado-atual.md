# Estado atual — Adapta Cliente

- task_id: F1-T03
- champion: Nardelly
- spec: `04_fase-atual/specs/spec-1-002.md`
- etapa: em_correcao
- autorizacao_implementacao: confirmada em 2026-10-13 20:59 BRT — “Autorizo a implementação da F1-T03 conforme o plano apresentado, mantendo o checklist jurídico pendente de aprovação e usando apenas dados sintéticos.”
- teste_humano: falhou em 2026-10-14 12:03 BRT — Champion informou que, no reteste do preview 0.0.17, ainda vê “bene la urbano” e “bene ate rural”, em vez de “Benefício urbano” e “Benefício rural”.
- verificacao_automatica: versão 0.0.17 (`b299fc5`) tem QA anterior PASS em setup, análise estática, build e integrações; `test.ran=false`. Browser anterior viu rótulos corretos no snapshot acessível, mas reteste humano mostrou que defeito visual persiste. Nova reprodução visual é necessária; não mudar copy/domínio antes de investigar.
- aprendizado: capturado:`06_notas/aprendizado-continuo/AP-2026-10-14-1136-select-radix.md`
- ultima_acao: relato de falha humana na 0.0.17 reabriu o debug da mesma F1-T03; sintoma restrito à renderização visual dos rótulos urbano/rural, não ao placeholder `Selecione…`.
- proxima_acao: reproduzir o seletor aberto no preview 0.0.17, capturar imagem/DOM/CSS/console e isolar discrepância visual antes de editar.
- atualizado_em: 2026-10-14T12:05:38-03:00
