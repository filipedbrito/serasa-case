# Análise de Receita — Crédito

## Objetivo

Entender, por produto, qual alavanca mais impacta a receita:

* volume (simulações)
* conversão
* receita por conversão

![mapa_mental](mapa_mental.png)

---

## Modelo

```
receita = volume × conversão × receita_por_conversão
```

---

## Estrutura

A análise é feita sobre:

```
perfil_cliente × produto
```

---

## Fluxo

![arquitetura](arquitetura.png)

* databricks: preparação dos dados (etl.ipynb)
* google sheets: exploração e análise

---

## Status

* base tratada e estruturada no databricks
* segmentação de perfis definida
* métricas principais calculadas
* análise em andamento na planilha

---

## Observação

Os dados não representam um funil linear (elegíveis pode ser maior que simulando).

---

## Referências

* exploratory_guide.md
* etl.ipynb
* planilha: https://docs.google.com/spreadsheets/d/1brGaTDOvhRGt9DIhHJLizVU40zYnfC6iLgBwJ-QLGxg/edit?usp=sharing
