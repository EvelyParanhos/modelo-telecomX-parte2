# Previsão de Churn de Clientes na Telecom X

## 🚀 Visão Geral do Projeto
Este projeto é a segunda fase de um trabalho de análise de dados sobre a evasão de clientes (churn) da Telecom X. Após a conclusão da Análise Exploratória de Dados (EDA) que identificou os principais fatores de risco, o foco deste repositório é a construção de um pipeline de Machine Learning robusto. O objetivo é desenvolver um modelo preditivo capaz de prever quais clientes têm maior probabilidade de churn, fornecendo uma ferramenta essencial para a proatividade da empresa em estratégias de retenção.

## 🎯 Objetivos do Projeto
* **Preparar os Dados:** Realizar o pré-processamento necessário para a modelagem, incluindo codificação, padronização e balanceamento de classes.
* **Construir Modelos:** Treinar e comparar a performance de dois modelos de classificação: Regressão Logística e Random Forest.
* **Avaliar e Selecionar o Modelo:** Utilizar **validação cruzada (k-fold)** e métricas como F1-Score para escolher o modelo mais confiável e estável.
* **Interpretar Resultados:** Analisar os fatores mais relevantes para a previsão de churn, extraindo insights acionáveis do modelo escolhido.

## ⚙️ Metodologia e Pipeline de Machine Learning

O pipeline de ML foi desenvolvido seguindo as melhores práticas:

1.  **Pré-processamento de Dados:**
    * **Codificação e Padronização:** Variáveis categóricas foram codificadas com **One-Hot Encoding**, enquanto as variáveis numéricas foram padronizadas com **StandardScaler** para otimizar o desempenho de modelos como a Regressão Logística.
    * **Balanceamento de Classes:** A técnica **SMOTE** foi aplicada no conjunto de dados para corrigir o desequilíbrio entre as classes de churn e não-churn, que era de aproximadamente 73% vs. 27%.

2.  **Modelagem e Avaliação:**
    * Foram treinados dois modelos de classificação: a **Regressão Logística** e o **Random Forest**.
    * A performance foi avaliada através da **validação cruzada (k=5)**, usando o **F1-Score** como métrica principal para obter uma estimativa de desempenho mais confiável.

## 📊 Principais Descobertas e Performance do Modelo

A Regressão Logística foi escolhida como o modelo final devido à sua **estabilidade e alta interpretabilidade**, que são mais valiosas para a tomada de decisões de negócio do que uma performance ligeiramente maior, mas instável.

* **Performance do Modelo Escolhido (Regressão Logística):**
    * **F1-Score Médio (Validação Cruzada):** `0.778`
    * **Estabilidade (Desvio Padrão):** `0.008` (Um valor extremamente baixo, que demonstra consistência)

### Fatores de Maior Impacto na Previsão de Churn (Análise dos Coeficientes):

* **Fatores que Reduzem o Churn:**
    * **Tempo de Cliente (`tenure`):** O fator mais forte para a retenção.
    * **Contrato de Longo Prazo:** Contratos de 2 anos e 1 ano.
    * **Serviços Agregados:** Adesão a **Suporte Técnico** e **Segurança Online**.
* **Fatores que Aumentam o Churn:**
    * **Contrato Mês a Mês:** O principal fator de risco.
    * **Serviço de Internet Fibra Óptica:** A presença deste serviço é um forte preditor de churn.
    * **Método de Pagamento:** O uso de **Cheque Eletrônico**.

## 💡 Recomendações Estratégicas Baseadas no Modelo

1.  **Foco nos Primeiros Meses:** Criar estratégias de suporte e engajamento intensivo para clientes nos primeiros 6 meses de contrato.
2.  **Otimizar a Experiência com Fibra Óptica:** Realizar uma análise de causa-raiz para os problemas associados a este serviço, que se mostrou um forte preditor de churn.
3.  **Incentivar Contratos Longos:** Desenvolver ofertas e benefícios para migrar clientes de planos mensais para contratos anuais ou bienais.

## 🛠️ Tecnologias Utilizadas
* **Python:** Linguagem principal.
* **Pandas:** Manipulação de dados.
* **Scikit-learn:** Pré-processamento, modelagem e avaliação.
* **Imbalanced-learn:** Balanceamento de classes (SMOTE).
* **Matplotlib, Seaborn & Plotly:** Visualização de dados.
