# 🚔 Desafio SQL — Acidentes nas Rodovias Federais (PRF 2007–2024)

> Dados públicos disponibilizados pela **Polícia Rodoviária Federal (PRF)**, convertidos para formato **Parquet** e prontos para análise.

---

## 📦 Ponto de Partida

Os dados já foram extraídos e transformados em arquivos **Parquet**. Você pode encontrá-los na pasta `data/dados_acidentes_prf` dentro deste repositório. Sua primeira tarefa é **carregá-los em um banco SQL** para responder às perguntas abaixo.

### Opções recomendadas

|Ferramenta|Como usar|
|---|---|
|**DuckDB**|`COPY accidents FROM 'data/dados_acidentes_prf/*.parquet' (FORMAT PARQUET);`|
|**SQLite**|Converta via `pandas` + `df.to_sql(...)`|
|**PostgreSQL**|Use `COPY` ou extensão `parquet_fdw`|

> 💡 **DuckDB é a escolha recomendada** ,lê Parquet nativamente, sem instalação de servidor, com sintaxe SQL padrão e performance excelente para análise local.

### Exemplo mínimo com DuckDB (Python)

```python
import duckdb

con = duckdb.connect("prf.duckdb")
con.execute("""
    CREATE TABLE acidentes AS
    SELECT * FROM read_parquet('data/dados_acidentes_prf/*.parquet')
""")
```

> 💡 **Dica de Ferramenta e Estudo:** Se achar mais confortável, você pode usar uma IDE de banco de dados como o **DBeaver** para executar seus comandos SQL ao invés do VSCode. Caso tenha dúvidas sobre a linguagem durante o desafio, consulte o tópico de SQL no arquivo [`Introdução aos fundamentos da engenharia de dados.md`](https://github.com/IgorTiburcio81/RoadMap_DataEngineer/blob/main/Introdução%20aos%20fundamentos%20da%20engenharia%20de%20dados.md)

---

## 📋 Dicionário de Dados (referência)

> ⚠️ Verifique os nomes exatos das colunas nos seus arquivos antes de escrever as queries.

|Coluna (esperada)|Descrição|
|---|---|
|`data_inversa`|Data do acidente (YYYY-MM-DD)|
|`ano`|Ano do acidente|
|`uf`|Unidade Federativa|
|`municipio`|Município do acidente|
|`br`|Número da rodovia federal|
|`km`|Quilômetro da rodovia|
|`mortos`|Número de mortos|
|`feridos_leves`|Número de feridos leves|
|`feridos_graves`|Número de feridos graves|
|`ilesos`|Número de ilesos|
|`pessoas`|Total de pessoas envolvidas|
|`tipo_acidente`|Classificação do tipo de acidente|
|`causa_acidente`|Causa principal registrada|
|`condicao_metereologica`|Condição climática no momento|
|`fase_dia`|Período do dia (dia, noite, etc.)|
|`regional`|Regional da PRF|

---

## 🎯 Desafio: Responda as perguntas com SQL

### 1. Visão Geral — KPIs

Responda com uma única query (ou queries separadas) que retornem os seguintes indicadores:

```
1.1 Qual o total de acidentes registrados no período (2007–2024)?

1.2 Qual o total de mortos no período?
    Qual o total de feridos leves?
    Qual o total de feridos graves?
    Qual o total geral de vítimas (mortos + feridos)?

1.3 Qual a média de pessoas envolvidas por acidente?
    Qual a média de mortos por acidente?

1.4 Qual o ano com maior número de acidentes?
    Qual o ano com maior número de mortes?

1.5 Construa a série histórica anual: para cada ano, retorne o total de
    acidentes, total de mortos e total de feridos.
    (Ordene por ano crescente.)
```

---

### 2. Recortes Geográficos

#### Por Estado

```
2.1 Qual estado (UF) teve o maior número de acidentes no período?
    Qual estado teve o maior número de mortes?

2.2 Liste o TOP 10 estados com maior número de acidentes,
    incluindo também o total de mortos de cada um.

2.3 Liste o TOP 10 estados com maior taxa de mortalidade
    (mortos / total de acidentes), considerando apenas estados
    com pelo menos 1.000 acidentes registrados.
```

#### Por Município

```
2.4 Liste o TOP 10 municípios com maior número de acidentes,
    incluindo a UF de cada um.

2.5 Liste o TOP 10 municípios com maior número de mortes,
    incluindo a UF de cada um.
```

#### Por Região

```
2.6 Distribua os acidentes pelas 5 regiões do Brasil:
     Norte, Nordeste, Centro-Oeste, Sudeste e Sul.

     Dica: você precisará mapear cada UF para sua região.
     Faça isso diretamente no SQL usando CASE WHEN.

     Retorne: região, total de acidentes, total de mortos,
     percentual de acidentes em relação ao total nacional.
```

---

## ✅ Critérios de Avaliação

| Critério       | Descrição                                                     |
| -------------- | ------------------------------------------------------------- |
| **Correção**   | As queries retornam os resultados esperados?                  |
| **Clareza**    | O código SQL está bem formatado e comentado?                  |
| **Eficiência** | Evita subqueries desnecessárias, usa agregações corretamente? |
| **Completude** | Responde todas as perguntas obrigatórias (seções 1 e 2)?      |

---
## 📎 Fonte dos Dados

- **Portal de Dados Abertos da PRF:** https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dados-abertos-da-prf
- Período: **2007 a 2024**
- Licença: Dados públicos — uso livre com atribuição à fonte.

---

_Bom desafio! 🚦 Use SQL como sua principal ferramenta de análise e deixe os dados contarem a história das rodovias brasileiras._