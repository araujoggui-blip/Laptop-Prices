# Laptop Prices Prediction with NLP

## Descrição

Este projeto foi desenvolvido para a disciplina **Projeto Aplicado II** do curso de **Banco de Dados** da **Universidade Presbiteriana Mackenzie**.

A proposta consiste em desenvolver uma análise preditiva de preços de laptops, combinando técnicas de **análise exploratória de dados (EDA)**, **processamento de linguagem natural (NLP)** e **aprendizado de máquina**.

Os dados utilizados foram obtidos a partir de uma base pública do Kaggle, contendo especificações técnicas detalhadas e preços, em euros, de **1.146 modelos de laptops**.

Dataset: [Laptop Prices](https://www.kaggle.com/datasets/abdelrahmanemad594/laptop-prices?resource=download)

---

## Organização

Este projeto é desenvolvido pela empresa fictícia **DataPrice Analytics**, especializada em **análise de dados e inteligência de mercado no setor de tecnologia**.

A empresa atua apoiando **varejistas e fabricantes** na definição de estratégias de precificação, utilizando modelos preditivos baseados em dados históricos de produtos.

Nesse contexto, o presente projeto busca prever preços de laptops a partir de suas especificações técnicas, auxiliando decisões estratégicas de mercado.

---

## Objetivo Principal

A proposta central do projeto é responder à seguinte pergunta:

**É possível melhorar a predição de preços de laptops extraindo features a partir dos campos de texto do dataset, como modelo de CPU e GPU, em comparação com um modelo que utiliza apenas dados numéricos?**

---

## Etapas do Projeto

### a) Aquisição e Preparação dos Dados

- Ingestão do arquivo `.csv`
- Remoção da coluna vazia `Unnamed: 16`
- Conversão da coluna `Ram` de string (ex.: `8GB`) para formato numérico
- Conversão da coluna `Cpu Rate` de string (ex.: `2.5GHz`) para formato numérico
- Tratamento de valores ausentes
- Padronização e normalização de strings

### b) Processamento de Texto (NLP)

- Extração de features das colunas `Cpu Model`, `Gpu Model` e `ScreenResolution`
- Uso de expressões regulares e tokenização
- Geração de variáveis como:
  - família e geração da CPU
  - presença de GPU dedicada
  - resolução da tela em formato numérico
  - representação textual da coluna `Product` com **TF-IDF**

### c) Análise Estatística Preditiva

- Distribuição das variáveis
- Identificação de outliers em `Price_Euros`
- Testes de hipótese, como **Kruskal-Wallis**, para comparar preços entre marcas e tipos de laptop
- Regressão linear múltipla como modelo baseline
- Matriz de correlação entre variáveis numéricas e o preço

### d) Aprendizado de Máquina

- Construção de modelos preditivos para estimar `Price_Euros`
- Comparação entre modelos com:
  - apenas variáveis numéricas
  - variáveis numéricas + features textuais extraídas via NLP

---

## Métricas de Avaliação

O desempenho dos modelos será avaliado com:

- **RMSE** — Root Mean Squared Error
- **MAE** — Mean Absolute Error
- **R²** — Coeficiente de Determinação

Também será utilizada **validação cruzada com 5 folds** para aumentar a robustez da avaliação.

---

## Análise Exploratória de Dados (EDA)

A análise exploratória considera, entre outros pontos:

- distribuição dos preços dos laptops
- comparação de preços entre marcas
- relação entre preço e quantidade de RAM
- relação entre preço e tipo de armazenamento
- identificação de outliers
- correlações entre variáveis numéricas

Essa etapa permite compreender melhor os padrões do conjunto de dados antes da modelagem.

---

## Estrutura do Projeto

```bash
Laptop-Prices/
│
├── data/
│   └── laptop_prices.csv
│
├── notebooks/
│   └── laptop_price_analysis.ipynb
│
├── docs/
│   └── relatorio_etapa_2.docx
│
└── README.md
