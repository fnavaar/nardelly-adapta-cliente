# AP-2026-10-14-1136 — rótulos visuais em seletor de benefício

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T03 / SPEC-1-002
- Sinal: a Champion reportou os rótulos “Benefício urbano” e “Benefício rural” visualmente escritos como “bene la urbano” e “bene ate rural”. A fonte e o snapshot acessível anterior continham os textos completos, então a discrepância de renderização foi observada, mas sua causa técnica exata não foi isolada. O placeholder “Selecione…” não era o problema.
- Evidência: captura `uploads/dc85ac48-image.png`; fonte em `src/pages/NovaFicha.tsx`; QA Skip 0.0.17 (`b299fc5`); snapshot acessível do listbox Radix no preview 0.0.17 retornando os três rótulos completos.
- Regra reutilizável: ao receber relato de rótulo visualmente corrompido com fonte/snapshot acessível corretos, registrar o texto esperado e o observado sem presumir que placeholder ou valor de dados estejam errados; comparar renderização visual no ambiente humano. Se necessário, testar controle acessível já existente sem mudar valores.
- Quando aplicar: divergência comprovada entre o texto visual observado pela pessoa e os rótulos no código/DOM acessível.
- Quando não aplicar: se a pessoa confirmar que o menu visual está correto, ou se a fonte/DOM também tiver grafia incorreta; investigar o caso específico antes de generalizar.
- Confiança: média — captura humana e snapshot automatizado diferem, mas a Champion ainda não retestou a versão corrigida.
- Privacidade: sem segredo, dado pessoal ou conteúdo bruto.
