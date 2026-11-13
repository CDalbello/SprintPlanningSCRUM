# Discovery — Fase 2: Diagnóstico do Ponto de Partida

> Status: **rascunho v0.1** · Fonte: relato da coordenação dos POs (ainda não validado com dados)

## 1. Panorama

| Dimensão | Situação atual |
|---|---|
| Escala | 9 times · 14 POs |
| Tamanho dos times técnicos | de 2 a 12–15 pessoas |
| Framework | Scrum imposto, com sprints fixas de 2 semanas |
| Horizonte de planejamento | POs planejam **4 sprints à frente** (~8 semanas) |
| Folga | **10%** da capacidade para imprevistos; **0%** para melhoria contínua |
| Eventos Scrum | Sem garantia de que acontecem; sem padrão entre os times |
| Scrum Master | Não existe papel fixo; o papel é acumulado sem padrão (tendência histórica, sem perspectiva de mudança) |
| Estrutura | PO e PM na mesma gerência; o time técnico está em outra gerência, ou seja, o Scrum Team é **matricial** |
| Ferramentas | Jira, em migração de Server para Cloud · itens rastreáveis · **Nave** disponível para métricas de fluxo |

## 2. Como as demandas e os prazos entram

Fontes de demanda observadas:

1. **Priorização estratégica de valor do PM** (o caminho ideal);
2. **Falhas e incidentes**;
3. **Escalations**;
4. **Atravessadores**, que acionam o time por fora do fluxo.

Não há política definida para:
- aceitar uma demanda nova (**ponto de compromisso**);
- decidir **o que sai** quando algo entra (*trade-off* de capacidade);
- **dar um prazo** (não há processo, dado de referência nem responsável claro).

## 3. O que "previsibilidade" significa para os gerentes

> "Receber uma demanda e conseguir **se comprometer rapidamente com uma data** para entregá-la."

Por trás disso há uma dor maior: **falta visibilidade das entregas de valor**. Entregar muito não basta se não for a coisa certa, e os times **não conhecem os próprios números** (tempos, vazão, desempenho).

**Leitura KMM:** essa definição corresponde a práticas que começam no **ML2** e se consolidam no **ML3**:
- *Service Level Expectation* (SLE): “85% dos itens deste tipo saem em até X dias”;
- distribuição de lead time por tipo de trabalho;
- previsão probabilística (Monte Carlo) para entregas maiores.

Ou seja, o pedido dos gerentes é atendível e mensurável, mas **não com o sistema de planejamento atual**.

## 4. Sintomas observados

| Sintoma | Mecanismo provável (lente de fluxo) | Prática KMM relacionada |
|---|---|---|
| Sprints quebram e não fecham | Compromisso feito por capacidade estimada, e não por capacidade demonstrada | Gestão do fluxo, uso de dados históricos |
| WIP alto | Sem limite de WIP; tudo começa, pouco termina | Limitar o WIP |
| Nada é despriorizado; “tudo se dá um jeito” | Sem política de reposição nem de *trade-off* | Políticas explícitas, reunião de reposição |
| Times “no talo” o tempo todo | Utilização perto de 100%, o que faz o lead time explodir e torna as datas imprevisíveis | Folga, limite de WIP |
| Furas-fila constantes | Urgências sem classe de serviço definida | Classes de serviço (expedite, data fixa etc.) |
| Planejamento “para inglês ver” | Plano determinístico de 8 semanas com 10% de folga num ambiente de alta variabilidade | Previsão probabilística |
| Sem conversa sobre melhoria | Sem tempo, sem papel e sem cadência para melhoria | Retrospectiva, revisão de operações, feedback loops |
| Fila de dependências e retrabalho | Bloqueios não visíveis; qualidade entra no fluxo tarde | Visualizar bloqueios, definição de pronto por etapa |

> **Argumento central para os gerentes:** com o sistema operando a ~100% de utilização e sem limite de WIP, a imprevisibilidade **é o comportamento esperado do sistema**, e não falha das pessoas. Isso tira a conversa do “apontar o dedo” e a leva para “mudar o sistema”.

## 5. O time de referência

Características:
- planeja e se organiza melhor;
- PM presente e assertivo;
- coordenação forte, mesmo sob impacto regulatório;
- equipe estável, que trabalha junta há anos;
- papéis e responsabilidades mais claros que nos demais.

**Ponto de atenção:** boa parte da maturidade desse time parece vir **das pessoas e da estabilidade** (conhecimento tácito), e não de **políticas explícitas do sistema**. No KMM essa distinção pesa: o desempenho que depende de pessoas específicas é frágil e não escala para os outros times. O diagnóstico deve mostrar **o que nesse time já é prática replicável** e o que é mérito individual.

## 6. Perfis típicos (hipótese)

| Perfil | Descrição | Faixa KMM provável |
|---|---|---|
| **A. Reativo sobrecarregado** | Maioria dos times: fura-fila, WIP alto, sprints que quebram, sem melhoria | ML0 → ML1 |
| **B. Organizado por pessoas** | Time de referência: boa coordenação, mas apoiado em pessoas e não em políticas | ML1 → ML2 |
| **C. Micro time** (2–3 pessoas) | Os eventos do Scrum pesam proporcionalmente mais; o trabalho tende a ser individual | ML0 → ML1 (a validar) |

### Revisão das hipóteses da Fase 1
- **H1 (revista):** a maioria dos times está entre **ML0 e ML1**, e não entre ML1 e ML2. O time de referência deve ficar perto de ML2.
- **H2 (reforçada):** a definição de previsibilidade dos gerentes corresponde ao alvo **ML2 → ML3**.
- **H3 (viável):** Jira + Nave permitem medir lead time, vazão, WIP e idade dos itens. **Risco:** a migração Server → Cloud pode quebrar a continuidade do histórico.
- **H4 (reforçada):** sem Scrum Master e sem gestor de fluxo, ninguém é dono do sistema de entrega.

## 7. Implicações para o desenho do modelo

1. **Não culpar o Scrum.** Muitos sintomas também violariam um Scrum bem praticado. O modelo deve ler a maturidade de fluxo *por meio* dos eventos atuais (Planning ≈ reposição, Daily ≈ Kanban meeting, Review ≈ entrega, Retro ≈ melhoria).
2. **Combinar evidência quantitativa e qualitativa:** métricas do Nave/Jira mais um questionário de práticas, para ter dado onde há dado e percepção onde não há.
3. **Escala de nível de time, normalizada:** comparar lead time e previsibilidade, e não vazão absoluta, já que os times vão de 2 a 15 pessoas.
4. **Tornar visível o papel que falta:** incluir no diagnóstico “quem faz a gestão do fluxo”, ponte para a recomendação de um papel equivalente ao Service Delivery Manager.
5. **Linguagem para gerentes:** o resultado precisa caber em uma página: nível atual, nível-alvo, três lacunas principais e o custo de não agir.
