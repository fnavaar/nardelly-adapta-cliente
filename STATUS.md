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
- **F1-T03 bloqueada; insumo B-CHK-01 parcialmente recebido:** Champion esclareceu que a página 1 do PDF enviado contém a lista geral, e as páginas 2–5 são “Provas Rurais”, exemplificativas/não exaustivas. O documento inclui imagens de exemplos com dados identificáveis, não copiadas para o repositório. Ainda é necessário definir se os documentos da terra listados na página 1 são universais ou condicionais a casos rurais/atividade na terra.
- **B-TIPO-01 continua pendente:** Champion precisa indicar os tipos representativos de demanda para a demonstração. O rol rural não exaustivo não substitui essa seleção.
- Baseline Skip v0.0.11: `pendencias` tem apenas `caso`, `descricao` e estados `aberta`/`resolvida`; ainda não há coleções para checklist/protocolo nem workflow documental. Não foi feita implementação da F1-T03.
- Pedido à parte: tornar “Tipo de benefício” seletor com todos os benefícios do INSS por família. Catálogo amplo está fora da Fase 1 segundo a SPEC-1-002; sem implementação e sujeito à decisão de escopo/fonte.
- Dados reais proibidos até política B-POL-01; seguir usando só fixtures sintéticas.
- F1-T04 e F1-T05 não iniciadas; F1-T04 depende da conclusão da F1-T03.

## Próximo passo
Champion indicar (a) os tipos representativos para a demonstração; (b) se “documentos da terra” da página 1 são aplicáveis a todo caso ou só a casos com contexto rural/atividade na terra. Então retomar a análise da F1-T03 e pedir autorização separada antes de implementar.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), B-CHK-01 (aprovação/condicionalidade final do checklist), **B-TIPO-01 (tipos representativos, pendente da Champion)**, B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (decisão do sistema). B-ENV-01 e B-INTAKE-01 resolvidos.
