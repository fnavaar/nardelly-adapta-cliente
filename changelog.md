# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-14 — F1-T03: menu de família substituído por Select acessível; aguardando reteste humano
- Após a Champion enviar captura do seletor aberto no preview 0.0.16 mostrando opções visualmente corrompidas (“bene la urbano/rural”) e “Selecione…” repetido, confirmou-se que o URL era o preview correto. A falha ocorria no menu nativo `<select>` apesar de os rótulos/value no DOM e na fonte estarem corretos.
- Correção mínima em `src/pages/NovaFicha.tsx`: somente Família do benefício passou ao Radix Select já instalado. O placeholder “Selecione…” é mostrado no gatilho, não como opção duplicada no menu. Textos/valores continuam `LOAS (benefício assistencial)` / `loas`, `Benefício urbano` / `urbano`, `Benefício rural` / `rural`.
- `package.json` atualizado para 0.0.17. Aplicado no Skip 60649 como versão `b299fc5`.
- QA Skip: setup/static/build/integrations PASS; `test.ran=false`. Browser autenticado com conta sintética abriu `/intake/nova`; após abrir o Radix listbox, snapshot retornou exatamente as três opções corretas, sem placeholder. Não enviou ficha; nenhum dado real. Produção não publicada.
- Estado alterado para `aguardando_teste_humano`; pedir reteste da Champion e manter F1-T03 aberta até aceite explícito. B-CHK-01 permanece pendente.
