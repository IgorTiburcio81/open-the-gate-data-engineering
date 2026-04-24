# Introdução aos fundamentos da engenharia de dados

## **O que são dados?**

Muito se fala sobre dados, mas, afinal, o que eles são? Dados são uma coleção de fatos e números. Eles são gerados o tempo todo ao nosso redor; por exemplo, quando você corre e utiliza um aplicativo para monitorar sua atividade, são gerados dados de velocidade, distância percorrida, batimentos cardíacos, entre outros. Esse é apenas um exemplo, pois temos contato com uma infinidade de dados diariamente e também geramos diversos registros a partir de nossas interações ao longo do dia. Esses dados, ao serem gerados, normalmente encontram-se desorganizados, ou seja, dados brutos. É exatamente nesse ponto que entra a engenharia de dados.

## **O que é engenharia de dados ?**

A engenharia de dados pode ser descrita de diferentes formas, mas olhando para onde a grande maioria das visões convergem podemos defini-la como, a construção de sistemas que processam dados brutos e a parti deles geram dados de alta qualidade, onde esses geram informações de valor. Então a grosso modo podemos dizer que a engenharia de dados é ação de transformar dados brutos em informações de alta qualidade. 
Esses dados tratados podem ser utilizados por analistas e cientistas de dados para gerar indicadores, predições e afins, gerando valor a partir deles. Porém, há uma linha tênue entre engenheiros e analistas de dados atualmente: existe uma divisão em que o analista é responsável por gerar insights a partir de dados tratados, enquanto o engenheiro é responsável pelo processo de tratamento e organização desses dados. Com o surgimento do _Analytics Engineer_, essa fronteira ficou ainda mais tênue, o que deixa a visão de 'transformar dados em informação' totalmente alinhada às tendências modernas.

## Canais para estudar dados 

https://www.youtube.com/@teomewhy - Teo Calvo

https://www.youtube.com/@pgdinamica - Programação Dinâmica

https://www.youtube.com/@DataTalksClub - Data Talks Club

https://www.youtube.com/@afaqueahmad7117 - Afaque Ahamad

https://www.youtube.com/@CibeleRussoUSP - Cibele Russo

https://www.youtube.com/@FranciscoRodrigues - Francisco Rodrigues

https://www.youtube.com/@univesptv - UNIVESP

# **Linguagens e Comunicação**

## SQL

O **SQL** é uma linguagem criada para consultar, manipular, inserir e deletar dados em sistemas de bancos relacionais. Criada ainda na década de 70, ela se **mantém** como a ferramenta _core_ no mercado de tecnologia. Mesmo após a ascensão do Big Data, o SQL continua presente em sistemas modernos de dados, como o **BigQuery** (Google Cloud), **Snowflake**, entre outros. Sua relevância atual deve-se à simplicidade e à performance, que geram alta produtividade tanto para engenheiros quanto para analistas.

**Onde aprender de graça???**

- https://www.youtube.com/playlist?list=PLvlkVRRKOYFRo651oD0JptVqfQGDvMi3j Curso de SQL do **Téo Calvo**
## Python

O **Python** é uma linguagem de alto nível extremamente versátil, utilizada em diversos tipos de projetos, mas consolidada fortemente na área de dados (Engenharia, Ciência e Análise). É uma ferramenta indispensável por possuir um ecossistema rico de bibliotecas e _frameworks_ que executam diversas etapas do processamento com maestria. Entre os principais, destacam-se:

- **Apache Airflow:** O principal orquestrador de fluxos de dados do mercado.
    
- **Manipulação e Cálculo:** Bibliotecas como **Pandas** e **NumPy**.
    
- **Machine Learning:** **Scikit-learn**, **TensorFlow** e **PyTorch**.
    
- **Big Data:** Integrações poderosas como o **PySpark**.

**Onde aprender de graça???**

- https://www.youtube.com/playlist?list=PLvlkVRRKOYFSpRkqnR0p2A-eaVlpLnN3D Curso de Python do **Téo Calvo**
- https://penseallen.github.io/PensePython2e/ Livro - Pense em Python - **Allen B. Downey**
## Git

O **Git** é um sistema de controle de versão distribuído, criado para que desenvolvedores possam rastrear alterações no código-fonte, manter ramificações (_branches_) independentes e colaborar no mesmo projeto sem sobrescrever o trabalho alheio. Na engenharia de dados, o Git é fundamental para garantir o fluxo de desenvolvimento organizado, seguro e centralizado, permitindo que diversas pessoas trabalhem simultaneamente no mesmo ecossistema de código.

**Onde aprender de graça???*

- https://git-scm.com/docs/gittutorial
- https://learngitbranching.js.org/?locale=pt_BR
- https://www.youtube.com/playlist?list=PLvlkVRRKOYFQyKmdrassLNxkzSMM6tcSL - Curso de Git e Github do **Téo Calvo**
# **Anatomia do Dado e Armazenamento**
## **Dados estruturados e não estruturados**

*Dados estruturados* são dados que possuem uma formatação clara, se encaixando perfeita mente em estruturar de tabelas, ou seja, linha e colunas. Esses podem ser quantitativos ou qualitativos, números, datas, nomes, textos curtos e etc. Esses dados são tipicamente armazenados em bancos de dados relacionais (SQL).

*Dados não estruturados* são que não possuem uma formatação predefinida ou um esquema, não se encaixando nas tradicionais estruturas de tabelas.  Exemplos de dados não estruturados são, vídeos, fotos, PDFs, posts em redes sociais. Esses dados são guardados em bancos de dados não relacionais ( NoSQL).

Mas também existe um meio termo entre esses dois, que são os dados **Semiestruturados**, eles não tem modelo de dados rígido predefinido, mas utilizam metadados para identificar características específicas e separar elementos. Como exemplos temos CSV, XML e Json.
## Paradigmas e Arquiteturas de Armazenamento

### **Bancos de dados**

- **OLTP (Processamento Transacional Online)** - São bancos de dados transacionais, amplamente **utilizados** em aplicações de software e web. Eles são projetados para **suportar** um alto volume de gravações contínuas, como diversos _inserts_, _deletes_ e _updates_. Por exemplo: quando fazemos uma compra em um e-commerce, geralmente há um banco OLTP por **trás** registrando essa operação, para que, futuramente, o time de engenharia de dados possa **processá-la**.

- **OLAP (Processamento Analítico Online)** - São bancos focados na leitura de grandes volumes de dados para fins analíticos. Diferentemente dos bancos OLTP, os sistemas OLAP não são voltados para aplicações rotineiras de ponta; seu principal foco é o armazenamento e a consulta de dados para geração de insights. Grandes exemplos são o **BigQuery** (GCP) e o **Redshift** (AWS), além de opções locais e eficientes como o **DuckDB**.

### **Data Warehouses**

Data Warehouses são bancos OLAP, neles ficam armazenados dados tratados e pronto para o consumo analítico. Os Data Warehouses são focados em dados estruturados (formato de tabela), onde podem ser conectados a ferramentas de BI como Looker, PowerBI, Tabelau ou Metabase, ou servirem modelos de Machine learning (aprendizado de maquina). Em Resumo, os Data Warehouses são ferramentas de armazenagem de dados tabulares já tratados e pronto para consumo. 
### **Data Lakes**

**Data Lakes** são repositórios voltados para o armazenamento de enormes volumes de dados (estruturados, semiestruturados ou não estruturados) com baixo custo. É neles que, normalmente, chegam os dados brutos (_raw data_) extraídos de diversas fontes. Embora sejam excelentes para lidar com a grande variedade de informações, exigem um controle rigoroso; sem uma boa governança, o seu Data Lake pode se tornar um **_Data Swamp_** (pântano de dados). Perder o controle sobre o que está armazenado pode custar caro e inviabilizar a utilidade do repositório.
### **Data Lakehouse**

O **Data Lakehouse** é a fusão das melhores características do Data Lake e do Data Warehouse. Ele permite o armazenamento de dados (estruturados, semiestruturados ou não estruturados) a baixo custo, como nos Data Lakes, mas conta com uma camada de metadados que possibilita a criação de esquemas. Nessa arquitetura, é possível indexar dados e realizar consultas rápidas, de forma semelhante a um Data Warehouse. Exemplos populares de tecnologias que viabilizam essa estrutura são o **Delta Lake** (nativo do Databricks) e o **Apache Iceberg**.
### **Bucket** 

**Buckets** são contêineres lógicos utilizados para armazenar objetos em serviços de _Cloud Storage_, como o **Amazon S3** e o **Google Cloud Storage (GCS)**. Nesses serviços, para que qualquer dado seja armazenado, é obrigatório que o objeto esteja contido dentro de um bucket, que atua como a unidade organizacional básica do sistema.

### **Indicação de leitura**

-  https://www.ibm.com/br-pt/think/topics/structured-vs-unstructured-data
-  https://medium.com/@TheWuraolah/what-is-data-structured-vs-unstructured-data-explained-simply-for-beginners-88c46fc9c28f
-  https://otiagonavarro.medium.com/english-version-https-medium-com-p-aff1fdb3e9af-edit-669a48ac8d15
-  https://blog.dsacademy.com.br/categoria/arquitetura-medalhao/
- https://www.ibm.com/br-pt/think/topics/data-warehouse-vs-data-lake-vs-data-lakehouse
- https://www.youtube.com/watch?v=V07Pk4de-5M
- https://medium.com/@le.oasis/data-engineering-for-beginners-data-lake-and-data-warehousing-2440a91f5990
