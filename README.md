# Laptop Price Prediction with NLP

## Descrição

Este projeto foi desenvolvido para a disciplina **Projeto Aplicado II** do curso de **Banco de Dados** da **Universidade Presbiteriana Mackenzie**.

A proposta consiste em desenvolver uma análise preditiva de preços de laptops, combinando técnicas de **análise exploratória de dados (EDA)**, **processamento de linguagem natural (NLP)** e **aprendizado de máquina**.

Os dados utilizados foram obtidos a partir de uma base pública do Kaggle, contendo especificações técnicas detalhadas e preços, em euros, de **1.146 modelos de laptops**.

Dataset: [Laptop Prices](https://www.kaggle.com/datasets/abdelrahmanemad594/laptop-prices/data)

---

## Organização

Este projeto é desenvolvido pela empresa fictícia **DataPrice Analytics**, especializada em análise de dados e inteligência de mercado no setor de tecnologia.

A empresa atua apoiando varejistas e fabricantes na definição de estratégias de precificação, utilizando modelos preditivos baseados em dados históricos de produtos.

Nesse contexto, o projeto busca gerar insights estratégicos sobre a formação de preços no mercado de laptops e desenvolver um modelo preditivo aplicável ao ambiente de negócios.

---

## Objetivo Principal

Este projeto tem como objetivo desenvolver um modelo preditivo capaz de estimar o preço de laptops com base em suas especificações técnicas, identificando quais componentes de hardware possuem maior impacto na formação de preço.

Além disso, busca-se avaliar a viabilidade de prever o valor de mercado de um laptop a partir de seus atributos, utilizando técnicas de aprendizado de máquina e processamento de linguagem natural.

---

## Perguntas de Negócio

- Quais componentes de hardware impactam mais no preço de um laptop?
- É possível prever o preço de um laptop com base em suas especificações técnicas?
- A inclusão de informações textuais, como modelo de CPU e GPU, melhora o desempenho do modelo preditivo?

---

## Etapas do Projeto

### a) Aquisição e Preparação dos Dados

- Ingestão do arquivo CSV
- Remoção da coluna vazia `Unnamed: 16`
- Conversão de variáveis como RAM e frequência da CPU para formato numérico
- Tratamento de valores ausentes
- Padronização e normalização de dados

### b) Processamento de Texto (NLP)

- Extração de informações de CPU e GPU via expressões regulares
- Identificação de presença de GPU dedicada
- Extração de resolução de tela
- Aplicação de **TF-IDF** na variável `Product`

### c) Análise Estatística

- Distribuição dos preços
- Identificação de outliers
- Testes de hipótese, como **Kruskal-Wallis**
- Correlação entre variáveis numéricas

### d) Machine Learning

- Regressão Linear
- Random Forest
- XGBoost
- Comparação entre modelos com e sem uso de features textuais extraídas por NLP

---

## Tecnologias Utilizadas

- pandas
- numpy
- matplotlib
- scipy
- scikit-learn


---

## Métricas de Avaliação

Os modelos serão avaliados com base nas seguintes métricas:

- **RMSE** (Root Mean Squared Error)
- **MAE** (Mean Absolute Error)
- **R²** (Coeficiente de Determinação)

Também será utilizada **validação cruzada com 5 folds**, com o objetivo de garantir maior robustez e confiabilidade aos resultados obtidos.

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

---

## Integrantes

Este projeto foi desenvolvido pelos seguintes integrantes:

- Ryan Rodrigues Pereira  
- Nour Hussein Barakat  
- Guilherme de Araújo Esp. Santo  

---

## Instituição

Universidade Presbiteriana Mackenzie  
Curso: Banco de Dados  
Projeto Aplicado II — 3º semestre — 2026
