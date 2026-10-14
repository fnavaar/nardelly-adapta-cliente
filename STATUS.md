# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-14 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** após aceite humano; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 em implementação** no escopo previamente autorizado: completar e verificar o mecanismo demonstrativo sintético já previsto na SPEC-1-002; conteúdo jurídico continuará explicitamente sem aprovação.
- A Champion aceitou o reteste visual dos nomes “Benefício urbano”/“Benefício rural” no preview 0.0.17 (`b299fc5`); isso é aceite parcial de uma correção anterior, não aceite da task documental.
- **B-CHK-01 permanece aberto:** provas rurais no PDF são exemplificativas. Nenhum item demonstrativo será apresentado como obrigação jurídica aprovada; nenhuma evidência ou rótulo poderá sugerir validade jurídica oficial.
- A inspeção do mecanismo F1-T03 encontrou problemas a corrigir e provar nesta rodada: checklist rural instanciado inclusive sem família/tipo reconhecido, itens sintéticos marcados `obrigatoria=true` apesar de pendente jurídico, possível criação concorrente de checklist duplicado por caso, checagem de protocolo duplicado apenas em hook de requisição (não atômica), UI sem tratar retorno após criar protocolo e erro em query de tela `try/catch` auditado.
- Nenhum dado real. Nenhuma publicação em produção. A alteração preexistente `.skip.config.json` permanece intocada.

## Próximo passo
Verificar o fluxo demonstrativo completo em ambiente preview com registros sintéticos, incluindo cada uma das cinco categorias rurais e um tipo desconhecido/incompleto, protocolo único e erro visível. Depois QA automatizado. B-CHK-01 precisará de checklist jurídico v1 aprovado antes de produção/conclusão F1-T03; este ciclo não inicia F1-T04.

## Bloqueios ativos
F1-T03: B-CHK-01 (conteúdo jurídico) bloqueia conclusão/produção, e aceite humano da implementação documental desta rodada. B-POL-01 mantém dados reais bloqueados. B-RACI-01, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX permanecem ativos. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
