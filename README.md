
# 🛒 Projeto: Previsão de Intenção de Compra de Clientes em Loja Web

## 🌟 Descrição do Projeto

Este projeto de Ciência de Dados visa desenvolver um sistema preditivo para antecipar a **intenção de compra** de clientes em um site de e-commerce. A capacidade de prever quais clientes têm maior probabilidade de realizar compras online, com base em suas características e comportamentos passados, permite que a empresa direcione seus esforços de marketing de forma mais eficaz e aprimore a experiência do cliente.

O objetivo final é classificar se um cliente realizará compras no site da empresa (variável alvo: `WebPurchases`).

## 🎯 Objetivo

Desenvolver e avaliar um modelo de Machine Learning capaz de analisar os padrões de comportamento dos clientes e identificar sinais que indicam a propensão deles para realizar compras no site da empresa.

## 📂 Base de Dados

O projeto utiliza o arquivo `marketing_campaign.csv`. A base de dados contém informações detalhadas sobre os clientes, incluindo dados demográficos, estado civil, renda, informações sobre compras anteriores e comportamento na web.

| Variável | Descrição |
| :--- | :--- |
| **Year\_Birth** | Ano de nascimento do cliente. |
| **Education** | Nível de escolaridade. |
| **Marital\_Status** | Estado civil. |
| **Income** | Renda anual da família. |
| **Kidhome** | Número de crianças na casa. |
| **Recency** | Número de dias desde a última compra. |
| **MntWines**, **MntFruits**, **MntMeatProducts**, **MntFishProducts**, **MntSweetProducts**, **MntGoldProds** | Valores gastos em diferentes categorias de produtos nos últimos 2 anos. |
| **NumStorePurchases** | Número de compras feitas diretamente nas lojas. |
| **NumWebVisitsMonth** | Número de visitas ao site da empresa no último mês. |
| **Complain** | 1 se o cliente reclamou nos últimos 2 anos, 0 caso contrário. |
| **WebPurchases** | **Variável Alvo:** Número de compras feitas pelo site da empresa (Convertida para binária 0 ou 1 no notebook). |

## 🛠️ Metodologia e Etapas

O projeto foi dividido nas seguintes etapas:

1.  **Preparação e Limpeza dos Dados (ETAPA 1):**
    * Análise exploratória inicial (`df.info()`, `df.head()`).
    * Tratamento de valores ausentes (Imputação de valores em `Income`).
    * Tratamento de *outliers* em variáveis de renda e nascimento.
    * Criação de novas *features* como `Age` (Idade) e `Spent` (Gasto Total).
    * Análise e Visualização de Dados (Storytelling com gráficos).
2.  **Engenharia de Features e Pré-processamento:**
    * Codificação de variáveis categóricas (One-Hot Encoding em `Education` e `Marital_Status`).
    * Redução de Dimensionalidade (PCA).
    * Divisão dos dados em treino e teste.
    * Padronização dos dados numéricos (StandardScaler).
3.  **Modelagem Preditiva (ETAPA 2):**
    * Foram testados dois modelos de classificação:
        * **Random Forest Classifier**
        * **Regressão Logística**
4.  **Avaliação dos Modelos:**
    * Utilização de métricas como *Classification Report* (Precision, Recall, F1-Score) e Matriz de Confusão para avaliar o desempenho e a credibilidade dos modelos.

## 📈 Resultados

O modelo de **Random Forest Classifier** apresentou o melhor desempenho geral na previsão da intenção de compra:

| Métrica | Random Forest | Regressão Logística |
| :--- | :--- | :--- |
| **Acurácia (Accuracy)** | **0.90** | 0.84 |
| **F1-Score (média ponderada)** | **0.90** | 0.84 |

O modelo Random Forest é o recomendado para a produção, com uma acurácia de **86%**.

## 💻 Tecnologias e Bibliotecas

* Python
* Pandas (manipulação de dados)
* NumPy (operações numéricas)
* Matplotlib e Plotly Express (visualização de dados)
* Seaborn (visualização de dados)
* Scikit-learn (Modelos de ML e pré-processamento)
    * `RandomForestClassifier`
    * `LogisticRegression`
    * `StandardScaler`
    * `PCA`

## 👤 Autor

* [Paulo Machado/Wekoda]
