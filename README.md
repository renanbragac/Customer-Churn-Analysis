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

## 📈 Resultados e Comparação
Avaliei os modelos utilizando a métrica **AUC-ROC**:

| Modelo | Score AUC | Principal Conclusão |
| :--- | :---: | :--- |
| **Regressão Logística** | **0.84** | Melhor performance geral e alta interpretabilidade. |
| **Random Forest** | **0.82** | Útil para identificar padrões não-lineares complexos. |



## 💡 Insights de Negócio
* **Fidelização:** Incentivar a migração de planos mensais para contratos anuais.
* **Onboarding:** Focar no sucesso do cliente nos primeiros 6 meses de contrato.
* **Venda Cruzada:** Clientes sem Suporte Técnico cancelam com mais frequência; oferecer esse serviço pode aumentar a retenção.
