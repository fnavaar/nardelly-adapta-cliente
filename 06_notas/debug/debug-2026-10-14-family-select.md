# Debug Summary — rótulos visuais das opções urbano e rural

**Data:** 2026-10-14 · **Task:** F1-T03 · **Estado:** aguardando teste humano; não concluída.

## Sintoma confirmado pela Champion
O problema relatado é a grafia visual das opções no seletor “Família do benefício”:
- `Benefício urbano` aparece como `bene la urbano`;
- `Benefício rural` aparece como `bene ate rural`.

O placeholder `Selecione…` não era o problema nem o critério de aceite. O endereço na captura `uploads/dc85ac48-image.png` corresponde ao preview 0.0.16 correto.

## Evidência e diagnóstico
A fonte `src/pages/NovaFicha.tsx` tem os textos corretos em `FAMILIAS` e valores `urbano`/`rural`. A captura da Champion mostra que a apresentação visual não corresponde ao texto esperado. O snapshot acessível do preview antigo retornava os textos corretos, portanto a causa técnica exata da distorção não foi isolada independentemente no navegador de verificação. Não atribuir a falha ao placeholder.

## Correção aplicada
No Skip 60649, versão 0.0.17 (`b299fc5`), somente o `<select>` nativo do campo Família foi trocado pelo Radix Select já existente. Os rótulos e valores de domínio permaneceram:
- `LOAS (benefício assistencial)` → `loas`
- `Benefício urbano` → `urbano`
- `Benefício rural` → `rural`

A troca é uma correção de apresentação para o sintoma visual; não altera validação, persistência ou regras jurídicas.

## Verificações
- QA Skip: setup PASS; análise estática PASS; build PASS; integrações PASS; suíte não executada (`test.ran=false`).
- No preview 0.0.17, o browser autenticado abriu o listbox Radix e o snapshot acessível exibiu exatamente as três opções corretas, inclusive “Benefício urbano” e “Benefício rural”. Ainda falta confirmação visual humana no navegador da Champion.
- Nenhuma ficha criada ou enviada; nenhum dado real; produção não publicada.

## Reteste humano pendente
No preview 0.0.17, conferir **somente se os nomes aparecem visualmente escritos exatamente “Benefício urbano” e “Benefício rural”**. “Selecione…” não é critério do defeito relatado. Não enviar a ficha. A F1-T03 só sai do gate humano após retorno explícito da Champion.
