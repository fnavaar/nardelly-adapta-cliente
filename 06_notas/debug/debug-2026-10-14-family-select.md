# Debug Summary — seletor de família de benefício: relato não reproduzido

**Data:** 2026-10-14 · **Task:** F1-T03 · **Estado:** bloqueada para evidência; não concluída.

## Resultado humano recebido
A Champion reportou que no campo “Família do benefício (LOAS, urbana ou rural)” as opções aparecem como “LOAS”, “bene la urbano” e “bene la rural”. Uma descrição visual da tela recebida em seguida cobre somente o topo da ficha, sem o seletor de família ou URL/contexto visível.

## Reprodução executada
- Projeto: Skip 60649, preview URL `https://central-de-processos-nardelly-65f79--preview.goskip.app`.
- Versão observada no status: 0.0.16 (`85f220f`); produção segue não publicada.
- Entrado com conta sintética de Atendimento e aberto `/intake/nova`.
- Inspecionado o snapshot e o DOM do `select#familia_beneficio`.
- Resultado real: `Selecione…`; `LOAS (benefício assistencial)` (`loas`); `Benefício urbano` (`urbano`); `Benefício rural` (`rural`).
- A fonte de `src/pages/NovaFicha.tsx` da árvore ativa define os mesmos textos em `FAMILIAS`.
- Nenhuma ficha criada/enviada; nenhum dado real usado.

## Conclusão
O relato não foi reproduzido no preview 0.0.16; a causa permanece desconhecida. O material posterior não mostra o seletor em questão nem a URL/ambiente, então não permite afirmar se a observação humana veio do preview atual. Alterar texto sem evidência comparável seria especulativo.

## Próximo passo
Pedir confirmação de que a Champion testou no preview 0.0.16; caso persista, solicitar captura com a lista aberta e URL/ambiente visível. Retomar o mesmo debug ao receber evidência comparável. F1-T03 segue bloqueada; não concluir nem iniciar outra task.