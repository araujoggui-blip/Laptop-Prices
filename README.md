# Laptop Price Prediction with NLP

## Descrição

Este projeto foi desenvolvido para a disciplina **Projeto Aplicado II** do curso de **Banco de Dados** da **Universidade Presbiteriana Mackenzie**.

A proposta consiste em desenvolver uma análise preditiva de preços de laptops, combinando técnicas de **análise exploratória de dados (EDA)**, **processamento de linguagem natural (NLP)** e **aprendizado de máquina**.

Os dados utilizados foram obtidos a partir de uma base pública do Kaggle, contendo especificações técnicas detalhadas e preços, em euros, de **1.146 modelos de laptops**.

Dataset: https://www.kaggle.com/datasets/abdelrahmanemad594/laptop-prices/data

---

## Organização

Este projeto é desenvolvido pela empresa fictícia **DataPrice Analytics**, especializada em análise de dados e inteligência de mercado no setor de tecnologia.

A empresa atua apoiando varejistas e fabricantes na definição de estratégias de precificação, utilizando modelos preditivos baseados em dados históricos de produtos.

---

## Objetivo Principal

Desenvolver um modelo preditivo capaz de estimar o preço de laptops com base em suas especificações técnicas, avaliando o impacto da inclusão de features extraídas de dados textuais por meio de técnicas de NLP.

Pergunta central:

**É possível melhorar a predição de preços de laptops utilizando dados textuais (CPU, GPU, etc.) em comparação com modelos que utilizam apenas dados numéricos?**

---

## Etapas do Projeto

### a) Aquisição e Preparação dos Dados

- Ingestão do arquivo CSV  
- Remoção da coluna vazia `Unnamed: 16`  
- Conversão de variáveis (RAM, CPU) para formato numérico  
- Tratamento de valores ausentes  
- Padronização de dados  

### b) Processamento de Texto (NLP)

- Extração de informações de CPU e GPU via regex  
- Identificação de GPU dedicada  
- Extração de resolução de tela  
- Aplicação de TF-IDF na variável Product  

### c) Análise Estatística

- Distribuição dos preços  
- Identificação de outliers  
- Testes de hipótese (Kruskal-Wallis)  
- Correlação entre variáveis  

### d) Machine Learning

- Regressão Linear  
- Random Forest  
- XGBoost  
- Comparação entre modelos com e sem NLP  

---

## Métricas de Avaliação

- RMSE  
- MAE  
- R²  

Validação cruzada com 5 folds.

---

## Estrutura do Projeto

```bash
Laptop-Prices/
│
├── data/
├── notebooks/
├── docs/
└── README.md

---

## Referências do Dataset

**Origem dos Dados:**  
O conjunto de dados foi obtido por meio da plataforma Kaggle, no dataset **Laptop Prices**  
(https://www.kaggle.com/datasets/abdelrahmanemad594/laptop-prices/data), publicado pelo usuário *abdelrahmanemad594*.

**Originalidade e Limitações:**  
O dataset contém **1.146 registros** com especificações técnicas detalhadas de laptops.  
Os preços estão em euros (€) e podem não refletir variações regionais de mercado.  
Inclui uma coluna vazia (`Unnamed: 16`) que será descartada no pré-processamento.

**Período da Coleta:**  
Modelos disponíveis comercialmente em **2017–2018**.

**Limitações de Uso:**  
Por se tratar de um dataset público e de fonte secundária, seu uso é destinado a fins acadêmicos e de pesquisa.

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
