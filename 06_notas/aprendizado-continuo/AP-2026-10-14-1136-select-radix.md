# AP-2026-10-14-1136 — seletor de lista longa no intake

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T03 / SPEC-1-002
- Sinal: o seletor nativo `<select>` da família do benefício tinha rótulos corretos no código e no DOM, mas o menu visual de opções da Champion aparecia corrompido e repetia o placeholder. O projeto já disponibilizava um Select Radix acessível.
- Evidência: captura `uploads/dc85ac48-image.png`; implementação em `src/pages/NovaFicha.tsx`; QA Skip 0.0.17 (`b299fc5`); listbox do preview via agent-browser mostrando três opções corretas, sem placeholder duplicado.
- Regra reutilizável: se rótulos do `<select>` nativo aparecem divergentes entre DOM e menu visual em um navegador real, reproduzir a captura e preferir o componente de seleção acessível existente no projeto, mantendo valores de domínio e removendo placeholder da lista de itens.
- Quando aplicar: defeito comprovado de renderização visual de seletor nativo com opções e placeholder redundante.
- Quando não aplicar: quando o problema é apenas terminológico, quando o DOM também contém rótulos errados, ou se o projeto não possui componente existente compatível; investigar antes de trocar.
- Confiança: média — falha visual na captura da Champion e menu Radix após correção foram observados; o browser automatizado antes da correção não reproduziu a falha visual.
- Privacidade: sem segredo, dado pessoal ou conteúdo bruto.
