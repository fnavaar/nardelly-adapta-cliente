# AP-2026-10-05 — Isolamento de sessão por aba e visibilidade da trilha

- Status: candidato
- Escopo: projeto do cliente
- Task/SPEC: F1-T01 / SPEC-1-001
- Sinal: o PocketBase JS SDK LocalAuthStore padrão compartilha auth state via localStorage entre abas; isso pode misturar identidades quando champion testa papéis simultaneamente. A trilha pode estar gravada no servidor e ainda assim falhar operacionalmente se não houver uma tela adequada para consultá-la.
- Evidência: origem `pocketbase/js-sdk` v0.26.9 (`src/stores/LocalAuthStore.ts`); no preview v0.0.10, aba 1 manteve Administração enquanto aba 2 autenticou Advogado; ao revogar, token fresco passou de HTTP 200 a HTTP 401 e, ao retornar à aba, o cliente apresentou login. A consulta da coleção `auditoria` retornou 47 eventos e a UI mostrou data/hora, ator, ação, entidade e estados.
- Regra reutilizável: se vários usuários/roles forem testados na mesma origem, usar armazenamento de auth isolado por sessão/aba; validar token e papel no servidor ao entrar/retomar áreas protegidas; garantir uma UI para ler a trilha exigida pelo aceite.
- Quando aplicar: apps PocketBase com múltiplas identidades simultâneas no mesmo navegador e auditoria como critério de aceite.
- Quando não aplicar: não substituir RLS/server-side rules por controles visuais; a interface é apoio, não fronteira de autorização.
- Confiança: alta para compartilhamento LocalAuthStore, bloqueio por papel, sessão revogada e visualização da trilha, todos verificados nesta versão; teste humano do clique de revogação ainda pendente.
- Privacidade: sem segredo ou dado pessoal; evidências usam apenas contas sintéticas.
