### Governança de dados:

A governança de dados é a função responsável pelo planejamento e controle de alto nível da gestão de dados que garante que eles estejam nas condições adequadas para apoiar as iniciativas e operações de negócios. Essa metodologia exige soluções de pessoas, processos e tecnologia em uma variedade de recursos. Para esse trabalho iremos estruturar a nossa governança com base em três pontos principais: Entendimento, Proteção e  Curadoria dos dados.

![data-governance-aws](https://d1.awsstatic.com/DataGovCircle.b5af9c5c3ca8cad21dfbbce119d34c78fa7827be.png)
<br>
<br>

#### 1. Entendimento


##### Arquitetura


A arquitetura do projeto será montada na cloud pública Amazon Web Service(AWS) e utilizará os seguintes serviços:

* S3 - Ingestão e Armazenamento
* Glue - Catálogo de dados e Qualidade de dados
* Lake Formation - Criação de database e tabela, controle de acesso
* SageMaker - Treinamento de modelos de aprendizado de máquina
* Microsoft PowerBI  - Visualização de métricas

![arquitetura](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/blob/main/projeto/ext/arquteturap5)


##### Catálogo

O AWS Glue Data Catalog é seu armazenamento persistente de metadados técnicos. É um serviço gerenciado que você pode usar para armazenar, anotar e compartilhar metadados na Nuvem AWS.  Ele fornece um repositório uniforme onde sistemas diferentes podem armazenar e encontrar metadados para monitorar dados em silos de dados. É usado também em conjunto com outras ferramentas no auxílio do controle de políticas de acesso. 

Será usado o AWS Glue Crawler para ler e descobrir metadados no conjunto de dados a ser utilizado para treinamento do modelo, bem como o Glue Data Catalog para registrar a criação de eventuais tabelas e base de dados. 
<br>
<br>


#### 2. Curadoria:


##### Data Lake

Um Data Lake  é uma arquitetura de armazenamento centralizada e escalável que permite armazenar grandes volumes de dados estruturados e não estruturados em seu formato original. a AWS oferece uma abordagem flexível e econômica para armazenar e analisar dados em grande escala e esses dados podem ser utilizados para treinar modelos de Machine Learning. 

Para criar o Data Lake de forma governada, utilizaremos o serviço AWS Lake Formation. O AWS Lake Formation integra-se aos serviços de segurança, armazenamento, análise e machine learning da AWS e os configura automaticamente para estar em conformidade com seus controles de acesso centralizados por meio de um console web. 


##### Integração (ingestão)

A ingestão de dados é o processo de coleta e importação de dados brutos ou não processados de várias fontes para um sistema de armazenamento ou processamento onde podem ser manipulados, analisados e utilizados para diferentes finalidades.

Será utilizado o AWS S3 e o console da interface web do usuário para fazer o upload manual dos arquivos


##### Catálogo e Qualidade de dados

O AWS Glue Data Catalog é seu armazenamento persistente de metadados técnicos. É um serviço gerenciado que você pode usar para armazenar, anotar e compartilhar metadados na Nuvem AWS.  Ele fornece um repositório uniforme onde sistemas diferentes podem armazenar e encontrar metadados para monitorar dados em silos de dados. É usado também em conjunto com outras ferramentas no auxílio do controle de políticas de acesso. 

Será usado o AWS Glue Crawler para ler e descobrir metadados no conjunto de dados a ser utilizado para treinamento do modelo, Glue Data Quality para criar automações que verifiquem padrões de qualidade em campos, bem como o Glue Data Catalog para registrar a criação de eventuais tabelas e base de dados. 
<br>
<br>

 
#### 3. Proteção:


##### Segurança dos dados

O serviço de geração de Data Lake AWS Lake Formation atua também na segurança dos dados onde ele permite controlar rigorosamente o acesso, compreender a linhagem e auditar quem está acessando quais dados. O AWS Lake Formation integra políticas de acesso a dados ao seu Catálogo de Dados, garantindo conformidade independentemente da origem, incluindo políticas de controle e criptografia em nível de tabela, linha e coluna para dados em repouso e em movimento.

Para o trabalho serão utilizados as configurações padrão de cada serviço, além de ser configurado somente um usuário no ambiente por conta da utilização de uma conta AWS para estudantes que restringe certas ações. 
<br>
<br>

##### Ciclo de vida dos dados 

O ciclo de vida dos dados na AWS (Amazon Web Services) geralmente segue um padrão que envolve várias etapas, desde a criação até o arquivamento ou exclusão que incluí:

* Criação e ingestão de dados
* Processamento e análise
* Armazenamento de dados quentes e mornos
* Armazenamento de dados frios e arquivamento:

Os dados frequentemente acessados ou em uso ativo podem ser mantidos em armazenamento de nível mais alto e custo um pouco maior como banco relacional, Data Warehouse ou o armazenamento padrão do AWS S3. 

Conforme os dados envelhecem ou se tornam menos ativos, eles podem ser movidos para armazenamento de custo mais baixo, como AWS S3 Glacier, que custa uma fração do que se pagaria em um armazenamento convencional. 
<br>  

Para esse trabalho só será utilizado a camada quente do ciclo de vida visto a necessidade de estar frequentemente utilizando os dados para treinamento do modelo. Após o treino e otimização do modelo, os dados serão excluídos sem utilização de camada fria para armazenamento por conta de restrições na conta de estudante da AWS.

![s3-ciclod-e-vida](https://miro.medium.com/v2/resize:fit:640/format:webp/1*PZryXkcXoVj99unK-XNqUA.png)
<br>
Exemplo de precificação de tipos de armazenamento do AWS S3
