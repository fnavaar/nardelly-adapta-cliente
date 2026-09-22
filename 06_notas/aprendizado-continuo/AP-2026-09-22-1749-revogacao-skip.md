# AP-2026-09-22-1749 — Revogação server-side no Skip

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T01 / SPEC-1-001
- Sinal: alterar apenas o campo funcional `ativo` não encerra tokens PocketBase já emitidos; a revogação imediata exige rotação server-side do `tokenKey`.
- Evidência: versão Skip 0.0.9; token sintético fresco recebeu HTTP 200 em `auth-refresh` antes da revogação e HTTP 401 no mesmo endpoint imediatamente depois; auditoria registrou a transição ativo=true → ativo=false.
- Regra reutilizável: toda revogação deve rotacionar `tokenKey` no hook server-side e ser testada com um token fresco validado antes da mudança.
- Quando aplicar: ao implementar revogação ou cessação imediata de acesso em coleções auth do Skip/PocketBase.
- Quando não aplicar: não usar como substituto de regras RLS por papel; `tokenKey` revogado não define o que cada papel pode fazer.
- Confiança: alta — comportamento reproduzido no backend real e confirmado por HTTP 200/401.
- Privacidade: sem segredo, credencial ou dado pessoal; somente fixtures sintéticas e IDs técnicos.
