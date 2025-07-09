# 📉 Previsão de Evasão de Clientes (Churn) — Telecom X

Este projeto tem como objetivo desenvolver um modelo preditivo capaz de identificar clientes com maior probabilidade de cancelarem seus serviços na empresa fictícia **Telecom X**.

## 🚀 Objetivos do Projeto

- Explorar e preparar os dados de clientes da Telecom X.
- Tratar valores ausentes e variáveis irrelevantes.
- Codificar variáveis categóricas (encoding).
- Aplicar normalização para modelos baseados em distância.
- Lidar com o desbalanceamento das classes usando SMOTE.
- Treinar e avaliar modelos preditivos de classificação.
- Identificar as variáveis mais relevantes para a evasão.
- Apresentar um relatório técnico com interpretação dos resultados.

## 🧰 Tecnologias e Bibliotecas Utilizadas

- Python 3.10
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib / Seaborn
- Jupyter Notebook

## 🧠 Etapas do Projeto

### 1. Análise Exploratória
- Identificação do desequilíbrio entre as classes (churn ~26%).
- Visualizações para entender os perfis de clientes.

### 2. Pré-processamento
- Exclusão de colunas irrelevantes (`customerID`, `Contas_Diarias`).
- Encoding de variáveis categóricas (`Contract`, `PaymentMethod`, etc.).
- Normalização com MinMaxScaler para colunas numéricas.
- Balanceamento do dataset com **SMOTE** nos dados de treino.

### 3. Seleção de Variáveis
- Análise de correlação com a variável `Churn`.
- Seleção das variáveis com maior impacto para o modelo.

### 4. Modelagem
Foram treinados dois modelos principais:
- **Regressão Logística** (com tuning de hiperparâmetros)
- **Random Forest Classifier** (com GridSearchCV)

### 5. Avaliação
As métricas utilizadas foram:
- Acurácia
- Precisão
- Recall
- F1-score
- Matriz de confusão

## 📊 Principais Resultados

| Modelo               | Accuracy | Recall Churn | F1-score Churn |
|----------------------|----------|--------------|----------------|
| Regressão Logística  | 0.74     | **0.79**     | **0.62**       |
| Random Forest        | 0.74     | 0.73         | 0.59           |

- A regressão logística apresentou melhor desempenho em **recall** da classe minoritária (clientes que evadem), crucial para o negócio.
- A Random Forest teve melhor performance na validação, mas demonstrou sinais de **overfitting**.

## 🔍 Conclusões

- Clientes com contratos mensais e sem suporte técnico ou segurança online têm maior propensão ao churn.
- O modelo pode ser utilizado para prever e priorizar clientes com risco de evasão, permitindo a empresa agir preventivamente.
- Recomendamos o uso do modelo de regressão logística para produção, devido ao melhor equilíbrio entre interpretabilidade e recall.

## 📁 Organização do Projeto

