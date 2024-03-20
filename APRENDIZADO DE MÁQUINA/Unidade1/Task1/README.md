# Breve resumo sobre os 3 primeiros capítulos do livro - Designing Machine Learning Systems de Chip Huyen

## Capítulo 1

- O capítulo 1 trás informações iniciais sobre o ML (Machine Leaning), abordando aspectos gerais sobre como utiliza-lá, quando se deve utilizar e aprofundando mais os conhecimentos sobre sistemas de ML
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
    
