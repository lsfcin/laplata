# laplata — Roadmap
> Pending work only — a finished item is cut, not ticked; done work is deleted and git is the history.

## Status

M1 pendente. Executável por qualquer modelo (não precisa Fable) — tarefas mecânicas de dados.

## Backlog

- [ ] Camada "extrato do bairro": relatório mensal narrado por LLM por bairro do Recife (depende M2)
- [ ] Dataset paper ("Brazilian money-leakage atlas") — ver academy/papers do programa
- [ ] Open Finance opt-in (extrato de vazamento pessoal) — fase distante, exige consentimento e cuidado

---

## Milestone 1 — data-hunt + first-viz 🔲 PENDING

### Problem
O programa instituto afirma ralos com números de imprensa (branches/instituto/RALOS.md tem TODOs). Precisa de fonte primária reproduzível e de UMA visualização que revele algo que 3 pessoas não sabiam (critério do goal laplata).

### Solution
Pipeline mínimo: download → DuckDB → 1 script de viz. Fontes na ordem: (1) estatísticas Pix BCB, (2) estudo especial BCB ago/2024 sobre bets (achar PDF primário), (3) POF/IBGE consumo das famílias. Perguntas candidatas pra first-viz: "quanto Recife manda pra bets por mês?" ou "quanto o comércio de PE paga de MDR por ano?".

### Checklist
- [ ] Levantar catálogos: dadosabertos.bcb.gov.br + estatísticas de pagamento BCB + microdados POF
- [ ] 1 dataset baixado e carregado (DuckDB)
- [ ] 1 visualização com tese, mostrada a 3 pessoas — registrar reações
- [ ] Números confirmados → substituir fontes de imprensa em RALOS.md pelas primárias

### Key Files
Nenhum ainda. Criar `src/ingest/` (um módulo por fonte) e `src/viz/`. Regras R1-R6 de code/SPECS.md aplicam.

### Scope
NÃO construir dashboard/site no M1. Uma viz estática que revela > plataforma vazia.
