# ML na Cloud

Materiais práticos da disciplina **Desenvolvimento de ML na Cloud**, com exemplos de treinamento, avaliação e operacionalização de modelos de machine learning.

## Conteúdo

### Aula 1

Introdução aos fundamentos de machine learning e ao uso de recursos de nuvem. A pasta também contém três diagramas em imagens `.jpg` e suas versões editáveis em Mermaid (`.mmd`), além do arquivo original do Draw.io.

### Aula 2

Exemplos introdutórios de uso do Azure Machine Learning:

- `ola_mundo.ipynb`: primeiro contato com o ambiente.
- `modelo_azure.ipynb`: exploração de um modelo no Azure.
- `treinamento.py`: treinamento distribuído de uma rede neural convolucional para classificação do dataset MNIST, com acompanhamento pelo MLflow.

### Aula 3

Exemplos de fluxos mais completos de machine learning:

- `automl/automl.ipynb`: experimento de AutoML.
- `mnist/mnist.ipynb` e `mnist.py`: treinamento do modelo MNIST.
- `hyperparam_tuning/analise_sent.py`: análise de sentimentos com `CountVectorizer`, `RandomForestClassifier`, métricas de classificação e registro no MLflow.
- `hyperparam_tuning/analise_sent.ipynb`: versão em notebook do experimento de análise de sentimentos.
- `dados-emprestimo/`: dataset e configuração `MLTable` para experimentos de aprovação de empréstimos.
- `sentiment_analysis_dataset/`: dataset utilizado nos experimentos de análise de sentimentos.

## Pré-requisitos

Para executar os notebooks e scripts, é recomendado ter:

- Python 3.8 ou superior;
- Jupyter Notebook ou Visual Studio Code com suporte a notebooks;
- acesso a um workspace do Azure Machine Learning para os exemplos em nuvem;
- dependências de Python usadas pelos exemplos, como `pandas`, `scikit-learn`, `tensorflow` e `mlflow`.

Os notebooks podem exigir configurações adicionais de autenticação, workspace, compute e armazenamento no Azure. Consulte as células de configuração de cada notebook antes da execução.

## Execução de scripts

Os scripts que recebem um dataset por argumento seguem o formato:

```bash
python Aula\ 3/hyperparam_tuning/analise_sent.py --dataset caminho/para/dataset.csv
```

O script de ajuste de hiperparâmetros também aceita opções como `--n-estimators` e `--criterion`:

```bash
python Aula\ 3/hyperparam_tuning/analise_sent.py \
	--dataset Aula\ 3/sentiment_analysis_dataset/dataset.csv \
	--n-estimators 10 \
	--criterion entropy
```

## Dados

- [Dataset de aprovação de empréstimos](https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset)
- [Dataset de análise de sentimentos](https://github.com/lucolivi/sentiment_analysis_dataset/raw/main/dataset.csv)
- [Dataset original de análise de sentimentos](https://www.kaggle.com/datasets/abhi8923shriv/sentiment-analysis-dataset/data)
