# Projeto ETL Local (PySpark)

Este repositório organiza um ETL simples usando **PySpark** e **notebooks** rodando localmente.

## Objetivo
- Ingerir dados do **Kaggle** (ou já existentes em `data/raw/`)
- Aplicar transformações básicas
- Gerar saídas em `data/processed/`
- Entregar: **notebook do ETL** + **datasets prontos** + **relatório** (`docs/`)

## Requisitos
- **Python 3.10+**
- **Java JDK 8/11/17** instalado e `JAVA_HOME` configurado
- Pacotes Python: `pyspark`, `jupyterlab`

### Instalação rápida (opcional, usando venv)
```bash
python3 -m venv .venv
source .venv/bin/activate   # Windows: .venv\\Scripts\\activate
pip install -U pip
pip install pyspark jupyterlab pandas

## Estrutura
repo/
├─ data/
│  ├─ raw/        # dados brutos (ex.: dump do Kaggle)
│  ├─ interim/    # dados intermediários (temporários)
│  └─ processed/  # saídas finais prontas para análise/modelagem
├─ notebooks/
│  └─ etl_pipeline.ipynb   # notebook principal (orquestra ingest/transform)
├─ src/
│  └─ etl/
│     ├─ __init__.py
│     ├─ ingest.py         # leitura/normalização
│     ├─ transform.py      # limpezas/joins/enriquecimentos
│     └─ utils.py          # utilitários (SparkSession, paths)
└─ docs/
   ├─ report.md            # relatório final
   └─ data_dictionary.md   # dicionário de dados
   