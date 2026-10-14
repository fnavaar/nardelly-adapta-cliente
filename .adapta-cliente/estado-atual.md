# Estado atual — Adapta Cliente

- task_id: F1-T03
- champion: Nardelly
- spec: `04_fase-atual/specs/spec-1-002.md`
- etapa: em_correcao
- autorizacao_implementacao: confirmada em 2026-10-13 20:59 BRT — “Autorizo a implementação da F1-T03 conforme o plano apresentado, mantendo o checklist jurídico pendente de aprovação e usando apenas dados sintéticos.”
- teste_humano: falhou em 2026-10-13 21:15 BRT — a Champion relatou que os nomes dos campos estão diferentes e que perde o progresso do preenchimento ao mudar de aba.
- verificacao_automatica: última versão aprovada pela pipeline foi 0.0.13; suíte de testes não executada (`test.ran=false`). Início de diagnóstico: leitura estática de `src/pages/NovaFicha.tsx` confirmou que os valores da ficha vivem apenas em estado React local; nenhuma persistência de rascunho foi implementada. Ainda falta reproduzir separadamente alternância de abas, navegação/retorno e possível recarga no preview, além de comparar rótulos com as três fichas originais.
- aprendizado: capturado:`06_notas/aprendizado-contínuo/AP-2026-10-13-1953-qa-skip-suite-not-executed.md`
- ultima_acao: teste humano da F1-T03 reportou discrepância nos nomes dos campos e perda de preenchimento ao trocar de aba; task mantida aberta para correção, sem iniciar outra.
- proxima_acao: reproduzir no preview os cenários de mudança de aba e validar os rótulos do intake contra as fichas de origem antes de escolher a correção mínima.
- atualizado_em: 2026-10-13T21:19:13-03:00
