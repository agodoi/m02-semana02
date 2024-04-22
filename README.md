# Banco de Dados I - Conceitos, Modelos e SQL Básico

Vamos criar uma aplicação web completa discutindo os principais conceitos envolvidos nos bancos de dados, como as modelagens (que serão cobradas nos artefatos e ponderadas) e iniciar a escrita de consultas aos bancos através de SQL.

# Tecnologias do Módulo

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana02/blob/main/imgs/TecnologiasM02.png">
   <img alt="Tecnologias Módulo 02" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana02/blob/main/imgs/TecnologiasM02.png)">
</picture>

# O que é um Sistema de Gerenciamento de Banco de Dados (SGBD)?

Um **Sistema de Gerenciamento de Banco de Dados (SGBD)**, também conhecido como **DBMS** (do inglês *Data Base Management System*), é um software que organiza, armazena, recupera e gerencia grandes volumes de dados de forma eficiente e segura. Ele atua como um intermediário entre os usuários e os dados, fornecendo uma interface para acessar, manipular e consultar as informações de forma organizada.

Os SGBDs são ferramentas essenciais para diversas aplicações, desde sistemas de e-commerce e bancos online até softwares de gestão empresarial e pesquisas científicas. Eles garantem a **integridade**, **consistência** e **disponibilidade** dos dados, além de facilitar o acesso e a análise das informações por parte dos usuários autorizados.

### Funções principais de um SGBD:

* **Armazenamento e organização de dados:** O SGBD estrutura os dados em um formato organizado, geralmente utilizando um modelo de dados específico, como relacional, hierárquico ou de rede.
* **Controle de acesso:** O SGBD define permissões de acesso aos dados, garantindo que apenas usuários autorizados possam consultar, modificar ou excluir informações.
* **Segurança:** O SGBD implementa medidas de segurança para proteger os dados contra acessos não autorizados, alterações indevidas e perda de informações.
* **Recuperação de dados:** O SGBD permite recuperar dados em caso de falhas no sistema ou perda acidental de informações.
* **Otimização de desempenho:** O SGBD otimiza o acesso aos dados para garantir um bom desempenho das consultas e operações.
* **Gerenciamento de transações:** O SGBD garante a integridade das transações, assegurando que as operações sejam realizadas de forma completa e consistente.
* **Suporte a consultas:** O SGBD fornece ferramentas para consultar e analisar os dados de diferentes maneiras, como através da linguagem SQL.

### Benefícios de usar um SGBD:

* **Organização e eficiência:** Os SGBDs organizam os dados de forma eficiente, facilitando o acesso e a análise das informações.
* **Segurança:** Os SGBDs protegem os dados contra acessos não autorizados, alterações indevidas e perda de informações.
* **Integridade dos dados:** Os SGBDs garantem a consistência e integridade dos dados, evitando duplicações e erros.
* **Compartilhamento de dados:** Os SGBDs facilitam o compartilhamento de dados entre diferentes aplicações e usuários autorizados.
* **Escalabilidade:** Os SGBDs podem ser dimensionados para atender às necessidades de diferentes empresas e organizações.
* **Flexibilidade:** Os SGBDs oferecem suporte a diferentes modelos de dados e linguagens de consulta, atendendo a diversas necessidades de negócio.

## Principais SGBDs disponíveis no mercado:

Atualmente, existem diversos SGBDs disponíveis no mercado, cada um com suas características e funcionalidades específicas. Alguns dos SGBDs mais populares incluem:

* **SGBDs relacionais [organização em tabelas]:**
    * **MySQL:** Um SGBD open-source muito popular, utilizado em diversos sites e aplicações da web.
    * **PostgreSQL:** Um SGBD open-source robusto e escalável, com foco em segurança e confiabilidade.
    * **Oracle Database:** Um SGBD comercial poderoso e escalável, utilizado em grandes empresas e organizações.
    * **Microsoft SQL Server:** Um SGBD comercial popular no ambiente Windows, com foco em integração com outras ferramentas da Microsoft.
* **SGBDs NoSQL [organização em documentos]:**
    * **MongoDB:** Um banco de dados NoSQL document-oriented, ideal para armazenar e consultar dados não estruturados.
    * **Cassandra:** Um banco de dados NoSQL distribuído, projetado para alta disponibilidade e escalabilidade.
    * **Redis:** Um banco de dados NoSQL em memória, ideal para armazenar dados que precisam ser acessados ​​rapidamente.
    * **CouchDB:** Um banco de dados NoSQL document-oriented, com foco em flexibilidade e escalabilidade.

A escolha do SGBD ideal depende das necessidades específicas de cada projeto, levando em consideração fatores como tipo de dados, volume de dados, desempenho, segurança, escalabilidade, custo e compatibilidade com outras ferramentas.

É importante avaliar cuidadosamente as necessidades do projeto antes de escolher um SGBD, considerando fatores como tipo de dados, volume de dados, desempenho, segurança, escalabilidade, custo e compatibilidade com outras ferramentas.

### Como vamos usar o PostgreSQL, o seu projeto estará no tipo de banco **RELACIONAL**.

## Modelagens Conceitual, Lógico e Físico

Para que não haja retrabalho, recomenda-se seguir os seguintes passos para montar seu banco de dados, conforme mostra a figura.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana02/blob/main/imgs/modelagens.png">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana02/blob/main/imgs/modelagens.png)">
</picture>


### Identificação do problema (levantamento de requisitos)

Nesta etapa, é realizado um estudo detalhado das atividades em questão. Quando não há conhecimento prévio sobre o negócio, entrevistas podem levantar informações relevantes sobre as necessidades dos futuros usuários. Os administradores de dados se reúnem com os usuários para entender e documentar seus requisitos.

### Modelagem Conceitual

Trata-se de um rascunho inicial do banco de dados, feito sob a ótica do usuário que cria os dados. Nessa etapa, definimos como os dados se relacionam e como serão armazenados, sem nos preocupar com a implementação no sistema. 

Uma das técnicas mais usadas é a abordagem entidade-relacionamento, que utiliza diagramas para representar as entidades (coisas que se quer guardar como informações, como clientes ou produtos), seus atributos (características das entidades) e como elas se relacionam (por exemplo, um cliente pode ter vários pedidos).

Portanto:

* A modelagem conceitual é como um rascunho do banco de dados, onde definimos o que queremos guardar e como as informações se relacionam.
* Essa etapa é importante porque nos permite ter uma visão geral do banco de dados antes de implementá-lo no sistema.
* Ao fazer a modelagem conceitual, pensamos sob a ótica do usuário que cria os dados, ou seja, definimos como ele vai ver e usar as informações.
* É importante levar em consideração alguns fatores técnicos para que a implementação do banco de dados seja eficiente, mas o foco principal nessa etapa é na visão do usuário.
* A modelagem conceitual define como os dados serão armazenados e relacionados, mas não se preocupa com os detalhes de como isso será feito no sistema.
* Uma das técnicas mais utilizadas para fazer a modelagem conceitual é a abordagem entidade-relacionamento (MER).
* A MER utiliza diagramas para representar as entidades, seus atributos e seus relacionamentos.
* Peter Chen foi o responsável por criar a notação MER em 1976, que é utilizada até hoje para modelar dados em ambientes relacionais.

**Importante destacar que o modelo conceitual não é associado e não faz parte de nenhum SGBD. O modelo conceitual é útil para identificar e analisar se as regras de negócio estão bem definidas e, dessa forma, evitar erros futuros.**
 

### Modelam Lógica

É a etapa onde detalhamos como o banco de dados será realmente implementado, escolhendo um tipo de banco de dados específico (como **PostgradeSQL**, Microsoft SQL Server, Oracle ou MySQL) e definindo como os dados serão armazenados e acessados nesse sistema. 

É importante fazer essa etapa depois de já ter definido o que queremos guardar e como as informações se relacionam na modelagem conceitual. Pular a modelagem conceitual pode trazer problemas no futuro, pois fica mais difícil garantir que todos os requisitos do projeto sejam atendidos corretamente.

Portanto:

* A modelagem lógica é a etapa onde detalhamos como o banco de dados será implementado na prática.
* Nessa etapa, escolhemos um tipo de banco de dados específico, como SQL Server, Oracle ou MySQL.
* Cada tipo de banco de dados tem suas próprias características e formas de armazenar e acessar os dados.
* É importante definir como os dados serão armazenados e acessados no banco de dados escolhido.
* A modelagem lógica deve ser feita depois que a modelagem conceitual já estiver concluída.
* A modelagem conceitual define o que queremos guardar e como as informações se relacionam, enquanto a modelagem lógica define como isso será implementado no sistema.
* Pular a modelagem conceitual pode trazer problemas no futuro, pois fica mais difícil garantir que todos os requisitos do projeto sejam atendidos corretamente.
* Ao fazer a modelagem conceitual, já pensamos em como os dados serão armazenados e acessados, o que facilita a modelagem lógica e evita problemas futuros.

### Modelagem Física

É a última etapa da modelagem de dados, onde definimos os detalhes técnicos de como o banco de dados será armazenado e acessado no sistema. Nessa etapa, escolhemos os tipos de dados que serão usados para cada campo, criamos as tabelas e relacionamentos entre elas, definimos índices para otimizar o acesso aos dados e implementamos as medidas de segurança e backup. 

A modelagem física é feita com base no modelo lógico e utiliza a linguagem SQL para criar as tabelas e estruturas do banco de dados.

Portanto:

* A modelagem física é a etapa onde definimos os detalhes técnicos de como o banco de dados será implementado no sistema.
* Nessa etapa, escolhemos os tipos de dados que serão usados para cada campo, como texto, número, data, etc.
* Criamos as tabelas para armazenar os dados e definimos os relacionamentos entre elas.
* Definimos índices para otimizar o acesso aos dados, o que significa que o sistema poderá encontrar as informações mais rapidamente.
* Implementamos as medidas de segurança para proteger os dados contra acessos não autorizados e perdas.
* Criamos um plano de backup para garantir que os dados possam ser recuperados em caso de falhas.
* A modelagem física é feita com base no modelo lógico, que define o que queremos guardar e como as informações se relacionam.
* A linguagem SQL é utilizada para criar as tabelas e estruturas do banco de dados.
* Nessa etapa, a tecnologia assume grande importância, pois precisamos escolher as ferramentas e técnicas adequadas para implementar o banco de dados de forma eficiente e segura.

### MER Modelo Entidade-Relacionamento

No universo dos bancos de dados, o **MER (Modelo Entidade-Relacionamento)** é uma ferramenta fundamental para a modelagem conceitual de dados. Ele serve para **representar de forma gráfica e abstrata** como os dados se relacionam no mundo real, facilitando a compreensão e o planejamento da estrutura de um banco de dados.

**O que o MER representa:**

* **Entidades:** Representam os objetos principais do domínio que queremos modelar, como clientes, produtos, pedidos, etc. É representada em um modelo conceitual por meio de um retângulo, com o nome da tabela ao centro dele. Essa entidade terá uma ou várias informações. Cada ocorrência dessas informações é chamada de instância e vai representar um conjunto exclusivo dos dados.
   * Entidade forte: são aquelas cuja existência não depende de outras entidades, ou seja, elas já possuem total sentido de existir. Em um sistema de notas, a entidade Alunos, por exemplo, independe de quaisquer outras para existir.
   * Entidade fraca: ao contrário das entidades fortes, as fracas são aquelas que dependem de outras entidades para existirem, pois individualmente elas não fazem sentido.


* **Atributos:** Representam as características das entidades, como nome, endereço, preço, data, etc.
* **Relacionamentos:** Representam as ligações entre as entidades, definindo como elas se relacionam entre si.

**Para que serve o MER:**

* **Visualizar a estrutura do banco de dados:** O MER fornece uma visão gráfica clara e intuitiva da estrutura do banco de dados, facilitando a compreensão e a análise do modelo.
* **Identificar falhas e redundâncias:** Ao visualizar o MER, é possível identificar facilmente falhas no modelo, como redundâncias de dados e inconsistências.
* **Comunicar o modelo de dados:** O MER serve como uma ferramenta de comunicação eficaz para compartilhar o modelo de dados com diferentes stakeholders, como analistas, desenvolvedores e usuários finais.
* **Facilitar o desenvolvimento do banco de dados:** Um MER bem elaborado facilita o processo de desenvolvimento do banco de dados, pois fornece uma base sólida para a criação das tabelas, relacionamentos e consultas SQL.

**Tipos de relacionamentos no MER:**

* **1:1:** Uma entidade está associada a no máximo uma instância de outra entidade.
* **1:N:** Uma entidade está associada a zero ou mais instâncias de outra entidade.
* **N:N:** Uma entidade está associada a zero ou mais instâncias de outra entidade, e vice-versa.

**Vantagens de usar o MER:**

* **Melhora a compreensão do modelo de dados:** O MER torna o modelo de dados mais intuitivo e fácil de entender, facilitando a comunicação entre diferentes stakeholders.
* **Reduz erros e redundâncias:** Ao visualizar o MER, é possível identificar facilmente falhas no modelo, como redundâncias de dados e inconsistências.
* **Facilita o desenvolvimento e a manutenção do banco de dados:** Um MER bem elaborado facilita o processo de desenvolvimento do banco de dados e sua posterior manutenção.
* **Melhora a qualidade do banco de dados:** Um MER bem estruturado contribui para a criação de um banco de dados mais eficiente, confiável e seguro.

**Ferramentas para criar MER:**

Existem diversas ferramentas disponíveis para criar diagramas MER, desde ferramentas online gratuitas até softwares pagos mais completos. Algumas opções populares incluem:

* **Draw.io:** [https://app.diagrams.net/](https://app.diagrams.net/)
* **Lucidchart:** [https://www.lucidchart.com/pages/](https://www.lucidchart.com/pages/)
* **Visual Paradigm:** [https://www.visual-paradigm.com/](https://www.visual-paradigm.com/)
* **StarUML:** [https://staruml.io/](https://staruml.io/)
* **Microsoft Visio:** [https://www.microsoft.com/en-us/store/collections/visio/pc](https://www.microsoft.com/en-us/store/collections/visio/pc)

