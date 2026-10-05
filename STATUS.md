# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-05 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup.
- Jornada sincronizada: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks); parser PASS com `--require-ids`.
- **Ambiente de construção definido: Skip (GoSkip + SkipCloud)** — B-ENV-01 resolvido.
- **F1-T01 concluída (1/5 tasks da fase; 20%)** em 2026-10-05 após aprovação humana explícita da Champion e revalidação dos critérios CA-1-001..005. Recibo em `05_entregas/recibo-f1-t01-2026-10-05.md`.
- QA Skip v0.0.10 passou em setup, análise estática, build, integrações e testes; provas de API/preview confirmaram autenticação dos sete papéis, segregação, trilha, autoelevação negada e revogação imediata.
- Dados reais bloqueados até a política de dados aprovada (B-POL-01); seguir usando somente massa sintética.
- **F1-T02..F1-T05 ainda não iniciadas.** F1-T02 depende da aceitação da F1-T01; só iniciar após novo pedido da Champion.
- A conclusão desta task não encerra a Fase 1; as demais tasks e validação do consultor continuam pendentes.

## Próximo passo
Aguardar novo pedido da Nardelly para analisar a F1-T02. Não começar trabalho novo automaticamente.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), B-CHK-01 (checklist jurídico v1), B-TIPO-01 (tipos representativos), B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (escolha do sistema) — detalhados nas SPECs. B-ENV-01 **resolvido**.
