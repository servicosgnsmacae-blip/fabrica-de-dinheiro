# Roadmap — AgencyOS v0.1

Este roadmap formaliza a evolução do AgencyOS. Nenhuma fase posterior deve começar antes que os critérios de conclusão e as dependências da fase atual estejam satisfeitos e Gustavo autorize o avanço quando aplicável.

## FASE 0 — Constituição e arquitetura

### Objetivo
Preservar, decompor e formalizar a arquitetura fundadora do AgencyOS.

### Entregáveis
- Master Plan preservado;
- Constituição;
- arquitetura conceitual;
- Agency DNA;
- lifecycle;
- learning system;
- governance;
- observability;
- economics;
- roadmap;
- status e decisões arquiteturais.

### Dependências
Nenhuma implementação técnica.

### Critérios de conclusão
- documentos coerentes entre si;
- princípios constitucionais explícitos;
- decisões abertas identificadas;
- escopo de implementação bloqueado;
- aprovação de Gustavo para avançar.

### Riscos
- ambiguidade conceitual;
- documentação contraditória;
- começar tecnologia antes de fechar domínio e autoridade.

### NÃO será construído
- agentes de produção;
- APIs externas;
- banco de produção;
- automações;
- publicação;
- geração de vídeo;
- integrações pagas.

---

## FASE 1 — Fundação técnica da plataforma

### Objetivo
Criar o núcleo técnico mínimo que represente conceitos já aprovados na arquitetura.

### Entregáveis
- estrutura técnica do projeto;
- modelos conceituais de agency, job, event, policy e audit;
- configuração e versionamento;
- contratos internos mínimos;
- ambiente de desenvolvimento e testes.

### Dependências
FASE 0 aprovada.

### Critérios de conclusão
- conceitos arquiteturais representados sem dependência de fornecedor específico;
- testes básicos de domínio;
- nenhuma integração externa necessária para demonstrar o núcleo.

### Riscos
- escolher tecnologia que acople a plataforma cedo demais;
- confundir modelos de dados com regras de negócio;
- criar abstrações prematuras.

### NÃO será construído
- pipeline de conteúdo completo;
- publicação real;
- analytics externo;
- monetização;
- múltiplas agências em produção.

---

## FASE 2 — Agência-Mãe mínima

### Objetivo
Implementar o Control Plane mínimo capaz de registrar, governar e acompanhar Agências de Ativo.

### Entregáveis
- registry de agências;
- lifecycle control;
- políticas e permissões básicas;
- orçamento conceitual;
- criação controlada de agência a partir de template;
- incident/escalation model mínimo.

### Dependências
Fundação técnica estável.

### Critérios de conclusão
- Agência-Mãe consegue criar, pausar, retomar e encerrar uma agência de teste;
- todas as transições ficam auditáveis;
- nenhuma agência consegue exceder permissões definidas.

### Riscos
- centralização excessiva;
- autoridade mal delimitada;
- lifecycle sem rollback.

### NÃO será construído
- conteúdo real;
- integração com YouTube/Instagram;
- evolução autônoma;
- escala de portfólio.

---

## FASE 3 — Primeira Agência de Ativo

### Objetivo
Criar a primeira espécie funcional de Asset Agency, inicialmente orientada a YouTube, ainda com execução controlada.

### Entregáveis
- template versionado;
- Agency DNA real;
- papéis internos mínimos;
- jobs e estados necessários ao pipeline piloto;
- sandbox funcional;
- critérios de pilot/active/scale.

### Dependências
Agência-Mãe mínima funcionando.

### Critérios de conclusão
- uma agência nasce por fluxo formal;
- opera em sandbox;
- respeita orçamento, permissões e memória própria;
- pode ser encerrada preservando conhecimento.

### Riscos
- misturar lógica específica de YouTube com o núcleo da plataforma;
- conceder autonomia excessiva cedo demais.

### NÃO será construído
- produção automática em escala;
- publicação irrestrita;
- 20 canais;
- aprendizado autônomo em produção.

---

## FASE 4 — Academia e sistema de aprendizado

### Objetivo
Construir o mecanismo institucional de conhecimento, experimentação e evolução controlada.

### Entregáveis
- memória episódica, semântica e procedural;
- evidence/provenance model;
- experiment registry;
- Champion/Challenger;
- promotion rules de conhecimento;
- Academy como camada de conhecimento reutilizável.

### Dependências
Primeira Asset Agency definida e jobs observáveis.

### Critérios de conclusão
- aprendizado não depende de chats de modelo;
- hipóteses podem ser testadas sem alterar produção diretamente;
- rollback é possível;
- conhecimento local só sobe para a plataforma por processo governado.

### Riscos
- transformar correlação em regra;
- memória sem proveniência;
- crescimento descontrolado de conhecimento.

### NÃO será construído
- auto-otimização irrestrita;
- transferência automática global de qualquer aprendizado.

---

## FASE 5 — Produção de conteúdo

### Objetivo
Implementar o pipeline de produção de conteúdo com separação de funções, QA e rastreabilidade.

### Entregáveis
- pesquisa;
- coleta de evidências;
- estratégia;
- roteiro;
- fact-check;
- QA;
- geração de assets necessária ao piloto;
- custos por job/conteúdo.

### Dependências
Learning System e governança mínima.

### Critérios de conclusão
- pacote de conteúdo pode ser produzido ponta a ponta em sandbox;
- fatos relevantes possuem proveniência;
- criador não é único aprovador;
- custos e versões são registrados.

### Riscos
- alucinação;
- conteúdo repetitivo ou fraco;
- custos sem controle;
- direitos autorais e políticas de plataforma.

### NÃO será construído
- publicação autônoma irrestrita;
- escala para vários canais.

---

## FASE 6 — Publicação e analytics

### Objetivo
Fechar o ciclo operacional real entre produção, publicação, confirmação e métricas.

### Entregáveis
- gateway de publicação;
- integração inicial com a plataforma-alvo;
- reconciliação pós-publicação;
- analytics ingest;
- métricas de conteúdo/agência;
- incident handling de publicação.

### Dependências
Pipeline de conteúdo aprovado em sandbox.

### Critérios de conclusão
- conteúdo aprovado pode ser publicado de forma controlada;
- estado real é reconciliado;
- analytics retorna à plataforma;
- incidentes materiais escalam corretamente.

### Riscos
- falha de API;
- publicação incorreta;
- credenciais e permissões;
- mudanças de política externa.

### NÃO será construído
- autonomia L4/L5;
- criação automática de dezenas de agências.

---

## FASE 7 — Evolução autônoma

### Objetivo
Permitir que a agência aprenda e melhore de forma controlada, usando dados reais.

### Entregáveis
- closed loop analytics → hypothesis → experiment → learning;
- Champion/Challenger operacional;
- promoção e rollback de versões;
- autonomia L3/L4 conforme evidência;
- regras econômicas de scale/recovery.

### Dependências
Produção, publicação, analytics, governança e observability maduros o suficiente.

### Critérios de conclusão
- a agência consegue testar melhorias sem comprometer produção;
- mudanças vencedoras são promovidas com evidência;
- mudanças ruins são revertidas;
- decisões econômicas usam dados rastreáveis.

### Riscos
- otimização para métrica errada;
- drift de comportamento;
- overfitting;
- aumento de custos sem ganho econômico.

### NÃO será construído
- autonomia de portfólio sem limites;
- replicação massiva antes da prova econômica.

---

## FASE 8 — Escala para múltiplas agências

### Objetivo
Transformar a primeira operação comprovada em um portfólio de múltiplas Agências de Ativo isoladas e governadas pela Agência-Mãe.

### Entregáveis
- 3–5 agências iniciais;
- isolamento de orçamento, memória, identidade e credenciais;
- portfolio dashboard;
- capital allocation;
- gestão de concorrência por recursos;
- preparação para 10–20 ativos.

### Dependências
Uma Asset Agency comprovada ponta a ponta, com economia e aprendizado controlados.

### Critérios de conclusão
- múltiplas agências operam sem contaminação entre si;
- falha local não derruba o portfólio;
- orçamento pode ser realocado por evidência;
- plataforma demonstra capacidade de escalar com governança.

### Riscos
- multiplicar falhas;
- custos de infraestrutura;
- excesso de dependência de um fornecedor;
- complexidade operacional;
- perda de observabilidade.

### NÃO será construído
- crescimento ilimitado sem gates;
- autonomia L5 sem limites de capital e risco definidos;
- novas espécies de agência sem template e governança próprios.

---

## Regra de avanço

Nenhuma fase posterior será iniciada automaticamente. O avanço depende de critérios de conclusão, ausência de bloqueios críticos e autorização de Gustavo quando a fase representar mudança material de escopo ou risco.
