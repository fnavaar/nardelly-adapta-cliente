# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-13 — F1-T03: segunda correção de rótulos; aguardando novo teste humano
- Segundo reteste humano: a Champion confirmou “o preenchimento permaneceu ao trocar de aba”, mas relatou que os rótulos ainda divergiam. A F1-T03 não foi aceita e permaneceu ativa.
- A comparação das três fichas e da decisão B-INTAKE-01 confirmou que o conteúdo específico por benefício na implementação anterior estava reduzido a uma caixa de texto por família, com títulos-resumo. Isto explica uma divergência estrutural possível, não meramente ortográfica.
- Correção 0.0.16 aplicada: cabeçalho e rótulos de intake aproximados da formulação das fichas; “Família do benefício” renomeada para explicitar que é família (LOAS/urbano/rural), mantendo “Tipo específico” em campo separado; detalhes do canal agora nomeados conforme a opção; a ficha do caso usa nomes completos em vez de abreviações (“Nascimento” → “Data de nascimento do titular”, “Titular” → “Nome do titular do benefício (autor do processo)” etc.). Nenhuma validação, obrigatoriedade ou regra jurídica foi alterada.
- Os blocos específicos continuam texto livre. Os títulos/placeholder passam a explicitar mais tópicos da ficha: LOAS (idade/deficiência, renda, CadÚnico, moradia, grupo familiar ilimitado, gastos); urbano (idade, benefícios anteriores, negativas, ação judicial, trabalho/contribuições e perguntas específicas conforme incapacidade/salário-maternidade/pensão/reclusão); rural (benefício, terras/períodos/companheiros/filhos/pais e benefícios correlatos). Nenhuma regra nova de obrigatoriedade foi criada; checklist jurídico rural permanece pendente.
- QA Skip 0.0.16 (`85f220f`): setup PASS, análise estática PASS, build PASS, integrações PASS; `test.ran=false`. Preview carregou `/intake/nova`; snapshot confirmou rótulos revisados e exibição dos blocos LOAS, urbano e rural ao selecionar cada família. A rota `/caso/:id` não foi validada autenticada nesta rodada porque não se criou caso sintético; isso fica para o reteste humano.
- Sem dados reais e sem envio/cadastro de teste nesta verificação. Produção não publicada. Reter alternância entre abas segue corrigida desde 0.0.15.
- F1-T03 fica `aguardando_teste_humano`; aguardar verificação humana dos rótulos e do fluxo antes de qualquer conclusão.

## 2026-10-13 — F1-T03: correção anterior após primeiro teste humano
- A primeira falha humana foi perda de preenchimento ao retornar à aba e rótulos divergentes.
- Causa da perda: `ProtectedRoute` desmontava a página durante revalidação de sessão no evento de foco. Corrigido mantendo formulário montado, em modo inerte, durante revalidação server-side.
- QA final 0.0.15 (`214bb2c`) passou setup/análise estática/build/integrações; a suíte não rodou (`test.ran=false`). Browser confirmou texto sintético preservado ao alternar aba. Produção não publicada.
- Relatório em `06_notas/debug/debug-2026-10-13-f1-t03.md` e `artifacts/relatorio-debug-f1-t03.md`.

## 2026-10-13 — F1-T03 analisada; B-TIPO-01 resolvido
- Cinco tipos rurais de demonstração aprovados; documentos da terra condicionais ao contexto rural. B-CHK-01 continua aberto porque as provas rurais são exemplificativas e não classificam a obrigatoriedade por item.
- Implementação autorizada e entregue apenas no preview; não houve publicação.
