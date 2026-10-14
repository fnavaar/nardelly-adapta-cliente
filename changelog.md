# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-14 — F1-T03: relato de opções divergentes no seletor de família; bloqueado para evidência
- A Champion informou que `Família do benefício (LOAS, urbana ou rural)` apresenta “LOAS”, “bene la urbano” e “bene la rural”.
- Reabri o debug e conferi a fonte do projeto Skip 60649 e o preview publicado para desenvolvimento 0.0.16 (`85f220f`). A constante `FAMILIAS` e o DOM real de `select#familia_beneficio` mostram “LOAS (benefício assistencial)”, “Benefício urbano” e “Benefício rural”, com valores `loas`, `urbano` e `rural`.
- Não foi possível reproduzir as strings do relato; por isso, nenhuma alteração foi feita e nenhum novo QA executado. Não presumir se o motivo é versão, ambiente ou exibição visual.
- Estado: F1-T03 bloqueada aguardando confirmação de que o teste foi feito no preview 0.0.16 (produção ainda não publicada) e captura da lista aberta com URL/contexto visível se o problema continuar. Evidência `artifacts/d33720da-ccd2-48ea-9c35-6769d979667e.png`; relatório operacional `artifacts/relatorio-debug-f1-t03-select-repro.md`.

## 2026-10-13 — F1-T03: correção de rótulos; aguardando reteste
- Correção v0.0.16 alinhou nomes da ficha/detalhe, mantendo os três valores de família (`loas`, `urbano`, `rural`) sem alterar schema ou regras. QA setup/estático/build/integrações passou; `test.ran=false`. Verificação de intake no preview; produção não publicada.
- O reteste humano agora encontrou texto diferente no seletor de família; o diagnóstico segue bloqueado até reproduzir o mesmo ambiente/contexto.
