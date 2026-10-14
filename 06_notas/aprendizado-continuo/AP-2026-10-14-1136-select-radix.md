# AP-2026-10-14-1136 — rótulos visuais em seletor de benefício

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T03 / SPEC-1-002
- Sinal: a Champion reportou que “Benefício urbano” aparecia como “bene la urbano” e “Benefício rural” como “bene ate rural”. O problema são esses dois nomes de opção, não o placeholder “Selecione…”. A fonte e o snapshot acessível retornam os rótulos completos, portanto a causa técnica exata da discrepância visual não foi isolada.
- Evidência: captura `uploads/dc85ac48-image.png`; fonte `src/pages/NovaFicha.tsx`; QA Skip 0.0.17 (`b299fc5`); snapshot acessível do listbox Radix no preview 0.0.17 retorna os três rótulos completos.
- Regra reutilizável: quando a pessoa relata grafia visual corrompida em opções, registre exatamente o texto esperado e o texto percebido; não redirecione o diagnóstico a placeholders ou elementos secundários não indicados. Compare a renderização visual no ambiente humano com fonte e árvore acessível.
- Quando aplicar: há diferença confirmada entre rótulo esperado e rótulo visual observado.
- Quando não aplicar: quando a pessoa confirma que as grafias visuais estão corretas ou quando a fonte já contém grafia errada; investigar o caso específico.
- Confiança: média — há captura humana e snapshot acessível divergentes; falta o reteste humano do preview corrigido.
- Privacidade: sem segredo, dado pessoal ou conteúdo bruto.
