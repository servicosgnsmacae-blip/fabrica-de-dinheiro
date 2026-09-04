# AgencyOS

AgencyOS é o sistema operacional de uma empresa autônoma de ativos digitais.

A arquitetura é baseada em uma **Agência-Mãe**, responsável por governança, portfólio, capital e regras, e em **Agências de Ativo**, responsáveis por operar ativos econômicos individuais como canais do YouTube ou perfis do Instagram.

Este projeto **não é uma coleção de automações**.

## Estado atual

- Arquitetura: **v0.1**
- Fase: **FASE 0 — Constituição e arquitetura**
- Implementação funcional: **não iniciada**
- Próximo gate: aprovação explícita de Gustavo para iniciar a FASE 1

## Comece por aqui

Uma nova sessão de Codex ou um novo colaborador deve ler:

1. `PROJECT_STATUS.md`
2. `docs/CONSTITUTION.md`
3. `docs/MASTER_PLAN.md`
4. `DECISIONS.md`
5. `docs/ROADMAP.md`

## Estrutura

```text
/
├── README.md
├── PROJECT_STATUS.md
├── DECISIONS.md
├── docs/
│   ├── MASTER_PLAN.md
│   ├── CONSTITUTION.md
│   ├── ARCHITECTURE.md
│   ├── AGENCY_DNA.md
│   ├── AGENCY_LIFECYCLE.md
│   ├── LEARNING_SYSTEM.md
│   ├── GOVERNANCE.md
│   ├── OBSERVABILITY.md
│   ├── ECONOMICS.md
│   └── ROADMAP.md
├── academy/
├── agents/
├── platform/
├── templates/
└── experiments/
```

## Regra de fase

Na FASE 0 não devem ser implementados agentes de produção, geração de vídeos, publicação em YouTube ou Instagram, APIs externas, automações, banco de dados de produção ou integrações pagas.

A próxima fase só começa após aprovação explícita do proprietário do sistema.
