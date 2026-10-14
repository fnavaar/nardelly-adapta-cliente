# Estado atual — Adapta Cliente

- task_id: F1-T03
- champion: Nardelly
- spec: `04_fase-atual/specs/spec-1-002.md`
- etapa: em_correcao
- autorizacao_implementacao: confirmada em 2026-10-13 20:59 BRT — “Autorizo a implementação da F1-T03 conforme o plano apresentado, mantendo o checklist jurídico pendente de aprovação e usando apenas dados sintéticos.”
- teste_humano: falhou em 2026-10-13 21:15 BRT — “Tenho tido problemas, além de os nomes dos campos estarem diferentes, quando eu mudo de aba, perco todo o progresso que tive no preenchimento dos dados.”
- verificacao_automatica: versão estável disponível no preview é Skip 0.0.13 (`dfa77aa`); `test.ran=false`. Diagnóstico estático confirma que `NovaFicha.tsx` mantém os valores somente em estado React local e não salva rascunho. Ainda não reproduzido se alternar uma aba do navegador, navegar para outra tela/aba interna ou recarregar causa o descarte; discrepâncias de rótulos ainda serão comparadas com as três fichas de atendimento.
- aprendizado: capturado:`06_notas/aprendizado-continuo/AP-2026-10-13-1953-qa-skip-suite-not-executed.md`
- ultima_acao: teste humano reprovou F1-T03 por nomes de campos divergentes e perda de preenchimento ao mudar de aba; task permanece aberta em correção.
- proxima_acao: reproduzir no preview separadamente alternância de aba do navegador, navegação para fora/retorno e recarga; confirmar diferenças dos rótulos frente às fichas de origem.
- atualizado_em: 2026-10-13T21:19:13-03:00
