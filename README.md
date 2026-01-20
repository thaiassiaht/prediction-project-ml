# 🧠 Prediction Project ML — Depression Risk Prediction

## Visão Geral

Este repositório apresenta um **sistema completo de Machine Learning para predição de risco de depressão**, desenvolvido como trabalho final da disciplina de Inteligência Artificial no curso de Ciência da Computação.

O projeto foi pensado com **padrões profissionais**, foco em **reprodutibilidade**, **organização modular** e **boas práticas de engenharia de software aplicadas a ML**, refletindo um pipeline próximo ao utilizado em contextos reais de pesquisa e indústria.

> ⚠️ **Nota importante**: o projeto está **conceitualmente completo e funcional**, porém **nem todos os módulos descritos abaixo estão presentes neste repositório público no momento**.

---

## 🎯 Objetivo

Desenvolver uma ferramenta de **triagem automatizada** para identificar indivíduos com possível risco de depressão, **sem substituir diagnóstico clínico**, mas auxiliando ações preventivas, especialmente em ambientes educacionais.

---

## 🧪 Abordagem Técnica

* Pipeline completo de pré-processamento de dados
* Treinamento e comparação entre múltiplos modelos supervisionados
* Otimização de hiperparâmetros com **GridSearchCV**
* Validação cruzada estratificada (**Stratified K-Fold**)
* Avaliação com métricas relevantes para saúde (Recall e F1-Score)
* Estrutura preparada para escalabilidade, reuso e experimentação

---

## 🤖 Modelos Implementados

* **K-Nearest Neighbors (KNN)**
* **Support Vector Machine (SVM)**
* **Multilayer Perceptron (MLP)**

📌 O **MLP apresentou o melhor desempenho geral**, com maior acurácia e F1-Score, porém foi considerado o melhor modelo testado já que não sacrificou precisão em troca do recall.

📌 O **SVM obteve o maior Recall**, métrica crítica em aplicações de saúde.

---

## 📊 Métricas Utilizadas

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

🔎 **Justificativa**:

* **Recall** foi priorizado para reduzir falsos negativos (casos de risco não identificados).
* **F1-Score** foi utilizado para balancear precisão e recall, especialmente em cenários com classes desbalanceadas.

---

## 🗂️ Estrutura do Projeto

Abaixo está a **estrutura arquitetural planejada** do projeto, seguindo boas práticas de projetos de Machine Learning.

```text
prediction_project/
│
├── config/
│   ├── data_config.yaml
│   ├── model_config.yaml
│   └── training_config.yaml
│
├── src/
│   ├── data/
│   │   ├── load_data.py
│   │   ├── preprocess.py
│   │   ├── split.py
│   │   └── feature_engineering.py
│   │
│   ├── models/
│   │   ├── base_model.py
│   │   ├── knn.py
│   │   ├── svm.py
│   │   ├── mlp.py
│   │   └── random_forest.py
│   │
│   ├── training/
│   │   ├── train.py
│   │   ├── cross_validation.py
│   │   └── hyperparameters.py
│   │
│   ├── evaluation/
│   │   ├── metrics.py
│   │   ├── confusion_matrix.py
│   │   └── plots.py
│   │
│   ├── inference/
│   │   └── predict.py
│   │
│   └── utils/
│       ├── logger.py
│       ├── save_load.py
│       └── random_seed.py
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── splits/
│
├── experiments/
│   ├── knn_exp.ipynb
│   ├── svm_exp.ipynb
│   └── mlp_exp.ipynb
│
├── results/
│   ├── metrics/
│   ├── figures/
│   └── tables/
│
├── requirements.txt
├── README.md
└── main.py
```

🧩 **Estado atual do repositório**:

* Os **notebooks de experimentação**, scripts principais de treinamento, avaliação e visualização estão disponíveis.
* Módulos de configuração, logging avançado e alguns utilitários estão **planejados para publicação completa na versão 2.0**.

---

## 🧠 Pontos Fortes Observáveis (Visão de Recrutador)

* Clareza arquitetural e separação de responsabilidades
* Uso correto de validação cruzada estratificada
* Escolha consciente de métricas alinhadas ao domínio
* Código orientado à reprodutibilidade
* Organização compatível com projetos reais de ML
* Preocupação ética no uso do modelo (triagem ≠ diagnóstico)

---

## 📄 Licença

Projeto com fins acadêmicos e educacionais.

---

📬 **Feedbacks, sugestões e colaborações são muito bem-vindos.**

