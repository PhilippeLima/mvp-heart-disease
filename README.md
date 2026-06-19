# MVP — Predição de Doença Cardíaca com Machine Learning

**Curso:** Machine Learning & Analytics — PUC-Rio  
**Autor:** Felipe Guimarães  
**Tipo de problema:** Classificação Binária

---

## Descrição

Este projeto desenvolve um modelo de Machine Learning capaz de prever a **presença ou ausência de doença cardíaca** em pacientes, com base em atributos clínicos como frequência cardíaca máxima, depressão do segmento ST, tipo de dor torácica e número de vasos coronários.

O objetivo não é substituir o diagnóstico médico, mas servir como ferramenta de triagem e suporte à decisão clínica.

---

## Dataset

| Atributo | Detalhe |
|---|---|
| **Nome** | Heart Disease Dataset (Cleveland) |
| **Fonte** | UCI Machine Learning Repository |
| **Arquivo** | `heart_disease_cleveland.csv` |
| **Registros** | 303 |
| **Features** | 13 preditores clínicos |
| **Variável-alvo** | `target` — 0 (sem doença) / 1 (com doença) |

---

## Estrutura do Repositório

```
├── mvp_heart_disease.ipynb        # Notebook principal (executável no Google Colab)
├── heart_disease_cleveland.csv    # Dataset utilizado
└── README.md                      # Este arquivo
```

---

## Como Executar

1. Acesse o notebook no Google Colab clicando no badge abaixo  
2. Vá em **Runtime → Run all**  
3. Nenhuma configuração manual é necessária — o dataset é carregado automaticamente via URL

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lippe-guimaraes/mvp-heart-disease/blob/main/mvp_heart_disease.ipynb)

---

## Modelos Avaliados

| Modelo | Papel |
|---|---|
| DummyClassifier | Baseline — referência mínima |
| Logistic Regression | Modelo linear, interpretável |
| K-Nearest Neighbors | Baseado em distância |
| Decision Tree | Árvore de decisão simples |
| Random Forest | Ensemble de árvores (melhor resultado) |
| Gradient Boosting | Boosting sequencial |

O **Random Forest com hiperparâmetros otimizados** (RandomizedSearchCV) foi o modelo final escolhido, com base no melhor equilíbrio entre F1-Score e Recall no conjunto de teste.

---

## Métricas Utilizadas

- Acurácia, Precisão, Recall, F1-Score, AUC-ROC
- Matriz de Confusão
- Análise de Overfitting (CV treino × teste)
- Análise de Falsos Negativos (críticos em diagnóstico médico)

---

## Bibliotecas

```
pandas · numpy · matplotlib · seaborn · scikit-learn
```
