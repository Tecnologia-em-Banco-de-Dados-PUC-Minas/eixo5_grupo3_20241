 **Aprendizado de máquina e algorítimos**
 
Uma vez que os dados foram limpos e tratados e o ambiente preparado para a execução do pipeline, iniciaremos a abordagem de aprendizado de máquina. 
 

Os algoritmos de aprendizado de máquina podem ser categorizados em três tipos principais, dependendo da natureza do problema e da forma como aprendem com os dados. Primeiramente, existem os algoritmos de aprendizado supervisionado, que são treinados com pares de entrada e saída para aprender a mapear relações entre variáveis de entrada e a variável de saída correspondente. Esses algoritmos são frequentemente usados em tarefas de classificação e regressão, onde o objetivo é prever uma classe ou um valor numérico. Em segundo lugar, temos os algoritmos de aprendizado não supervisionado, que são treinados com conjuntos de dados sem rótulos e são usados para encontrar padrões intrínsecos e estruturas nos dados, como clusters ou associações. Eles são úteis em problemas de segmentação de dados e detecção de anomalias. Por fim, temos os algoritmos de aprendizado por reforço, que aprendem a tomar decisões sequenciais interagindo com um ambiente dinâmico, recebendo recompensas ou penalidades por suas ações. 

Para alcançar o nosso objetivo de trabalho foram escolhidos os algoritmos KNN, Naive Bayes e XGBoost.

KNN (k-nearest neighbors): Enquadra-se na categoria de aprendizado baseado em instância, onde o modelo faz previsões com base na similaridade entre os exemplos de treinamento e os novos dados de entrada.

Naive Bayes: Pertence à categoria de aprendizado probabilístico, onde é aplicado o teorema de Bayes com a suposição "ingênua" de independência condicional entre os recursos.

XGBoost (Extreme Gradient Boosting): Pertence à categoria de aprendizado de conjunto (ensemble learning), onde vários modelos fracos são combinados para formar um modelo forte, e utiliza árvores de decisão como modelos base.


 **Preparação de dados para aprendizagem de máquina**

Quando se trabalha com problemas de aprendizado de máquina um ponto crucial é o processo de balanceamento das variáveis de destino, que devem ter uma distribuição igual entre suas categorias, caso contrário a variável é considerada desbalanceada.
 Quando se lida com conjuntos de dados desbalanceados, o que significa que uma ou mais classes têm muito mais exemplos do que outras, pode ocorrer problemas durante o treinamento do modelo e resultar em modelos tendenciosos ou com baixo desempenho em classes minoritárias.
 Uma estratégia para a resolução do problema de desbalanceamento, é a aplicação do "oversampling" que nada mais é do que a criação de instâncias adicionais para a classe menos representadas, visando o equilíbrio do número de instâncias entre as classes.
 Para usar a estratégia "oversampling" de forma aleatória será utilizado a ferramenta RandomOverSampler  que aumenta o número de exemplos das classes minoritárias selecionando aleatoriamente observações dessas classes e replicando-as até que haja um equilíbrio relativo entre as classes no conjunto de dados.
 Dessa forma, os modelos de aprendizado de máquina não serão tendenciosos para a classe mais frequente.

Ademais a separação adequada dos dados em conjuntos de treino e teste é fundamental para avaliar objetivamente o desempenho de um modelo de aprendizado de máquina. Essa prática consiste em dividir o conjunto de dados em duas partes distintas: uma parte é utilizada para treinar o modelo, enquanto a outra é reservada para avaliar sua capacidade de generalização. Geralmente, uma proporção significativa dos dados é destinada ao conjunto de treinamento, enquanto uma porção menor é reservada para o conjunto de teste. O objetivo é garantir que o modelo seja treinado em uma variedade representativa de dados e, em seguida, testado em dados não vistos durante o treinamento. Isso ajuda a evitar o overfitting, onde o modelo se ajusta demasiadamente aos dados de treino e tem dificuldade em generalizar para novos exemplos.
 A separação dos dados de treino e teste deve ser realizada de forma aleatória e estratificada, garantindo que as distribuições das classes sejam mantidas em ambos os conjuntos. Essa prática é essencial para garantir a confiabilidade das avaliações de desempenho do modelo e para tomar decisões informadas sobre sua eficácia em cenários do mundo real.

  **Preparação de ambiente para execução dos algorítimos**

A seguir uma demonstração de configuração para execução dos trabalhos na plataforma Sagemaker da AWS que fará a execução por meio de jupyter notebook.
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/c865cbd6-2ab7-4ba7-b23d-d1b737c225da)

Página principal do SageMaker

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/60059e50-3ac4-44b4-af6b-dfb6bf8f5d25)

Por questões de governança e permissionamento de acessos, é necessário criar um domínio no serviço. Esse domínio hospeda usuários e gerencia permissões de acessos. 

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/12796d15-393b-4703-80e5-584729a14992)

Criação de usuário padrão

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/1a967c07-b3bb-4315-9249-4dc4dcd16663)

Criação de studio jupyter lab. Dentro dele são armazenados scripts executado bibliotecas entre outros. 

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/6b1b478f-c927-4a3e-bb5d-4d9b6ea4d2b0)

Página do studio Jypter lab




 
 
 

 
