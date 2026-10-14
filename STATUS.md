# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-13 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** com aceite humano “tudo funcionando”; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 é a única task ativa e segue aberta, aguardando novo teste humano após correção.** Preview Skip 0.0.16 (`85f220f`); produção não publicada.
- No teste humano de 0.0.15, a Champion confirmou que o preenchimento permanece ao trocar de aba, mas relatou rótulos divergentes. Foram revistos os textos do formulário e os nomes exibidos em `Dados da ficha`; versão 0.0.16 passou setup, análise estática, build e integrações. A suíte de testes do projeto não foi executada (`test.ran=false`).
- A versão 0.0.16 foi aberta no preview; os textos do intake e os três blocos condicionais LOAS, urbano e rural apareceram. A rota de detalhe de caso requer um ID de caso autenticado e não foi revalidada nesta rodada sem criar registro. O QA da plataforma não executou a suíte.
- **Limite de conteúdo:** cada bloco específico LOAS/urbano/rural permanece uma resposta de texto livre; agora seus títulos e orientações listam os tópicos encontrados nas fichas. Essa correção não cria uma pergunta/campo separado por tópico nem define obrigatoriedade jurídica. Não transformar a demonstração numa ficha estrutural mais extensa sem decisão de escopo; checklist rural permanece pendente de aprovação jurídica.
- **Persistência:** alternar para outra aba e voltar foi corrigido; rascunho segue em memória somente enquanto a ficha estiver montada. Navegar para fora/recarregar pode descartar o rascunho, pois não foi aprovado armazenamento local de dados pessoais (B-POL-01).
- **B-CHK-01 aberto:** provas rurais exemplificativas sem definição item a item de obrigatoriedade. Itens demonstrativos seguem marcados `PENDENTE APROVAÇÃO JURÍDICA`.
- **B-TIPO-01 resolvido:** cinco tipos rurais definidos; documentos da terra condicionais ao contexto rural. Decisão `06_notas/decisao-f1-t03-tipos-e-documentos-rurais-2026-10-13.md`.
- Não usar dados reais; não concluir F1-T03 nem iniciar outra task antes de aprovação humana explícita do reteste.

## Próximo passo
A Champion testar o preview 0.0.16, verificando se os rótulos agora correspondem às fichas, se o rascunho permanece ao alternar abas e se o fluxo documental funciona. Se algum nome continuar diferente, informar o texto da tela/campo exato.

## Bloqueios ativos
B-POL-01 (política de dados), B-RACI-01 (nomes por papel), **B-CHK-01 (aprovação jurídica final do checklist)**, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
