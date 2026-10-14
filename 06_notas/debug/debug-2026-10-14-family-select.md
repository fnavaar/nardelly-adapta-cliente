# Debug Summary — rótulos visuais das opções urbano e rural

**Data:** 2026-10-14 · **Task:** F1-T03 · **Estado:** correção do rótulo aceita; task documental ainda aberta/bloqueada.

## Sintoma confirmado pela Champion
O problema relatado era a grafia visual das opções:
- `Benefício urbano` aparecia como `bene la urbano`;
- `Benefício rural` aparecia como `bene ate rural`.

O placeholder `Selecione…` não era o problema nem o critério de aceite. A captura `uploads/dc85ac48-image.png` é da tela de intake no preview.

## Correção e reteste
No Skip 60649, a versão 0.0.17 (`b299fc5`) trocou somente o `<select>` nativo de Família do benefício para o Radix Select já existente, mantendo os valores persistidos `loas`, `urbano`, `rural` e os textos de código. QA: setup PASS; análise estática PASS; build PASS; integrações PASS; a suíte não executou (`test.ran=false`). O browser autenticado mostrou no listbox acessível os três rótulos completos; a Champion depois confirmou “os nomes foram corrigidos”. Reteste do rótulo aceito.

Nenhuma ficha foi enviada/criada, não foi usado dado real e a produção não foi publicada.

## Verificação da F1-T03 completa
A aprovação acima cobre apenas o defeito de rótulo. A SPEC-1-002 exige checklist jurídico v1 aprovado (B-CHK-01), bem como evidência da demonstração documental CA-1-102..106. O bloqueador segue aberto, a decisão da Champion diz que provas rurais são exemplificativas, e não foi encontrado recibo F1-T03 nem evidência de execução ponta a ponta em `05_entregas/`. Não há base para concluir a task inteira.

## Gate atual
F1-T03 permanece aberta/bloqueada por B-CHK-01 e ausência de evidência da demonstração completa. Não iniciar F1-T04. Próximo: obter checklist v1 aprovado e retomar as provas restantes com fixtures sintéticas.
