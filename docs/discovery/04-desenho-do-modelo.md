# Discovery — Fase 4: Desenho do Modelo

> Status: **rascunho v0.1** · Nome de trabalho: **KMM-S** (KMM adaptado para times Scrum, uso interno)
> Os códigos dos itens (ex.: `2.WIP.1`) são **deste modelo** e não correspondem aos códigos oficiais do KMM.

---

## 1. Estrutura geral

O modelo tem **duas camadas**, que se confirmam uma à outra:

| Camada | O que mede | Fonte | Papel no resultado |
|---|---|---|---|
| **1. Checklist de práticas** | O que o time **faz** | Avaliação com evidência | **Define o nível** |
| **2. Indicadores de fluxo** | O que o sistema **entrega** | Nave / Jira | **Confirma ou questiona o nível** e dá os números para os gerentes |

**Dimensões** (base nas práticas gerais do Kanban, mais papéis):

| Código | Dimensão |
|---|---|
| VIS | Visualizar |
| WIP | Limitar o trabalho em andamento |
| FLX | Gerir o fluxo |
| POL | Políticas explícitas |
| CAD | Cadências (ciclos de feedback) |
| MEL | Melhoria contínua |
| PAP | Papéis e responsabilidades |

---

## 2. Regras de aplicação

### Quem preenche
**Recomendação:** o **PO preenche** e a **coordenação calibra** em uma conversa de cerca de 30 minutos por time.

- Os 14 POs têm visões diferentes de “sim”; uma pessoa calibrando os 9 times garante que o painel compare coisas comparáveis.
- Quando um time tem mais de um PO, eles respondem **juntos**: é uma resposta por time.
- **Opcional:** validar o resultado com o time numa retrospectiva, o que aumenta a adesão e corrige pontos cegos.

### Como responder
- Cada item é **Sim** ou **Não**. Não há “parcial”.
- **Sim** somente se a prática acontece **de forma consistente nas últimas 4 sprints** e há **evidência** (coluna “Como verificar”).
- Na dúvida, marque **Não**. O objetivo é diagnosticar, não pontuar bem.

### Cadência
- **Trimestral** (a cada ~6 sprints). O primeiro ciclo é a linha de base.

---

## 3. Regras de cálculo do nível

1. **Nível consolidado = N** quando **todos** os itens (transição e centrais) do ML1 até o ML_N estão marcados como Sim.
2. **Em transição para N+1** quando há pelo menos um item do nível N+1 marcado como Sim.
3. **Progresso no nível** = itens Sim do nível N+1 ÷ total de itens do nível N+1.
4. **Pendências de base:** itens Não em níveis **abaixo** de algum Sim aparecem destacados no painel. Ex.: o time mede o lead time (ML2), mas a Daily não acontece (ML1).
5. **Bloqueadores** (lacunas L1 a L4 da Fase 3) são sinalizados à parte, porque **não dependem do esforço do time**.

> A regra é propositalmente rígida: um nível só vale se a base estiver de pé, como no KMM. O progresso percentual e as pendências evitam que essa rigidez esconda o avanço.

---

## 4. Checklist

Legenda: **T** = prática de transição · **C** = prática central · 🔒 = item ligado a um bloqueador (L1 a L4)

### ML1 — Focado no time

| Código | T/C | Prática | Como verificar |
|---|---|---|---|
| 1.VIS.1 | T | Existe um quadro no Jira usado pelo time que reflete o trabalho real | Os itens “em andamento” no quadro batem com o que as pessoas dizem fazer na Daily |
| 1.VIS.2 | T | Os tipos de trabalho são distinguíveis no quadro (história, bug, incidente, tarefa técnica) | Inspeção do quadro |
| 1.CAD.1 | T | A Daily acontece em pelo menos 80% dos dias da sprint | Agenda / relato do time |
| 1.CAD.2 | T | A Planning acontece em todas as sprints, com PO e time | Agenda / ata |
| 1.MEL.1 | T | A retrospectiva acontece pelo menos uma vez por mês | Agenda / registro |
| 1.POL.1 | T | Existe uma Definition of Done escrita e conhecida pelo time | Documento; o time sabe dizer onde está |
| 1.VIS.3 | C | Bloqueios são sinalizados no quadro (flag ou coluna) | Inspeção do quadro |
| 1.WIP.1 | C | Há acordo explícito sobre quantos itens cada pessoa toca em paralelo | Acordo escrito ou repetido igual por mais de uma pessoa |
| 1.FLX.1 | C | A Daily é conduzida pelo quadro, com foco em itens parados e bloqueados, e não como ronda de status por pessoa | Observar uma Daily |
| 1.POL.2 | C | Demandas que chegam por fora (direto na pessoa) são registradas no Jira antes de serem trabalhadas | Comparar relatos com o Jira |
| 1.MEL.2 | C | As ações da retro são registradas e revisitadas na retro seguinte | Registro das retros |
| 1.PAP.1 | C | Há uma pessoa nomeada que facilita os eventos, mesmo acumulando papel | O time sabe dizer quem é |

### ML2 — Orientado ao cliente

| Código | T/C | Prática | Como verificar |
|---|---|---|---|
| 2.VIS.1 | T | O quadro mapeia o fluxo de ponta a ponta (do refinamento até a produção), incluindo etapas de espera (ex.: “aguardando homologação”) | Inspeção do quadro |
| 2.FLX.1 | T | O time conhece o próprio lead time típico | PO ou time responde sem consultar, e o valor bate com o Nave (±20%) |
| 2.FLX.2 | T | A vazão é medida em itens por semana ou por sprint | Relatório ou painel existente |
| 2.POL.1 | T | 🔒 Existe critério explícito de “pronto para começar” (ponto de compromisso) | Documento; os itens na sprint atendem ao critério |
| 2.POL.2 | T | Demandas não planejadas que entram na sprint são marcadas (label) para medição | Label no Jira em uso |
| 2.CAD.1 | T | A Review acontece com stakeholders ou clientes em pelo menos 3 de cada 4 sprints | Agenda / participantes |
| 2.WIP.1 | C | 🔒 Há limite de WIP em ao menos uma etapa do fluxo, e ele é respeitado | Limite configurado no quadro; violações raras e discutidas |
| 2.POL.3 | C | 🔒 Há classes de serviço definidas (ex.: urgente, data fixa, padrão), com regra de quem pode acionar urgência e **o que sai** quando algo entra | Política escrita; casos recentes seguiram a regra |
| 2.FLX.3 | C | A idade dos itens em andamento é monitorada, e itens envelhecidos são discutidos na Daily | Painel de aging; observar uma Daily |
| 2.CAD.2 | C | A Planning usa a vazão histórica para definir quanto cabe, e não só pontos estimados | Observar uma Planning |
| 2.CAD.3 | C | A Review discute prazos e entregas, além do produto | Observar uma Review / pauta |
| 2.MEL.1 | C | Ao menos uma melhoria por mês é baseada em dado de fluxo | Registro das retros |
| 2.PAP.1 | C | 🔒 Há uma pessoa nomeada responsável por acompanhar o fluxo do time (WIP, bloqueios, idade dos itens) | O time e o PO sabem dizer quem é |

### ML3 — Adequado ao propósito ⭐ alvo de previsibilidade

| Código | T/C | Prática | Como verificar |
|---|---|---|---|
| 3.FLX.1 | T | Há SLE publicado por tipo de demanda (“85% em até X dias”) | Documento ou painel visível aos stakeholders |
| 3.FLX.2 | T | Ao receber uma demanda, o PO responde com data baseada no SLE ou no histórico em até 1 dia útil | Casos recentes |
| 3.VIS.1 | T | Dependências com outros times são visíveis no quadro | Inspeção do quadro |
| 3.POL.1 | T | 🔒 Há política de aceite de demanda acordada com a gerência e os stakeholders (canal único, quem prioriza, o que sai) | Documento aprovado; furas-fila recentes seguiram o canal |
| 3.CAD.1 | T | Há revisão de entrega do serviço periódica (ex.: mensal) com cliente ou gerência: SLE previsto × realizado | Agenda / ata |
| 3.MEL.1 | T | Há capacidade reservada para melhoria (ex.: ≥10% da sprint) e ela é usada | Itens de melhoria concluídos no trimestre |
| 3.FLX.3 | C | 🔒 Entregas maiores são previstas de forma probabilística (ex.: Monte Carlo) e a previsão é atualizada a cada sprint, substituindo o plano fixo de 4 sprints | Previsão publicada e histórico de atualizações |
| 3.FLX.4 | C | O SLE foi cumprido em pelo menos 85% dos itens nos últimos 3 meses | Nave |
| 3.WIP.1 | C | A capacidade é alocada por classe de serviço (ex.: % para urgências e para regulatório) | Política escrita; distribuição real próxima da combinada |
| 3.CAD.2 | C | Há revisão de operações entre times (ex.: mensal) com os gerentes: dependências, gargalos, capacidade | Agenda / ata |
| 3.CAD.3 | C | Bloqueios recorrentes são analisados e tratados (revisão de riscos) | Registro de causas e ações |
| 3.PAP.1 | C | 🔒 O papel de gestão de fluxo é formalizado e reconhecido pela gerência | Comunicado, descrição de papel ou alocação formal |
| 3.POL.2 | C | Há critérios de adequação (*fitness criteria*) definidos com o cliente (prazo, qualidade, previsibilidade) | Documento acordado |

### ML4 a ML6 — Horizonte (avaliação da área, não por time)

Estes itens são avaliados **uma vez para a área como um todo** e aparecem no painel como contexto.

| Código | Nível | Prática |
|---|---|---|
| 4.WIP.1 | ML4 | O número de iniciativas em paralelo no portfólio é limitado |
| 4.FLX.1 | ML4 | A capacidade é alocada por tipo de risco (regulatório, evolução, dívida técnica) |
| 4.POL.1 | ML4 | A priorização do portfólio usa custo de atraso e perfil de risco |
| 4.CAD.1 | ML4 | Há revisão de portfólio e de riscos consolidada |
| 5.MEL.1 | ML5 | Há experimentação sistemática (hipótese → experimento → aprendizado) |
| 5.FLX.1 | ML5 | Métricas de resultado de negócio são acompanhadas junto com métricas de fluxo |
| 5.PAP.1 | ML5 | Iniciativas de melhoria nascem em qualquer nível, não só na liderança |
| 6.CAD.1 | ML6 | Há revisão de estratégia alimentada por dados dos serviços |
| 6.POL.1 | ML6 | Existe prática de descontinuar produtos e serviços que perderam sentido |

**Total:** 12 itens no ML1, 13 no ML2, 13 no ML3 (38 por time) e 9 de horizonte.

---

## 5. Camada 2: indicadores de fluxo

| Indicador | Cálculo | O que revela | Leitura indicativa *(a calibrar com os dados reais)* |
|---|---|---|---|
| **Lead time P50 / P85** | Percentis do tempo entre “em andamento” e “concluído”, por tipo | O prazo que o time consegue cumprir hoje | — (base para o SLE) |
| **Variabilidade** | P85 ÷ P50 | Quão confiável é uma data | ≤ 2 previsível · 2–4 instável · > 4 imprevisível |
| **Trabalho não planejado** | % de itens que entraram durante a sprint | Peso dos furas-fila | ≤ 15% · 15–30% · > 30% |
| **Plano × entregue** | % de itens do compromisso da sprint concluídos | Credibilidade do planejamento | ≥ 80% · 60–80% · < 60% |
| **Transbordo** | % de itens que passam por mais de uma sprint | Itens grandes demais ou WIP alto | ≤ 15% · 15–30% · > 30% |
| **WIP por pessoa** | Itens em andamento ÷ pessoas do time | Sobrecarga e troca de contexto | ≤ 1,5 · 1,5–2,5 · > 2,5 |
| **Itens envelhecidos** | % do WIP com idade acima do P85 | Risco de atraso agora | ≤ 10% · 10–25% · > 25% |
| **Eficiência de fluxo** *(se o Nave fornecer)* | Tempo ativo ÷ lead time | Quanto do tempo é espera | ≥ 40% · 15–40% · < 15% |

**Verificação de coerência:** se o checklist indicar ML2 ou mais, mas dois ou mais indicadores estiverem na faixa vermelha, o painel sinaliza **“nível a revisar”**. Isso protege o modelo contra respostas otimistas.

> Os indicadores **não comparam times por volume** (vazão absoluta), porque os times vão de 2 a 15 pessoas. Só comparam **previsibilidade e saúde do fluxo**.

---

## 6. Painel (especificação)

### Visão 1 — Mapa da área (a tela para os gerentes)
- **Os 9 times lado a lado**, cada um com: nível consolidado, barra de progresso para o próximo nível, selo “a revisar” quando houver incoerência.
- **Distribuição por nível:** quantos times em ML0, ML1, ML2, ML3.
- **Linha do alvo:** ML3, a previsibilidade pedida pelos gerentes.
- **Destaque dos bloqueadores:** “X de 9 times estão bloqueados por L1 (sem dono do fluxo)”.

### Visão 2 — Mapa de calor das práticas
- Linhas: os 38 itens (agrupados por nível e dimensão) · Colunas: os 9 times.
- Mostra **lacunas sistêmicas** (o mesmo Não em todos os times = problema da organização, não do time).

### Visão 3 — Indicadores de fluxo
- Os indicadores da camada 2 por time, com as faixas verde, amarela e vermelha.
- Para cada time, a frase-resposta: **“Hoje, 85% das histórias saem em até X dias.”**

### Visão 4 — Evolução
- Nível e indicadores por ciclo trimestral (a partir do segundo ciclo).

### Visão 5 — Detalhe do time
- Checklist completo, pendências de base, próximos 3 itens recomendados para evoluir.

---

## 7. Mensagem que o painel deve sustentar

1. **Onde estamos:** distribuição dos 9 times por nível.
2. **Onde queremos chegar:** ML3, a previsibilidade definida pelos próprios gerentes.
3. **O que impede:** lacunas sistêmicas e bloqueadores que o time **não resolve sozinho** (L1 a L4).
4. **O que pedimos:** decisões da gerência (dono do fluxo, política de aceite de demanda, fim do plano fixo de 4 sprints, capacidade para melhoria).

---

## 8. Próximo passo — Fase 5 (validação)

1. Construir o painel e o formulário de checklist;
2. **Piloto** com o time de referência e um time típico, com dados do Nave (Anexo A);
3. Ajustar itens ambíguos e calibrar as faixas dos indicadores;
4. Rodar com os 9 times e apresentar aos gerentes.
