# Análise de Churn de Clientes: Telecom

🇺🇸 [Click here for English version](README.md)

## 📌 Visão Geral
Este projeto prevê a rotatividade de clientes (churn) em uma empresa de telecomunicações. O objetivo é identificar clientes com alto risco de saída para que a empresa possa agir preventivamente.



## 📊 Os Dados
O dataset contém **7.043 clientes** e 21 variáveis, cobrindo:
* **Demografia:** Gênero, idosos, dependentes.
* **Serviços:** Fibra óptica, suporte técnico, streaming, etc.
* **Conta:** Tempo de contrato (tenure), tipo de contrato e cobranças.

## 🛠️ Fluxo de Trabalho
1. **Tratamento de Dados:** Limpeza de valores nulos e aplicação de **One-Hot Encoding**.
2. **EDA:** Clientes com **contratos mensais** e **Fibra Óptica** são os que mais cancelam.
3. **Modelagem:** Comparação entre **Regressão Logística** e **Random Forest** (hiperparâmetros padrão).

## 📈 Resultados

| Modelo | Score AUC | Conclusão |
| :--- | :---: | :--- |
| **Regressão Logística** | **0.84** | Melhor performance e fácil de explicar ao negócio. |
| **Random Forest** | **0.82** | Ótimo para capturar padrões complexos. |



## 💡 Insights de Negócio
* **Fidelização:** Incentivar a migração de planos mensais para anuais.
* **Onboarding:** Focar no sucesso do cliente nos primeiros 6 meses.
* **Suporte:** Clientes sem Suporte Técnico têm maior propensão ao churn.
