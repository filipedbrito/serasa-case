# Análise de Receita — Crédito

## Objetivo

Identificar, por produto e perfil de cliente, quais alavancas mais impactam a receita:

* volume (simulações)
* conversão
* receita por conversão

---

## Modelo

Receita pode ser decomposta como:

```
receita = volume × conversão × receita_por_conversão
```

---

## Observações sobre os dados

O dataset não representa um funil estritamente linear.

* `elegíveis` pode ser maior que `simulando`
* possível existência de múltiplas ofertas por usuário
* métricas podem estar em granularidades diferentes

A interpretação deve considerar um modelo de múltiplas oportunidades de crédito, e não um funil clássico.

---

## Segmentação de clientes

Perfis construídos a partir de:

* score de crédito
* renda
* status de negativação
* idade (ajuste secundário)

Perfis definidos:

* premium
* bom_pagador
* potencial
* medio
* inicio_credito
* baixa_qualidade
* baixo_score
* restrito

Objetivo da segmentação: reduzir a variabilidade e permitir análise e ação direcionada.

---

## Estrutura da análise

Tabela principal:

```
perfil_cliente × produto
```

Métricas disponíveis:

* total_simulando
* total_elegiveis
* total_conversao
* total_receita

---

## Métricas derivadas

```
conversao = total_conversao / total_elegiveis
receita_por_conversao = total_receita / total_conversao
receita_por_simulacao = total_receita / total_simulando
```

A métrica principal para comparação é:

```
receita_por_simulacao
```

---

## Status

Concluído:

* análise de volume e sazonalidade
* construção de perfis de cliente
* agregação perfil × produto
* cálculo de métricas principais
* exploração inicial dos dados

Pontos de atenção:

* elegibilidade maior que volume em alguns produtos
* taxas de conversão muito estáveis ao longo do tempo
* necessidade de validação das definições de métricas

---

## Próximos passos

1. Analisar a tabela `perfil × produto` com foco em:

   * receita
   * conversão
   * receita_por_simulacao

2. Classificar combinações em:

* alto volume + alta receita → escalar
* alto volume + baixa receita → otimizar
* baixo volume + alta receita → expandir
* baixo volume + baixa receita → despriorizar

3. Validar com o time:

* definição de elegibilidade
* granularidade dos dados
* lógica de conversão

---

## Links

Planilha:
https://docs.google.com/spreadsheets/d/1brGaTDOvhRGt9DIhHJLizVU40zYnfC6iLgBwJ-QLGxg/edit?usp=sharing

Notebook:
https://dbc-905e5752-09c9.cloud.databricks.com/editor/notebooks/3207783246180340?o=7474647676028865

---

## Nota

A análise está estruturada até o nível de perfil × produto.

O próximo passo é consolidar os achados e direcionar ações de negócio, após validação das premissas de dados.