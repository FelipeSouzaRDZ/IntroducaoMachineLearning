
---

# Classificação de Score de Crédito: Introdução ao Machine Learning

Este projeto foi desenvolvido como um exemplo básico de classificação para alunos iniciantes em Machine Learning. O objetivo principal é demonstrar o fluxo de trabalho inicial de um cientista de dados, desde o pré-processamento até a comparação de modelos preditivos.

## Contexto do Problema
O cenário simula o trabalho em um banco que possui uma base de dados com **100.000 clientes**. A tarefa consiste em criar um modelo capaz de classificar automaticamente o **score de crédito** desses clientes baseando-se em seu histórico.

Os scores disponíveis na base são:
* **Good** (Bom)
* **Standard** (Médio)
* **Poor** (Ruim)

## Tecnologias e Bibliotecas
As seguintes ferramentas foram utilizadas no desenvolvimento:
* **Pandas**: Manipulação e análise de dados.
* **Scikit-Learn**: Pré-processamento, separação de dados e modelos (KNN e Random Forest).
* **LightGBM**: Modelo de Gradient Boosting de alta performance.
* **Google Colab**: Ambiente de execução na nuvem.

## Estrutura do Projeto

### 1. Pré-Processamento
Nesta etapa, os dados foram preparados para os modelos. Como algoritmos de Machine Learning geralmente não processam texto diretamente, utilizamos o `LabelEncoder` para converter colunas categóricas em números:
* **Profissão**
* **Mix de Crédito**
* **Comportamento de Pagamento**

### 2. Divisão de Dados
A base foi dividida utilizando a técnica de `train_test_split`, reservando **30% dos dados para teste** e 70% para o treinamento dos modelos.

### 3. Modelos Testados
Três algoritmos diferentes foram aplicados para comparação de desempenho:
* **Random Forest (Floresta de Decisão)**
* **KNN (K-Nearest Neighbors)**
* **LightGBM**

## Resultados
Após o treinamento, as previsões foram comparadas com os dados de teste reais. O modelo que apresentou o melhor desempenho para este problema específico foi a **Árvore de Decisão (Random Forest)**.

## Como Utilizar
1.  Monte seu Google Drive para carregar a base `clientes.csv`.
2.  Execute as células de pré-processamento para tratar as variáveis categóricas.
3.  Treine os modelos e verifique a acurácia através da função `accuracy_score`.
4.  Utilize o modelo campeão para classificar a base de novos clientes (`clientesNovos.csv`).

---
> **Nota:** Este script é uma adaptação para fins educacionais baseada em dados do [Kaggle](https://www.kaggle.com/).