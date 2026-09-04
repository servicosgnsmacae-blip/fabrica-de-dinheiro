# Constituição do AgencyOS v0.1

## Preâmbulo

O AgencyOS é o sistema operacional de uma empresa autônoma de ativos digitais. Esta Constituição estabelece princípios não negociáveis para toda a plataforma, para a Agência-Mãe, para as Agências de Ativo, para agentes, modelos, ferramentas e processos.

Nenhum módulo, agente, automação, integração ou decisão operacional pode contrariar estes princípios sem decisão arquitetural explícita registrada em `DECISIONS.md` e aprovação do proprietário do sistema.

## Artigo 1 — Autoridade

**A Agência-Mãe governa; as Agências de Ativo executam.**

A Agência-Mãe define políticas, limites, templates, orçamento, regras de autonomia, critérios de escala e critérios de encerramento. Agências de Ativo operam dentro desses limites e não podem unilateralmente alterar regras que afetem o portfólio inteiro.

**Gustavo é o proprietário do sistema e o alocador final de capital.** Nenhum agente ou componente pode remover essa autoridade.

## Artigo 2 — Separação entre criação e aprovação

**Quem cria não aprova o próprio trabalho.**

Toda entrega materialmente relevante deve possuir validação independente compatível com o risco. O agente que cria pode fornecer justificativas e evidências, mas não pode ser a única autoridade de aprovação da própria saída.

## Artigo 3 — Verdade e proveniência

**IA não é fonte da verdade.**

Memória de modelo, inferência ou texto gerado não substituem fonte verificável.

**Fatos importantes precisam de proveniência.** Sempre que uma afirmação puder afetar reputação, publicação, decisão financeira, política, conformidade ou aprendizado, sua origem deve ser registrável.

## Artigo 4 — Auditabilidade

**Toda decisão relevante precisa ser auditável.**

O sistema deve permitir reconstruir por que uma decisão foi tomada e com quais dados.

**Toda ação relevante deve registrar, no mínimo:**

- agente ou papel executor;
- modelo e fornecedor utilizados;
- versão do agente, prompt, política ou processo aplicável;
- custo atribuível;
- dados e evidências utilizados;
- decisão tomada;
- resultado observado;
- data/hora e identificadores necessários à reconstrução do evento.

## Artigo 5 — Limitação do raio de explosão

**O raio de explosão de erros deve ser limitado.**

Falhas em uma agência, credencial, experimento, modelo ou integração não devem comprometer outras agências ou o portfólio inteiro. Isolamento, limites de gasto, escopo de permissões, rollback e circuit breakers são requisitos arquiteturais, não melhorias opcionais.

## Artigo 6 — Substituibilidade

**Ferramentas e fornecedores precisam ser substituíveis.**

Claude, OpenAI, ferramentas de voz, vídeo, imagem, publicação, analytics ou qualquer outro fornecedor são componentes da plataforma. Nenhum fornecedor pode ser tratado como a própria arquitetura.

## Artigo 7 — Memória institucional

**Memória pertence à plataforma, não às conversas dos modelos.**

Conhecimento durável deve ser persistido em estruturas controladas pela plataforma. Conversas, sessões e contexto temporário podem auxiliar a execução, mas não são fonte canônica de memória institucional.

## Artigo 8 — Autonomia progressiva

**Autonomia é conquistada progressivamente.**

Nenhuma agência ou agente nasce com autoridade máxima. A autonomia aumenta conforme evidências de confiabilidade, qualidade, segurança e desempenho econômico.

Níveis de autonomia devem permanecer explícitos e reversíveis.

## Artigo 9 — Economia governa escala

**Resultado econômico governa escala.**

Volume de conteúdo, seguidores, visualizações ou quantidade de agentes não são objetivos finais. Orçamento e expansão dependem de evidência econômica e risco aceitável.

## Artigo 10 — Aprendizado controlado

**Aprendizado acontece por experimentação controlada.**

Observação não vira política automaticamente. O fluxo esperado é:

`evento → dados → análise → hipótese → experimento → evidência → aprendizado → política candidata → aprovação → produção`

## Artigo 11 — Mudança segura

**Nenhuma mudança importante entra diretamente em produção.**

Mudanças relevantes devem passar por ambiente de teste, validação, rollout controlado ou mecanismo equivalente proporcional ao risco.

## Artigo 12 — Champion / Challenger

**Champion/Challenger deve ser utilizado para evolução.**

A versão comprovada permanece como Champion. Novas versões entram como Challengers e só assumem produção após demonstrarem ganho suficiente em critérios definidos. Rollback deve permanecer possível.

## Artigo 13 — Plataforma antes da escala

**A plataforma deve conseguir operar um ativo corretamente antes de escalar para dezenas.**

O AgencyOS não multiplicará uma operação ainda não comprovada. O primeiro objetivo é operar uma Agência de Ativo ponta a ponta com rastreabilidade, qualidade, economia e capacidade de aprendizado.

## Artigo 14 — Fonte de verdade por domínio

Cada domínio deve possuir uma fonte canônica. Exemplos: métricas vêm das plataformas de analytics, custos do mecanismo financeiro, estados do registro de agências, políticas do mecanismo de governança. Modelos de IA podem interpretar dados, mas não substituem a fonte canônica.

## Artigo 15 — Princípio do menor privilégio

Agentes, ferramentas e integrações recebem apenas as permissões necessárias para sua função. Permissões de leitura, escrita, publicação, gasto e alteração de política devem ser separáveis.

## Artigo 16 — Encerramento com preservação de conhecimento

Uma Agência de Ativo pode ser pausada, recuperada ou encerrada. O ativo pode morrer; o aprendizado útil não. O encerramento deve interromper gastos, revogar acessos desnecessários, preservar analytics, extrair aprendizados e registrar post-mortem.

## Cláusula de supremacia

Em caso de conflito entre esta Constituição e documentação operacional, prevalece esta Constituição até que uma decisão arquitetural explícita seja registrada e aprovada por Gustavo.
