# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-13 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup.
- Jornada sincronizada: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks); parser PASS com `--require-ids`.
- **Ambiente de construção definido: Skip (GoSkip + SkipCloud)** — B-ENV-01 resolvido.
- **F1-T01 concluída (1/5 tasks; 20%)** em 2026-10-05, após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido:** campos da ficha aprovados com ajustes, em `06_notas/decisao-intake-campos-2026-10-13.md`.
- **F1-T02 concluída (2/5 tasks; 40%)** em 2026-10-13, com aceite humano “tudo funcionando” e revalidação CA-1-101; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`. Skip 0.0.11 está somente no preview, sem publicação em produção. No QA, `test.ran=false`; provas de API/preview e regressão estão discriminadas no recibo.
- **F1-T03 em `aguardando_autorizacao`:** B-TIPO-01 resolvido com cinco tipos rurais representativos: aposentadoria por idade rural; benefício por incapacidade permanente/temporária rural; salário-maternidade rural; pensão por morte rural; auxílio-reclusão rural.
- **Regra documental definida:** documentos da terra da página geral são condicionais ao contexto rural; não serão solicitados automaticamente em casos sem contexto rural/atividade na terra.
- **B-CHK-01 permanece aberto:** o PDF rural é exemplificativo/não exaustivo e não define quais provas são obrigatórias versus alternativas. Não se pode inventar checklist jurídico fechado. A decisão está em `06_notas/decisao-f1-t03-tipos-e-documentos-rurais-2026-10-13.md`.
- Baseline Skip v0.0.11: `pendencias` tem apenas `caso`, `descricao` e estados `aberta`/`resolvida`; não há coleções de checklist/protocolo nem workflow documental. Nenhuma implementação da F1-T03 foi iniciada.
- Pedido à parte: catálogo amplo de benefícios INSS continua fora da Fase 1/F1-T03, sem implementação.
- Dados reais proibidos até política B-POL-01; usar somente massa sintética.
- F1-T04 e F1-T05 não iniciadas; F1-T04 depende da conclusão da F1-T03.

## Próximo passo
Aguardar autorização explícita para implementar a F1-T03 com a estrutura da SPEC e plano B claramente rotulado: checklist versionado e itens demonstrativos sintéticos como `PENDENTE APROVAÇÃO JURÍDICA`, sem obrigatoriedade jurídica inventada; estados, protocolos, devolução, bloqueio, exceção auditada e demonstração dos cinco tipos.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), **B-CHK-01 (aprovação/condicionalidade jurídica final do checklist)**, B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (decisão do sistema). B-TIPO-01 resolvido; B-ENV-01 e B-INTAKE-01 resolvidos.
