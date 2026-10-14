# STATUS — Nardelly Advogados · adapta-cliente

**Data:** 2026-10-14 · **Fase atual:** 1 (fundação segura, intake e registro documental)

## Estado
- **F1-T01 concluída (1/5 tasks; 20%)** após aceite humano explícito; recibo `05_entregas/recibo-f1-t01-2026-10-05.md`.
- **B-INTAKE-01 resolvido. F1-T02 concluída (2/5 tasks; 40%)** após aceite humano; recibo `05_entregas/recibo-f1-t02-2026-10-13.md`.
- **F1-T03 continua aberta; não concluída.** A Champion confirmou que, na versão 0.0.17 (`b299fc5`), os rótulos “Benefício urbano” e “Benefício rural” estão corrigidos. Esse é aceite parcial do reteste do seletor, não da task documental inteira.
- Verificação em browser: o Radix Select abriu e apresentou no snapshot os itens corretos. QA 0.0.17: setup/estático/build/integrações passaram; suíte não executada (`test.ran=false`). Produção não publicada.
- **Bloqueio de conteúdo jurídico B-CHK-01 permanece:** a SPEC-1-002 diz que F1-T03 só pode ser concluída com checklist v1 registrado e aprovado. A decisão da Champion mantém provas rurais exemplificativas e itens pendentes de aprovação. `05_entregas/` não possui recibo F1-T03 nem evidência do fluxo ponta a ponta CA-1-102..106 (protocolo, devolução, bloqueio/ exceção, trilha, casos sintéticos por tipo).
- B-POL-01 também segue bloqueando dados reais e persistência local do rascunho. Os blocos LOAS/urbano/rural permanecem em texto livre; sem decisão para transformá-los em campos separados.

## Próxima ação
Aguardar a definição/aprovação jurídica do checklist v1 para B-CHK-01. Depois retomar validação da mesma F1-T03 ponta a ponta com dados sintéticos. Não iniciar F1-T04 enquanto F1-T03 não cumprir os critérios e for aprovada.

## Bloqueios ativos
**F1-T03 bloqueada por B-CHK-01 e ausência de evidência documentada do fluxo completo**, além de B-POL-01, B-RACI-01, B-BASE-01, B-ADV-01 e B-ADVBOX-ADVOX. B-TIPO-01, B-ENV-01 e B-INTAKE-01 resolvidos.
