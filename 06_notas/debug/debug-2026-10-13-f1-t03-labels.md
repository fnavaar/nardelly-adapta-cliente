# Debug Summary — F1-T03: rótulos divergentes após confirmação da correção de abas

**Data:** 2026-10-13 · **Task:** F1-T03 · **Estado:** aguardando teste humano; não concluída.

## Resultado humano recebido
A Champion confirmou que, no reteste da versão 0.0.15, o preenchimento permaneceu após trocar de aba; marcou que ainda há rótulos divergentes. A falha de retenção foi resolvida; a task continua aberta pelo critério de validação de rótulos/fluxo.

## Comparação das fontes e implementação
As fichas LOAS, urbano e rural compartilham um núcleo: data/canal/atendente/indicação; pessoa atendida e se é titular; dados do titular; perguntas familiares condicionais; solicitação de documentos; contrato. Os rótulos centrais foram alinhados. A distinção “Família do benefício” vs “Tipo específico de benefício” foi mantida e explicitada para evitar mistura.

O detalhe do caso anteriormente mostrava abreviações (“Titular”, “Nascimento”, “Contrato assinado?”, “Parente já atendeu?”); foram substituídas por nomes completos associados aos campos reais. Também foram adicionados rótulos do detalhe para canal, atendente, indicação, vínculo, perguntas familiares, solicitação de documentos e assinatura à rogo, quando esses dados existem.

## Conteúdo por família — limite confirmado
- O código persiste cada bloco (`loas_dados`, `urbano_dados`, `rural_dados`) como **um único texto livre**.
- As fichas de origem têm várias perguntas distintas por benefício/família (exemplos: LOAS renda/CadÚnico/moradia/grupo/gastos; urbano idade/benefícios anteriores/negativas/ação judicial/vínculos e perguntas de incapacidade/salário-maternidade/pensão/reclusão; rural terras/companheiros/filhos/pais e seções específicas do benefício).
- A decisão aprovada B-INTAKE-01 diz que os blocos são condicionais, que grupo familiar LOAS não tem limite fixo e que obrigatoriedade por pergunta específica fica para B-CHK-01. Não autoriza expressamente converter cada pergunta em coluna/campo persistido.
- Por isso, nesta correção alinharam-se cabeçalho e instruções e deixaram-se explícitos os tópicos no placeholder, sem criar requisitos ou validações individuais. A divergência humana pode persistir se o pedido for campos/controles separados; isso exige confirmar o nível estrutural esperado antes de expandir o schema/formulário.

## Alterações e prova
- Alterados: `src/pages/NovaFicha.tsx`, `src/pages/CasoDetalhe.tsx` — textos de rótulos/títulos/instruções apenas; sem alterações de schema, dados, validações ou regras jurídicas.
- QA Skip 0.0.16 (`85f220f`): setup, análise estática, build e integrações passaram; `test.ran=false` (suíte não executada pela plataforma).
- Preview 0.0.16: `/intake/nova` autenticado como conta sintética de Atendimento; snapshot confirmou rótulos visíveis e o bloco condicional de cada família. Não enviamos formulário nem criamos caso sintético. Por isso, a tela de detalhe não foi navegada com registro válido nesta execução.
- Nenhum dado real usado; produção não publicada.

## Reteste pendente
Aguardar a Champion conferir no preview 0.0.16 os rótulos da ficha e do detalhe e informar se correspondem às fichas. Se a divergência for que cada pergunta deve ter controle/campo próprio em vez do campo livre da família, registrar essa definição antes de novo escopo; não inventar campos ou obrigatoriedade jurídica.
