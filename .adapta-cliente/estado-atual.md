# Estado atual — Adapta Cliente

- task_id: F1-T03
- champion: Nardelly
- spec: `04_fase-atual/specs/spec-1-002.md`
- etapa: aguardando_teste_humano
- autorizacao_implementacao: confirmada em 2026-10-13 20:59 BRT — “Autorizo a implementação da F1-T03 conforme o plano apresentado, mantendo o checklist jurídico pendente de aprovação e usando apenas dados sintéticos.”
- teste_humano: pendente — o teste de 2026-10-13 21:15 BRT falhou; reteste solicitado após correção de rótulos e perda de rascunho em 0.0.15.
- verificacao_automatica: QA Skip 0.0.15 (`214bb2c`) passou em setup, análise estática, build e integrações; `test.ran=false`, a plataforma não executou a suíte. Preview testado: um valor sintético em “Nome da pessoa que está sendo atendida” permaneceu após alternar à segunda aba e retornar. Rótulos revisados aparecem no preview. Nenhum formulário foi enviado; dados sintéticos apenas. Produção não publicada.
- aprendizado: capturado:`06_notas/aprendizado-continuo/AP-2026-10-13-2137-preservar-formulario-revalidacao.md`
- ultima_acao: falha humana investigada e corrigida. A revalidação de sessão ao recuperar foco agora mantém a tela montada e bloqueia interação até a confirmação do servidor. Principais rótulos foram alinhados às fichas enviadas. Evidência e limites em `06_notas/debug/debug-2026-10-13-f1-t03.md`.
- proxima_acao: Champion testar a versão 0.0.15 no preview, especialmente alternância de aba, revalidação visual, rótulos e fluxo documental; informar aprovação ou falha remanescente.
- atualizado_em: 2026-10-13T21:38:25-03:00
