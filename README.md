# Análise de Receita — Crédito

## Objetivo

Entender, por produto, qual alavanca mais gera receita incremental:

* volume (simulações)
* conversão
* receita por conversão

![mapa_mental](mapa_mental.png)

---

## Modelo

Receita é decomposta como:

```
receita = volume × conversão × receita_por_conversão
```

A análise busca identificar qual desses drivers mais impacta a receita em cada produto.

---

## Estrutura

A análise é conduzida a partir de:

```
perfil_cliente × produto
```

com métricas de:

* volume (simulações)
* elegibilidade
* conversão
* receita

---

## Observação sobre os dados

Os dados não seguem um funil estritamente linear:

* elegíveis pode ser maior que simulando
* possível múltiplas ofertas por usuário

A leitura deve considerar um modelo de múltiplas oportunidades, não um funil clássico.

---

## Status

* perfis de cliente definidos
* base agregada por perfil × produto construída
* métricas principais calculadas
* análise exploratória em andamento

---

## Próximo passo

Identificar, por produto:

* onde escalar (volume)
* onde otimizar (conversão)
* onde explorar ticket (receita por conversão)

---

## Referências

* exploratory_guide.md
* notebook: https://dbc-905e5752-09c9.cloud.databricks.com/editor/notebooks/3207783246180340?o=7474647676028865
* planilha: https://docs.google.com/spreadsheets/d/1brGaTDOvhRGt9DIhHJLizVU40zYnfC6iLgBwJ-QLGxg/edit?usp=sharing

![arquitetura](arquitetura.png)