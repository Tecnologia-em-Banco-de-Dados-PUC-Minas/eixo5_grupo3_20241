### Pré-processamento de dados

#### 1. Preparação do ambiente

Para a etapa de pré-processamento de dados, foi definida pelo grupo a utilização da plataforma AWS pela  infraestrutura de computação global escalável, confiável e segura. Usamos o Athena para realizar consultas interativas, para facilitar a análise de dados diretamente no S3, que é um serviço de armazenamento de objetos que oferece escalabilidade, disponibilidade de dados, segurança e performance onde  criamos o bucket "grupo3-2024-1-MachineLearning" e o subimos nossos dados como objeto "Churn_Modelling.csv e configuramos uma política de criptografia para proteger os dados em repouso e em trânsito. Outro serviço usado foi o Glue que nos possibilitou criar nosso banco de dados.

Criação do armazenamento no AWS S3
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/1e492f78-0d65-417d-b629-1438bcc2a089)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/13510c83-de42-4070-97c2-272b9a004408)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/8e09123c-53a6-4a42-ac7d-e9a18820ea87)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/640f35de-7e7f-49f6-b4b4-8d756e19eaff)

Criação da base de dados e tabela na nuvem usando Athena e Glue

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/be72b3a6-b364-4a51-bf18-4cfc87aa3ab4)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/e42a5ec2-96ca-482a-a555-a3aed6960603)

Tabela criada
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/ef2a69e0-bb5e-4315-99a1-83e0a7c26387)
Preview da tabela com descrição dos campos
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/ec0d72b1-c4cc-49d1-b8b6-cef916d9f847)


#### 2. Limpeza de dados

##### Exclusão de colunas desnecessárias

Algumas colunas apresentam apenas informações de individualização dos dados do cliente, não sendo capazes de influenciar o resultado da variável ‘Target’ de mudar ou não de banco.  Como a manutenção deste tipo de dados apenas reduziria a acurácia do modelo, foram excluídas as colunas ‘CustomerId’, ‘Surname’ e ‘RowNumber’.
 
##### Convertendo variáveis categóricas em numéricas

Durante a análise exploratória do banco de dados, identificamos que algumas variáveis são categóricas. Essas variáveis representam dados qualitativos e podem ser agrupadas em categorias específicas. Para otimizar o desempenho do modelo de aprendizado de máquina, é recomendado transformar essas variáveis categóricas em formatos numéricos. Dessa forma, o modelo pode processá-las de maneira mais eficiente.
No nosso dataset temos duas variáveis categóricas, “Geography” e “Gender” com as seguintes características:
“Geography”:  “France”, “Germany” ou “Spain”.
“Gender”:  “Male” ou “Female”.
Para transformar essas variáveis em formato numérico, usamos a função get_dummies() (também conhecida como OneHotEncoder). Criando novas colunas para cada categoria única, indicando a presença ou ausência dessa categoria em cada linha original.



