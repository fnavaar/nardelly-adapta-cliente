# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-14 — F1-T03: Radix Select e critério de reteste corrigido
- A Champion esclareceu que o defeito relatado não era o placeholder “Selecione…”. O problema são os rótulos visuais das opções: “Benefício urbano” aparece como “bene la urbano” e “Benefício rural” como “bene ate rural”.
- A captura confirmou que a tela era o preview 0.0.16 correto. A fonte de `src/pages/NovaFicha.tsx` continha os rótulos completos, enquanto a captura do menu mostrava texto visualmente alterado. A causa técnica exata da discrepância não foi reproduzida de modo independente no browser de verificação.
- Foi aplicado no Skip 60649 o seletor Radix já existente apenas para o campo Família do benefício, como correção de apresentação, mantendo textos e valores (`loas`, `urbano`, `rural`); versão 0.0.17 (`b299fc5`). A observação sobre o placeholder não faz parte do critério de aceite.
- QA: setup/static/build/integrations PASS; `test.ran=false`. Snapshot acessível do listbox da 0.0.17 retornou os rótulos completos; ainda falta confirmação visual humana. Nenhuma ficha foi enviada/criada, nenhum dado real utilizado, produção não publicada.
- Estado: `aguardando_teste_humano`. Retestar especificamente se o menu mostra visualmente “Benefício urbano” e “Benefício rural”.
