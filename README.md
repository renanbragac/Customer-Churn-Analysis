# Análise de Churn de Clientes: Setor de Telecomunicações

🇺🇸 [Click here for the English version](README_EN.md)

## 📌 Visão Geral do Projeto
Este projeto tem como objetivo prever a rotatividade de clientes (churn) em uma empresa de telecomunicações. Ao identificar clientes com alto risco de cancelamento, a empresa pode agir preventivamente para melhorar a retenção e proteger o faturamento mensal.



## 📊 Os Dados
O conjunto de dados consiste em **7.043 clientes** com 21 variáveis, incluindo:
* **Demografia:** Gênero, idosos, parceiros e dependentes.
* **Serviços:** Internet (Fibra óptica/DSL), suporte técnico, segurança online, etc.
* **Informações da Conta:** Tempo de contrato (tenure), tipo de contrato e cobranças mensais.

## 🛠️ Fluxo de Trabalho Técnico
1. **Tratamento de Dados:** Limpeza de valores ausentes e aplicação de **One-Hot Encoding** em variáveis categóricas.
2. **Análise Exploratória (EDA):** Identificamos que clientes com **contratos mensais** e serviço de **Fibra Óptica** possuem taxas de churn significativamente mais altas.
3. **Modelagem:** Comparação entre **Regressão Logística** e **Random Forest** utilizando hiperparâmetros padrão para estabelecer um baseline.

# 🧪 Análise de Performance: Random Forest vs. Regressão Logística

Nesta etapa, comparamos os dois modelos utilizando o Score AUC e a **Matriz de Confusão** para entender onde cada modelo está falhando.


## 1. 📈 Resultados e Comparação
Avaliei os modelos utilizando a métrica **AUC-ROC**:

| Modelo | Score AUC | Principal Conclusão |
| :--- | :---: | :--- |
| **Regressão Logística** | **0.84** | Melhor performance geral e alta interpretabilidade. |
| **Random Forest** | **0.82** | Útil para identificar padrões não-lineares complexos. |

---

## 2. Matrizes de Confusão

| Modelo | Verdadeiros Negativos (0) | Falsos Positivos (Erro tipo I) | Falsos Negativos (Erro tipo II) | Verdadeiros Positivos (1) |
| :--- | :---: | :---: | :---: | :---: |
| **Random Forest** | 743 | 79 | 154 | 151 |
| **Logistic Regression** | 602 | 220 | 64 | 241 |

---

## 3. Insights

Ao analisar os dados acima, é possível perceber comportamentos distintos:

### 🌲 Random Forest
* **Alta Precisão:** O modelo é cauteloso e raramente dá alarmes falsos (**79 FPs**).
* **Baixo Recall:** Ele deixa passar muitos casos reais (**154 FNs**).

### 📈 Regressão Logística
* **Alto Recall:** Captura a maioria dos positivos (**241**), errando apenas 64.
* **Baixa Precisão:** Gera muitos alarmes falsos (**220**).

---

## 🛠️ Conclusão e Próximos Passos

É possível notar que **os modelos ainda não estão perfeitos**. Os resultados atuais servem como uma base inicial e apresentam desequilíbrios entre precisão e recall.

Para elevar a performance, as próximas etapas do projeto provavelmente devem incluir:
1. **Fine-Tuning de Hiperparâmetros**
2. **Feature Engineering**
3. **Ajustes de Threshold**
