# Projeto Integrador Interdisciplinar II — Terra Signal

Solução integrada para estruturar, processar, armazenar e analisar os dados de clientes da Terra Signal (empresa fictícia de telecomunicações), usando a Arquitetura Medalhão e análise exploratória.

## Estrutura do repositório

```
bases/
  history.csv                     # camada Bronze: base oficial do professor (não alterar)
  silver/
    base_silver.csv               # camada Silver: base tratada e validada (gerada pelo notebook 02)
docs/
  dicionario_dados.csv            # dicionário de dados atualizado (Silver)
  relatorio_qualidade_bronze_silver.csv  # indicadores de qualidade Bronze x Silver
  registro_tratamentos.csv        # tratamentos aplicados, justificativas e impactos
notebooks/
  01_exploracao_inicial.ipynb     # Semanas 1–2: exploração, qualidade e dicionário de dados
  02_tratamento_silver.ipynb      # Semana 3: tratamento e validação da camada Silver
requirements.txt                  # bibliotecas Python utilizadas
```

Os arquivos de `bases/silver/` e `docs/` são gerados ao executar o notebook 02. Para ler a Silver mantendo `tenure` como inteiro com nulos, use `pd.read_csv(caminho, dtype={"tenure": "Int64"})`.

## Como executar

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux / Mac
source .venv/bin/activate

pip install -r requirements.txt
```

Abra os notebooks da pasta `notebooks/` no VS Code ou Jupyter, selecione o kernel do `.venv` e execute todas as células, em ordem (01 e depois 02). Os notebooks leem a base pelo caminho relativo `../bases/history.csv`.

## Etapas do projeto

| Semana | Etapa | Status |
|---|---|---|
| 01–02 | Conhecimento dos dados, qualidade e dicionário | Finalizado |
| 03 | Processamento e Arquitetura Medalhão | Em andamento |
| 04 | Armazenamento e consultas SQL | Pendente |
| 05–06 | Análise exploratória e relações com o cancelamento | Pendente |
| 07 | Integração, documentação e revisão | Pendente |
| 08 | Apresentação final | Pendente |

## Fluxo de branches

- `main`: versão estável, revisada pelo trio.
- `develop`: integração do trabalho em andamento.
- `feature/<descricao>`: uma branch por tarefa (ex.: `feature/etapa1-exploracao`), aberta a partir de `develop` e integrada via Pull Request.
