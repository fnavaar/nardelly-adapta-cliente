# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-14 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** após aceite humano; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 segue aberta, aguardando teste humano da correção de seletor na versão 0.0.17 (`b299fc5`).** O seletor Família do benefício usa agora o Radix Select existente, corrigindo o controle nativo cuja captura mostrava rótulos corrompidos e “Selecione…” duplicado; valores e regras continuam inalterados.
- QA 0.0.17: setup, análise estática, build e integrações passaram. A suíte de testes não rodou (`test.ran=false`). Preview verificado com conta sintética: listbox contém exatamente três famílias legíveis, sem placeholder como opção. Não houve criação/envio de ficha nem uso de dados reais. Produção não publicada.
- Blocos de benefício LOAS/urbano/rural continuam como texto livre; não houve decisão para estruturá-los pergunta a pergunta. B-CHK-01 segue aberto; exemplos documentais não são requisitos jurídicos aprovados. B-POL-01 segue bloqueando dados reais e persistência local de rascunhos.

## Próximo passo
A Champion retestar no preview 0.0.17: abrir o seletor e conferir as três opções legíveis, sem duplicata; escolher cada família e confirmar que aparece seu bloco condicional. Não enviar a ficha. Informar aprovação ou qualquer falha restante.

## Bloqueios ativos
Aceite humano da F1-T03 pendente; B-POL-01, B-RACI-01, B-CHK-01, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
