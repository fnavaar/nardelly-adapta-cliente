# Changelog — Nardelly Advogados · adapta-cliente

## 2026-09-22 — F1-T01 implementada; aguardando teste humano
- Projeto Skip `Central de Processos — Nardelly` criado (id 60649; SkipCloud running).
- Autenticação com sete papéis funcionais, vínculo server-side e massa sintética criada.
- RBAC/RLS server-side fail-closed aplicado em usuários, casos, pendências, rotas de triagem e auditoria.
- Trilha append-only com ator, data/hora, estado anterior e novo; negações e autoelevação auditadas.
- Revogação gira `tokenKey`: token fresco autenticou antes (HTTP 200) e foi recusado imediatamente após (HTTP 401); fixture restaurada ao final.
- QA Skip v0.0.9: setup, análise estática, build, integrações e testes passaram.
- Provas API isoladas passaram: sete logins, três negações HTTP 403, autoelevação HTTP 403, revogação e auditoria; preview testado com login/administração.
- **Gate pendente:** teste humano e aceite explícito da champion Nardelly.

## 2026-09-22 — DEBUG task F1-T01: falhas das provas GREEN → corrigido
- Sintoma: coleções base publicadas inicialmente sem campos/regras completos; negações retornavam 400 antes dos gates; auditoria sem autodate; rate limit contaminou uma rodada; token já emitido não era invalidado por `ativo=false`.
- Causa raiz confirmada: `new Collection({...})` não persistiu fields/regras nesse runtime; createRules restritivas interceptavam antes dos hooks; rotação de token não estava implementada.
- Correção: migrações 0003/0004 com `fields.add`, regras completas e autodates; gates fail-closed; hooks sem duplicidade; `refreshTokenKey()` na revogação; suíte isolada sem login em massa.
- Resultado: QA v0.0.9 verde e reprodução final passou.

## 2026-09-22 — Champion confirmado e Jornada sincronizada
- Champion **@Nardelly** confirmado por Navaar (antes responsável provisório); B-RACI-01 segue aberto apenas para os nomes por papel da operação (call de setup).
- Jornada `fase_1.md` validada pós-sincronizador: 7 UUIDs gerados pelo portal (5 tasks + 2 subtasks), parser PASS com `--require-ids`.
- Visibilidade pública do repo autorizada; pendente de ação manual no GitHub (Settings → Change visibility) por ausência de ferramenta no conector/credencial do CLI.

## 2026-09-22 — Handoff inicial (Fase 1)
- Pasta operacional criada pela consultoria com a estrutura canônica.
- Jornada `04_fase-atual/fase.md` com F1-T01..T05 (fase-format:2).
- SPECs F1 (4) em `04_fase-atual/specs/`.
- Manifesto de integridade: `handoff-manifest.json`.
- Privacidade: escopo base/definitivo, análise crítica, requisitos e fases futuras ficam na consultoria.
- Repositório GitHub `fnavaar/nardelly-adapta-cliente` criado e publicado em 22/09.