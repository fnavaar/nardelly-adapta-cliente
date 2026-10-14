# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-13 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- Escopo definitivo v1.0 aprovado (5 fases); SPECs F1 (4) e tasks F1-T01..T05 publicadas.
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** com aceite humano “tudo funcionando”; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 permanece aberta, aguardando reteste humano**, após correção de uma falha reportada no primeiro teste. Versão atual do preview: Skip 0.0.15 (`214bb2c`); produção não publicada.
- **Correção reproduzida e revalidada:** alternar para outra aba e voltar fazia a ficha perder o valor porque `ProtectedRoute` desmontava a tela ao mostrar a validação da sessão. Agora a rota/formulário continua montada e não interativa enquanto a revalidação ocorre; se falhar, sessão é encerrada como antes.
- Rótulos principais do intake foram aproximados da linguagem das fichas enviadas: pessoa atendida, titular/autor, escolaridade, profissão, histórico do parente e solicitação de documentos. O preview mostrou os rótulos revisados.
- QA 0.0.15: setup, análise estática, build e integrações passaram. A suíte do projeto não foi executada (`test.ran=false`). Reteste browser com texto puramente sintético ficou visível após alternar de aba e retornar. Registro detalhado: `06_notas/debug/debug-2026-10-13-f1-t03.md`.
- Limite remanescente conhecido: o rascunho existe em memória enquanto a ficha permanece montada; não há persistência após navegar para fora ou recarregar. Isso evita armazenar dados pessoais localmente sem política aprovada. Perguntas específicas extensas dos blocos LOAS/urbano/rural continuam agrupadas em texto livre; necessidade de granularidade adicional deve ser confirmada no reteste, sem inventar regras.
- **B-CHK-01 permanece aberto:** provas rurais exemplificativas não definem, item a item, obrigatoriedade jurídica. Os itens demonstrativos permanecem marcados `PENDENTE APROVAÇÃO JURÍDICA`.
- **B-TIPO-01 resolvido:** aposentadoria por idade rural; benefício por incapacidade permanente/temporária rural; salário-maternidade rural; pensão por morte rural; auxílio-reclusão rural. Documentos da terra são condicionais ao contexto rural. Decisão em `06_notas/decisao-f1-t03-tipos-e-documentos-rurais-2026-10-13.md`.
- Nenhum dado real usado. Não houve teste humano de ponta a ponta nem aceite da F1-T03; não iniciar outra task.

## Próximo passo
Aguardar a Champion retestar o preview 0.0.15 e informar aprovação ou a falha remanescente. Não concluir F1-T03 até aceite humano explícito.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), **B-CHK-01 (aprovação jurídica final do checklist)**, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
