# 00-Tasks_Gerais — Fase 1 · Nardelly Advogados (Plano 2763bf86)

**Gerado em:** 2026-09-22 · **Fonte:** SPECs 1-001..004 (Drive) · **Projeção operacional** — o canônico dos campos do card é a Jornada `fase_1.md` (fase-format:2)

## Tasks

| ID | Task | SPEC | Critérios | Leva | Pré-condições | Ponto de parada | Evidência esperada | Status |
|---|---|---|---|---|---|---|---|---|
| F1-T01 | Implantar o acesso da equipe com papéis e trilha de auditoria | SPEC-1-001 | CA-1-001..005 | 1 | B-ENV-01 autorizado | ambiente sem controle no servidor | logs das provas negativas + recibo | ☐ |
| F1-T02 | Estruturar o recebimento de casos: ficha de intake e cadastro completo | SPEC-1-002 | CA-1-101 | 2 | F1-T01 aceita | campo obrigatório não definido | captura + trilha + recibo | ☐ |
| F1-T03 | Controlar documentos de cada caso com checklist, protocolo e devolução | SPEC-1-002 | CA-1-102..106 | 3 | F1-T02 aceita; B-CHK-01/B-TIPO-01 | conteúdo jurídico não aprovado | roteiro da demonstração + recibo | ☐ |
| F1-T04 | Medir a operação: árvore de funil, estoque e baseline | SPEC-1-003 | CA-1-201..205 | 4 | F1-T03 aceita | nó da árvore sem marco definido | contagem conferida + capturas + recibo | ☐ |
| F1-T05 | Provar a conexão com o ADVBOX antes de qualquer integração | SPEC-1-004 | CA-1-401..405 | 4 | B-ADV-01 + B-ADVBOX-ADVOX | acesso não concedido / custo contratual | relatório + varredura + recibo | ☐ |

## Regras de execução

- **Uma task por vez**; ao concluir, provas + teste humano antes da próxima; `[x]` somente com evidência e aceite.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup; prazos a definir com fonte humana — não inventados.
- Cobertura: CA-1-001..005 + CA-1-101..106 + CA-1-201..205 + CA-1-401..405 = 20/20 (SPEC-1-001: T01; SPEC-1-002: T02..T03; SPEC-1-003: T04; SPEC-1-004: T05).
- Grafo: T01→T02→T03→T04; T05 paralelizável a partir de T01, mas uma task por vez.
- UUIDs gerados pelo portal na Jornada canônica (`00.tasks_per_fase/fase_1.md`): T01 `53479f4d-5f1b-405d-a40d-ca4ab56659dc` (+ subtasks `bb8dac49-2db0-4ef4-9a62-2b73bcfa813a`, `0feb7b0d-3073-48dc-ab7d-a499cf1ab139`), T02 `8a429a35-da91-4ecf-80bf-6d29d07da255`, T03 `40f16555-9f24-45d2-bb49-5ede691f41e4`, T04 `4babdba4-e217-4701-959b-924eefb7c5ea`, T05 `680b9453-0196-421e-bc3e-edb1f0fde7e5`. Não criar, reutilizar ou apagar UUIDs manualmente.
