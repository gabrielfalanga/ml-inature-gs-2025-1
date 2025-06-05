# 🌿 iNature — Análise e Modelagem de Dados para Classificação de Desastres Naturais

## 📚 Índice

- [🔍 Descrição do Problema](#-descrição-do-problema)
- [🧪 Metodologia Utilizada](#-metodologia-utilizada)
- [📈 Resultados Obtidos](#-resultados-obtidos)
- [🧠 Conclusões](#-conclusões)
- [👥 Equipe iNature](#-equipe-inature)

## 📝 Descrição do Problema

Eventos relacionados a desastres naturais geram impactos significativos na vida das pessoas e no meio ambiente. Com a intensificação desses eventos devido às mudanças climáticas, torna-se essencial compreender seus padrões e características. O projeto **iNature** propõe o uso da ciência de dados para **classificar tipos de desastres naturais com base em informações históricas** — como número de afetados, danos econômicos, mortes, período do ano, entre outros.

O objetivo principal é **desenvolver modelos preditivos que auxiliem na identificação automática do tipo de desastre**, contribuindo para ações mais rápidas de prevenção e resposta.

---

## 🔍 Metodologia Utilizada

### 1. Pré-processamento dos Dados
- **Carregamento do dataset** com informações de desastres naturais.
- **Limpeza e tratamento de valores ausentes**.
- **Conversão de variáveis categóricas** e ajustes de tipos.
- **Padronização e normalização** das variáveis numéricas.

### 2. Análise Exploratória (EDA)
- Visualização da **distribuição de classes** (desastres).
- Análise de **correlação entre variáveis numéricas**.
- Identificação de **desequilíbrio de classes**.

### 3. Modelagem
Foram testados três modelos de classificação:
- **Regressão Logística**
- **Random Forest**
- **SVM (Support Vector Machine)**

Avaliação com base em:
- **Acurácia**
- **F1-Score Macro** (média entre classes)
- **F1-Score Weighted** (ponderado pelo número de amostras)
- **Matriz de Confusão** para interpretação detalhada dos erros.

> Obs.: Foi aplicado `StandardScaler` nos modelos sensíveis à escala.

---

## 📊 Resultados Obtidos

| Modelo              | Acurácia | F1-score (Macro) | F1-score (Weighted) |
|---------------------|----------|------------------|----------------------|
| **Random Forest**   | 0.6395   | **0.5519**       | **0.6315**           |
| Regressão Logística | 0.4968   | 0.2633           | 0.4532               |
| SVM                 | 0.4806   | 0.2219           | 0.4260               |

- O modelo **Random Forest** teve o melhor desempenho geral.
- As métricas de macro F1-score revelaram **impacto do desbalanceamento de classes**, com algumas categorias raras sendo completamente ignoradas por certos modelos.
- A **matriz de confusão** evidenciou que classes majoritárias (como 5 e 12) dominaram as previsões.

---

## ✅ Conclusões

- Os dados apresentam um **forte desbalanceamento**, o que prejudicou o desempenho de modelos mais sensíveis como SVM e Regressão Logística.
- **Random Forest demonstrou robustez**, sendo mais equilibrado na previsão das classes e superando os demais em todas as métricas.
- A análise sugere que futuras etapas poderiam incluir:
  - **Técnicas de balanceamento** (como oversampling/SMOTE).
  - **Feature engineering** com base em domínio climático/geográfico.
  - Testes com **modelos mais complexos** (XGBoost, LightGBM, redes neurais).

---

## 👥 Equipe iNature
- Gabriel Falanga - RM 555061
- Arthur Spedine - RM 554489
- Matheus Esteves - RM 554769

---


