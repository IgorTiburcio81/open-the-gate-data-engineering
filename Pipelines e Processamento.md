# **Pipelines e Processamento de Dados**

### Pipelines

Um pipeline de dados é um conjunto de etapas, um fluxo de dados de uma ponta a outra. Pense em um pipeline como uma linha de montagem de uma fábrica, onde cada máquina ou funcionário executa uma etapa importante no processo. Vamos tomar como exemplo a produção de uma embarcação: no início temos apenas o metal bruto, mas na linha de produção ele vai sendo moldado, polido e por fim vira um navio. Com os dados não é muito diferente disso, pois pegamos dados brutos e moldamos, ou melhor, modelamos e por fim temos uma informação. É justamente essa esteira onde um dado entra bruto e sai tratado que chamamos de pipeline.

### Ingestão

A ingestão de dados é a fase de início do dado no pipeline. É o momento em que o dado é extraído de uma fonte, por exemplo, quando consultamos um banco de dados transacional ou quando fazemos uma chamada em uma API e alocamos esse dado em algum lugar. Usei como exemplo APIs e bancos de dados, mas esse dado pode vir de um ERP, dispositivo IoT, SaaS e etc. A ingestão é uma parte fundamental na construção de um pipeline, pois é essencial que esse dado venha com a mesma integridade da fonte para o nosso destino, que pode ser um Data Warehouse, Data Lake e etc.

Podemos dizer que a etapa de ingestão de dados é como engarrafar uma bebida fina: é preciso ter todo o cuidado para que o conteúdo não seja contaminado no processo, pois no final isso pode alterar o sabor. Brincadeiras à parte, essa etapa exige atenção principalmente nos tipos de dados. Deixo um alerta principalmente para dados numéricos sendo transferidos entre bancos de dados diferentes. Ocorre de, em alguns casos, surgirem variações de valores pela maneira que os bancos lidam com a quantidade de casas decimais. Logo, se em algum momento você se deparar com um erro desses, não se preocupe: extraia os valores como string ou varchar e só depois da ingestão converta para decimal, float ou tipo semelhante.

### ETL e ELT

ETL (extrair, transformar e carregar) ou ELT (extrair, carregar e transformar) são termos cotidianos para qualquer profissional da área de dados. Eles representam como o processo será feito nos pipelines. No caso de um ETL, o processo ocorre da seguinte forma: primeiro o dado é extraído da fonte, depois é transformado e só então vai para um Data Warehouse ou outra opção de destino. Você deve estar pensando "o que seria essa transformação?". Pode ser um tratamento de nulos, remoção de duplicatas ou mudança de formatação. No ELT ocorre o contrário: o dado é extraído da fonte e logo é ingerido, para só então ser tratado. O ELT é amplamente aplicado nas plataformas de nuvem, pois aproveita o processamento nativo dos Data Warehouses para transformar os dados, aliado a ferramentas como o dbt, que serão comentadas posteriormente.

### Orquestração

Até agora foram apresentados o pipeline e suas etapas, além das ferramentas base utilizadas na área de dados como Python e SQL. Mas como essas ferramentas se comunicam? Como elas são executadas em sequência? Como grandes empresas mantêm dezenas de pipelines funcionando juntos? A resposta para isso são os orquestradores. São eles que dizem que horas cada tarefa será executada, em que ordem e até mesmo organizam para que uma tarefa que dependa de outra seja executada na sequência correta.

Ficou confuso? Vamos voltar para o exemplo da construção de um navio: imagine se tentarem montar o navio sem moldar as chapas de metal antes; não daria certo. Do mesmo jeito que nos pipelines não dá certo pular etapas, os orquestradores organizam essa linha de montagem da informação. Temos alguns orquestradores no mercado, entre eles os mais famosos são o Apache Airflow e o Dagster. São ferramentas essenciais para a construção de pipelines robustos de dados e um padrão na mochila de ferramentas de um engenheiro de dados.

### Docker

Agora imagine tudo o que falamos até agora funcionando junto, envolvendo cloud, Linux, Windows e etc. Se você está familiarizado com a área de tecnologia, já deve ter ouvido o famoso "na minha máquina funciona". Muitas vezes, quando esses pipelines são construídos localmente (no seu computador), eles funcionam perfeitamente, mas quando colocados em um servidor, na cloud ou até mesmo no computador de um colega, eles simplesmente não funcionam. Para evitar isso surge o Docker. Ele conteineriza o projeto, sendo basicamente uma caixa com tudo o que seu projeto precisa para rodar, como bibliotecas, frameworks, dependências e etc. Então você deixa tudo isso nesse container e, quando ele vai para a nuvem ou para qualquer outro lugar, tudo continua funcionando perfeitamente, pois tudo o que é necessário para aquele projeto funcionar está guardado no container.

Deixo um alerta sobre o Docker: ele não funciona no Windows nativamente. Para fazê-lo funcionar é necessário usar o WSL, que funciona como uma máquina virtual Linux no Windows, porém isso consome uma quantidade valiosa de memória RAM. Então, se você pensa em desenvolver localmente alguns pipelines um pouco mais exigentes, recomendo utilizar uma distro Linux.
