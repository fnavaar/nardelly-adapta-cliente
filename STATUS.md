# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-13 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup.
- Jornada sincronizada: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks); parser PASS com `--require-ids`.
- **Ambiente de construção definido: Skip (GoSkip + SkipCloud)** — B-ENV-01 resolvido.
- **F1-T01 concluída (1/5 tasks da fase; 20%)** em 2026-10-05 após aprovação humana explícita e revalidação dos critérios CA-1-001..005. Recibo em `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 RESOLVIDO (2026-10-13):** Champion aprovou "com ajustes" a definição de campos da ficha de intake (18 obrigatórios, condicionais e opcionais; bloco específico por família LOAS/urbano/rural). Decisão em `06_notas/decisao-intake-campos-2026-10-13.md`.
- **F1-T02 com análise concluída** (plano, riscos e provas apresentados em 2026-10-13): aguardando autorização explícita de implementação. Nada implementado.
- Dados reais bloqueados até a política de dados aprovada (B-POL-01); usar somente massa sintética.
- F1-T03..F1-T05 não iniciadas; F1-T03 também depende de F1-T02 e de B-CHK-01/B-TIPO-01.

## Próximo passo
Champion autorizar a implementação da F1-T02; após implementação e verificações automáticas, apresentar roteiro de teste humano.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), B-CHK-01 (checklist jurídico v1), B-TIPO-01 (tipos representativos), B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (escolha do sistema) — detalhados nas SPECs. B-ENV-01 **resolvido**; B-INTAKE-01 **resolvido**.
