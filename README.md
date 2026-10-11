# ClearBank – Análise de Transações

Projeto do desafio final do módulo de Python aplicado à análise de dados.

O notebook lê o arquivo "transacoes.csv" de uma fintech fictícia (ClearBank), valida e limpa os dados, calcula métricas financeiras mensais, sinaliza transações suspeitas, exibe um relatório formatado e salva o resultado em "relatorio.json".

## Arquivos do repositório

| Arquivo | Descrição |
| "desafio-final.ipynb" | Notebook com o código e as saídas salvas |
| "transacoes.csv" | Arquivo de entrada de exemplo (25 linhas: 20 válidas e 5 inválidas) |
| "README.md" | Arquivo de orientação de aplicação |

## Como executar

### Google Colab

1. Acesse [colab.research.google.com](https://colab.research.google.com) e abra o menu **Arquivo → Fazer upload de notebook**, selecionando "desafio-final.ipynb".
2. Envie o arquivo "transacoes.csv" para o Colab pelo painel de arquivos (ícone de pasta à esquerda).
3. Execute todas as células em ordem: **Ambiente de execução → Executar tudo**.

### Jupyter Notebook local

1. Tenha o Python 3.10 ou superior instalado e execute "pip install notebook".
2. Coloque "desafio-final.ipynb" e "transacoes.csv" na mesma pasta.
3. Rode "jupyter notebook", abra o notebook e execute todas as células em ordem.

## O que o notebook gera

- **Resumo da limpeza:** total de linhas lidas, válidas e inválidas.
- **Relatório mensal no terminal:** quantidade de transações, total de crédito, total de débito, saldo, valor médio, maior e menor valor de cada mês, além do período analisado.
- **Transações suspeitas:** lista das transações com valor acima de R$ 10.000,00.
- **"relatorio.json":** relatório completo da análise, salvo ao executar a célula principal.

## Validações aplicadas

As linhas com "id" vazio ou não numérico, "cliente_id" vazio, data fora do formato AAAA-MM-DD, "tipo" diferente de "credito" ou "debito", ou "valor" não numérico ou menor ou igual a zero são descartadas sem interromper o programa.

## Tecnologias

Python 3.10+ com os módulos nativos "csv", "json" e "datetime".
