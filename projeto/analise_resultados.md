### **Análise dos resultados e conclusão**

<br>

No estudo foram utilizados três algoritmos de aprendizado de máquinas para identificar os clientes que irão encerrar o seu relacionamento com a instituição financeira. Para identificar qual deles é o mais adequado à tarefa, foram calculadas as métricas de acurácia (Accuracy Score), precisão (Precision Score), Recall Score e F-Score.
O primeiro algoritmo testado foi o KNN (K-Nearest Neighbors), que faz uma abordagem dos dados baseada na proximidade entre pontos plotados em um gráfico. O algoritmo foi configurado para a tomada de decisão com base nos 5 pontos mais próximos existentes na base de dados para classificação dos clientes da base de teste, alcançando:

Accuracy Score – 0,673

Precision Score – 0,648

Recall Score – 0,768

F-Score – 0,703

<br>

O segundo algoritmo foi o Naive Bayes, que utiliza probabilidades condicionais para prever a possibilidade do objeto de estudo pertencer à uma classe. Em fase anterior do estudo foram excluídos os atributos com maior grau de correlação, gerando uma base de dados mais adequada a aplicação do Naive Bayes que funciona melhor quando os atributos são independentes, já que presume essa condição. Com a aplicação na base de testes, obtivemos os seguintes resultados:

Accuracy Score – 0,692

Precision Score – 0,71

Recall Score – 0,657

F-Score – 0,682

<br>

Também foi utilizado o algoritmo XGBoost (Extreme Gradient Boosting), que calcula múltiplas árvores de decisão para identificar a melhor classificação para o objeto de análise. Tendo sido escolhido para testagem por costumar obter bons resultados em dados estruturados, apresentou os seguintes resultados:

Accuracy Score – 0,879

Precision Score – 0,857

Recall Score – 0,912

F-Score – 0,884

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/0b348eec-da4b-4767-a8c7-b19ff06a2e58)

Para a correta análise dos resultados obtidos é importante a compreensão das métricas e as necessidades do negócio.


<br>
 
A acurácia (Accuracy Score) mede a proporção de previsões positivas em relação ao total de instâncias, permitindo uma visão geral do modelo, principalmente em casos como o do estudo que tem uma base de dados bastante equilibrada.

A precisão (Precision Score) mede a proporção de “verdadeiros positivos” em relação ao total de previsões positivas. É mais relevante nos casos em que “falsos positivos” são demasiadamente prejudiciais.

O Recall Score mede a proporção de “verdadeiros positivos” em relação a todas as instâncias positivas, sendo mais relevante em casos em que “falsos negativos” são mais prejudiciais.

O F-Score apresenta a médias harmônica do Precision Score e Recall Score sendo um bom parâmetro para identificar um modelo mais equilibrado.

Considerando que em um cenário de churn, objeto do presente estudo, falsos negativos (clientes erroneamente classificados como não-churn) são indesejados, percebemos que o Recall é a métrica que melhor indica a performance em identificar corretamente os clientes em risco de evasão, viabilizando a adoção de medidas preventivas.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/d13e4129-7051-44d3-b00d-6198806ff1d9)

<br>

#### Conclusão

<br>

Para analisar e classificar o resultado de uma métrica de desempenho dos algoritmos testados, estabelecemos benchmarks ou padrões de referência. Um resultado é considerado bom se a métrica atinge ou supera os padrões de excelência indicando uma alta eficácia do modelo. Um Recall Score acima de 90% pode ser classificado como bom, pois demonstra uma capacidade robusta de identificar a maioria dos casos positivos. Um resultado é médio quando a métrica atinge um desempenho aceitável, porém ainda possui margem para melhorias, como um Recall Score entre 70% e 89%, que indica uma boa identificação de casos positivos, mas não ideal. Um resultado é considerado ruim se a métrica fica significativamente abaixo dos padrões esperados, como um Recall Score abaixo de 70%, sugerindo que o modelo não está capturando adequadamente os casos positivos e, portanto, pode levar a decisões onde uma escolha ou ação que não é a melhor possível dadas as circunstâncias e informações disponíveis. Em outras palavras, é uma decisão que, embora possa ser adequada ou satisfatória, não maximiza os benefícios ou resultados desejados. Essa ação, no contexto de modelos de aprendizado de máquina é denominada de decisão subótima.

Em um cenário de previsão de churn, uma decisão subótima seria classificar incorretamente um cliente que está prestes a cancelar o serviço (um falso negativo) como não estando em risco. Isso significa que a instituição financeira não tomará as medidas preventivas necessárias para tentar reter esse cliente, resultando em perda de receita e potencial aumento na taxa de churn. 
 
Com base na análise das métricas de desempenho dos três algoritmos testados, concluímos que o XGBoost é o mais adequado para prever o churn de clientes bancários. Ele se destacou não apenas pela sua alta acurácia, mas principalmente pelo excelente Recall Score de 91,2%, crucial para identificar a maioria dos clientes em risco de evasão e permitir a adoção de medidas preventivas eficazes. Assim, a instituição financeira pode focar em estratégias direcionadas de retenção, minimizando as oportunidades perdidas e potencializando a satisfação e fidelidade dos clientes. O uso do XGBoost, portanto, oferece uma vantagem significativa no gerenciamento proativo da base de clientes, contribuindo para a estabilidade e crescimento da organização.



