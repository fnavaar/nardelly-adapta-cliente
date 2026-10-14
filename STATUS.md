# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-14 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** após aceite humano; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 é a única task ativa e está bloqueada aguardando evidência diagnóstica.** A Champion relatou “bene la urbano” e “bene la rural”. No preview Skip 0.0.16 (`85f220f`), o código e o DOM mostram “LOAS (benefício assistencial)”, “Benefício urbano” e “Benefício rural”; as strings relatadas não foram reproduzidas. A captura enviada depois mostra somente o topo da ficha, sem o seletor aberto ou URL/contexto, e não permite confirmar que é o mesmo estado observado. Nenhum código foi alterado; produção não publicada.
- QA anterior 0.0.16: setup/análise estática/build/integrações passaram; a suíte não rodou (`test.ran=false`). Nenhum novo QA nesta rodada sem alteração.
- Evidência do preview: `artifacts/d33720da-ccd2-48ea-9c35-6769d979667e.png`; relatório: `artifacts/relatorio-debug-f1-t03-select-repro.md`.
- Blocos LOAS/urbano/rural seguem texto livre; B-CHK-01 e B-POL-01 continuam pendentes. Não usar dados reais.

## Próximo passo
A Champion confirmar que estava no preview 0.0.16 e, se a divergência persistir, enviar captura da lista Família do benefício aberta com URL/ambiente visível. Só então retomar o mesmo debug.

## Bloqueios ativos
**Divergência do seletor não reproduzida e sem captura do campo em uso**; B-POL-01, B-RACI-01, B-CHK-01, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
