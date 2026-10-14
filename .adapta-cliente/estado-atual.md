# Estado atual — Adapta Cliente

- task_id: F1-T03
- champion: Nardelly
- spec: `04_fase-atual/specs/spec-1-002.md`
- etapa: em_correcao
- autorizacao_implementacao: confirmada em 2026-10-13 20:59 BRT — “Autorizo a implementação da F1-T03 conforme o plano apresentado, mantendo o checklist jurídico pendente de aprovação e usando apenas dados sintéticos.”
- teste_humano: falhou em 2026-10-14 08:24 BRT — Champion reportou “bene la urbano” e “bene la rural” e enviou captura do seletor aberto no preview correto (`central-de-processos-nardelly-65f79--preview.goskip.app/intake/nova`), na qual o menu nativo mostra opções visualmente corrompidas e o placeholder selecionado aparece duplicado.
- verificacao_automatica: pendente — substituição do `<select>` nativo pelo Select Radix existente em preparação; QA e reteste visual ainda não executados.
- aprendizado: capturado:`06_notas/aprendizado-continuo/AP-2026-10-13-2137-preservar-formulario-revalidacao.md`
- ultima_acao: confirmação da captura original e inspeção de `NovaFicha.tsx`: o campo de família usa `<select>` nativo, enquanto o projeto já tem componente Radix Select; valores de domínio `loas`, `urbano`, `rural` não estão errados.
- proxima_acao: trocar apenas o seletor de família para o componente Radix existente, retirar a opção vazia redundante do menu, verificar preview/QA e retornar ao teste humano.
- atualizado_em: 2026-10-14T08:59:14-03:00
