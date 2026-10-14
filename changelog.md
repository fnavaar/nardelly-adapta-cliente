# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-14 — Pedido da Champion: estudo e implementação da API ADVBOX
- Pedido recebido às 14:09 BRT: “estude, entenda e implemente toda a documentação dessa API: https://guia.advbox.com.br/api”.
- Estudo realizado: documentação de desenvolvedor localizada em https://api.softwareadvbox.com.br (o link da central de ajuda aponta para artigos de token/n8n). Documentação completa dos 22 endpoints baixada de /llms-full.txt (121 KB, doc v1.25.0 de 22/09/2026).
- Resumo técnico: base https://app.advbox.com.br/api/v1; Bearer Token fornecido pela ADVBOX a parceiros/integradores aprovados; limites GET 30/min, POST 500/dia por rota, PUT 500/dia; 22 endpoints em 7 recursos (Customers 4, Lawsuits 8, Posts/Tarefas 2, Publications 1, Transactions 4, Documents 2, Settings 1); GET /settings deve ser consultado primeiro para obter os IDs da conta.
- DÚVIDA: integração ADVBOX não consta na SPEC da Fase 1 (F1-T01..T05). Escopo, objetivos e prioridade dependem de decisão do consultor. Nada foi implementado; a task ativa F1-T03 permanece bloqueada e intocada.
- Pré-requisitos identificados para qualquer implementação: token de API (gerado em Conta e assinatura → Nossos produtos → API ADVBOX) e plano/integração habilitada no escritório.
- Às 14:16 BRT, a Champion solicitou integração produtiva ADVBOX–Skip “fora da metodologia”. A SPEC-1-004 limita F1-T05 a uma prova timeboxed em ambiente de teste e exclui integração produtiva; F1-T03 segue ativa e bloqueada. DÚVIDA: o consultor deve decidir sobre nova SPEC/escopo, prioridade e pré-condições. Nenhuma alteração foi feita no Skip e nenhum gate foi alterado.

## 2026-10-14 — F1-T03 retomada: plano B sintético, sem aprovação jurídica
- Com autorização da Champion (“pode prosseguir”, 12:36 BRT), retomada a mesma F1-T03 dentro da SPEC-1-002; nenhuma nova task aberta.
- Antes de implementar, a revisão do código e do estado Skip 60649 confirmou migração 0006 aplicada e achou: hook cria checklist rural até para família/tipo vazio ou não reconhecido; todos os itens de demonstração eram `obrigatoria=true` apesar do rótulo `PENDENTE APROVAÇÃO JURÍDICA`; protocolo dependia apenas de checagem de duplicidade em hook de requisição sem índice único; UI podia deixar estado da pendência inconsistente após falha ao atualizar depois de criar protocolo; e o carregamento de dados do caso mostrava erro sem status acessível em um caminho.
- Escopo desta rodada é fechar mecanismos técnicos com massa sintética conforme o plano B da SPEC. O conteúdo e a aprovação jurídica do checklist continuam pendentes; nenhuma pesquisa ou requisito legal será inventado.
- `.skip.config.json` já estava alterado antes deste ciclo e será preservado. Preview atual é 0.0.17 (`b299fc5`); produção não publicada.

## 2026-10-14 — F1-T03: aplicação/QA bloqueados
- Foram escritos ajustes no working tree do Skip para plano B sintético opcional, roteamento server-side de checklist/protocolo/transições/devolução/encaminhamento e atualização de UI. A migração 0007, hooks e UI ainda não estão aplicados no preview.
- `skip_project_apply_changes` retornou `Unknown error`. O status consultado em seguida confirmou 13 arquivos pendentes (incluindo `.skip.config.json`, alteração preexistente), versão/preview ainda 0.0.17 (`b299fc5`), produção não publicada; lista de migrações continua até 0006. QA não executou.
- Nenhuma ficha, protocolo, pessoa ou outro registro de teste foi criado; não houve gravação de dados de cliente.
- Estado: F1-T03 `bloqueada`. Próxima ação: revisar arquivos pendentes e recuperar aplicação/QA, sem descartar mudanças; só então avaliar teste sintético no preview. B-CHK-01 permanece pendente; não iniciar F1-T04.