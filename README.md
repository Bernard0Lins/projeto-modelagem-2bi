# Projeto de Modelagem Estatística - Previsão de Custos Médicos

Este repositório contém o projeto avaliativo do 2º Bimestre da disciplina de **Modelagem Estatística**, ministrada pelo Prof. Pedro Girotto.

O objetivo principal é aplicar técnicas de Ciência de Dados para analisar um dataset de seguros de saúde, realizando limpeza de dados, análise exploratória (EDA), testes de hipótese e construção de modelos preditivos (Regressão e Classificação).


##  Sobre os Dados

O dataset utilizado é o **Medical Cost Personal Datasets**, disponibilizado originalmente para acompanhar o livro *Machine Learning with R* de Brett Lantz.

* **Fonte:** [Kaggle - Medical Cost Personal Datasets](https://www.kaggle.com/mirichoi0218/insurance)
* **Licença:** Database Contents License (DbCL) v1.0 / Domínio Público.
* **Dimensões:** 1338 linhas e 7 colunas.

### Dicionário de Variáveis:
* `age`: Idade do beneficiário principal.
* `sex`: Gênero (male/female).
* `bmi`: Índice de Massa Corporal (IMC).
* `children`: Número de filhos/dependentes cobertos pelo plano.
* `smoker`: Se é fumante (yes/no).
* `region`: Região residencial nos EUA (northeast, southeast, southwest, northwest).
* `charges`: Custos médicos individuais cobrados pelo seguro (Variável Alvo da Regressão).


## Metodologia e Etapas

[cite_start]O projeto foi desenvolvido em Python (Jupyter Notebook) seguindo o pipeline abaixo:

1.  **Análise Exploratória (EDA):**
    * Visualização de distribuições (Histogramas e Boxplots).
    * Testes de Hipótese (Teste T) para validar impacto do tabagismo nos custos.
    * Matriz de correlação e análise multivariada.
2.  **Pré-processamento:**
    * Tratamento de duplicatas.
    * Encoding de variáveis categóricas (One-Hot Encoding).
    * Definição de Baseline (Dummy Regressor).
3.  **Modelagem (Regressão):**
    * Objetivo: Prever a variável `charges`.
    * Modelos: Regressão Linear Múltipla (Statsmodels), Regressão Polinomial e Random Forest.
    * Avaliação: RMSE, MAE, R² e Diagnóstico de Resíduos.
4.  **Modelagem (Classificação):**
    * Objetivo: Prever a variável `smoker` (Detecção de risco).
    * Modelos: Regressão Logística e Naive Bayes (Gaussian).
    * Avaliação: Curva ROC, AUC e Matriz de Confusão.
5.  **Otimização:**
    * Tuning de hiperparâmetros utilizando `GridSearchCV` para o modelo Random Forest.


## Como Executar o Projeto

### Pré-requisitos
* Python 3.11 instalado.
* Git instalado.

### Instalação

1.  Clone o repositório:
    ```bash
    git clone [https://github.com/SEU_USUARIO/projeto-modelagem-2bi.git]
    ```
2.  Entre na pasta do projeto:
    ```bash
    cd projeto-modelagem-2bi
    ```
3.  Instale as dependências listadas no `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```

### Execução
Abra o arquivo `main.ipynb` no VS Code ou Jupyter Lab e execute as células sequencialmente.

---

## 📂 Organização do Repositório

```text
📁 projeto-modelagem-2bi
├── 📄 main.ipynb   
├── 📄 requirements.txt        
└── 📄 README.md                
