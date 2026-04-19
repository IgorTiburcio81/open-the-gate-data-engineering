# 🛠️ Engenharia de Dados: A Trilha Gratuita

> **"A engenharia de dados não é sobre ferramentas caras — é sobre resolver problemas com eficiência."**
---

## 📢 Nossa Missão

Muitas pessoas acreditam que entrar na área de Engenharia de Dados exige investir milhares de reais em bootcamps ou cursos fechados. Este repositório nasceu para provar o contrário.

**Tudo o que você precisa para construir uma base sólida** de fundamentos até arquiteturas modernas de nuvem você encontra disponível gratuitamente na internet. Nosso trabalho é sistematizar, curar e guiar o seu aprendizado, separando o ruído do que realmente importa.

Se você está começando do zero ou migrando de carreira, este é o seu ponto de partida.

---
## 🧭 O que você encontrará aqui

Este não é apenas uma lista de links. Aqui você terá:

|O que|Como|
|---|---|
|**Conteúdo autoral**|Explicações diretas sobre conceitos complexos, escritas para quem está chegando|
|**Curadoria de elite**|Os melhores canais, artigos e livros gratuitos do ecossistema de dados|
|**Trilha progressiva**|Uma jornada que vai do "O que é um dado?" até arquiteturas como Lakehouse e Data Mesh|
|**Ferramentas reais**|Guias práticos de Airflow, dbt, Docker, Spark, Kafka e muito mais|
|**Projetos do básico ao avançado**|Desafios e projetos com dados reais para compor seu portfólio|

---

## 🗺️ Trilha de Aprendizado

O conteúdo segue uma progressão pensada para maximizar seu aprendizado.  Cada módulo é pré-requisito para o próximo.

```
Módulo 1 — Fundamentos de Dados
         │
         ▼
Módulo 2 — Pipelines, Processamento & Ferramentas
         │
         ▼
Módulo 3 — Modelagem de Dados
         │
         ▼
Módulo 4 — Projetos Locais  (Docker · DuckDB · dbt · Spark · Kafka)
         │
         ▼
Módulo 5 — Projetos em Cloud  (GCP Free Tier · Databricks Free)
```

---

## 📦 Módulos

### Módulo 1 — Fundamentos de Dados

> Status: ✅ **Disponível · em expansão**

A base de tudo. Antes de escrever uma linha de código, você precisa entender o ecossistema.

**Conteúdos:**

- O que são dados e como são gerados
- O papel da Engenharia de Dados no mercado
- Dados estruturados, semiestruturados e não estruturados
- Paradigmas de armazenamento: OLTP vs OLAP
- Arquiteturas: Data Warehouse, Data Lake e Data Lakehouse
- Linguagens essenciais: SQL, Python e Git

📄 [`introducao-fundamentos.md`](https://claude.ai/chat/modulo-01/introducao-fundamentos.md)

---

### Módulo 2 — Pipelines, Processamento & Ferramentas

> Status: 🔜 **Em breve**

O coração da Engenharia de Dados: como mover, transformar e orquestrar dados com qualidade e confiabilidade. Conceitos e ferramentas são apresentados juntos, você ira aprende o "porquê" e o "como" no mesmo contexto.

|Tema|Conceito|Ferramenta|
|---|---|---|
|Containerização|Ambientes reproduzíveis|Docker|
|Ingestão|Fontes, conectores e estratégias de carga|Python, APIs, bancos relacionais|
|Transformação|ETL vs ELT, trade-offs e boas práticas|dbt|
|Orquestração|Agendamento e dependências entre tarefas|Apache Airflow|
|Processamento batch|Grandes volumes em janelas de tempo|Apache Spark|
|Processamento streaming|Dados em tempo real e eventos contínuos|Apache Kafka|

---

### Módulo 3 — Modelagem de Dados

> Status: 🔜 **Em breve**

Dados bem modelados são a diferença entre um pipeline frágil e uma plataforma analítica confiável.

**O que será abordado:**

- Star Schema e Modelagem Dimensional
- Arquitetura Medallion: Bronze → Silver → Gold
- Boas práticas de modelagem para consumo analítico

---
### Módulo 4 — Projetos Locais

> Status: 🔜 **Em breve**

Teoria sem prática não coloca ninguém no mercado. Todos os projetos deste módulo rodam **100% na sua máquina**, sem depender de conta em nuvem.

**Projetos planejados:**

| Nível            | Projeto                                             | Stack                  |
| ---------------- | --------------------------------------------------- | ---------------------- |
| 🟢 Iniciante     | Pipeline simples de ingestão e transformação        | Python + SQL + DuckDB  |
| 🟡 Intermediário | Pipeline orquestrado com camadas Bronze/Silver/Gold | Airflow + dbt + DuckDB |
| 🟡 Intermediário | Arquitetura Medallion com processamento distribuído | Docker + Spark  + dbt  |

---

### Módulo 5 — Projetos em Cloud

> Status: 🔜 **Em breve**

Com a base local consolidada, é hora de escalar para ambientes reais de produção, usando plataformas gratuitas para que o custo não seja uma barreira.

**Plataformas utilizadas:**

- **GCP Free Tier** — BigQuery, Cloud Storage
- **Databricks Free Edition** — Spark gerenciado, Delta Lake e notebooks colaborativos

**Projetos planejados:**

| Nível            | Projeto                                        | Stack                      |
| ---------------- | ---------------------------------------------- | -------------------------- |
| 🟡 Intermediário | Pipeline em nuvem com ingestão e transformação | GCP + BigQuery + dbt Cloud |
| 🔴 Avançado      | Lakehouse completo com Delta Lake e jobs Spark | Databricks + Delta Lake    |

---

## 🎯 Como usar este repositório

1. **Siga a ordem dos módulos** — a trilha foi desenhada de forma progressiva
2. **Acesse os links sugeridos** — não apenas leia; explore os materiais indicados
3. **Coloque a mão na massa** — tente replicar os conceitos antes de avançar
4. **Participe dos desafios** — cada módulo terá exercícios práticos
5. **Contribua** — viu um material melhor? Abra uma Pull Request!

---
## 🤝 Como contribuir

Contribuições são muito bem-vindas! Veja como participar:

- ⭐ **Dê uma star** — ajuda o repositório a chegar em mais pessoas
- 🐛 **Abra uma issue** — encontrou um link quebrado ou um erro de conteúdo?
- 📬 **Abra uma Pull Request** — quer adicionar um material gratuito de qualidade?
- 💬 **Compartilhe** — indique para alguém que está tentando entrar na área

Antes de contribuir, leia o [`CONTRIBUTING.md`](https://github.com/IgorTiburcio81/RoadMap_DataEngineer/blob/main/CONTRIBUTING.md)).

---

## 👥 Para quem é este repositório

- Pessoas iniciando na área de dados do **zero**
- Profissionais de outras áreas em **transição de carreira**
- Desenvolvedores querendo entender o **ecossistema de dados**
- Analistas que querem evoluir para **engenharia**

---

## 📬 Contato & Comunidade

Mantido com ☕ e dedicação.  
Dúvidas, sugestões ou quer trocar uma ideia sobre dados? Abra uma issue ou me encontre em  [`igor-tiburcio`](https://www.linkedin.com/in/igor-tiburcio/).

---

_Este repositório é e sempre será gratuito.
