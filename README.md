# 📊 Previsão de Churn com Framework SEMMA

Projeto desenvolvido para a disciplina de **Aprendizado de Máquina** com o objetivo de construir um modelo preditivo capaz de identificar usuários com alta probabilidade de evasão (**Churn**).

O diferencial deste projeto é a aplicação estruturada do framework analítico **SEMMA** (*Sample, Explore, Modify, Model, Assess*), garantindo boas práticas de ciência de dados desde a separação temporal das amostras até a avaliação de impacto no negócio.

---

# 🎯 Objetivo do Projeto

Desenvolver um pipeline de Machine Learning capaz de:

* Identificar clientes com maior risco de cancelamento;
* Minimizar problemas de *data leakage*;
* Validar estabilidade temporal utilizando uma base *Out-of-Time* (OOT);
* Avaliar o impacto do modelo tanto por métricas técnicas quanto por métricas de negócio.

---

# 📂 Base de Dados

Dataset utilizado:

https://www.kaggle.com/datasets/teocalvo/analytical-base-table-churn/data?utm_source=chatgpt.com

---

# 🛠️ Tecnologias Utilizadas

## Linguagem

* Python

## Manipulação e Análise de Dados

* Pandas
* NumPy

## Machine Learning

* Scikit-Learn

  * Pipelines
  * RandomForestClassifier
  * GridSearchCV
  * Train/Test Split
  * Métricas de avaliação

## Engenharia de Atributos

* Feature-engine

## Visualização de Dados

* Matplotlib
* Seaborn

---

# 🧠 Metodologia: Framework SEMMA

O projeto foi desenvolvido seguindo rigorosamente as cinco etapas do framework SEMMA:

## 1. Sample (Amostragem)

* Separação da safra mais recente como base **Out-of-Time (OOT)**;
* Divisão dos dados restantes em treino e teste;
* Estratificação da variável alvo para manter a distribuição de churn entre as amostras.

## 2. Explore (Exploração)

* Verificação de qualidade dos dados;
* Análise bivariada entre clientes que deram churn e clientes que permaneceram;
* Avaliação inicial de importância das variáveis utilizando Árvore de Decisão.

## 3. Modify (Modificação)

* Discretização (*binning*) de variáveis contínuas;
* Aplicação de *One-Hot Encoding*;
* Construção de pipelines para garantir consistência nas transformações e evitar *data leakage*.

## 4. Model (Modelagem)

* Treinamento de modelo Random Forest;
* Otimização de hiperparâmetros com GridSearchCV;
* Validação cruzada (*Cross Validation*) para maior robustez.

## 5. Assess (Avaliação)

* Avaliação utilizando:

  * ROC AUC
  * Acurácia
* Comparação de desempenho entre:

  * Treino
  * Teste
  * Out-of-Time (OOT)
* Análise de negócio utilizando curvas de Lift/Gains;
* Serialização do modelo final em arquivo `.pkl`.

---

# 📈 Resultados e Impacto de Negócio

O modelo demonstrou ganho significativo em relação a uma abordagem aleatória, permitindo identificar clientes com maior probabilidade de churn de forma eficiente.

Principais resultados observados:

* O modelo apresentou desempenho consistente entre treino, teste e base OOT;
* A estratégia baseada em score preditivo aumentou significativamente a eficiência das campanhas de retenção;
* Ao focar apenas os clientes classificados com maior risco, foi possível capturar uma parcela relevante dos churners totais;
* O modelo permite direcionar ações de retenção de forma mais estratégica, reduzindo desperdício de orçamento e aumentando o potencial de ROI.

---

# 🚀 Instalação e Execução

## 1. Clone o repositório

```bash
git clone https://github.com/RafaelHenriqueMM/Previsao_de_Churn_com_Framework_SEMMA.git
```

## 2. Acesse a pasta do projeto

```bash
cd Previsao_de_Churn_com_Framework_SEMMA
```

## 3. Crie um ambiente virtual

```bash
python -m venv venv
```

## 4. Ative o ambiente virtual

### Windows

```bash
venv\Scripts\activate
```

### Linux/macOS

```bash
source venv/bin/activate
```

## 5. Instale as dependências

```bash
pip install -r requirements.txt
```
---

# 📌 Conclusão

Este projeto demonstra a aplicação prática de técnicas de Machine Learning orientadas a negócio, utilizando boas práticas de modelagem, engenharia de atributos e validação temporal.

Além do foco técnico, o trabalho busca evidenciar como modelos preditivos podem gerar impacto real em estratégias de retenção de clientes.
