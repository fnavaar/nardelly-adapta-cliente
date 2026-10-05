# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-05 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup.
- Jornada sincronizada: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks); parser PASS com `--require-ids`.
- **Ambiente de construção definido: Skip (GoSkip + SkipCloud)** — B-ENV-01 resolvido.
- **F1-T01 concluída (1/5 tasks da fase; 20%)** em 2026-10-05 após aprovação humana explícita e revalidação dos critérios CA-1-001..005. Recibo em `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **F1-T02 selecionada e bloqueada antes da implementação**: CA-1-101/RN-101 dependem da lista aprovada de dados mínimos obrigatórios do intake; a SPEC e o esquema atual não especificam essa lista. Não inventar campos. Champion/jurídico deve definir a regra antes de nova análise de implementação.
- Dados reais bloqueados até a política de dados aprovada (B-POL-01); usar somente massa sintética.
- F1-T03..F1-T05 não iniciadas; F1-T03 também depende de F1-T02 e de B-CHK-01/B-TIPO-01.

## Próximo passo
Obter e registrar os campos mínimos obrigatórios do intake, incluindo quais faltas devem gerar pendências. Após essa decisão, retomar a análise da F1-T02; a autorização para implementar será solicitada separadamente.

## Bloqueios ativos
B-INTAKE-01 (campos obrigatórios do intake não definidos; impede demonstrar CA-1-101/RN-101), B-POL-01 (política de dados), B-RACI-01 (nomes por papel), B-CHK-01 (checklist jurídico v1), B-TIPO-01 (tipos representativos), B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (escolha do sistema) — detalhados nas SPECs. B-ENV-01 **resolvido**.
