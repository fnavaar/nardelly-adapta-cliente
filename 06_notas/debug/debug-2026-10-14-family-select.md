# Debug Summary — menu de família de benefício nativo com rótulos corrompidos

**Data:** 2026-10-14 · **Task:** F1-T03 · **Estado:** aguardando teste humano; não concluída.

## Sintoma recebido
A Champion informou que, no seletor “Família do benefício (LOAS, urbana ou rural)”, as opções apareciam como “LOAS”, “bene la urbano” e “bene la rural”. Captura `uploads/dc85ac48-image.png` mostrou o endereço correto do preview: `https://central-de-processos-nardelly-65f79--preview.goskip.app/intake/nova`. No menu nativo havia uma opção “Selecione…” repetida e rótulos visualmente ilegíveis/corrompidos.

## Causa identificada
`src/pages/NovaFicha.tsx` usava um `<select>` HTML nativo para a família do benefício, incluindo um `<option value="">Selecione…</option>`. No preview antigo, os nomes corretos estavam no DOM, mas o menu renderizado no ambiente da Champion tinha aparência incorreta e placeholder duplicado. A divergência era do controle visual nativo, não dos valores de domínio. O projeto já disponibilizava um seletor personalizado Radix, sem precisar adicionar dependências.

## Correção
Apenas o campo Família do benefício foi trocado para o componente Radix Select já existente. O placeholder agora é renderizado no gatilho e não como item de menu; as opções continuam exatamente:
- `LOAS (benefício assistencial)` → `loas`
- `Benefício urbano` → `urbano`
- `Benefício rural` → `rural`

Nenhuma regra jurídica, validação, dado persistido ou outro campo foi alterado. `package.json` foi incrementado para `0.0.17`.

## Verificações
- Skip 60649, versão 0.0.17, hash `b299fc5`; preview ativo: `https://central-de-processos-nardelly-65f79--preview.goskip.app`.
- QA: setup PASS; análise estática PASS; build PASS; integrações PASS; testes reportados como OK, mas não executados pela plataforma (`test.ran=false`).
- Agent-browser: login sintético de Atendimento; abriu `/intake/nova`; o botão Família do benefício abriu um listbox contendo exatamente três opções — LOAS (benefício assistencial), Benefício urbano, Benefício rural — sem “Selecione…” como item de menu. Nenhuma ficha enviada/criada e nenhum dado real usado.
- Projeto não publicado em produção. Há uma mudança administrativa pendente `.skip.config.json`, registrada pelo Skip; não foi editada manualmente.

## Teste humano solicitado
No preview 0.0.17, abrir “Família do benefício” e confirmar que o menu tem exatamente três opções legíveis — LOAS (benefício assistencial), Benefício urbano e Benefício rural —, sem uma segunda opção “Selecione…”. Selecionar cada família e confirmar que aparece o bloco condicional correspondente. Não enviar a ficha.

## Gate atual
`aguardando_teste_humano`. Só a Champion pode aprovar o reteste; F1-T03 continua aberta. O checklist jurídico continua pendente de aprovação.