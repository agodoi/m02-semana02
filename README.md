# Banco de Dados I - Conceitos, Modelos e SQL Básico

Vamos criar uma aplicação web completa discutindo os principais conceitos envolvidos nos bancos de dados, como as modelagens (que serão cobradas nos artefatos e ponderadas) e iniciar a escrita de consultas aos bancos através de SQL.

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
