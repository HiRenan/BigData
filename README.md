# Projeto de Big Data: Análise Preditiva de Churn de Clientes

## 📖 Visão Geral

Este repositório contém o projeto final desenvolvido para a disciplina de **Big Data e Mineração de Dados**, como parte da Residência em Inteligência Artificial Aplicada do UniSENAI. O objetivo foi construir uma solução de dados de ponta a ponta para prever a probabilidade de *churn* (cancelamento) de clientes, aplicando conceitos de análise, engenharia de dados e machine learning.

O trabalho foi desenvolvido em dupla por Renan Mocelin e Lucas Porfirio.

## 🎯 Objetivo do Projeto

O objetivo central foi elaborar e implementar um pipeline de dados e um modelo de mineração para prever a probabilidade de churn de clientes. A solução visa analisar dados históricos para identificar os principais fatores de risco e gerar um "score de risco" acionável, permitindo que as áreas de negócio desenvolvam campanhas de retenção mais eficazes.

## 📊 Dataset

Utilizamos o dataset **"Telco Customer Churn"**, um conjunto de dados público e popular para problemas de classificação, disponível no Kaggle.

* **Link para o Dataset:** [https://www.kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## 🛠️ Etapas do Projeto

O projeto foi estruturado em um fluxo de trabalho completo, simulando um case real da indústria:

1.  **Análise Exploratória de Dados (EDA):** Investigação inicial dos dados para identificar padrões e gerar hipóteses. Os principais insights revelaram que o **tipo de contrato**, o **tempo de permanência (tenure)** e o **valor da cobrança mensal** são os fatores mais influentes no churn.

2.  **Engenharia de Atributos e Pré-processamento:** Transformação das variáveis categóricas em formato numérico (`One-Hot Encoding`) e padronização das variáveis contínuas (`StandardScaler`) para preparar os dados para a modelagem.

3.  **Seleção de Variáveis (Feature Selection):** Aplicação de um modelo Random Forest sobre todos os atributos para identificar, de forma orientada por dados, as variáveis com maior poder preditivo.

4.  **Modelagem Preditiva:** Treinamento e avaliação de dois modelos de classificação (Regressão Logística e Random Forest). O modelo de Regressão Logística foi selecionado como a solução final por sua performance robusta e maior interpretabilidade.

5.  **Arquitetura do Pipeline de Dados:** Desenho de uma arquitetura de pipeline escalável na nuvem **AWS**, utilizando serviços como S3 (Data Lake), AWS Glue (ETL), Amazon SageMaker (Modelagem) e QuickSight (BI).

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Bibliotecas Principais:** Pandas, Scikit-learn, Matplotlib, Seaborn
* **Ambiente:** Google Colab
* **Cloud (Arquitetura):** Amazon Web Services (AWS)

## ⚙️ Como Executar o Notebook

O projeto está contido no notebook `BigData (1).ipynb` . Para executá-lo:

1.  Abra o notebook no Google Colab.
2.  Para a etapa de obtenção de dados via API, será necessário gerar sua própria chave `kaggle.json` no site do Kaggle e fazer o upload quando o script solicitar.
3.  Execute as células em ordem sequencial.

---
