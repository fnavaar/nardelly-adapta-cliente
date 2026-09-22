# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-09-22 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup.
- Jornada sincronizada: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks); parser PASS com `--require-ids`.
- **Ambiente de construção definido: Skip (GoSkip + SkipCloud)** — regra geral do consultor (22/09); B-ENV-01 resolvido.
- **F1-T01 em `aguardando_teste_humano`**: implementação técnica concluída e verificações automáticas passaram; falta apenas o teste e aceite da champion.
- Dados reais bloqueados até a política de dados aprovada (B-POL-01); massa sintética até lá.
- F1-T01 ainda não está concluída: `[x]` e recibo só após aprovação humana explícita.

## Próximo passo
Nardelly executar o roteiro humano da F1-T01 no preview do Skip e informar se funcionou; não iniciar F1-T02 antes do aceite.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), B-CHK-01 (checklist jurídico v1), B-TIPO-01 (tipos representativos), B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (escolha do sistema) — detalhados nas SPECs. B-ENV-01 **resolvido** (Skip, 22/09).