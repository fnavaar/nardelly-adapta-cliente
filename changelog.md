# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-14 — F1-T03: relato de opções divergentes no seletor de família; aguardando evidência
- A Champion reportou que `Família do benefício (LOAS, urbana ou rural)` apresenta “LOAS”, “bene la urbano” e “bene la rural”.
- Conferidos a fonte de `src/pages/NovaFicha.tsx` na árvore Skip 60649 e o preview 0.0.16 (`85f220f`): `FAMILIAS` e o DOM do `select#familia_beneficio` mostram “LOAS (benefício assistencial)”, “Benefício urbano” e “Benefício rural”, com valores `loas`, `urbano`, `rural`.
- A captura posteriormente descrita pela Champion mostra o cabeçalho e a parte inicial do formulário, mas não o seletor nem a URL/contexto; assim, não identifica o ambiente/versão ou a origem dos textos relatados. Não se alterou código; não houve novo QA.
- Estado: F1-T03 bloqueada até a Champion confirmar que estava no preview 0.0.16 (produção não publicada) e, se persistir, enviar captura com seletor aberto e URL/contexto visível. Evidência `artifacts/d33720da-ccd2-48ea-9c35-6769d979667e.png`; relatório `artifacts/relatorio-debug-f1-t03-select-repro.md`.
