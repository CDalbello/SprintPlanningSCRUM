# Anexo A — Pedido de extração de dados (Nave / Jira)

> Objetivo: testar a hipótese de nível de maturidade e montar um exemplo real de previsibilidade para os gerentes.
> Pode ser **anonimizado** (sem nomes de pessoas, sem título das demandas).

## Escopo da amostra

- **Times:** 2 times, idealmente **o time de referência** e **um time típico** (perfil “reativo sobrecarregado”).
- **Período:** últimos **6 meses** (mínimo 3).
- **Atenção:** extrair **antes** da virada Jira Server → Cloud, ou confirmar que o histórico de transições foi migrado.

## Dados por item (uma linha por issue)

| Campo | Para quê |
|---|---|
| ID (pode ser anonimizado) | Identificação |
| Time | Comparação entre times |
| Tipo de item (história, bug, tarefa, incidente…) | Lead time por tipo |
| Data de criação | Tempo de espera antes do compromisso |
| Data em que entrou em andamento (1ª transição para “em progresso”) | Início do lead time |
| Data de conclusão | Fim do lead time |
| Status atual | Identificar WIP e idade dos itens |
| Sprint(s) em que esteve | Medir “transbordo” entre sprints |
| Entrou durante a sprint? (sim/não) | Medir furas-fila |
| Prioridade / label de urgência, se houver | Avaliar classes de serviço implícitas |
| Story points, se houver | Comparar estimativa × tempo real |
| Tempo bloqueado / flag de bloqueio, se houver | Medir eficiência de fluxo |

## Métricas prontas do Nave (se for mais fácil que a extração bruta)

- **Cycle time / lead time:** distribuição e percentis 50, 70, 85 e 95;
- **Vazão** (itens concluídos por semana);
- **CFD** (diagrama de fluxo cumulativo);
- **Idade do WIP** (*aging*);
- **Eficiência de fluxo**, se disponível;
- **Previsão Monte Carlo**, se disponível.

## O que vamos produzir com isso

1. Lead time por tipo de demanda e o **SLE atual implícito** (“hoje, 85% das histórias saem em até X dias”);
2. Comparação **plano da sprint × entregue** e proporção de **trabalho não planejado**;
3. Relação entre **WIP e lead time** (evidência do “rodar no talo”);
4. Posição provisória de cada time na régua KMM;
5. Um **exemplo de resposta** a “quando fica pronto?” com dados reais, que é o argumento para os gerentes.
