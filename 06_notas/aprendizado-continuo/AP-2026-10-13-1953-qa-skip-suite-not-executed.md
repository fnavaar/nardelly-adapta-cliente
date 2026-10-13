# AP-2026-10-13-1953 — Diferenciar QA executado de suíte não executada

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T02 / SPEC-1-002
- Sinal: no resultado de `skip_project_apply_changes` da versão 0.0.11, setup, análise estática, build e integrações vieram com `ok: true`, enquanto a etapa `test` retornou `ok: true` e `ran: false`. Portanto, o pipeline aceitou a versão sem executar a suíte de testes do projeto.
- Evidência: resposta observada do QA Skip 60649 v0.0.11; ressalva descrita no recibo `05_entregas/recibo-f1-t02-2026-10-13.md`; CA-1-101 revalidado separadamente por API com caso sintético, exatamente uma pendência e evento RN-101 correspondente.
- Regra reutilizável: não declarar “testes passaram” quando `qa.test.ran` é falso. Registrar as etapas do pipeline que passaram, dizer explicitamente que a suíte não rodou e citar separadamente as provas manuais/API efetivamente executadas.
- Quando aplicar: conclusão de qualquer QA Skip cujo resultado contenha `test.ran: false`.
- Quando não aplicar: quando `test.ran: true`; nesse caso, reportar o resultado real da suíte.
- Confiança: alta — baseada diretamente no resultado estruturado do pipeline observado nesta versão.
- Privacidade: sem segredo, dado pessoal ou conteúdo bruto.
