### **Otimizações e próximas etapas**

<br>

Para a conclusão dos estudos, foi elaborada a presente sessão para elucidar próximas etapas na produção de um modelo de aprendizado de máquina. Uma empresa que deseja se aproveitar dos benefícios de usar a inteligência artificial deve seguir as seguintes boas práticas para manter seu modelo otimizado e em consonância com a governança da organização e com as leis de proteção de dados. 

<br>

#### Feature Store

Uma feature store é uma ferramenta essencial para gerenciar e servir features de forma
eficiente e consistente em um projeto de machine learning. No contexto da predição de
churn, a feature store facilita o armazenamento centralizado, a reutilização e o
versionamento das features, garantindo que todos os modelos utilizem as mesmas versões
das features e dados pré-processados. Isso é crucial para manter a integridade e a
consistência das previsões. A feature store permite a extração de features em tempo real
ou batch, integrando-se facilmente com pipelines de dados e modelos de machine
learning, o que acelera o desenvolvimento e a implementação de novas features. Além
disso, promove a colaboração entre equipes de data science, assegurando que todas as
partes interessadas tenham acesso às mesmas features de alta qualidade e validadas,
melhorando assim a precisão e a robustez dos modelos de predição de churn. Na cloud AWS, há possibilidade do uso da ferramenta do SageMaker chamada SageMaker Feature Store

<br>

#### Implementação e Integração (ML Ops)
Implementar o modelo treinado em um ambiente de produção. Utilizar
pipelines de CI/CD para garantir atualizações contínuas e automáticas bem como
estabelecer sistemas de monitoramento para avaliar o desempenho do modelo em tempo
real. Monitorar métricas como acurácia, precisão, recall e F-Score continuamente.
Gerenciamento de Versões: Manter um controle de versões dos modelos para permitir
rollback em caso de problemas e para comparar o desempenho de diferentes versões ao
longo do tempo.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo3_20241/assets/69175639/7cf26db1-0893-45f0-82cf-ed3d0c859905)

1. ML ops por databricks

<br>

#### Otimizações no Modelo

Entre as ações de otimizações no modelo estão: refinar os hiperparâmetros do modelo XGBoost para
melhorar ainda mais seu desempenho bem como identificar e criar novas features que possam aumentar a capacidade
preditiva do modelo (feature engineering). É uma boa prática realizar validação cruzada para garantir que o modelo generaliza bem
para dados não vistos.

<br>

#### Cruzamento com Demais Bases de Dados
Cruzar os dados de churn com outras bases de dados relevantes, como histórico de transações, interações com o serviço de atendimento ao
cliente, dados demográficos bem como fazer o enriquecimento dos dados incorporando dados externos que possam fornecer insights
adicionais, como tendências econômicas ou comportamentais ou de redes sociais. Esses cruzamentos possibilitam criar estratégias de retenção baseadas nos insights do modelo como por exemplo; utilizar as predições do modelo para segmentar os clientes em
grupos de risco e personalizar estratégias de retenção. É possível também desenvolver campanhas de marketing e ações de
retenção específicas para os clientes identificados como de alto risco de churn.

<br>

#### Conformidade com a LGPD (Lei Geral de Proteção de Dados)
A Organização deve manter políticas de governança de dados e ferramentas de segurança em todo o ciclo de vida do dado para que não haja vazamentos de informações ou ainda uso indevido do modelo de aprendizado de máquina. Dentre as ações possíveis de serem tomadas estão:
- Anonimização e Pseudonimização: Garantir que os dados dos clientes estejam anonimizados ou pseudonimizados para proteger a privacidade.
- Consentimento dos Dados: Certificar-se de que há consentimento explícito dos clientes para o uso de seus dados para análises e predições.
- Auditorias de Dados: Realizar auditorias regulares para assegurar que o uso dos dados está em conformidade com a LGPD. Manter registros de todas as atividades de processamento de dados.

<br> 

#### Conclusão
Para manter a eficiência e eficácia de modelos de aprendizado de máquina bem como a inteligência de negócio apurada, é necessário recolher feedback das campanhas de retenção e ajustar o modelo com base nos resultados observados. Ademais, por em prática e otimizar a esteira de MLops fazendo o re-treino do modelo regularmente com dados mais recentes ajuda a manter sua relevância e precisão. Se faz necessário avaliar continuamente o impacto das predições no negócio e ajustar as estratégias conforme os dados forem se alterando. Implementar esses passos ajudará a garantir que o modelo de predição de churn seja robusto, eficaz e em conformidade com as regulamentações, além de proporcionar insights valiosos para a retenção de clientes.
