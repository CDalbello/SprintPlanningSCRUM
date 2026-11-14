# Planilha KMM-S

**Link:** https://docs.google.com/spreadsheets/d/1JQihXuvIhUpDUmWEQCUCw1zt-rEwFLhGDZEHGr2u6pw/edit
**Versão do modelo:** 0.1 · Locale pt-BR (fórmulas com `;`)

## Abas

| Aba | Para quê | Quem mexe |
|---|---|---|
| Leia-me | Instruções e regras | — |
| Painel | Resultado dos 9 times + gráficos | Ninguém (só a célula do ciclo) |
| Checklist | 38 itens × 9 times (Sim/Não) | POs + coordenação |
| Indicadores | Números do Nave/Jira por time | Coordenação |
| Times | Nome, PO, tamanho, perfil | Coordenação |
| Horizonte | 9 itens ML4–ML6, uma resposta para a área | Coordenação |
| Parâmetros | Faixas dos indicadores, alvo, bloqueadores | Coordenação |
| Histórico | Cópia do Painel a cada ciclo | Coordenação |

**Cores:** amarelo = preencher · azul = parâmetro ajustável · resto = fórmula.

## Regras de cálculo (Painel)

- **Nível consolidado:** todos os itens do ML1 até o ML N com Sim. Em branco = Não.
- **Progresso:** Sim do próximo nível ÷ itens do próximo nível.
- **Pendências de base:** itens sem Sim abaixo do maior nível com algum Sim.
- **Bloqueador ativo:** algum item ligado (coluna G do Checklist) sem Sim.
- **Nível a revisar:** nível ≥ `Parâmetros!B13` e vermelhos ≥ `Parâmetros!B12`.

## Como evoluir

| Mudança | Como fazer |
|---|---|
| Novo item | Nova linha no fim do Checklist (código, nível, tipo, dimensão). As fórmulas usam intervalos abertos. |
| Ligar item a bloqueador | Preencher coluna G do Checklist com L1–L4. |
| Novo bloqueador (L5) | Linha em Parâmetros + coluna no Painel ao lado de R (copiar fórmula de R). |
| Novo time | Linha em Times; estender colunas do Checklist (hoje H:P) e as linhas de Indicadores e Painel; ajustar `$H$2:$P` nas fórmulas do Painel. |
| Mudar faixas | Editar Parâmetros (azul). |
| Mudar alvo | `Parâmetros!B14`. |
| Fechar ciclo | Copiar `Painel!A5:J13` → colar como valores em Histórico (colunas C:L), preencher ciclo e data. |

Toda mudança de estrutura: registrar em [decisoes.md](decisoes.md) e [versoes.md](versoes.md).

## Teste feito na criação

Respostas fictícias em 2 times conferiram nível, progresso, pendências, bloqueadores e status dos indicadores. Dados de teste apagados.
