# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-13 — F1-T03: PDF do checklist documental recebido; duas definições ainda pendentes
- A Champion esclareceu: a página 1 da ficha de solicitação corresponde aos documentos gerais; as páginas 2 em diante são provas rurais, com rol **exemplificativo**, não exaustivo.
- PDF recebido: `uploads/5c8eb6a6-SOLICITA_O_DOC_GERAIS_E_SOL_DOC_RURAIS_8057_60__4234.pdf` (5 páginas). Lido por extração de texto e inspeção das páginas ilustradas. Apenas o conteúdo operacional foi resumido aqui; as imagens/modelos com nomes, fotos, documentos e dados identificáveis não foram reproduzidas nem transcritas.
- Resumo sem dados pessoais: a primeira página lista documentos pessoais e comprovante de residência, mas também inclui documentos ligados a terra (ITR/INCRA, compra e venda, partilha em caso de herança) e blocos condicionais a benefício/incapacidade, salário-maternidade, pensão por morte e auxílio-reclusão. As páginas rurais incluem exemplos de prova do trabalho/ligação rural e blocos condicionais por existência de filhos, cônjuge/companheiro ou pais.
- O caráter exemplificativo do rol rural está confirmado pela Champion. Não se deve transformar sua lista em enumeração fechada ou rejeitar outros meios de prova documentais; a interface precisará permitir anexar/registrar “outro documento”, mantendo categoria/descrição e a associação ao caso.
- **Ainda falta:** (1) B-TIPO-01 — a lista dos tipos representativos de demanda a percorrer na demonstração (a Champion ainda não enumerou nenhum); (2) delimitação da condicionalidade dos documentos “da terra” que aparecem na página 1 — o cabeçalho da página não os vincula explicitamente apenas aos casos rurais, e não se deve aplicá-los a todo cliente sem confirmação.
- Estado: F1-T03 permanece `bloqueada`; insumo documental recebido não equivale a aprovação de implementação. Nenhuma alteração do produto.

## 2026-10-13 — F1-T03 analisada; bloqueada por insumos jurídicos/operacionais
- F1-T02 foi aceita pela Champion (“tudo funcionando”) e encerrada com recibo `05_entregas/recibo-f1-t02-2026-10-13.md`; revalidação final CA-1-101 comprovou pendência e auditoria para uma falta sintética.
- F1-T03 exige CA-1-102..106: checklist versionado por tipo, estados de pendência documental, protocolo, devolução com motivo/orientação aprovada, bloqueio de avanço e exceção jurídica justificada/auditada.
- Baseline Skip 60649 v0.0.11: existem `casos`, `pessoas`, `pendencias` e `auditoria`; pendências só têm `caso`, `descricao` e status `aberta`/`resolvida`. Sem coleções de checklist/protocolo ou fluxo de estados documentais; nenhuma alteração feita.
- B-CHK-01: checklist precisa de fornecimento/aprovação do advogado responsável/Champion. B-TIPO-01: lista de tipos representativos precisa da Champion. A SPEC permite estrutura vazia marcada como pendente de aprovação, mas não se pode concluir o fluxo sem insumos aprovados nem inventar conteúdo jurídico.
- Catálogo amplo de benefícios INSS continua sendo pedido separado; fora do escopo desta task sem decisão formal.

## 2026-10-13 — F1-T02 concluída; pedido adicional de catálogo amplo encaminhado à decisão de escopo
- Champion declarou “tudo funcionando”; aceite cobre intake, pendências e trilha observados no preview.
- Revalidação CA-1-101: caso sintético com um obrigatório ausente gerou exatamente uma pendência correspondente e evento de auditoria RN-101.
- Skip 0.0.11 permanece no preview, não publicado; migração 0005 `applied`. `.skip.config.json` pendente era preexistente e foi preservado.
- Regressão F1-T01: sete logins, negações 403, autoelevação 403 e revogação 200→401.
- QA: setup, análise estática, build e integrações OK; `qa.test.ran=false`, portanto a suíte não rodou.
- Recibo `05_entregas/recibo-f1-t02-2026-10-13.md`; fase 2/5 (40%).
- Novo pedido: tornar Tipo de benefício seletor com catálogo amplo INSS por família. Sem implementação; SPEC-1-002 diz catálogo amplo fora da Fase 1 e associado à Fase 2.

## 2026-10-13 — F1-T02 implementada; aguardando aceite humano
- Autorização explícita (“autorizado”). RED: caso incompleto anterior ao hook não gerava pendências.
- Skip 0.0.11: campos aprovados do intake, coleção `pessoas`, hook RN-101, páginas `/intake/nova` e `/caso/:id`.
- GREEN via API: faltas geraram pendências; condicionais de canal/vínculo/sindicato e tarefa de senha MEU INSS conferidas; auditoria RN-101 visível.
- Regressão F1-T01: sete logins, três negações 403 auditadas, autoelevação 403, revogação 200→401.
- A suíte de testes do projeto não rodou (`qa.test.ran=false`); verificações de API e preview documentadas separadamente.

## 2026-10-13 — B-INTAKE-01 resolvido
- Champion aprovou “com ajustes”: indicação obrigatória; senha Meu INSS opcional com tarefa de nova senha; sindicato condicional; escolaridade, profissão e parente obrigatórios; grupo familiar LOAS sem limite fixo. Definição em `06_notas/decisao-intake-campos-2026-10-13.md`.

## 2026-10-05 — F1-T02 analisada; bloqueada por definição do intake
- F1-T01 concluída (1/5). F1-T02 aguardava lista aprovada de campos obrigatórios para CA-1-101; nenhuma implementação iniciada.

## 2026-10-05 — F1-T01 concluída após aprovação humana
- Champion confirmou “Teste aprovado” após os testes humanos. Revalidação: sete logins, negações 403 auditadas, autoelevação bloqueada e revogação 200→401. Recibo em `05_entregas/recibo-f1-t01-2026-10-05.md`.

## 2026-10-05 — F1-T01 debug
- Causas confirmadas: sessão entre abas, autorização por papel e ausência de UI da trilha. v0.0.10 corrigiu isolamento por aba, gates por papel e tela `/auditoria`; QA e preview verificados.

## 2026-09-22 — F1-T01 e handoff
- Skip 60649 criado; RBAC/RLS, sete papéis, auditoria e fixtures sintéticas. Champion confirmada; repo operacional criado.
