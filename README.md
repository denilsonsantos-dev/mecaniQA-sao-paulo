# MecâniQA - Módulo Fundacional de Análise

Este repositório contém o desenvolvimento de um projeto acadêmico da disciplina **Modelos de Aprendizado de Máquina**.

A proposta consiste em atuar como a equipe de Ciência de Dados da **MecâniQA**, uma empresa fictícia que desenvolve soluções preditivas para oficinas mecânicas e auto centers. O projeto terá como foco a construção do módulo fundacional de análise de dados da plataforma, buscando compreender o histórico de manutenções automotivas e estabelecer uma base para futuras soluções preditivas.

O problema de negócio consiste na ocorrência de picos inesperados na demanda por manutenções preventivas, que podem ocasionar falta de peças em estoque em determinados períodos, ociosidade da equipe de mecânicos em outros momentos e dificuldades no planejamento operacional das oficinas.

## Estrutura do repositório

A organização atual do projeto separa os dados, notebooks e código-fonte, mantendo na raiz apenas os arquivos relacionados à configuração e à visão geral do projeto.

```text
mecaniqa-projeto/
├── data/
│   ├── raw/
│   │   └── dataset.csv              # dataset original, sem alterações
│   └── processed/                   # dados tratados e transformados
├── notebooks/
│   └── 01_exploracao_inicial.ipynb  # exploração inicial da base
├── src/                             # código-fonte reutilizável
├── requirements.txt                 # dependências do projeto
├── .gitignore
└── README.md
```

### Por que separar os dados em `raw/` e `processed/`?

A pasta `data/raw/` mantém o dataset original exatamente como foi recebido. A ideia é evitar alterações diretas no dado de origem, permitindo que qualquer tratamento ou transformação produza uma nova versão em `data/processed/`.

Essa separação também mantém o caminho do dataset original estável (`data/raw/dataset.csv`), independentemente das versões tratadas que forem produzidas durante o projeto.

### Papel dos notebooks

Os notebooks em `notebooks/` são utilizados para exploração e análise durante o desenvolvimento. O primeiro notebook, `01_exploracao_inicial.ipynb`, concentra a importação do dataset, a indexação temporal e a inspeção inicial da base.

À medida que o projeto evoluir, funções e partes reutilizáveis da lógica de análise poderão ser extraídas para `src/`, deixando os notebooks mais focados na experimentação e na apresentação dos resultados.

## Objetivos

Durante o desenvolvimento do projeto, serão realizadas as seguintes atividades:

- Modelagem dos dados históricos de manutenção;
- Limpeza e tratamento dos dados temporais;
- Análise dos registros de:
  - Trocas de óleo;
  - Manutenções de motor;
- Implementação de um modelo de previsão **Baseline**, utilizando regras simples como referência para futuras soluções mais avançadas.

## Equipe

**Nome do Time:** `SÃO PAULO`

| Integrante |
|------------|
| Denilson Santos da Silva |
| Gabriel Arlisson de Souza Santos Torres |
| João Arthur Nascimento Mascarenhas |
| Tony Cleriston Oliveira dos Santos Junior |
| Vinicius Cerqueira Oliveira |

## Como executar o notebook

Crie um ambiente virtual, instale as dependências e abra o notebook:

```bash
python -m venv .venv
source .venv/bin/activate  # no Windows: .venv\Scripts\activate

pip install -r requirements.txt

jupyter notebook notebooks/01_exploracao_inicial.ipynb
```
