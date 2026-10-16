# Projeto Integrador Interdisciplinar II — Terra Signal

Solução integrada para estruturar, processar, armazenar e analisar os dados de clientes da Terra Signal (empresa fictícia de telecomunicações), usando a Arquitetura Medalhão e análise exploratória.

## Estrutura do repositório

```
bases/
  history.csv                     # base oficial fornecida pelo professor (não alterar)
notebooks/
  01_exploracao_inicial.ipynb     # Etapa 1: exploração, qualidade e dicionário de dados
requirements.txt                  # bibliotecas Python utilizadas
```

## Como executar

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux / Mac
source .venv/bin/activate

pip install -r requirements.txt
```

Abra `notebooks/01_exploracao_inicial.ipynb` no VS Code ou Jupyter, selecione o kernel do `.venv` e execute todas as células. O notebook lê a base pelo caminho relativo `../bases/history.csv`.

## Etapas do projeto

| Semana | Etapa | Status |
|---|---|---|
| 01–02 | Conhecimento dos dados, qualidade e dicionário | Em andamento |
| 03 | Processamento e Arquitetura Medalhão | Pendente |
| 04 | Armazenamento e consultas SQL | Pendente |
| 05–06 | Análise exploratória e relações com o cancelamento | Pendente |
| 07 | Integração, documentação e revisão | Pendente |
| 08 | Apresentação final | Pendente |

## Fluxo de branches

- `main`: versão estável, revisada pelo trio.
- `develop`: integração do trabalho em andamento.
- `feature/<descricao>`: uma branch por tarefa (ex.: `feature/etapa1-exploracao`), aberta a partir de `develop` e integrada via Pull Request.
