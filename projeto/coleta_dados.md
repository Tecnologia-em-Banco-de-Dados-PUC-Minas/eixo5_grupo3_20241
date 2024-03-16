#### Governança de dados:

A governança de dados é a função responsável pelo planejamento e controle de alto nível da gestão de dados que garante que eles estejam nas condições adequadas para apoiar as iniciativas e operações de negócios. Essa metodologia exige soluções de pessoas, processos e tecnologia em uma variedade de recursos. Para esse trabalho iremos estruturar a nossa governança com base em três pontos principais: Entendimento, Proteção e  Curadoria dos dados.

![data-governance-aws](https://d1.awsstatic.com/DataGovCircle.b5af9c5c3ca8cad21dfbbce119d34c78fa7827be.png)

##### Entendimento

###### Arquitetura

A arquitetura do projeto será montada na cloud pública Amazon Web Service(AWS) e utilizará os seguintes serviços:

* S3 - Ingestão e Armazenamento
* Glue - Catálogo de dados e Qualidade de dados
* Lake Formation - Criação de database e tabela, controle de acesso
* SageMaker - Treinamento de modelos de aprendizado de máquina
* Microsoft PowerBI  - Visualização de métricas

![arquitetura](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/blob/main/projeto/ext/arquteturap5)
