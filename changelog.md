# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-13 — F1-T03 analisada; B-TIPO-01 resolvido; aguardando autorização
- A Champion definiu cinco tipos rurais para a demonstração ponta a ponta: aposentadoria por idade rural; benefício por incapacidade permanente/temporária rural; salário-maternidade rural; pensão por morte rural; auxílio-reclusão rural.
- A Champion definiu que os documentos da terra da página geral são condicionais ao contexto rural/atividade na terra.
- A decisão foi registrada em `06_notas/decisao-f1-t03-tipos-e-documentos-rurais-2026-10-13.md`; **B-TIPO-01 está resolvido**.
- **B-CHK-01 permanece aberto:** o PDF de provas rurais é exemplificativo/não exaustivo e não define, com segurança, quais itens são requisitos obrigatórios individuais e quais são alternativas. Não será criado conteúdo jurídico fechado por inferência.
- A análise da F1-T03 encontrou Skip 60649 v0.0.11 no preview, produção não publicada; existem `casos`, `pessoas`, `pendencias`, `rotas_triagem` e `auditoria`, mas não existem coleções de checklist/protocolo nem workflow documental.
- Plano para autorização: construir somente o mínimo da SPEC-1-002 — checklist versionado, pendência documental com seis estados, protocolo único, recebimento/ciência, devolução com motivo/orientação, bloqueio de avanço, exceção jurídica auditada, histórico e demonstração com fixtures sintéticas. Usar plano B explicitamente marcado `PENDENTE APROVAÇÃO JURÍDICA` e itens demonstrativos sintéticos; aceitar “outro documento” e alternativas sem rejeição automática.
- Estado: F1-T03 `aguardando_autorizacao`; nenhuma alteração de produto foi iniciada.

## 2026-10-13 — F1-T03: PDF do checklist documental recebido; análise inicial
- A Champion esclareceu que a página 1 corresponde aos documentos gerais e as páginas seguintes às provas rurais, com rol exemplificativo.
- O PDF foi lido por extração de texto e inspeção das páginas ilustradas. Imagens/modelos com dados identificáveis não foram reproduzidos nem transcritos.
- O resumo operacional identificou documentos gerais, documentos da terra, blocos condicionais por benefício e provas rurais condicionais por filhos, cônjuge/companheiro e pais.
- O documento não define quais provas rurais são obrigatórias ou alternativas; não transformar o rol em checklist fechado sem aprovação jurídica.
- Nenhuma alteração do produto.

## 2026-10-13 — F1-T03 analisada; inicialmente bloqueada
- F1-T03 exige CA-1-102..106: checklist versionado, estados documentais, protocolo, devolução, bloqueio de avanço e exceção auditada.
- Baseline Skip 60649 v0.0.11 tinha coleções `casos`, `pessoas`, `pendencias`, `rotas_triagem` e `auditoria`; pendência mínima com `caso`, `descricao`, `status` aberta/resolvida; sem checklist/protocolo.
- B-CHK-01 e B-TIPO-01 foram registrados como dependências; não se pode inventar conteúdo jurídico.

## 2026-10-13 — F1-T02 concluída; pedido adicional de catálogo amplo encaminhado
- Champion declarou “tudo funcionando”; aceite cobre intake, pendências e trilha no preview.
- CA-1-101 revalidado com caso sintético e auditoria RN-101. Recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- Skip 0.0.11 permanece em preview; produção não publicada; `qa.test.ran=false`.
- Catálogo amplo de benefícios INSS ficou fora do escopo da Fase 1/F1-T02, sem implementação.

## 2026-10-13 — F1-T02 implementada e aceita
- Migração 0005 aplicada; hook RN-101, telas de intake/caso, pendências explícitas e auditoria.
- Aceite humano: “tudo funcionando”.

## 2026-10-05 — F1-T02 analisada; bloqueada por definição de intake
- B-INTAKE-01 exigia lista de campos obrigatórios/condicionais; nenhuma implementação foi iniciada antes da decisão.

## 2026-10-05 — F1-T01 concluída após aprovação humana
- Champion declarou “Teste aprovado”; critérios CA-1-001..005 revalidados. Recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
