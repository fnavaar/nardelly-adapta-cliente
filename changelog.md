# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-13 — F1-T03 analisada; bloqueada por insumos jurídicos/operacionais
- F1-T02 foi aceita pela Champion (“tudo funcionando”) e encerrada com recibo `05_entregas/recibo-f1-t02-2026-10-13.md`; a revalidação final CA-1-101 comprovou que um único campo obrigatório ausente gera exatamente uma pendência correspondente e evento RN-101 de auditoria.
- F1-T03 é a próxima tarefa da sequência e exige CA-1-102..106: checklist versionado por tipo, seis estados de pendência documental, protocolo de recebimento, devolução com motivo/orientação aprovada, bloqueio de avanço e exceção jurídica justificada/auditada.
- Baseline somente leitura no Skip 60649 v0.0.11: existem coleções `casos`, `pessoas`, `pendencias` e `auditoria`; a coleção `pendencias` ainda só tem `caso`, `descricao` e status `aberta`/`resolvida`. Não há coleções de checklist/protocolo nem fluxo documental; nenhuma alteração do produto foi realizada.
- **Bloqueios ativos:** B-CHK-01 — checklist jurídico v1 precisa ser fornecido/aprovado pelo advogado responsável/Champion; B-TIPO-01 — lista de tipos de demanda representativos da demonstração precisa ser fornecida pela Champion. A Champion informou que fornecerá os insumos posteriormente.
- A SPEC-1-002 permite construir estrutura com checklist vazio identificado `PENDENTE APROVAÇÃO JURÍDICA`, mas CA-1-102..106 e a demonstração exigem os insumos aprovados e tipos representativos; sem ambos não se pode validar o comportamento final nem concluir a task. Não substituir com conteúdo jurídico inventado ou exemplos não aprovados.
- Estado `.adapta-cliente/estado-atual.md`: F1-T03 `bloqueada`; sem autorização de implementação. STATUS atualizado; aguardar os dois insumos, depois retomar análise e solicitar autorização separada.
- Pedido anterior sobre “Tipo de benefício” — catálogo do INSS agrupado por família — continua independente e sem implementação. Não misturar ao escopo da F1-T03 sem decisão formal do consultor.

## 2026-10-13 — F1-T02 concluída; novo pedido de catálogo amplo encaminhado à decisão de escopo
- Após receber o roteiro de teste humano da F1-T02, a Champion declarou “tudo funcionando”. A aprovação cobre a ficha de intake, geração de pendências e trilha observadas no preview.
- Revalidação CA-1-101: caso sintético com todos os obrigatórios preenchidos, exceto “Profissão atual”, gerou exatamente uma pendência para esse campo; consulta administrativa confirmou um evento de auditoria correspondente com ator `sistema (RN-101)`. Caso e valores são sintéticos.
- Skip 0.0.11 continua no preview e não publicado. Migração 0005 consta `applied`; status Skip conserva `.skip.config.json` como alteração pendente (preexistente e não alterada).
- Regressão F1-T01 reexecutada: sete logins; três negações 403; autoelevação 403; revogação 200→401; fixture reativada após a prova.
- Fechamento do QA descrito com precisão: setup/análise estática/build/integrações OK; `qa.test.ran=false`, portanto a suíte de testes do projeto não rodou.
- Recibo criado em `05_entregas/recibo-f1-t02-2026-10-13.md`; tabela operacional e STATUS atualizados: F1-T02 concluída, 2/5 tarefas da fase (40%).
- **Novo pedido, após aprovação:** Champion deseja que “Tipo de benefício” seja um seletor com todos os benefícios do INSS, agrupados por família. Sem implementação. A SPEC-1-002 classifica catálogo amplo de tipos como fora do escopo da Fase 1/F1-T02 e associado à Fase 2; levar ao consultor para definir escopo apropriado e fonte oficial atualizada antes de qualquer código.

## 2026-10-13 — F1-T02 implementada (RN-101); aguardando teste humano
- Autorização explícita da Champion (“autorizado”, 2026-10-13 19:16 BRT) posterior ao relatório de análise; etapa `implementando` registrada antes da primeira alteração.
- RED confirmado: caso incompleto criado no estado anterior sem gerar pendências (0 registros) — falha que motiva CA-1-101.
- Implementação no projeto Skip 60649, versão 0.0.11 (QA setup, análise estática, build e integrações passaram; a suíte de testes do projeto não rodou, `qa.test.ran=false`):
  - Migração 0005: campos aprovados do intake em `casos` e nova coleção `pessoas`.
  - Hook `intake_pendencias` (RN-101, after-success): pendências explícitas por obrigatório ausente, condicionais, tarefa de nova senha do MEU INSS quando vazia, auditoria e erro logado.
  - Telas `/intake/nova` e `/caso/:id`; link “Nova ficha de intake” para Atendimento/Cadastro.
- GREEN confirmado por API; regressão F1-T01 completa PASS (7 logins, 3 negações 403 auditadas, autoelevação 403, revogação 200→401, fixture reativada).
- Estado então: `aguardando_teste_humano`; F1-T02 não concluída até aceite explícito.

## 2026-10-13 — B-INTAKE-01 resolvido; F1-T02 pronta para autorização
- Champion aprovou a proposta dos campos de intake “com ajustes”: indicação obrigatória; senha MEU INSS opcional com tarefa automática de nova senha; sindicato condicional; escolaridade, profissão e parente já atendido obrigatórios; grupo familiar LOAS sem limite fixo.
- Definição resultante: 18 obrigatórios, condicionais e opcionais; blocos específicos LOAS/urbano/rural em `06_notas/decisao-intake-campos-2026-10-13.md`.
- Análise entregue; nenhuma implementação iniciada antes da autorização separada.

## 2026-10-05 — F1-T02 analisada; bloqueada por definição de intake
- F1-T01 concluída (1/5 tasks, 20%).
- F1-T02 selecionada, sem implementação. SPEC-1-002 CA-1-101/RN-101 exigiam pendências por obrigatório ausente, mas não enumeravam campos.
- DÚVIDA/B-INTAKE-01 registrada: Champion/jurídico precisava definir campos obrigatórios e condicionais.

## 2026-10-05 — F1-T01 concluída após aprovação humana
- Champion confirmou “Teste aprovado” após o roteiro dos critérios 3–5; os testes 1–2 também já haviam sido aprovados.
- Revalidação: sete logins; negações HTTP 403 para três papéis; negações auditadas; autoelevação bloqueada; revogação HTTP 200→401; fixture reativada.
- QA Skip 0.0.10 passou; recibo em `05_entregas/recibo-f1-t01-2026-10-05.md`. Estado fase: 1/5 (20%).

## 2026-10-05 — F1-T01 debug: falhas humanas corrigidas
- Causas: sessão PocketBase compartilhada via localStorage entre abas, rota administrativa sem role-check, login sempre encaminhava para admin e auditoria não tinha UI.
- Correções v0.0.10: sessão isolada por aba, refresh/validação de papel, bloqueio server-side, fixtures sintéticas e `/auditoria`.
- Verificações: QA passou; advogado bloqueado em `/admin/usuarios`; isolamento de sessão e auditoria visíveis no preview.

## 2026-09-22 — F1-T01 implementada; aguardando teste humano
- Projeto Skip 60649 criado; sete papéis, RBAC/RLS server-side, auditoria append-only e fixtures sintéticas.
- QA v0.0.9 passou; provas de API passaram. Gate humano permanecia pendente.

## 2026-09-22 — DEBUG F1-T01: causas técnicas corrigidas
- Falhas iniciais em schema, RLS, autodates, rate limit e revogação; correções nas migrações 0003/0004 e hooks. Validação final v0.0.9 passou.

## 2026-09-22 — Champion confirmado e handoff operacional
- Champion @Nardelly confirmado; jornada fase 1 validada; repo `fnavaar/nardelly-adapta-cliente` criado para operação do cliente.
