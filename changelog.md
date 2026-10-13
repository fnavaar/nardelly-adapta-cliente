# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-13 — F1-T02 concluída; novo pedido de catálogo amplo encaminhado à decisão de escopo
- Após receber o roteiro de teste humano da F1-T02, a Champion declarou “tudo funcionando”. A aprovação cobre a ficha de intake, geração de pendências e trilha observadas no preview.
- Revalidação CA-1-101: caso sintético com todos os obrigatórios preenchidos, exceto “Profissão atual”, gerou exatamente uma pendência para esse campo; consulta administrativa confirmou um evento de auditoria correspondente com ator `sistema (RN-101)`. Caso e valores são sintéticos.
- Skip 0.0.11 continua no preview e não publicado. Migração 0005 consta `applied`; status Skip conserva `.skip.config.json` como alteração pendente (preexistente e não alterada).
- Regressão F1-T01 reexecutada: sete logins; três negações 403; autoelevação 403; revogação 200→401; fixture reativada após a prova.
- Fechamento do QA descrito com precisão: setup/análise estática/build/integrações OK; `qa.test.ran=false`, portanto a suíte de testes do projeto não rodou.
- Recibo criado em `05_entregas/recibo-f1-t02-2026-10-13.md`; tabela operacional e STATUS atualizados: F1-T02 concluída, 2/5 tarefas da fase (40%).
- **Novo pedido, após aprovação:** Champion deseja que “Tipo de benefício” seja um seletor com todos os benefícios do INSS, agrupados por família. Sem implementação. A SPEC-1-002 classifica catálogo amplo de tipos como fora do escopo da Fase 1/F1-T02 e associado à Fase 2; levar ao consultor para definir escopo apropriado e fonte oficial atualizada antes de qualquer código. Confirmar se deseja que o agrupamento reflita as famílias atuais da ficha (LOAS, urbano e rural) ou outra taxonomia após a decisão de escopo.

## 2026-10-13 — F1-T02 implementada (RN-101); aguardando teste humano
- Autorização explícita da Champion (“autorizado”, 2026-10-13 19:16 BRT) posterior ao relatório de análise; etapa `implementando` registrada antes da primeira alteração.
- RED confirmado: caso incompleto criado no estado anterior sem gerar pendências (0 registros) — falha que motiva CA-1-101.
- Implementação no projeto Skip 60649, versão 0.0.11 (QA setup, análise estática, build e integrações passaram; a suíte de testes do projeto não rodou, `qa.test.ran=false`):
  - Migração 0005: campos aprovados da ficha de intake na coleção `casos` (data, canal+detalhe, atendente, indicação, dados do atendido, titular, benefício, senha MEU INSS, sindicato, escolaridade, profissão, parente, contrato, documentos, blocos LOAS/urbano/rural) e nova coleção `pessoas` (titular, atendido, representante, grupo familiar sem limite fixo, dependente, assinante à rogo, parente cliente) com RLS pelos papéis da SPEC-1-001.
  - Hook `intake_pendencias` (RN-101, after-success): cada obrigatório ausente vira pendência explícita vinculada ao caso; condicionais exigidos por canal/vínculo/filiação/parente/contrato/documentos; senha MEU INSS ausente cria a tarefa “gerar nova senha junto à agência do INSS”; cada pendência gerada é auditada (ator “sistema (RN-101)”, caso, rótulo); falha de gravação é logada, nunca silenciosa; o caso nunca é descartado.
  - Telas: `/intake/nova` (ficha com blocos condicionais por família; acesso atendimento/cadastro) e `/caso/:id` (dados da ficha + pendências do caso); link “Nova ficha de intake” no painel dos papéis de atendimento/cadastro.
- GREEN confirmado por API: caso com faltas gerou uma pendência por campo (+ tarefa INSS quando senha vazia); caso com `parente_ja_atendido=nao` não gerou pendência de parente (correto); condicionais de canal/vínculo/sindicato comprovados; eventos RN-101 visíveis na trilha via Administração.
- Regressão F1-T01 completa PASS: 7 logins, 3 negações 403 auditadas, autoelevação 403, revogação do advogado 200→401, fixture reativada.
- Estado: `aguardando_teste_humano`; F1-T02 não concluída até aceite explícito.

## 2026-10-13 — B-INTAKE-01 resolvido; F1-T02 pronta para autorização
- Champion respondeu à proposta de campos do intake com “Aprovar com ajustes”; ajustes aplicados: indicação obrigatória; senha MEU INSS opcional com tarefa automática de nova senha no INSS quando ausente; sindicato condicional (informar qual quando filiado); escolaridade, profissão e parente já atendido obrigatórios; grupo familiar do bloco LOAS sem limite fixo de 6 pessoas.
- Definição resultante: 18 campos obrigatórios (ausência gera pendência explícita), condicionais por canal/vínculo/família e opcionais; bloco específico por família LOAS/urbano/rural. Registrada em `06_notas/decisao-intake-campos-2026-10-13.md`.
- Análise da F1-T02 concluída (achados, plano, riscos e provas apresentados à Champion); nenhuma implementação iniciada; autorização foi solicitada em mensagem separada (portão do método).

## 2026-10-05 — F1-T02 analisada; bloqueada por definição de intake
- F1-T01 segue concluída (1/5 tasks; 20%), com aceite humano e recibo registrados.
- Selecionada a próxima task elegível, F1-T02 — estruturar recebimento de casos e ficha de intake; nenhuma implementação foi iniciada.
- Inspeção do Skip 60649 v0.0.10: a coleção `casos` contém `titulo`, `status`, `descricao`, `criado_por` e datas; não há ainda tela/coleção de intake ou campos mínimos.
- `SPEC-1-002` CA-1-101/RN-101 exigem criar pendências explícitas para cada dado obrigatório ausente, mas não enumeram esses dados. A SPEC ordena parar se campo obrigatório não estiver definido.
- Registrada DÚVIDA/B-INTAKE-01: champion/jurídico precisa fornecer lista aprovada de campos mínimos e quais ausências geram pendências. Não inventar conteúdo jurídico ou regra operacional. Retomar análise da F1-T02 após decisão; depois será pedido gate separado para implementação.

## 2026-10-05 — F1-T01 concluída após aprovação humana
- Champion Nardelly confirmou “Teste aprovado” após o roteiro de reteste dos critérios 3, 4 e 5; somado à aprovação anterior dos testes 1 e 2, todos os critérios humanos da task foram aceitos.
- Revalidação automatizada: os sete papéis autenticaram; atendimento→criar rota, cadastro→validar pendência e supervisão→criar usuário foram negados HTTP 403; as negações foram auditadas; autoelevação foi negada/auditada; a revogação invalidou o mesmo token em HTTP 401 imediatamente após resposta 200 antes da revogação. Fixture sintética reativada ao final.
- QA Skip 0.0.10 passou; preview mostrou controle de papel, isolamento de sessão por aba e trilha de auditoria.
- Task marcada concluída em `04_fase-atual/fase.md`; recibo em `05_entregas/recibo-f1-t01-2026-10-05.md`.
- Estado da fase: 1/5 tasks (20%). F1-T02..T05 não iniciadas; não iniciar outra task sem novo pedido da Champion.

## 2026-10-05 — F1-T01 DEBUG após falhas humanas; correções prontas para reteste
- Champion aprovou os testes humanos 1 e 2; reportou falha nos testes 3 (fluxo para alternar/validar papéis), 4 (troca de sessão após revogação em abas) e 5 (trilha sem visualização na interface).
- Causa confirmada: PocketBase LocalAuthStore padrão compartilha estado via localStorage entre abas; rota administrativa não exigia papel; login sempre encaminhava para admin; trilha existia no backend (47 eventos observados), mas não tinha página para consulta.
- Correções no projeto Skip 60649, versão 0.0.10: authStore isolado por aba em sessionStorage; rotas autenticadas fazem authRefresh ao carregar/retomar foco e validam papel; /admin/usuarios apenas administração; seletor de sete fixtures e painel por papel com prova negativa; nova /auditoria paginada com ator, data/hora, ação, entidade e estados.
- Verificações: QA 0.0.10 PASS; advogado bloqueado em /admin/usuarios; administração continuou com sua identidade em outra aba; auditoria visível.

## 2026-09-22 — F1-T01 implementada; aguardando teste humano
- Projeto Skip `Central de Processos — Nardelly` criado (id 60649; SkipCloud running).
- Autenticação com sete papéis funcionais, vínculo server-side e massa sintética criada.
- RBAC/RLS server-side fail-closed aplicado em usuários, casos, pendências, rotas de triagem e auditoria.
- Trilha append-only com ator, data/hora, estado anterior e novo; negações e autoelevação auditadas.
- Revogação gira `tokenKey`: token fresco autenticou antes (HTTP 200) e foi recusado imediatamente após (HTTP 401); fixture restaurada ao final.
- QA Skip v0.0.9: setup, análise estática, build, integrações e testes passaram.
- Provas API isoladas passaram: sete logins, três negações HTTP 403, autoelevação HTTP 403, revogação e auditoria; preview testado com login/administração.
- **Gate pendente:** teste humano e aceite explícito da champion Nardelly.

## 2026-09-22 — DEBUG task F1-T01: falhas das provas GREEN → corrigido
- Sintoma: coleções base publicadas inicialmente sem campos/regras completos; negações retornavam 400 antes dos gates; auditoria sem autodate; rate limit contaminou uma rodada; token já emitido não era invalidado por `ativo=false`.
- Causa raiz confirmada: `new Collection({...})` não persistiu fields/regras nesse runtime; createRules restritivas interceptavam antes dos hooks; rotação de token não estava implementada.
- Correção: migrações 0003/0004 com `fields.add`, regras completas e autodates; gates fail-closed; hooks sem duplicidade; `refreshTokenKey()` na revogação.
- Resultado: QA v0.0.9 verde e reprodução final passou.

## 2026-09-22 — Champion confirmado e Jornada sincronizada
- Champion **@Nardelly** confirmado por Navaar (antes responsável provisório); B-RACI-01 segue aberto apenas para os nomes por papel da operação (call de setup).
- Jornada `fase_1.md` validada pós-sincronizador: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks), parser PASS com `--require-ids`.
- Visibilidade pública do repo autorizada; pendente de ação manual no GitHub (Settings → Change visibility) por ausência de ferramenta no conector/credencial do CLI.

## 2026-09-22 — Handoff inicial (Fase 1)
- Pasta operacional criada pela consultoria com a estrutura canônica.
- Jornada `04_fase-atual/fase.md` com F1-T01..T05 (fase-format:2).
- SPECs F1 (4) em `04_fase-atual/specs/`.
- Manifesto de integridade: `handoff-manifest.json`.
- Privacidade: escopo base/definitivo, análise crítica, requisitos e fases futuras ficam na consultoria.
- Repositório GitHub `fnavaar/nardelly-adapta-cliente` criado e publicado em 22/09.
