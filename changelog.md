# Changelog — Nardelly Advogados · adapta-cliente

## 2026-10-14 — F1-T03 retomada: plano B sintético, sem aprovação jurídica
- Com autorização da Champion (“pode prosseguir”, 12:36 BRT), retomada a mesma F1-T03 dentro da SPEC-1-002; nenhuma nova task aberta.
- Antes de implementar, a revisão do código e do estado Skip 60649 confirmou migração 0006 aplicada e achou: hook cria checklist rural até para família/tipo vazio ou não reconhecido; todos os itens de demonstração eram `obrigatoria=true` apesar do rótulo `PENDENTE APROVAÇÃO JURÍDICA`; protocolo dependia apenas de checagem de duplicidade em hook de requisição sem índice único; UI podia deixar estado da pendência inconsistente após falha ao atualizar depois de criar protocolo; e o carregamento de dados do caso mostrava erro sem status acessível em um caminho.
- Escopo desta rodada é fechar mecanismos técnicos com massa sintética conforme o plano B da SPEC. O conteúdo e a aprovação jurídica do checklist continuam pendentes; nenhuma pesquisa ou requisito legal será inventado.
- `.skip.config.json` já estava alterado antes deste ciclo e será preservado. Preview atual é 0.0.17 (`b299fc5`); produção não publicada.
