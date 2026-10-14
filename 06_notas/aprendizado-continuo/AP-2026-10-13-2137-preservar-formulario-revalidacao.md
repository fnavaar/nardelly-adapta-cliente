# AP-2026-10-13-2137 — Preservar formulários durante revalidação de sessão

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T03 / SPEC-1-002.
- Sinal: a rota protegida revalida a sessão no evento de foco; ao trocar a aba, renderizar `checking` no mesmo guard desmontava o formulário e apagava o estado React não salvo.
- Evidência: reprodução no preview 0.0.13; correção em `src/components/ProtectedRoute.tsx`; reteste no preview 0.0.15 preservou o texto sintético após alternar para outra aba e retornar.
- Regra reutilizável: durante revalidação de sessão na mesma rota, manter os filhos montados, bloquear temporariamente a interação e mostrar estado ocupado; redirecionar e limpar sessão se a revalidação falhar. Cargas iniciais ou mudança de permissões continuam atrás do gate.
- Quando aplicar: páginas protegidas com formulário/estado local não salvo que revalidam sessão ao recuperar foco.
- Quando não aplicar: primeira carga ou transição para uma permissão/rota diferente; nesses casos manter o gate de autorização antes de renderizar conteúdo protegido.
- Confiança: alta — causa reproduzida e correção verificada no preview; o reteste do usuário continua pendente.
- Privacidade: sem credenciais, dados pessoais ou conteúdo bruto.
