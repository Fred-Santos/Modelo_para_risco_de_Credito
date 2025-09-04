# Modelo de Risco de Crédito — ETL e Modelagem com PySpark

Este projeto tem como objetivo **construir um modelo preditivo de risco de crédito**, abordando desde a etapa de engenharia de dados até a criação do modelo final.  
O foco principal é estruturar um **pipeline de ETL** utilizando PySpark, consolidar as variáveis em uma tabela única e treinar algoritmos de machine learning para prever o risco de crédito (*behavior model*).  

---

## 📊 Fonte dos Dados
Os dados são provenientes da competição [Home Credit - Credit Risk Model Stability](https://www.kaggle.com/competitions/home-credit-credit-risk-model-stability/data).  

> ⚠️ Os datasets **não estão versionados no GitHub** devido ao tamanho (>100MB).  
> Para reproduzir os experimentos, baixe os arquivos pelo Kaggle e extraia-os em `data/raw/`.

---

## 🛠️ Etapas do Projeto

### 1. Engenharia de Dados (ETL)
- **Leitura** dos dados brutos com PySpark (`data/raw/`)
- **Limpeza e tratamento**: remoção de nulos, normalização de colunas e casts de tipos
- **Enriquecimento**: criação de novas variáveis derivadas
- **Unificação** das tabelas em uma estrutura consolidada para treino do modelo

### 2. Modelagem
- Construção de modelos de classificação para risco de crédito
- Teste de diferentes algoritmos de ML
- Avaliação de desempenho com métricas como **AUC**, **KS**, **precisão**, **recall** e **F1**

### 3. Relatórios e Documentação
- `notebooks/etl_pipeline.ipynb`: orquestra o processo de ETL
- `docs/report.md`: resumo dos experimentos e principais resultados
- `docs/data_dictionary.md`: definição final das variáveis utilizadas

---

## 📂 Estrutura do Repositório
```bash
repo/
├── data/
│   ├── raw/        # dados brutos (não versionados no GitHub)
│   ├── interim/    # dados intermediários
│   └── processed/  # dados finais prontos para análise/modelagem
├── notebooks/
│   └── etl_pipeline.ipynb   # notebook principal do ETL
├── src/
│   └── etl/        # scripts de apoio (ingestão, transformações, utils)
├── docs/
│   ├── report.md
│   └── data_dictionary.md
├── requirements.txt
├── .gitignore
└── README.md

```

### 🚀 Como Rodar Localmente

## Clonar este repositório:

git clone https://github.com/Fred-Santos/Modelo_para_risco_de_Credito.git
cd Modelo_para_risco_de_Credito


## Criar um ambiente virtual e instalar dependências:

python -m venv .venv
.venv\Scripts\activate  # Windows
pip install -r requirements.txt


Baixar os dados no Kaggle e extraí-los em data/raw/.

Iniciar o Jupyter Lab:

jupyter lab


## Executar o notebook principal:

Abra notebooks/etl_pipeline.ipynb

Execute as células em sequência para rodar o ETL completo
