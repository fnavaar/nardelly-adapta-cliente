# Debug Summary — seletor de família de benefício: relato não reproduzido

**Data:** 2026-10-14 · **Task:** F1-T03 · **Estado:** bloqueada para evidência; não concluída.

## Resultado humano recebido
A Champion reportou que no campo “Família do benefício (LOAS, urbana ou rural)” as opções aparecem como “LOAS”, “bene la urbano” e “bene la rural”.

## Reprodução executada
- Projeto: Skip 60649, preview URL `https://central-de-processos-nardelly-65f79--preview.goskip.app`.
- Versão observada no status: 0.0.16 (`85f220f`); produção segue não publicada.
- Entrado com conta sintética de Atendimento e aberto `/intake/nova`.
- Inspecionado o snapshot e o DOM do `select#familia_beneficio`.
- Resultado real: `Selecione…`; `LOAS (benefício assistencial)` (`loas`); `Benefício urbano` (`urbano`); `Benefício rural` (`rural`).
- A fonte de `src/pages/NovaFicha.tsx` da árvore ativa define os mesmos textos em `FAMILIAS`.
- Nenhuma ficha criada/enviada; nenhum dado pessoal real usado.

## Conclusão
A divergência relatada não foi reproduzida neste preview e a source-of-truth atual já contém opções em português. A causa permanece desconhecida. Pode ser diferença do ambiente/versão, cache ou contexto visual, mas nenhuma hipótese foi confirmada. Alterar rótulos sem reproduzir poderia introduzir erro.

## Próximo passo
Pedir confirmação de que a Champion estava no preview 0.0.16; se sim e o defeito persistir, pedir uma captura com a lista expandida e a URL/ambiente visível. Retomar o mesmo debug quando houver evidência comparável. F1-T03 permanece bloqueada; não concluir ou iniciar outra task.