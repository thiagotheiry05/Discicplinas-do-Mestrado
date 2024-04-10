# Breve resumo sobre o capítulo 5 do livro - Designing Machine Learning Systems de Chip Huyen

## Capítulo 5

### Resumo

A engenharia de caracteristicas desempenha um papel fundamental no processo de desenvolvimento de modelos de machine learning, influenciando diretamente a capacidade do modelo de aprender padrões e fazer previsões precisas. Ao longo desse processo, se deparamos com uma variedade de técnicas e considerações importantes que moldam a qualidade e eficácia dos recursos utilizados, elas incluem lidar com valores ausentes, escalonamento, discretização, codificação de características categóricas e geração das antigas, mas ainda muito eficazes, características cruzadas, bem como as novas e emocionantes características posicionais. 

 - Começando pelas técnicas, a manipulação adequada de valores ausentes é crucial, pois a presença de dados faltantes pode distorcer as análises e prejudicar a precisão do modelo, você pode preencher os valores ausentes com certos valores (imputação) ou remover os valores ausentes (deleção). Além disso, a escala dos recursos é importante para garantir que recursos com diferentes magnitudes tenham um impacto uniforme no modelo. Também tem técnica de discretização que foi citada no livro por completude, pois raramente foi encontrado discretização útil. A intersecção de características é a técnica de combinar duas ou mais características para gerar novas características, essa técnica é útil para modelar as relações não lineares entre características, porém é importante considerar os problemas potenciais associados a ela, como aumento da dimensionalidade, esparsidade dos dados e dificuldades interpretativas. 

- Um desafio na engenharia de recursos é evitar o vazamento de dados, que ocorre quando informações do rótulo "vazam" para o conjunto de recursos usados para fazer previsões. Isso pode levar a modelos que parecem funcionar bem durante a avaliação, mas falham quando aplicados a dados reais devido à incorporação de informações não disponíveis durante a inferência. Detectar e mitigar o vazamento de dados requer monitoramento cuidadoso do desempenho do modelo, medição da importância dos recursos e condução de estudos para identificar recursos que contribuem significativamente para o modelo.

- A engenharia de bons recursos envolve a criação de recursos que são úteis para o modelo, generalizáveis para dados não vistos e não introduzem vazamento de dados. Isso pode incluir remover recursos irrelevantes, garantir que os recursos sejam representativos dos dados e considerar o impacto potencial de cada recurso no desempenho do modelo. A importância do recurso mede a contribuição de um recurso para o desempenho geral do modelo e é uma consideração importante na avaliação e interpretação do modelo. Em última análise, a engenharia de recursos desempenha um papel crítico na criação de modelos de machine learning eficazes e precisos. Ao entender e aplicar adequadamente técnicas de engenharia de recursos, os engenheiros de dados podem melhorar a qualidade dos modelos e garantir que produzam resultados precisos e confiáveis em uma variedade de cenários.

### Principais pontos:

- Handling Missing Values:
O tratamento de valores ausentes é uma parte crucial da engenharia de recursos e envolve decidir como lidar com pontos de dados que estão faltando em um conjunto de dados. Isso pode incluir preenchimento de valores ausentes com estatísticas resumidas, remoção de registros com valores ausentes ou imputação de valores ausentes com base em outros dados disponíveis.

- Scaling:
O dimensionamento refere-se ao processo de normalização dos valores dos recursos para uma escala específica. Isso é importante para garantir que os recursos com diferentes magnitudes tenham um impacto uniforme no modelo durante o treinamento.

- Discretization:
A discretização envolve a transformação de recursos contínuos em recursos discretos, dividindo-os em intervalos ou categorias. Isso pode ser útil para simplificar a complexidade do modelo ou para lidar com requisitos específicos de algoritmos.

- Encoding Categorical Features:
A codificação de recursos categóricos é o processo de transformar variáveis categóricas em uma forma numérica que possa ser utilizada por algoritmos de aprendizado de máquina. Isso pode ser feito por meio de técnicas como codificação one-hot, codificação ordinal ou codificação de frequência.

- Feature Crossing:
A cruzamento de recursos é a técnica de combinar dois ou mais recursos para gerar novos recursos. Isso é útil para modelar relacionamentos não lineares entre os recursos e pode ser especialmente útil para modelos que têm dificuldade em aprender esses relacionamentos.

- Discrete and Continuous Positional Embeddings:
As incrustações posicionais discretas e contínuas são técnicas usadas em aplicações de aprendizado de máquina, como processamento de linguagem natural (NLP) e visão computacional, para representar a posição de elementos em uma sequência de dados. Isso é importante para modelos como o Transformer, que processa dados em paralelo e requer informações explícitas sobre a posição dos elementos.

- Data Leakage:
O vazamento de dados refere-se à situação em que informações do rótulo vazam para o conjunto de recursos usados para fazer previsões. Isso pode levar a modelos que parecem funcionar bem durante a avaliação, mas falham quando aplicados a dados reais devido à incorporação de informações não disponíveis durante a inferência.

- Common Causes for Data Leakage:
Este tópico explora as causas comuns de vazamento de dados, como divisão incorreta de dados, escala antes da divisão, preenchimento de valores ausentes com base em toda a população de dados e manipulação inadequada de duplicatas.

- Detecting Data Leakage:
Detectar vazamento de dados envolve monitorar o desempenho do modelo, medir a importância dos recursos e conduzir estudos de ablação para identificar recursos que contribuem significativamente para o modelo. Também é importante verificar novos recursos adicionados ao modelo para garantir que não incorporem vazamentos de dados.

- Engineering Good Features:
Engenharia de bons recursos refere-se à criação de recursos que são úteis para o modelo, generalizáveis para dados não vistos e não introduzem vazamento de dados. Isso envolve remover recursos irrelevantes, garantir que os recursos sejam representativos dos dados e considerar o impacto potencial de cada recurso no desempenho do modelo.

- Feature Importance:
A importância do recurso mede a contribuição de um recurso para o desempenho geral do modelo. Isso pode ser medido usando técnicas como SHAP (SHapley Additive exPlanations) ou funções de importância de recurso integradas em algoritmos específicos, como XGBoost.

- Feature Generalization:
A generalização do recurso refere-se à capacidade de um recurso de funcionar bem em dados não vistos. Isso envolve garantir que os recursos tenham uma cobertura adequada e uma distribuição de valores que se sobrepõe entre os conjuntos de treinamento e teste. Recursos que não generalizam bem podem levar a modelos que não se comportam adequadamente em dados 


### Identificação das Melhores Práticas:

Na engenharia de recursos, algumas práticas são especialmente críticas para o sucesso de um modelo de aprendizado de máquina. Das mencionados no capítulo, vale ressaltar: 

- Tratamento de Valores Ausentes: Lidar adequadamente com valores ausentes é crucial para garantir a qualidade dos dados de entrada do modelo. A presença de valores ausentes pode distorcer as estimativas do modelo e afetar negativamente seu desempenho. Preencher esses valores com estatísticas resumidas, remover registros ou imputar valores ausentes com base em outras informações disponíveis são abordagens comuns para lidar com esse problema.

- Dimensionamento de Recursos: Dimensionar os recursos é importante para garantir que eles tenham magnitudes comparáveis e não influenciem desproporcionalmente o modelo durante o treinamento. O dimensionamento ajuda a evitar que recursos com escalas diferentes dominem a contribuição para a função de custo do modelo, garantindo uma convergência mais rápida e estável durante o treinamento.

- Manipulação de Recursos Categóricos: Codificar adequadamente os recursos categóricos é essencial para transformá-los em uma forma numérica utilizável pelos algoritmos de aprendizado de máquina. A escolha da técnica de codificação adequada, como codificação one-hot, codificação ordinal ou codificação de frequência, pode impactar significativamente o desempenho do modelo.

- Criação de Novos Recursos: O cruzamento de recursos é uma prática valiosa para modelar relacionamentos não lineares entre os recursos e melhorar o desempenho do modelo. Ao combinar dois ou mais recursos para gerar novos recursos, os engenheiros de dados podem capturar informações mais ricas e complexas, possibilitando que o modelo aprenda padrões mais sutis nos dados.

- Prevenção de Vazamento de Dados: Detectar e prevenir vazamentos de dados é crucial para garantir que o modelo generalize bem para dados reais e não seja influenciado por informações futuras ou inadequadamente correlacionadas. Evitar vazamentos de dados garante que o modelo seja avaliado de forma justa e forneça previsões precisas em situações do mundo real.

Essas práticas são fundamentais porque influenciam diretamente a qualidade dos dados de entrada e, consequentemente, o desempenho e a capacidade de generalização do modelo de aprendizado de máquina.








       
      
    
