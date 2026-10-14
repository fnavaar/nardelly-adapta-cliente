# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-13 — F1-T03: correção após primeiro teste humano; aguardando reteste
- Às 21:15 BRT a Champion relatou dois problemas: rótulos de campos diferentes das fichas e perda de preenchimento ao mudar de aba. F1-T03 não foi aceita e permaneceu a única task ativa.
- **Causa reproduzida no preview 0.0.13:** ao recuperar foco, `ProtectedRoute` mudava o estado para `checking` e substituía o conteúdo protegido por uma tela de carregamento; isso desmontava `NovaFicha` e apagava os valores em estado React.
- **Correção em `src/components/ProtectedRoute.tsx`:** conservar a rota montada durante revalidação de foco; apresentar sobreposição de validação e tornar o conteúdo temporariamente inerte; preservar o gate inicial, a revalidação server-side e o redirecionamento se a sessão for inválida.
- **Correção de linguagem em `src/pages/NovaFicha.tsx`:** alinhar rótulos principais à linguagem das fichas do escritório (pessoa atendida, segurado/titular/autor, escolaridade, profissão atual, parente e solicitação/prazo de documentos), e detalhar o texto introdutório de benefício rural. Não se adicionou regra jurídica nem se mudou a definição aprovada dos campos da F1-T02.
- QA Skip 0.0.14 inicialmente passou; revisão de segurança levou ao overlay inerte adicional. **QA final 0.0.15 (`214bb2c`):** setup, análise estática, build e integrações OK; `test.ran=false`, suíte do projeto não executada.
- Reproduzido e retestado com agent-browser no preview 0.0.15: preencheu-se somente texto sintético no campo “Nome da pessoa que está sendo atendida”; após abrir outra aba e retornar, o campo continuou com `RASCUNHO SINTETICO F1T03 V015`. Também se confirmou visualmente a exibição dos rótulos revisados. Nenhuma ficha foi enviada; nenhuma massa real foi criada.
- Preview: `https://central-de-processos-nardelly-65f79--preview.goskip.app/entrar`; produção continua sem publicação.
- **Limite explícito:** valores são preservados quando o usuário alterna abas do navegador e a mesma tela permanece montada. Navegar para fora da ficha ou recarregar ainda perde rascunho; não foi adicionado armazenamento local de dados pessoais, aguardando a política B-POL-01. Perguntas de detalhe por família permanecem agrupadas em campos de texto; confirmar no reteste se isso é parte da divergência percebida, sem presumir desenho jurídico.
- F1-T03 continua aberta; estado `aguardando_teste_humano`; aguardar reteste/aceite explícito da Champion. Evidência detalhada em `06_notas/debug/debug-2026-10-13-f1-t03.md`.

## 2026-10-13 — F1-T03 analisada; B-TIPO-01 resolvido; aguardando autorização
- A Champion definiu cinco tipos rurais representativos e que documentos da terra são condicionais ao contexto rural; decisão em `06_notas/decisao-f1-t03-tipos-e-documentos-rurais-2026-10-13.md`.
- B-CHK-01 permanece aberto porque a lista rural é exemplificativa e não define itens jurídicos obrigatórios individuais.
- A F1-T03 foi implementada após autorização explícita, com conteúdo demonstrativo marcado como pendente de aprovação jurídica; QA e relato da primeira falha/reteste acima.

## 2026-10-13 — F1-T03: checklist documental recebido
- O PDF foi lido; dados pessoais de seus modelos visuais não foram reproduzidos. A Champion confirmou a natureza exemplificativa do rol rural. Não inventar obrigatoriedade por inferência.

## 2026-10-13 — F1-T02 concluída e F1-T01
- F1-T02 aceita após “tudo funcionando”; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`. QA não executou a suíte de testes (`test.ran=false`). F1-T01 foi aceita em 2026-10-05; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
