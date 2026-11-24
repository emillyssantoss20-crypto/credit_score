# MVP — Análise de Dados e Boas Práticas: Classificação de Score de Crédito

Análise exploratória e pré-processamento de uma base de dados de crédito de clientes, desenvolvidos como MVP da disciplina **Análise de Dados e Boas Práticas** (Pós-graduação PUC-Rio).

O trabalho termina na preparação dos dados: não há treinamento nem comparação de modelos de aprendizado de máquina.

## Notebook

- **Google Colab:** [<link do Colab>](https://colab.research.google.com/drive/13bq6nxKTj4U0XGQPIbfYbt0QqNoFdS5C?usp=sharing)
- **Arquivo neste repositório:** `<nome-do-notebook>.ipynb`

## Objetivo

<Descrever em 2–3 frases o problema e o objetivo analítico.>

Perguntas investigadas:

- **H1:** <pergunta 1>
- **H2:** <pergunta 2>

## Dados

| Item | Descrição |
|---|---|
| Base | Credit Score Classification |
| Autor | Rohan Paris |
| Fonte | [Kaggle](https://www.kaggle.com/datasets/parisrohan/credit-score-classification) |
| Licença | CC0: Public Domain |
| Data de obtenção | 20/11/2026 |
| Arquivo original usado | `train.csv` (100.000 linhas × 28 colunas) |
| Arquivo neste repositório | `credit_score_train.csv.gz` (100.000 linhas × 26 colunas) |
| Unidade de observação | um cliente em um mês (12.500 clientes × 8 meses, de janeiro a agosto) |
| Alvo | `Credit_Score` (Good, Standard, Poor) |

### Alterações feitas antes da publicação

- Remoção das colunas `Name` e `SSN`, por serem identificadores pessoais sem uso analítico. O cliente continua identificado por `Customer_ID`.
- Uso apenas do `train.csv`; o `test.csv` foi descartado porque não contém a coluna alvo.
- Compactação em gzip para respeitar o limite de upload de arquivos do GitHub pelo navegador. O conteúdo é idêntico ao CSV sem compactação.

Todas as demais colunas e valores estão exatamente como no arquivo original. As limpezas e transformações estão documentadas no notebook.

## Como executar

1. Abra o notebook pelo link do Colab acima.
2. Clique em **Ambiente de execução → Executar tudo**.

Os dados são carregados diretamente deste repositório, sem necessidade de upload ou de conta pessoal:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/<usuario>/<repositorio>/main/credit_score_train.csv.gz"
df = pd.read_csv(url)
```

## Dependências

| Biblioteca | Versão |
|---|---|
| Python | <versão> |
| pandas | <versão> |
| numpy | <versão> |
| matplotlib | <versão> |
| seaborn | <versão> |

As versões correspondem ao ambiente do Google Colab usado na execução final (ver seção 3 do notebook).

## Estrutura do repositório

```
├── README.md
├── <nome-do-notebook>.ipynb
└── credit_score_train.csv.gz
```

## Autora

Emilly Santos — matrícula <matrícula>
