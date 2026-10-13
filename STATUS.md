# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-13 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **Champion: @Nardelly — confirmado por Navaar em 22/09/2026.** Nomes por papel da operação (B-RACI-01) a definir na call de setup.
- Jornada sincronizada: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks); parser PASS com `--require-ids`.
- **Ambiente de construção definido: Skip (GoSkip + SkipCloud)** — B-ENV-01 resolvido.
- **F1-T01 concluída (1/5 tasks; 20%)** em 2026-10-05 após aprovação humana explícita e revalidação dos critérios CA-1-001..005. Recibo em `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 RESOLVIDO (2026-10-13):** Champion aprovou "com ajustes" a definição de campos da ficha de intake (18 obrigatórios, condicionais e opcionais; bloco específico por família LOAS/urbano/rural). Decisão em `06_notas/decisao-intake-campos-2026-10-13.md`.
- **F1-T02 concluída (2/5 tasks; 40%)** em 2026-10-13, com aceite humano explícito (“tudo funcionando”) e revalidação de CA-1-101; recibo em `05_entregas/recibo-f1-t02-2026-10-13.md`. Skip 0.0.11 está no preview; produção não publicada. A etapa `test` do QA retornou `ran=false`; as provas API/preview e regressão foram executadas à parte e estão discriminadas no recibo.
- **F1-T03 bloqueada por B-CHK-01 e B-TIPO-01:** a SPEC-1-002 requer checklist jurídico v1 aprovado e lista de tipos de demanda representativos para demonstrar o fluxo; esses insumos ainda não constam nas notas operacionais. A Champion informou que fornecerá os dados posteriormente. O projeto atual tem coleção de pendências mínima (`caso`, `descricao`, `status` aberta/resolvida), sem coleções de checklist/protocolo nem fluxo de estados documentais. Nenhuma implementação da F1-T03 foi iniciada.
- **Solicitação adicional após aceite:** tornar “Tipo de benefício” um campo selecionável com catálogo de benefícios do INSS agrupado por família. Registrada no changelog para análise de escopo/fonte; não implementada nem incorporada ao escopo F1-T02. A SPEC-1-002 diz que o catálogo amplo é fora de escopo da Fase 1 e pertence à Fase 2.
- Dados reais bloqueados até a política de dados aprovada (B-POL-01); usar somente massa sintética.
- F1-T04..F1-T05 não iniciadas; F1-T04 depende de F1-T03 aceita; F1-T05 depende de B-ADV-01/B-ADVBOX-ADVOX.

## Próximo passo
Aguardar da Champion o checklist jurídico v1 (B-CHK-01) e a lista de tipos representativos de demanda (B-TIPO-01). Com os dois insumos, retomar análise da F1-T03; implementação exige autorização separada.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), **B-CHK-01 (checklist jurídico v1; pendente da Champion/jurídico)**, **B-TIPO-01 (tipos representativos; pendente da Champion)**, B-BASE-01 (baseline), B-ADV-01 (acesso ADVBOX), B-ADVBOX-ADVOX (escolha do sistema) — detalhados nas SPECs. B-ENV-01 **resolvido**; B-INTAKE-01 **resolvido**.
