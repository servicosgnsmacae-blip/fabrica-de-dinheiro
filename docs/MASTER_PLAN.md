# Master Plan — AgencyOS v0.1

## 1. O que estamos construindo

O AgencyOS será o **sistema operacional de uma empresa autônoma de ativos digitais**.

No topo existe uma **Agência Mãe**.

Ela não produz vídeos, posts ou thumbnails diretamente. A função dela é:

- encontrar oportunidades;
- criar novas agências;
- distribuir orçamento;
- estabelecer regras;
- acompanhar desempenho;
- transferir aprendizado;
- acelerar vencedores;
- corrigir operações problemáticas;
- desligar operações que deixaram de fazer sentido.

Abaixo dela existem as **Agências de Ativo**.

Uma agência pode administrar, por exemplo:

> YouTube Channel #001  
> Instagram Profile #004  
> TikTok #007  
> Newsletter #012

Cada agência é uma unidade operacional autônoma, com objetivo, orçamento, identidade, memória, equipe de IAs e indicadores próprios.

A arquitetura geral fica assim:

```text
                        GUSTAVO
                           │
                           ▼
                    AGÊNCIA MÃE
                     / AgencyOS
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
    Agência #001      Agência #002     Agência #003
      YouTube           Instagram         YouTube
          │                │                │
       Agentes           Agentes          Agentes
          │                │                │
          └────────────────┼────────────────┘
                           │
                    SERVIÇOS CENTRAIS
                           │
          IA / dados / mídia / APIs / memória
          analytics / financeiro / segurança
```

---

# 2. Missão

**Criar, operar, aprender, escalar e encerrar ativos digitais de forma autônoma, transformando atenção em lucro sustentável com o mínimo possível de intervenção humana.**

A palavra importante é **lucro**, não quantidade de conteúdo.

Uma agência que produz 500 vídeos e perde dinheiro é pior que uma agência que produz 20 e gera margem.

---

# 3. Visão

Construir uma empresa em que uma pequena estrutura humana consiga administrar **dezenas ou centenas de ativos digitais**, utilizando agentes de IA especializados e infraestrutura compartilhada.

O estado futuro é algo como:

> Gustavo acompanha o portfólio.  
> A Agência Mãe acompanha as agências.  
> As agências acompanham seus agentes.  
> Os agentes executam o trabalho.

Sua função deixa de ser operador.

Você passa a ser **proprietário do sistema e alocador de capital**.

---

# 4. Princípios arquiteturais

Estes princípios devem virar constituição da plataforma.

### 1. A Agência Mãe governa; as agências executam

Nenhuma agência decide sozinha questões que possam comprometer a empresa inteira.

### 2. Quem cria não aprova

O agente que escreveu um roteiro não é o responsável final por validar os fatos daquele roteiro.

### 3. IA não é fonte da verdade

Dados importantes devem vir de APIs, documentos, bancos, analytics ou fontes verificáveis.

### 4. Toda ação importante deixa registro

Precisamos conseguir descobrir:

> quem decidiu;  
> por quê;  
> com quais dados;  
> utilizando qual modelo;  
> qual versão da regra;  
> quanto custou;  
> qual foi o resultado.

### 5. Automação deve aumentar com confiança

Uma agência nova não recebe autonomia total no primeiro dia.

Ela conquista autonomia.

### 6. Erro deve ter raio de explosão pequeno

Uma agência com problema não pode destruir outras 19.

### 7. Tudo deve ser substituível

Claude, OpenAI, ferramenta de vídeo, voz, thumbnail ou editor nunca podem ser o próprio sistema.

São fornecedores do sistema.

Podemos trocar qualquer um.

### 8. Resultado econômico governa escala

Mais orçamento para o que funciona.

Menos orçamento para o que não funciona.

### 9. Memória precisa ser institucional

Aprendizado não pode ficar enterrado dentro de conversas com Claude.

### 10. Plataforma primeiro, quantidade depois

Não criaremos 20 canais para descobrir depois que o sistema está errado.

Primeiro construímos uma máquina que consegue operar **um** corretamente.

Depois replicamos.

---

# 5. Os grandes módulos da plataforma

## A. Control Plane — Agência Mãe

É o cérebro corporativo.

### Portfolio Manager

Conhece todas as agências:

- receita;
- custo;
- margem;
- estágio;
- saúde;
- crescimento;
- riscos;
- capital investido.

### Agency Factory

Responsável por **criar novas agências** a partir de modelos aprovados.

Por exemplo:

> Criar agência YouTube  
> Nicho: história econômica  
> Idioma: inglês  
> País principal: EUA  
> Objetivo: AdSense  
> Orçamento mensal: X  
> Template: YouTube Dark v4

E nasce uma agência.

### Capital Allocator

Decide onde colocar recursos.

Exemplo:

> Agência 3: ROAS excelente → aumentar produção.

> Agência 9: prejuízo persistente → reduzir orçamento.

### Governance Engine

Mantém:

- políticas;
- limites;
- permissões;
- aprovação;
- copyright;
- regras editoriais;
- padrões de qualidade;
- restrições de publicação.

### Opportunity Engine

Procura oportunidades de:

- novos nichos;
- idiomas;
- formatos;
- plataformas;
- temas;
- mercados.

### Incident Center

Recebe exceções.

Exemplos:

> strike;

> vídeo bloqueado;

> monetização suspensa;

> conta desconectada;

> custo anormal;

> queda drástica de alcance.

Só situações relevantes devem chegar até você.

---

# 6. Anatomy de uma Agência

Cada agência precisa possuir sua própria **Constituição**.

Eu chamaria isso de:

## Agency DNA

Contém tudo que define aquela operação.

Por exemplo:

**Identidade**

Nome, nicho, idioma, audiência, posicionamento.

**Objetivo**

AdSense, afiliado, lead, assinatura, produto etc.

**North Star Metric**

O principal resultado buscado.

**Economia**

Orçamento, custo máximo por conteúdo, margem desejada.

**Estratégia editorial**

Temas permitidos, temas proibidos, formatos, duração.

**Brand DNA**

Voz, avatar, estilo, identidade visual.

**Políticas**

Fontes permitidas, risco aceitável, requisitos de aprovação.

**Capabilities**

Quais ferramentas e agentes aquela agência pode utilizar.

**Autonomia**

O que pode executar sozinha.

**Kill Criteria**

Condições que justificam pausa ou encerramento.

---

# 7. Equipe interna de uma agência

Não quero uma IA tentando fazer tudo.

Quero especialização.

Uma agência poderá possuir papéis como:

```text
Agency Manager
       │
       ├── Market Intelligence
       ├── Research
       ├── Fact Checking
       ├── Content Strategist
       ├── Script Writer
       ├── Script QA
       ├── Creative Director
       ├── Voice / Avatar
       ├── Media Producer
       ├── Video Editor
       ├── Thumbnail
       ├── Publisher
       ├── Audience Manager
       ├── Analytics
       ├── Growth
       └── Finance
```

Importante:

Isso não significa obrigatoriamente **15 modelos diferentes rodando**.

São **15 responsabilidades**.

No início, um mesmo modelo pode executar várias funções separadas.

A arquitetura deve permitir que futuramente uma função seja substituída por outro modelo ou serviço sem reconstruirmos a empresa.

---

# 8. Serviços compartilhados

As agências não devem reinventar tudo.

Existirá uma camada central de serviços.

### Identity Service

Controla contas, canais, marcas, clones, vozes e personagens.

### Model Gateway

Escolhe qual IA executar determinada tarefa.

Claude pode ser melhor em uma coisa, outro modelo em outra.

### Tool & Connector Registry

Catálogo de:

- APIs;
- MCPs;
- serviços;
- plataformas;
- ferramentas internas.

### Content Factory

Infraestrutura de:

- roteiro;
- imagem;
- voz;
- avatar;
- vídeo;
- legendas;
- thumbnails.

### Publishing Gateway

Centraliza integração com:

- YouTube;
- Instagram;
- TikTok;
- outras plataformas.

### Analytics Engine

Centraliza métricas.

### Finance Engine

Centraliza:

- custos;
- receita;
- margem;
- ROI;
- orçamento.

### Knowledge & Memory Engine

Mantém o cérebro institucional da empresa.

### Experimentation Engine

Gerencia testes controlados.

### Policy & Safety Engine

Verifica regras antes da execução.

### Observability Engine

Mostra o que cada agente e agência está fazendo.

---

# 9. Como nasce uma agência

Uma agência nunca deve simplesmente ser criada porque uma IA achou o nicho interessante.

O nascimento terá um processo.

## Estado 1 — Candidate

Existe uma oportunidade.

Ainda não existe agência.

## Estado 2 — Investment Thesis

A Agência Mãe cria uma tese:

> oportunidade;  
> mercado;  
> concorrência;  
> monetização;  
> custo;  
> risco;  
> conteúdo disponível;  
> hipótese econômica.

## Estado 3 — Agency Specification

É criado o DNA.

## Estado 4 — Sandbox

A agência existe, mas não publica.

Ela pesquisa, cria roteiros, thumbnails e vídeos em ambiente de teste.

## Estado 5 — Pilot

Recebe recursos limitados e começa a operar.

## Estado 6 — Active

Comprovou capacidade operacional.

## Estado 7 — Scale

Comprovou economia.

Recebe mais capital.

## Estado 8 — Mature

Operação previsível.

Pouca intervenção.

## Estado 9 — Recovery

Algo deu errado.

A Agência Mãe tenta recuperar.

## Estado 10 — Paused

Sem produção, mantendo dados e aprendizado.

## Estado 11 — Retired

Encerrada definitivamente.

---

# 10. Como ela aprende

Essa é uma das partes mais importantes da arquitetura.

Não quero simplesmente:

> IA lê Analytics → muda prompt.

Isso pode virar caos.

O aprendizado precisa ser controlado.

Existirão três memórias.

### Memória episódica

O que aconteceu.

> Vídeo 193 teve CTR de 8,4%.

### Memória semântica

O que aprendemos.

> Thumbnails com rosto + número apresentam CTR superior nesse público.

### Memória procedural

Como devemos trabalhar.

> Para esse canal, gerar inicialmente três thumbnails nesse padrão.

Ou seja:

```text
Evento
   ↓
Dados
   ↓
Análise
   ↓
Hipótese
   ↓
Experimento
   ↓
Resultado
   ↓
Aprendizado
   ↓
Nova política
```

Nunca:

```text
Vídeo ruim
   ↓
IA entra em pânico
   ↓
muda tudo
```

---

# 11. Como a agência evolui

A agência precisa possuir versões.

Por exemplo:

> YouTube Agency v1.0

Depois:

> v1.1

Depois:

> v2.0

Uma alteração importante só entra em produção depois de demonstrar ganho.

Podemos ter:

**Production**

Modelo atual.

**Candidate**

Nova estratégia sendo testada.

**Champion**

Versão vencedora.

**Challenger**

Versão tentando superá-la.

Esse princípio é muito poderoso.

A própria empresa começa a fazer evolução seletiva.

---

# 12. Combate à alucinação

Alucinação não será tratada como um problema de prompt.

Será tratada como **problema arquitetural**.

Teremos várias barreiras.

### Proveniência

Todo fato relevante sabe de onde veio.

### Evidence Store

A pesquisa mantém fontes.

### Fact Checker independente

Outro estágio valida afirmações.

### Confidence Threshold

Afirmações abaixo de determinado grau de confiança são rejeitadas ou escaladas.

### Structured Outputs

Agentes conversam por estruturas definidas, e não apenas por textos soltos.

### Source of Truth

Dados financeiros vêm do financeiro.

Analytics vêm da plataforma.

Publicação vem da API.

Nunca da memória do modelo.

### Pre-publication QA

Antes de sair:

- factual;
- política;
- copyright;
- qualidade;
- marca;
- formato;
- segurança.

### Reconciliation

Depois da publicação, o sistema confirma:

> realmente foi publicado?

> horário correto?

> thumbnail correta?

> vídeo certo?

---

# 13. Níveis de autonomia

Uma agência ganha confiança progressivamente.

### L0 — Manual

Tudo precisa de aprovação.

### L1 — Assisted

IA prepara; humano executa.

### L2 — Supervised Automation

IA executa tarefas simples.

Tarefas importantes exigem aprovação.

### L3 — Autonomous Operations

Produção normal acontece sem humano.

Exceções são escaladas.

### L4 — Self-Optimizing

Além de operar, propõe e testa melhorias.

### L5 — Portfolio Autonomous

Agência Mãe consegue criar, capitalizar, escalar e encerrar operações dentro de limites previamente definidos.

Nosso objetivo de longo prazo é **L4/L5**.

Não começaremos nele.

---

# 14. Economia como parte do sistema operacional

Cada item produzido deve ter economia rastreável.

Por vídeo, por exemplo:

> Pesquisa: R$0,84  
> IA: R$1,70  
> Voz: R$2,20  
> Avatar: R$4,80  
> Imagens: R$1,30  
> Renderização: R$3,40  
> Total: R$14,24

Depois:

> Receita 7 dias: R$49  
> Receita 30 dias: R$187  
> Receita lifetime: R$421

Assim poderemos medir:

**Lucro por vídeo**

**Lucro por série**

**Lucro por tema**

**Lucro por canal**

**Lucro por agência**

**Retorno sobre capital**

E a Agência Mãe passa a decidir racionalmente onde investir.

---

# 15. O que acontece quando uma agência morre

Matar uma agência também será um processo.

Podem existir gatilhos:

- economia inviável;
- mercado desapareceu;
- risco excessivo;
- monetização perdida;
- conteúdo esgotado;
- outra agência tornou-se superior;
- estratégia não funcionou após determinada quantidade de testes.

O encerramento deve:

1. parar novos trabalhos;
2. deixar jobs existentes terminarem ou cancelá-los;
3. parar gastos;
4. revogar acessos desnecessários;
5. preservar analytics;
6. preservar aprendizados;
7. arquivar conteúdo;
8. transferir conhecimento útil para a Agência Mãe;
9. registrar a causa da morte.

A agência desaparece.

**O aprendizado permanece.**

Essa é uma diferença enorme.

---

# 16. Interface humana

Não quero que você tenha que abrir 30 sistemas.

A visão é um **Executive Cockpit**.

Você entra e encontra:

```text
PORTFÓLIO

Agências ativas            18
Receita 30d        R$ 184.300
Custo               R$ 31.700
Lucro               R$152.600

ESCALANDO
YouTube #04
YouTube #11
Instagram #02

ATENÇÃO
YouTube #08: monetização
Instagram #05: API desconectada

ENCERRAMENTO SUGERIDO
YouTube #14
Motivo: 90 dias abaixo do retorno mínimo
```

Você não administra vídeos.

Você administra **capital e exceções**.

---

# 17. Limites da Agência Mãe

Existe algo que eu quero deixar claro desde a arquitetura.

A Agência Mãe **não deve alterar todas as operações porque encontrou uma ideia nova**.

Ela administra:

**templates**, **políticas**, **capital**, **infraestrutura** e **aprendizado global**.

Uma descoberta feita no Canal A pode virar uma hipótese para o Canal B.

Não uma regra automática.

Isso evita contaminar 20 canais com uma conclusão errada.

---

# 18. Estrutura conceitual final

Eu enxergo cinco camadas:

```text
┌───────────────────────────────────────────┐
│               EXECUTIVE                   │
│                Gustavo                    │
├───────────────────────────────────────────┤
│              CONTROL PLANE                │
│             Agência Mãe                   │
├───────────────────────────────────────────┤
│             AGENCY RUNTIME                │
│ Agency 001 │ Agency 002 │ Agency 003 ... │
├───────────────────────────────────────────┤
│            SHARED SERVICES                │
│ AI │ Media │ APIs │ Data │ Finance │ QA  │
├───────────────────────────────────────────┤
│               DATA PLANE                  │
│ Memory │ Events │ Metrics │ Costs │ Audit│
└───────────────────────────────────────────┘
```

Essa é a espinha dorsal.

---

# 19. Roadmap

Agora vem uma regra que considero fundamental para nosso projeto:

**nenhuma implementação começa antes da arquitetura ser aprovada.**

## Fase 0 — Arquitetura

Estamos aqui.

Precisamos fechar:

- visão;
- domínio;
- módulos;
- limites;
- responsabilidades;
- ciclo de vida;
- níveis de autonomia;
- fluxo de informação;
- modelo de memória;
- modelo de permissões;
- modelo econômico;
- modelo de aprendizado;
- arquitetura de dados;
- arquitetura de agentes;
- arquitetura de integrações;
- políticas de segurança;
- observabilidade;
- critérios de escala e encerramento.

**Gate 0: Architecture Approved.**

Somente depois passamos para implementação.

---

## Fase 1 — Foundation

Construir o núcleo do AgencyOS:

- registro de agências;
- identidade;
- jobs;
- eventos;
- estados;
- permissões;
- configuração;
- logs;
- custo;
- modelos;
- conectores.

Ainda sem tentar criar uma fábrica gigantesca de vídeos.

---

## Fase 2 — Agency Factory

Construir a capacidade de:

> criar → configurar → iniciar → pausar → encerrar

uma agência.

Primeiro template:

**YouTube Agency.**

---

## Fase 3 — Canal Piloto

Somente uma agência real.

**Channel #001.**

Executamos o ciclo inteiro.

```text
Opportunity
→ Research
→ Script
→ QA
→ Production
→ Publish
→ Analytics
```

Objetivo aqui não é ganhar milhões.

É provar a plataforma.

---

## Fase 4 — Closed Loop

Adicionar:

```text
Analytics
→ Learning
→ Experiment
→ Improvement
→ New Content
```

Agora a agência começa a aprender.

---

## Fase 5 — Economics

Adicionar completamente:

- custos;
- receita;
- ROI;
- orçamento;
- capital allocation;
- unit economics.

Aqui deixa de ser fábrica de conteúdo.

Começa a virar **empresa**.

---

## Fase 6 — Segunda espécie de agência

Criamos, por exemplo:

**Instagram Agency.**

Ela utilizará a mesma infraestrutura.

Mas terá outro DNA e outro runtime específico.

---

## Fase 7 — Portfolio

3–5 agências simultaneamente.

Testamos:

- isolamento;
- concorrência por recursos;
- governança;
- capital allocation;
- incidentes;
- observabilidade.

---

## Fase 8 — Autonomous Portfolio

Agência Mãe começa a:

- propor novas agências;
- iniciar testes;
- aumentar investimentos;
- reduzir investimentos;
- colocar agências em recuperação.

Ainda obedecendo limites de autoridade.

---

## Fase 9 — Scale

Então:

**5 → 10 → 20 canais.**

Não antes.

---

# 20. O que não vamos fazer agora

Até esta arquitetura estar aprovada:

**Codex não constrói plataforma.**

**Não criamos banco.**

**Não escolhemos framework.**

**Não montamos n8n.**

**Não criamos 20 agentes.**

**Não conectamos YouTube.**

**Não conectamos Instagram.**

**Não automatizamos publicação.**

Primeiro definimos **o sistema**.

Depois escolhemos as tecnologias que implementarão o sistema.

Essa ordem provavelmente vai nos economizar semanas ou meses de retrabalho.

---

## Leitura arquitetural fundadora

O projeto que estamos desenhando não é mais:

**“automatizar um canal dark.”**

É:

> **Construir uma holding digital operada por agentes, capaz de criar, administrar, evoluir e liquidar negócios de mídia autônomos.**

E esta distinção é essencial porque muda completamente o tipo de arquitetura que devemos construir.

**Este documento fica congelado como Master Plan fundador v0.1.**
