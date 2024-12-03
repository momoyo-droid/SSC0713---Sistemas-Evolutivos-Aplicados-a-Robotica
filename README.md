# SSC0713---Sistemas-Evolutivos-Aplicados-a-Robotica
Desenvolvimento do projeto I da disciplina de Sistemas Evolutivos Aplicados a Robótica resolvendo o problema da mochila com uma estratégia de algoritmo genético

# Sumário
- [Definição de Algoritmo Genético](#Definição de Algoritmo Genético)

# Definição de Algoritmo Genético
Algoritmo de otimização baseado na Teoria da Evolução de Charles Darwin
___

# Como funciona?
A Teoria da Evolução de Darwin é fundamentada no mecanismo da Seleção Natural, que explica como as espécies evoluem e se adaptam ao ambiente ao longo do tempo. Esse processo ocorre por meio de etapas evolutivas como cruzamento (crossover), mutação, elitismo e seleção por torneio, entre outras. Essas etapas permitem o desenvolvimento de indivíduos mais adaptados, aumentando suas chances de sobrevivência.

Analogamente, os algoritmos genéticos são técnicas inspiradas na evolução biológica que buscam soluções aproximadas para problemas complexos. Eles passam por várias gerações de indivíduos (ou soluções candidatas) para encontrar respostas ótimas. Esse método é especialmente útil para resolver problemas da classe NP-difícil, como o ["Problema do Caixeiro Viajante"](http://www.mat.ufrgs.br/~portosil/caixeiro.html) e o ["Problema da Mochila"](https://www.ime.unicamp.br/~mac/db/2015-1S-122181-1.pdf).

Sendo assim, especificamente para este projeto, vamos trabalhar com o algoritmo evolutivo para o Problema da Mochila!
___

# Estrutura padrão de um Algoritmo Genético
- Inicialização da População <br>
  O primeiro passo é criar uma população inicial de soluções candidatas. O tamanho dessa população é crucial: se for muito pequena, o algoritmo pode convergir rapidamente
  para soluções não tão ótimas, ficando preso em máximos locais. Por outro lado, populações muito grandes aumentam o custo computacional, tornando o processo mais lento. O
  ideal é encontrar um equilíbrio que permita uma boa exploração do espaço de soluções.

- Avaliação de cada indivíduo <br>
  Cada indivíduo da população é avaliado por meio de uma função chamada Fitness. Essa função mede a qualidade da solução que o indivíduo representa. Indivíduos com
  valores de fitness mais altos são considerados mais aptos, ou seja, têm maior chance de "sobreviver" e contribuir para as próximas gerações.

- Seleção de alguns indivíduos <br>
  Com base na avaliação, selecionamos os indivíduos que participarão da próxima fase. O objetivo aqui é garantir que as melhores soluções sejam priorizadas, mas sem
  perder a diversidade da população. Algumas das estratégias de seleção mais comuns incluem: <br>
    - Proporcional ao Fitness: Indivíduos com fitness mais alto têm maior probabilidade de serem escolhidos, mas isso pode levar à convergência precoce. <br>
    - Ranking: Os indivíduos são ordenados com base no fitness, garantindo uma pressão seletiva equilibrada, o que favorece a exploração contínua do espaço de soluções.

- Crossover e Mutação <br>
  Crossover (ou cruzamento): Esta é a fase em que dois indivíduos "pais" combinam suas características para gerar novos "filhos". Genes (cromossomos) de cada pai são
  selecionados aleatoriamente, criando uma nova solução que pode herdar as melhores características de ambos.<br>
  Mutação: Aqui, pequenas alterações são introduzidas nos genes dos indivíduos, com o objetivo de preservar a diversidade genética e evitar que o algoritmo fique preso em
  soluções subótimas. A taxa de mutação deve ser cuidadosamente ajustada — muito alta pode gerar caos (muita aleatoriedade entre os indivíduos), enquanto muito baixa pode
  reduzir a capacidade de exploração.
  
- Concepção da nova geração <br>
  A nova geração deve ter o mesmo tamanho da anterior. Uma técnica comum nessa etapa é o elitismo, que preserva os melhores indivíduos da geração atual, garantindo que as
  soluções mais promissoras não sejam descartadas. Isso contribui para uma convergência mais eficiente, mantendo o progresso acumulado.
  
- Finaliza algoritmo (ou repete os passos até que estar satisfeito com as soluções encontradas) <br>
  O algoritmo genético continua iterando até que uma condição de parada seja atendida. As condições mais comuns incluem: <br>
    - Falta de progresso significativo entre as gerações (convergência). <br>
    - Alcance de um nível de fitness considerado satisfatório. <br>
    - Um número máximo de gerações predefinido.
___

# O Problema da Mochila



