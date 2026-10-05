# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-05 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup.
- Jornada sincronizada: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks); parser PASS com `--require-ids`.
- **Ambiente de construção definido: Skip (GoSkip + SkipCloud)** — B-ENV-01 resolvido.
- **F1-T01 em `aguardando_teste_humano`** após correção das falhas reportadas pela Champion. QA técnico v0.0.10 e provas automatizadas/preview passaram; novo reteste humano dos critérios 3–5 pendente.
- Testes humanos originais 1 e 2 foram aprovados pela Champion; testes 3, 4 e 5 falharam, agora corrigidos tecnicamente e aguardam reteste/aceite.
- Dados reais bloqueados até a política de dados aprovada (B-POL-01); usar somente massa sintética.
- F1-T01 não está concluída; não iniciar F1-T02 até aceite humano explícito.

## Próximo passo
Nardelly retestar no preview (a) seletor e negação da administração por advogado, (b) sessões advogado/admin em abas distintas e cessação imediata após revogação via interface, (c) visualização da trilha com data/hora, ator, ação e estados anterior/novo; informar o resultado.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), B-CHK-01 (checklist jurídico v1), B-TIPO-01 (tipos representativos), B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (escolha do sistema) — detalhados nas SPECs. B-ENV-01 **resolvido**.