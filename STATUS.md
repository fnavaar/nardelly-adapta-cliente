# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-14 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** após aceite humano; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 é a única task ativa, aguardando reteste humano da versão 0.0.17 (`b299fc5`).** O problema relatado pela Champion é que os nomes das opções aparecem visualmente como “bene la urbano” e “bene ate rural”, em vez de “Benefício urbano” e “Benefício rural”. A Champion esclareceu que o placeholder “Selecione…” não era o defeito.
- A correção trocou o controle nativo por Radix Select já existente, mantendo os rótulos e valores de dados. No preview 0.0.17, o listbox observado pelo browser acessível retorna “LOAS (benefício assistencial)”, “Benefício urbano” e “Benefício rural”. Falta o reteste visual humano para confirmar que a distorção percebida foi resolvida.
- QA 0.0.17: setup, análise estática, build e integrações passaram; a suíte não foi executada pela plataforma (`test.ran=false`). Não houve criação/envio de ficha nem uso de dados reais. Produção não publicada.
- Os blocos LOAS/urbano/rural permanecem como texto livre; não houve decisão para estruturar as perguntas uma a uma. B-CHK-01 e B-POL-01 seguem pendentes.

## Próximo passo
A Champion retestar no preview 0.0.17 se as opções aparecem visualmente como **“Benefício urbano”** e **“Benefício rural”**. O placeholder “Selecione…” não é critério de falha. Não enviar a ficha; informar aprovação ou se os nomes ainda aparecem distorcidos.

## Bloqueios ativos
Aceite humano da F1-T03 pendente; B-POL-01, B-RACI-01, B-CHK-01, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
