# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-14 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** com aceite humano; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 é a única task ativa, aberta e bloqueada por divergência de diagnóstico.** A Champion informou rótulos “LOAS”, “bene la urbano” e “bene la rural” no campo de família. No preview Skip 0.0.16 (`85f220f`), o código e o DOM exibem “LOAS (benefício assistencial)”, “Benefício urbano” e “Benefício rural”. O relato não foi reproduzido; não se alterou código. Produção não publicada.
- QA anterior 0.0.16: setup/análise estática/build/integrações passaram; a suíte não rodou (`test.ran=false`). Nenhum novo QA após o diagnóstico, pois não houve alteração.
- Evidência da tela `/intake/nova`: `artifacts/d33720da-ccd2-48ea-9c35-6769d979667e.png`; resumo: `artifacts/relatorio-debug-f1-t03-select-repro.md`.
- Limites conhecidos mantidos: os blocos LOAS/urbano/rural seguem em campos de texto livre; B-CHK-01 e B-POL-01 continuam sem resolução. Não usar dados reais.

## Próximo passo
A Champion confirmar o ambiente/versão testado e, caso a divergência persista, enviar uma captura da lista aberta com URL visível. Só depois, se reproduzida, decidir correção mínima. Não concluir F1-T03 nem iniciar outra task.

## Bloqueios ativos
**Divergência ainda não reproduzida nos rótulos do seletor**; B-POL-01, B-RACI-01, B-CHK-01, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
