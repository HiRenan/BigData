# Projeto de Big Data: Análise Preditiva de Churn de Clientes

## 📖 Visão Geral

[cite_start]Este repositório contém o projeto final desenvolvido para a disciplina de **Big Data e Mineração de Dados**[cite: 949], como parte da Residência em Inteligência Artificial Aplicada do UniSENAI. O objetivo foi construir uma solução de dados de ponta a ponta para prever a probabilidade de *churn* (cancelamento) de clientes, aplicando conceitos de análise, engenharia de dados e machine learning.

[cite_start]O trabalho foi desenvolvido em dupla por Renan Mocelin e Lucas Porfirio[cite: 948].

## 🎯 Objetivo do Projeto

[cite_start]O objetivo central foi elaborar e implementar um pipeline de dados e um modelo de mineração para prever a probabilidade de churn de clientes[cite: 151]. [cite_start]A solução visa analisar dados históricos para identificar os principais fatores de risco e gerar um "score de risco" acionável, permitindo que as áreas de negócio desenvolvam campanhas de retenção mais eficazes[cite: 153].

## 📊 Dataset

Utilizamos o dataset **"Telco Customer Churn"**, um conjunto de dados público e popular para problemas de classificação, disponível no Kaggle.

* **Link para o Dataset:** [https://www.kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## 🛠️ Etapas do Projeto

O projeto foi estruturado em um fluxo de trabalho completo, simulando um case real da indústria:

1.  [cite_start]**Análise Exploratória de Dados (EDA):** Investigação inicial dos dados para identificar padrões e gerar hipóteses[cite: 167]. [cite_start]Os principais insights revelaram que o **tipo de contrato**, o **tempo de permanência (tenure)** e o **valor da cobrança mensal** são os fatores mais influentes no churn[cite: 298, 874].

2.  [cite_start]**Engenharia de Atributos e Pré-processamento:** Transformação das variáveis categóricas em formato numérico (`One-Hot Encoding`) e padronização das variáveis contínuas (`StandardScaler`) para preparar os dados para a modelagem[cite: 365, 367].

3.  [cite_start]**Seleção de Variáveis (Feature Selection):** Aplicação de um modelo Random Forest sobre todos os atributos para identificar, de forma orientada por dados, as variáveis com maior poder preditivo[cite: 371].

4.  [cite_start]**Modelagem Preditiva:** Treinamento e avaliação de dois modelos de classificação (Regressão Logística e Random Forest)[cite: 379]. [cite_start]O modelo de Regressão Logística foi selecionado como a solução final por sua performance robusta e maior interpretabilidade[cite: 386].

5.  [cite_start]**Arquitetura do Pipeline de Dados:** Desenho de uma arquitetura de pipeline escalável na nuvem **AWS**, utilizando serviços como S3 (Data Lake), AWS Glue (ETL), Amazon SageMaker (Modelagem) e QuickSight (BI) [cite: 325-339, 911, 916, 923].

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Bibliotecas Principais:** Pandas, Scikit-learn, Matplotlib, Seaborn
* **Ambiente:** Google Colab
* **Cloud (Arquitetura):** Amazon Web Services (AWS)

## ⚙️ Como Executar o Notebook

[cite_start]O projeto está contido no notebook `BigData (1).ipynb` [cite: 1-142]. Para executá-lo:

1.  Abra o notebook no Google Colab.
2.  Para a etapa de obtenção de dados via API, será necessário gerar sua própria chave `kaggle.json` no site do Kaggle e fazer o upload quando o script solicitar.
3.  Execute as células em ordem sequencial.

---
