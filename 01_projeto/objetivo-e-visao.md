# Objetivo e visão do projeto

## Objetivo
Construir uma central operacional simples e auditável que reúna as atividades, informações, documentos, pendências, responsáveis, prazos e decisões de rota dos casos previdenciários — reduzindo retrabalho e perda de contexto e tornando clara a posição de cada caso para a equipe.

## Métrica norte
Árvore de funil (DH-01): entradas → cadastro completo → documentação → triagem → rota definida → distribuição administrativa/judicial, com tempos entre marcos, retrabalho, pendências vencidas e casos sem próxima ação. Baseline a certificar na Fase 1 (B-BASE-01) com fonte, período e denominador.

## Fases
1. **Fase 1 — Fundação segura, intake e registro documental:** acesso/papéis/auditoria, ficha de intake, cadastro de caso, checklist versionado, pendência documental única, protocolo, baseline e prova técnica do ADVBOX.
2. **Fase 2 — Regras, roteamento, filas e migração controlada:** catálogo amplo versionado, roteamento determinístico aprovado, SLA/urgência/alçadas, migração do estoque em ondas.
3. **Fase 3 — Integrações, comunicação e visão ponta a ponta:** ADVBOX e demais integrações provadas, sincronização idempotente, mensagens aprovadas, painel ponta a ponta.
4. **Fase 4 — Loops e agentes operacionais:** saúde das pendências, qualidade documental, confiabilidade das integrações, capacidade e fluxo; busca assistida condicionada.
5. **Fase 5 — Validação integral** do conjunto F1–F4.

## Regras do jogo
- A decisão jurídica (direito, enquadramento, prova, via, conteúdo) é sempre humana e identificada.
- A central é o sistema mestre e canal oficial (DH-06); integrações só entram quando provadas.
- Dados reais somente após política aprovada, matriz de acesso testada e ambiente autorizado (DH-04).
- Nenhuma API, permissão ou comportamento é presumido sem prova técnica (ADVBOX e demais).
