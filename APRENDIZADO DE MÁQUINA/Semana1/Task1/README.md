# Breve resumo sobre os 3 primeiros capítulos do livro - Designing Machine Learning Systems de Chip Huyen

## Capítulo 1

- O capítulo 1 trás informações iniciais sobre o ML (Machine Leaning), abordando aspectos gerais sobre como utiliza-lá, quando se deve utilizar e aprofundando mais os conhecimentos sobre sistemas de ML.
  
  - Quando devemos usar o ML:
Nesse topíco do capitulo 1 é abordado diferentes aspectos que devem ser considerados antes de iniciar um projeto de ML, destacando que o ML não é uma solução mágica que pode resolver todos os problemas e que nem sempre é a solução ótima. A discussão é estruturada em torno de seis considerações principais:
     - Capacidade de Aprendizado:
  O sistema deve ter a capacidade de aprender a partir dos dados disponíveis. Isso contrasta com sistemas que não têm essa capacidade intrínseca, como bancos de dados relacionais.
     - Padrões Complexos:
  ML é apropriado quando existem padrões complexos nos dados que precisam ser aprendidos. Isso inclui problemas em que os padrões não são facilmente discerníveis ou especificáveis manualmente.
     - Disponibilidade de Dados:
  Os dados devem estar disponíveis ou serem coletáveis, pois o aprendizado de máquina depende dos dados para treinar modelos. Problemas que não têm dados disponíveis ou são difíceis de coletar podem não ser adequados para ML.
     - Problema Preditivo:
  ML é mais apropriado para problemas preditivos, nos quais é necessário fazer previsões com base nos dados disponíveis. Isso contrasta com problemas descritivos ou de classificação onde não há necessidade de previsão.
     - Dados não Vistos:
  Os padrões aprendidos pelo modelo são úteis apenas se os dados não vistos compartilharem esses padrões. Isso enfatiza a importância de garantir que os dados de teste e os dados de treinamento venham de distribuições semelhantes.
     - Repetitividade:
  ML é mais adequado para problemas repetitivos, onde cada padrão é repetido várias vezes, tornando mais fácil para as máquinas aprenderem. Isso contrasta com problemas onde cada instância é única ou rara.
     - Custo das Previsões Erradas:
  ML é especialmente adequado quando o custo das previsões erradas é baixo. Isso é relevante em problemas onde os erros são toleráveis ou facilmente corrigíveis.
     - Escala:
  ML é mais apropriado quando o problema é em grande escala, envolvendo um grande volume de dados ou muitas previsões. Isso inclui problemas como classificação de grandes volumes de e-mails ou previsão de resultados em uma escala massiva.
     - Padrões em Constante Mudança:
  ML é útil para problemas onde os padrões estão constantemente mudando, pois os modelos podem ser atualizados com novos dados sem a necessidade de reescrever regras manualmente. Isso é particularmente importante em ambientes dinâmicos, onde as regras fixas podem se tornar rapidamente obsoletas.

  - Compreendendo os sistemas de aprendizado de máquina:
Nesta seção, é analisado como os sistemas de aprendizado de máquina são diferentes tanto da pesquisa em aprendizado de máquina (ou como frequentemente ensinado na escola) quanto do software tradicional, e como entender isso será útil no processo de projetar e desenvolver os sistemas de aprendizado de máquina
     - Aprendizado de máquina em pesquisa versus produção:
As principais diferenças entre a pesquisa em aprendizado de máquina (ML) e a implementação de sistemas de ML em produção na indústria é que enquanto muitas pessoas com experiência em ML adquiriram seu conhecimento por meio da acadêmico, há desafios específicos ao levar os sistemas de ML para a produção em larga escala. Algumas das diferenças-chave entre ML na pesquisa e ML na produção incluem:
        - Requisitos:
  Na pesquisa, o foco costuma ser o desempenho do modelo, visando obter resultados de ponta em conjuntos de dados de referência. Na produção, diferentes partes interessadas têm diferentes requisitos, como desempenho do modelo, latência, entre outros.
        - Prioridade Computacional:
  Enquanto na pesquisa a prioridade está no treinamento rápido do modelo e alto rendimento computacional, na produção é essencial ter inferência rápida e baixa latência.
        - Dados:
  Na pesquisa, os conjuntos de dados são geralmente limpos e bem formatados, enquanto na produção os dados podem ser ruidosos, desestruturados e em constante mudança.
        - Justiça (Fairness):
  A justiça nem sempre é uma prioridade na pesquisa, mas é crucial na produção para evitar viés nos modelos que podem resultar em discriminação.
        - Interpretabilidade:
  Enquanto na pesquisa o foco geralmente é no desempenho do modelo, na produção a interpretabilidade é essencial para que os usuários entendam como as decisões são tomadas e para facilitar a depuração e melhoria do modelo.
      - Aprendizado de máquina versus software tradicional:
  Apesar de ML ser parte da engenharia de software (SWE) e de o desenvolvimento de software tradicional ter sido usado com sucesso em produção por mais de meio século, ainda existem desafios únicos para aplicativos de ML que exigem ferramentas próprias. Enquanto na SWE existe uma separação clara entre código e dados, nos sistemas de ML isso não é tão simples. Os sistemas de ML são compostos tanto por código quanto por dados, e frequentemente incluem artefatos criados a partir desses dois elementos. A tendência dos últimos anos tem mostrado que as aplicações desenvolvidas com os melhores dados tendem a ser mais bem-sucedidas. Isso significa que, em vez de focar apenas na melhoria dos algoritmos de ML, a maioria das empresas precisa se concentrar em melhorar seus conjuntos de dados, que podem mudar rapidamente. Outro desafio é o tamanho dos modelos de ML, que pode ser enorme. Atualmente, é comum que esses modelos tenham centenas de milhões, se não bilhões, de parâmetros, o que exige uma grande quantidade de memória RAM para carregá-los. Isso representa um desafio significativo para colocar esses modelos em produção, especialmente em dispositivos com recursos limitados.

## Capítulo 2 

- O capítulo 2 trás as motivações e o objetivo de se criar um ML, mostrando como estruturar seus problemas, tendo em vista que a dificuldade de seu trabalho pode mudar significativamente dependendo de como você irá estruturar seu problema.

  - Objetivos de Negócios e de Aprendizado de Máquina:
Para que um projeto de ML seja bem-sucedido em uma organização empresarial, é crucial alinhar o desempenho do sistema de ML ao desempenho geral do negócio. Isso significa identificar quais métricas de desempenho do negócio o novo sistema de ML deve influenciar. Além disso, é crucial manter expectativas realistas sobre os retornos esperados do investimento em ML. Embora o ML tenha o potencial de trazer benefícios significativos para as empresas, esses ganhos geralmente exigem investimento a longo prazo e maturidade na adoção da tecnologia. Empresas que investem consistentemente em ML ao longo do tempo tendem a colher os maiores benefícios.

  - Requisitos para sistemas de ML:
Os requisitos especificados para um sistema de ML variam de caso de uso para caso de uso. No entanto, a maioria dos sistemas deve ter essas quatro características: confiabilidade, escalabilidade, manutenibilidade e adaptabilidade.
    - confiabilidade: O sistema deve continuar a executar a função correta no nível desejado de desempenho mesmo diante da adversidade (falhas de hardware ou software e até mesmo erros humanos).
    - escalabilidade: Independentemente da forma como seu sistema cresce, deve haver maneiras razoáveis de lidar com esse crescimento.
    - Capacidade de manutenção: É importante configurar sua infraestrutura de forma que diferentes colaboradores possam trabalhar usando ferramentas com as quais se sintam confortáveis, e quando um problema ocorre, diferentes colaboradores devem ser capazes de trabalhar juntos para identificar o problema e implementar uma solução.
    - Adaptabilidade: Para se adaptar às mudanças nas distribuições de dados e nos requisitos comerciais, o sistema deve ter capacidade tanto para descobrir aspectos de melhoria de desempenho quanto para permitir atualizações sem interrupção do serviço.
    - 
  - Processo interativo:
Desenvolver um sistema de ML é um processo iterativo e, na maioria dos casos, nunca termina. Uma vez que um sistema é colocado em produção, ele precisará ser continuamente monitorado e atualizado.

  - Estruturando problemas de ML:
Saber como o ML pode ser util e utilizado na demanda que foi pedido, a importância de estruturar corretamente os problema,nem todos os problemas são naturalmente problemas de ML e que é necessário identificar claramente as entradas, saídas e a função objetivo que guiará o processo de aprendizado.
    - Tipos de tarefas de ML:
      - Classificação versus regressão: Modelos de classificação classificam entradas em diferentes categorias, enquanto modelos de regressão produzem um valor contínuo.
      - Classificação binária versus multiclasse: A classificação binária envolve apenas duas classes possíveis, enquanto a classificação multiclasse lida com mais de duas classes.
      - Classificação multirrótulo versus multiclasse: Na classificação multirrótulo, um exemplo pode pertencer a múltiplas classes, enquanto na multiclasse cada exemplo pertence a apenas uma classe.
      - Múltiplas maneiras de enquadrar um problema: Alterar a maneira como você enquadra um problema pode torná-lo significativamente mais fácil ou mais difícil.
    - Funções objetivo: Para aprender, um modelo de aprendizado de máquina precisa de uma função objetivo para guiar o processo de aprendizado. Também chamada de função de perda, a função objetivo tem o objetivo de minimizar (ou otimizar) a perda causada por previsões incorretas. Em aprendizado supervisionado, essa perda pode ser calculada comparando as saídas do modelo com as etiquetas verdadeiras.
  - Mente versus dados: O progresso na última década mostra que o sucesso de um sistema de ML depende em grande parte dos dados nos quais foi treinado. Em vez de se concentrarem em melhorar os algoritmos de ML, a maioria das empresas se concentra em gerenciar e melhorar seus dados. Apesar do sucesso de modelos que utilizam enormes quantidades de dados, muitos são céticos em relação à ênfase nos dados como o caminho a seguir.

## Capítulo 3 

- O capítulo 3 aborda o crescimento do aprendizado de máquina nos últimos anos está intimamente ligado ao aumento dos grandes dados, sistemas de dados em larga escala, mesmo sem ML, são complexos e podem ser difíceis de compreender para quem não tem experiência. Este capítulo trás os conceitos básicos de engenharia de dados, desde fontes e formatos de dados até modelos de dados e bancos de dados. Discute também a passagem de dados entre processos e serviços, bem como a distinção entre dados históricos e de streaming, as habilidades em coletar, processar, armazenar e recuperar grandes volumes de dados é crucial para quem deseja construir sistemas de ML em produção.
  - Fonte de dados: Um sistema de ML pode trabalhar com dados de várias fontes diferentes. Esses dados têm características distintas, podem ser usados para diferentes propósitos e requerem diferentes métodos de processamento. Compreender as fontes de onde vêm seus dados pode ajudá-lo a usá-los de maneira mais eficiente.
  - Formato de dados: escolher o formato de dados correto é essencial para garantir a eficiência e a escalabilidade do seu sistema de armazenamento de dados. É importante entender as características de cada formato e considerar as necessidades específicas da sua aplicação ao fazer essa escolha, esta secção destacou a diferença entre formatos de dados em texto e binários, enfatizando a eficiência e a economia de espaço proporcionadas pelos formatos binários. Embora os formatos de texto sejam legíveis e amplamente utilizados, os formatos binários são mais compactos e eficientes em termos de armazenamento, especialmente para conjuntos de dados grandes.
  - modelos de dados: Os modelos de dados descrevem como os dados são representados. Esses modelos determinam não apenas como os sistemas são construídos, mas também os problemas que podem resolver.
     - modelo relacional: O modelo relacional organiza os dados em relações, sendo que cada relação é um conjunto de tuplas. Tabelas são comumente usadas para representar relações, com cada linha sendo uma tupla.
     - Dados Estruturados vs. Não Estruturados: Dados estruturados seguem um esquema pré-definido, facilitando a análise, mas se tornam restritivos se os esquemas mudarem frequentemente. Por outro lado, dados não estruturados não possuem um esquema pré-definido, oferecendo flexibilidade, mas exigindo esforços para extrair estrutura
  - Mecanismos de Armazenamento de Dados e Processamento: Os mecanismos de armazenamento de dados e processamento são componentes fundamentais na infraestrutura de sistemas de informação e aplicativos. Eles fornecem a estrutura para armazenar e acessar dados de forma eficiente e também determinam como esses dados são processados para atender às necessidades de negócios.
  - Modos de fluxo de dados: Os diferentes modos de fluxo de dados e métodos de processamento em sistemas de produção é um aspecto fundamental abordado, e a passagem de dados entre processos, que pode ocorrer de três maneiras principais: por meio de bancos de dados, serviços e transportes em tempo real são detalhados nessa secção, ao passar dados por bancos de dados, um processo escreve os dados em um banco de dados, e outro processo os lê posteriormente. No entanto, isso pode ser inviável se os processos forem executados por diferentes empresas ou se a latência for crítica. Por outro lado, a passagem de dados por serviços envolve o envio de requisições e respostas através de uma rede que conecta os processos. Essa abordagem é comum em arquiteturas orientadas a serviços, permitindo que diferentes componentes sejam desenvolvidos, testados e mantidos independentemente. Uma alternativa é a passagem de dados por transportes em tempo real, onde um intermediário coordena a comunicação entre os serviços. Isso reduz a complexidade e a dependência direta entre os serviços, facilitando a escalabilidade e a manutenção do sistema








       
      
    
