# Discovery — Fase 3: Ponte KMM ↔ Scrum

> Status: **rascunho v0.1** · Escopo: modelo completo (ML0 a ML6)
> Base: *Kanban Maturity Model* (Anderson & Bozheva, Kanban University). Descrições **adaptadas e resumidas** para uso interno.
> Os nomes e códigos oficiais das práticas devem ser conferidos no livro antes da versão 1.0.

---

## 1. Princípio da adaptação

O modelo **não avalia se o time “faz Scrum direito”**. Ele avalia **a maturidade do sistema de entrega**, usando o Scrum como a estrutura que já existe.

- Os eventos do Scrum são tratados como **cadências** do Kanban (cada uma com um propósito de fluxo).
- Os papéis do Scrum são tratados como **responsabilidades** do Kanban (quem cuida da demanda, quem cuida da entrega).
- Os artefatos do Scrum são tratados como **visualizações e políticas** do Kanban.

Quando um elemento do Scrum não cobre uma prática do KMM, isso é registrado como **lacuna** (seção 4), e não como erro do time.

---

## 2. Tradução de vocabulário

### 2.1 Eventos → Cadências

| Scrum | Cadência Kanban / KMM | Propósito de fluxo | Cobertura |
|---|---|---|---|
| Sprint Planning | **Reposição** (*Replenishment*) | Escolher o que entra no sistema, respeitando a capacidade **demonstrada** | Parcial: decide em lote a cada 2 semanas e usa estimativa, não dado |
| Daily Scrum | **Reunião Kanban** (*Team Kanban Meeting*) | Olhar o quadro da direita para a esquerda: o que está parado, envelhecendo ou bloqueado | Parcial: costuma virar “status por pessoa” |
| Sprint Review | **Planejamento de entrega** + parte da **Revisão de entrega do serviço** | Validar valor entregue e calibrar expectativas com o cliente | Parcial: raramente discute lead time, SLE ou previsibilidade |
| Sprint Retrospective | **Retrospectiva** | Melhorar o processo do time | Coberta na teoria; na prática fica sem tempo |
| Refinamento do backlog | **Kanban upstream / Discovery** | Preparar opções, descartar o que não vale e definir o ponto de compromisso | Parcial: não há critério explícito de “pronto para comprometer” |
| — | **Revisão de entrega do serviço** (*Service Delivery Review*) | Comparar o desempenho real com a expectativa do cliente | **Ausente** |
| — | **Revisão de operações** (*Operations Review*) | Visão entre times: dependências, capacidade, gargalos | **Ausente** |
| — | **Revisão de riscos** (*Risk Review*) | Aprender com bloqueios e falhas recorrentes | **Ausente** |
| — | **Revisão de estratégia** (*Strategy Review*) | Ajustar o portfólio de serviços à estratégia | **Ausente** |

### 2.2 Papéis → Responsabilidades

| Scrum (situação atual) | Responsabilidade KMM | Observação |
|---|---|---|
| Product Owner (com PM) | **Service Request Manager**: dono da demanda, prioriza e decide o que entra | Existe, mas não controla os furas-fila (escalations, atravessadores) |
| Scrum Master (inexistente, papel acumulado) | **Service Delivery Manager**: dono do fluxo, cuida de WIP, bloqueios e prazos | **Lacuna crítica**: ninguém é dono do sistema de entrega |
| Developers | Time de entrega | Hoje opera a ~100% de utilização |
| Gerentes (técnico e de produto) | Patrocínio, revisão de operações, políticas entre times | Sem cadência própria para olhar o fluxo |

### 2.3 Artefatos e métricas

| Scrum | Equivalente Kanban / KMM | Diferença-chave |
|---|---|---|
| Product Backlog | Backlog / opções upstream | O Kanban separa **opções** (descartáveis) de **compromissos** |
| Sprint Backlog | Trabalho comprometido (WIP) | O Scrum limita o WIP pelo **tempo** (sprint); o Kanban, por **quantidade** em cada etapa |
| Definition of Done | Políticas de saída por etapa | O Kanban explicita critérios em **cada** coluna, e não só no fim |
| Sprint Goal | Objetivo de entrega | Sem equivalente direto; continua útil |
| Velocity (pontos) | **Vazão** (*throughput*, itens por período) | Vazão conta itens reais e não depende de estimativa |
| Estimativa em pontos / horas | **Lead time** e sua distribuição | O Kanban prevê com histórico, não com estimativa |
| Burndown | **CFD** (diagrama de fluxo cumulativo) e **idade do WIP** | O CFD mostra filas e gargalos; a idade do item mostra risco em tempo real |
| Compromisso da sprint | **SLE** (“85% em até X dias”) e previsão probabilística | Compromisso **por item / tipo de demanda**, e não por lote |

---

## 3. Os níveis, lidos pela lente de um time Scrum

### Resumo

| Nível | Nome (KMM) | Pergunta central | Previsibilidade | Escopo |
|---|---|---|---|---|
| **ML0** | Inconsciente (*Oblivious*) | “Existe um processo?” | Nenhuma | Indivíduo |
| **ML1** | Focado no time (*Team-Focused*) | “Como o time se organiza?” | Baixa e dependente de pessoas | Time |
| **ML2** | Orientado ao cliente (*Customer-Driven*) | “O que o cliente recebe, de ponta a ponta?” | Começa a ser medida | Serviço / produto |
| **ML3** | Adequado ao propósito (*Fit-for-Purpose*) | “Atendemos a expectativa do cliente de forma consistente?” | **Gerida com dados (SLE, previsões)** | Serviços interligados |
| **ML4** | Protegido contra riscos (*Risk-Hedged*) | “Como equilibramos risco, custo e valor no portfólio?” | Quantitativa, por classe de risco | Portfólio |
| **ML5** | Líder de mercado (*Market Leader*) | “Como melhoramos de forma contínua e superior?” | Otimizada | Organização |
| **ML6** | Construído para sobreviver (*Built for Survival*) | “Quem precisamos ser no futuro?” | Estratégica | Organização / negócio |

> No KMM, cada nível a partir do ML1 tem práticas **de transição** (que preparam o nível) e práticas **centrais** (que o consolidam). A régua de avaliação (Fase 4) usará essa distinção para mostrar o progresso **dentro** de um nível, e não só entre níveis.

**Faixa provável dos times:** ML0 a ML1 (a maioria) e ML1 a ML2 (time de referência).
**Alvo da previsibilidade pedida pelos gerentes:** ML3.

---

### ML0 — Inconsciente

**Foco:** trabalho individual; o processo não é percebido como algo a gerir.

| Dimensão | Como aparece num time Scrum |
|---|---|
| Visualizar | Quadro no Jira existe, mas não reflete a realidade, ou cada pessoa tem a sua lista |
| Limitar WIP | Inexistente; cada um puxa o que quiser ou recebe por fora |
| Gerir fluxo | Ninguém olha o fluxo; “cada um cuida do seu” |
| Políticas | Implícitas; dependem de quem pede |
| Cadências | Eventos do Scrum ausentes ou cerimoniais |
| Melhoria | Não acontece |

**Sinais:** demandas chegam direto nas pessoas; o PO não sabe o que o time está fazendo; a sprint é só um intervalo de datas.

---

### ML1 — Focado no time

**Foco:** o time se organiza para coordenar o próprio trabalho. A previsibilidade ainda é baixa e o time tende à sobrecarga.

| Dimensão | Transição → Central |
|---|---|
| Visualizar | Quadro do time com etapas básicas (A fazer / Fazendo / Feito) → tipos de trabalho e bloqueios visíveis |
| Limitar WIP | Consciência de que há trabalho demais → limites por pessoa ou acordos informais |
| Gerir fluxo | Daily olha o quadro → Daily foca nos itens parados e bloqueados, não em status por pessoa |
| Políticas | Definition of Done existe → critérios básicos de “pronto para começar” |
| Cadências | Daily, Planning e Retro acontecem de forma regular |
| Melhoria | Retro identifica problemas → ações de melhoria acompanhadas |

**Sinais no Scrum:** os eventos acontecem, mas a sprint quebra com frequência; furas-fila são absorvidos “com jeitinho”; o time sabe o que faz, mas não quanto tempo leva.

**Resultado observável ao consolidar:** transparência interna, coesão, menos trabalho escondido.

---

### ML2 — Orientado ao cliente

**Foco:** sair da visão do time e enxergar o **serviço ao cliente de ponta a ponta**. A previsibilidade começa a ser medida.

| Dimensão | Transição → Central |
|---|---|
| Visualizar | Fluxo completo mapeado (da ideia à produção, incluindo homologação e deploy) → filas e esperas visíveis como etapas |
| Limitar WIP | Limite de WIP por etapa do fluxo, e não só pela sprint → **ponto de compromisso** explícito |
| Gerir fluxo | Medir **lead time** e **vazão** → acompanhar a **idade dos itens** em andamento |
| Políticas | Critérios de entrada e saída por etapa → **classes de serviço** iniciais (ex.: urgente / data fixa / padrão) com regras de quem pode furar a fila |
| Cadências | Planning funcionando como **reposição** baseada em capacidade demonstrada → Review com o cliente discutindo também o **prazo**, e não só o produto |
| Melhoria | Melhorias guiadas por dados de fluxo |

**Sinais no Scrum:** o PO consegue dizer “esse tipo de item costuma levar entre X e Y dias”; urgências seguem uma regra combinada; a Planning considera a vazão histórica.

**Resultado observável ao consolidar:** entregas mais consistentes, menos surpresa para o cliente, conversa sobre prazo baseada em dado.

---

### ML3 — Adequado ao propósito ⭐ *alvo de previsibilidade*

**Foco:** atender **de forma consistente** às expectativas do cliente, com compromissos baseados em dados e coordenação entre serviços.

| Dimensão | Transição → Central |
|---|---|
| Visualizar | Dependências entre times visíveis → quadro de serviços interligados |
| Limitar WIP | WIP gerido no nível do sistema (vários times) → capacidade alocada por classe de serviço |
| Gerir fluxo | **SLE** por tipo de demanda (“85% em até X dias”) → **previsão probabilística** (Monte Carlo) para entregas maiores |
| Políticas | Critérios explícitos de aceite de demanda (o que entra, o que sai, quem decide) → **SLA / acordos** com clientes internos |
| Cadências | **Revisão de entrega do serviço** e **revisão de riscos** → **revisão de operações** entre times |
| Papéis | Alguém responde pelo fluxo de cada serviço (**Service Delivery Manager**) |
| Melhoria | Critérios de adequação (*fitness criteria*) definidos com o cliente e usados para priorizar melhorias |

**Sinais no Scrum:** ao receber uma demanda, o time responde em minutos com uma data e uma probabilidade; o plano de 4 sprints vira uma **previsão atualizada continuamente**; os gerentes acompanham o fluxo numa cadência própria.

**Resultado observável:** **é exatamente a previsibilidade descrita pelos gerentes.**

---

### ML4 — Protegido contra riscos

**Foco:** gestão quantitativa de risco no **portfólio**. Decisões de o que fazer (e o que **não** fazer) consideram custo de atraso, incerteza e capacidade.

| Dimensão | Como se manifesta |
|---|---|
| Visualizar | Portfólio de iniciativas com risco e custo de atraso visíveis |
| Limitar WIP | WIP limitado no **portfólio** (quantas iniciativas em paralelo) |
| Gerir fluxo | Alocação de capacidade por tipo de risco (ex.: % regulatório, % evolução, % dívida técnica) |
| Políticas | Critérios de seleção baseados em custo de atraso e perfil de risco |
| Cadências | Revisão de portfólio e de riscos consolidada |
| Melhoria | Uso estatístico do histórico para reduzir variabilidade |

**Relevância local:** o impacto regulatório no time de referência é um caso típico de ML4 (risco com data fixa, que deveria ter capacidade reservada).

---

### ML5 — Líder de mercado

**Foco:** melhoria contínua como cultura; o sistema de entrega é uma vantagem competitiva.

- Experimentação sistemática (hipótese → experimento → aprendizado);
- Otimização do fluxo ponta a ponta, incluindo áreas de negócio;
- Liderança em todos os níveis (*acts of leadership*);
- Métricas de resultado (impacto no negócio) além de métricas de fluxo.

**Relevância local:** horizonte de longo prazo; serve para mostrar aos gerentes que previsibilidade (ML3) é um meio, e não um fim.

---

### ML6 — Construído para sobreviver

**Foco:** a organização se reinventa: revisa a própria identidade, os serviços que oferece e o modelo de negócio.

- Revisão de estratégia contínua, alimentada por dados dos serviços;
- Capacidade de abandonar produtos e serviços que não fazem mais sentido;
- Cultura e propósito explícitos e compartilhados.

**Relevância local:** fora do alcance dos POs; incluído para completar a régua.

---

## 4. Lacunas estruturais do Scrum atual em relação ao KMM

| # | Lacuna | Nível em que vira bloqueio | Impacto na previsibilidade |
|---|---|---|---|
| L1 | **Ninguém é dono do fluxo** (sem SM, sem gestor de entrega) | ML1 → ML2 | Alto: sem dono, nenhuma das práticas abaixo se sustenta |
| L2 | **Sem limite de WIP por etapa**; o único limite é a sprint, e ela é furada | ML1 → ML2 | Alto: WIP alto aumenta o lead time e a variabilidade |
| L3 | **Sem ponto de compromisso nem classes de serviço**; furas-fila sem regra | ML2 | Alto: qualquer urgência desmonta o plano |
| L4 | **Planejamento determinístico** (4 sprints, 10% de folga) | ML2 → ML3 | Alto: produz um plano que não se cumpre e gera desconfiança |
| L5 | **Métricas baseadas em estimativa** (pontos), sem lead time e vazão | ML2 | Médio: impede responder “quando fica pronto?” |
| L6 | **Sem cadência entre times** (revisão de operações) | ML3 | Médio: dependências e gargalos ficam invisíveis para a gerência |
| L7 | **Sem tempo para melhoria** (0% da capacidade) | ML1 | Médio: o sistema não evolui; problemas se repetem |
| L8 | **Scrum Team matricial** (PO e time em gerências diferentes) | ML2 → ML3 | Médio: decisões de prioridade e capacidade ficam divididas |

---

## 5. Implicações para a Fase 4 (desenho)

1. **Régua com duas camadas:** práticas observáveis (questionário / checklist) + resultados medidos (Nave / Jira).
2. **Foco operacional em ML0 a ML3**, com ML4 a ML6 descritos como horizonte.
3. **Transição e central** em cada nível, para mostrar progresso real mesmo sem mudar de nível.
4. **Lacunas L1 a L4 como “bloqueadores”:** sem resolvê-las, nenhum time chega ao ML3, qualquer que seja o esforço do time. É a mensagem principal para os gerentes.
5. **Referências complementares** a considerar: *Kanban Guide for Scrum Teams* (Scrum.org) e o *Kanban Guide* (Kanban University), úteis para mostrar que Kanban e Scrum são compatíveis.
