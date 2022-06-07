# Projeto 3 - Reproduzindo o Experimento de um Artigo Científico

**Atividade**

O objetivo geral do projeto é reproduzir um experimento (total ou parcialmente) de um artigo científico. O tema do artigo deve estar relacionado a Ciência de Redes e Saúde.
Para encontrar artigos publicados com dados de redes, fez-se o uso do seguinte link: https://icon.colorado.edu/#!/networks)[https://icon.colorado.edu/#!/networks

A equipe tem  a liberdade de adaptar e simplificar o experimento, conforme a disponibilidade dos dados, dos algoritmos e do grau de dificuldade na reprodução.

Para a reprodução do experimento, pode ser usada qualquer ferramenta/framework de processamento de redes complexas.

# 1. Apresentação
O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação Ciência e Visualização de Dados em Saúde, oferecida no primeiro semestre de 2022, na Unicamp.

|Nome  | RA | Especialização|
|--|--|--|
| Francisco Neto  | 263798  | Aluno especial| 
| Kátia Santana  | 233661  | Mestrado Ciências da Computação|
| Lukas da Rosa  | 183167  | Graduação Elétrica |

# 2. Referência bibliográfica do artigo lido
Reguly T, Breitkreutz A, Boucher L, et al. Comprehensive curation and analysis of global interaction networks in Saccharomyces cerevisiae. J Biol. 2006;5(4):11. doi:10.1186/jbiol36

# 3. Breve descrição do artigo

O artigo escolhido apresenta um estudo de redes biológicas complexas e predição da função gênica que possibilitam métodos de alto rendimento - HTP - a fim de detectar interações genéticas e protéicas. O estudo toma como base a genética da levedura Saccharomyces cerevisiae.

Utilizamos um banco de dados abrangente de interações genéticas e protéicas com evidências experimentais associadas à levedura Saccharomyces cerevisiae, tendo cerca de 33 mil interações combinados com todos os conjuntos de dados  triagem de alto rendimento - HTP.

As pesquisas feitas pelos autores tiveram como fonte de busca o PubMed e rendeu 53.117 publicações que continham dados de interação em um ou mais genes e/ou proteínas de levedura em desenvolvimento. Um total de 5.434 das 5.726 proteínas atualmente previstas são referenciadas pelo menos uma vez na literatura primária.


# 3.1. Resumo - Saccharomyces cerevisiae

Saccharomyces cerevisiae é uma espécie de levedura domesticada há pelo menos 3 mil anos e seu extensivo uso e considerável valor econômico decorrem do fato de que algumas cepas deste fungo unicelular são utilizadas em diversos processos industriais empregados na elaboração de produtos fermentados – como o etanol, e suas cepas são empregadas na alimentação humana e animal. Estudos mostram uma avaliação dos benefícios de sua aplicação na alimentação animal. A Figura abaixo ilustra uma amostra da levedura Saccharomyces cerevisiae.

![Isso é uma imagem](/P3/assets/levedura.jpg)

Há cerca de uma década, o genoma de Saccharomyces cerevisiae gerou dezenas de ferramentas genômicas funcionais para interrogação da função de genes e proteínas, incluindo microarrays de DNA para perfil de expressão gênica global e localização de fatores de ligação ao DNA e um conjunto abrangente de genes cepas de deleção para análise fenotípica. Após a descoberta do genoma, técnicas de triagem de alto rendimento (HTP) destinadas a identificar novos complexos de proteínas e redes de genes começaram a complementar as abordagens bioquímicas e genéticas convencionais.

Além de análises HTP de redes de interação de proteínas de levedura, mapas iniciais de dois híbridos de levedura foram gerados para o verme nematoide Caenorhabditis
elegans, a mosca da fruta Drosophila melanogaster e, mais recentemente, para humanos. Os vários conjuntos de dados gerados por essas técnicas começaram a revelar uma a rede global subjacente à complexidade celular.


# 3.2. Breve descrição do experimento/análise do artigo que foi replicado
Descreva brevemente a parte do artigo cujo experimento ou análise foi reproduzido. Explique o que foi usado como entrada e saída.

# 4. Dados usados como entrada
Dataset	Endereço na Web	Resumo descritivo
Título do Dataset	http://base1.org/	Breve resumo (duas ou três linhas) sobre o dataset.

# 5. Método

O método escolhido para reproduzir o dataset deste artigo foi usar as funções algorítmicas de Kruskal e Prim, além da função Community Detection via Edge Betweenness para construir árvores geradoras mínimas.  Mas, o que exatamente é uma árvore geradora mínima?

Primeiramente é necessário entender o que é uma árvore geradora. Uma árvore geradora é simplesmente um conjunto de arestas do grafo que gera uma árvore. Toda árvore é um grafo conexo acíclico. Mas é mais fácil imaginar o mesmo grafo com pelo menos uma aresta entrando e no máximo uma aresta saindo de cada vértice. Uma árvore geradora  é um subconjunto de um grafo com o mesmo número de vértices que o grafo e arestas igual ao número de vértices -1, isto é, ela é chamada **mínima** se, dentre todas as árvores geradoras que existem no grafo, a soma dos pesos nas arestas dela é o menor possível, conforme mostra a imagem a seguir.

![Isso é uma imagem](/P3/assets/xnQzT.png)

Conforme mencionado anteriormente, o algoritmo de Prim (também conhecido como algoritmo de Jarník) é um algoritmo "ambicioso" que encontra uma árvore geradora mínima para um grafo não direcionado ponderado, ou seja, ele encontra um subconjunto das arestas que forma uma árvore que inclui todos os vértices, onde o peso total de todas as arestas da árvore é minimizado. O algoritmo opera construindo esta árvore um vértice por vez, a partir de um vértice inicial arbitrário, a cada passo adicionando a menor (baixo peso) conexão possível da árvore para outro vértice.

O algoritmo Kruskal é usado para construir uma árvore geradora mínima para um determinado grafo. Ele também tem um custo mínimo para a soma de todos os pesos das arestas em uma árvore geradora. Este algoritmo ordena todas as arestas em ordem crescente de seus pesos de arestas e continua adicionando nós à árvore apenas se a aresta escolhida não formar nenhum ciclo. Além disso, ele escolhe a aresta com um custo mínimo no início e a aresta com um custo máximo no final. Assim, pode-se dizer que o algoritmo de Kruskal faz uma escolha localmente ótima, com a intenção de encontrar a solução ótima global. É por isso que é chamado de algoritmo "ambicioso".

Para aplicação deste modelo foi utilizado a plataforma de código aberto Cytoscape. Nesta plataforma foi utilizado uma função chamada CyFinder que contém as sub-funções utilizadas para análise, são elas: Community Detection - Edge Betweenness e Spanning Forest Kurskal/ Spanning Forest Prim.

## 5.1. Cytoscape

Cytoscape é uma plataforma de software de código aberto que auxilia na visualização e análise de redes moleculares e vias biológicas, bem como expressão gênica. O Cytoscape oferece um conjunto básico de aplicativos principais para executar essas tarefas, mas também oferece uma opção para adicionar plug-ins feitos pelo usuário na forma de arquivos de instalação do Java Archive (JAR) Maven. Esses plug-ins podem ser semelhantes aos aplicativos principais e podem ajudar na visualização, geração e análise da rede. Nosso projeto foi desenvolvido para o Cytoscape 3.8.2 [1], [2]. CyFinder é um aplicativo Cytoscape que auxilia na localização e visualização de subgráficos dentro de uma rede selecionada. O CyFinder realiza suas tarefas envolvendo uma API simples de gráficos e algoritmos de gráfico com tarefas do Cytoscape que convertem as redes do Cytoscape para os gráficos na API e executam os algoritmos. Como o formato de arquivo gráfico padrão ao usar o Cytoscape assume arestas não direcionadas, a primeira funcionalidade do CyFinder é tornar a rede selecionada não direcionada, tornando todas as arestas não direcionadas ou adicionando arestas direcionadas em sentido inverso para todas as arestas direcionadas

## 5.2. Cytoscape - Funções 

CyFinder oferece atualmente três Algoritmos de Community Detection: Fastgreedy, Edge Betweenness, Label Propagation e Walktrap.
Community Detection nos permite encontrar coleções não sobrepostas de genes que são fortemente coexpressos entre si e fracamente coexpressos com genes em outras comunidades. Em Community Detection encontramos clusters de Nodes relacionados em uma Rede.
Os algoritmos de Detecção da Comunidade variam em método; portanto, seus resultados e desempenho diferem. Fastgreedy é o mais rápido, enquanto Edge Betweenness é o mais lento. As Comunidades geradas pelos algoritmos pertencem à estrutura da Comunidade da Rede de entrada com a melhor Modularidade. A modularidade é uma propriedade numérica que dá a qualidade da potencial estrutura da Comunidade de uma Rede. As implementações dos algoritmos de Detecção Comunitária são baseadas naqueles no pacote de software igraph. Os algoritmos têm uma variante sem peso na qual todas as arestas recebem um valor igual de 1 e uma variante ponderada na qual um atributo de peso é escolhido entre os atributos de aresta das redes no Cytoscape.

O algoritmo Edge Betweenness, também chamado de algoritmo de Girvan-Newman, baseia-se na noção de Edge Betweenness. Se encontrarmos todos os caminhos mais curtos entre todos os pares de nós na rede, então podemos definir o Edge Betweenness de uma aresta como o número desses caminhos mais curtos que a incluem. A variante ponderada ajusta os valores de Edge Betweenness para levar em conta os pesos de Edge. O algoritmo começa com uma comunidade com todos os nós, remove a aresta com a maior interatividade da aresta e gera os componentes conectados resultantes como as comunidades da iteração, em seguida, recalcula os valores. As Comunidades com a melhor modularidade são geradas.

# 6. Resultados

A Figura abaixo mostra algumas das redes que foram geradas pela função de detecção de comunidades com a sub-função Egde Betweenness. Cada uma das redes está separada em um arquivo de imagem na pasta /P3/assets/ImageResults. Nela é possível ver cada uma das redes. Também é possível acessar o arquivo PROJET3.cys e ver com detalhes cada uma das redes.

![Isso é uma imagem](/P3/assets/communityall2.png)

Através da função Spanning Forest foi possível chegar à três configurações de árvores geradoras mínimas. 

* Árvore gerado mínima de Kurskal. 

![Isso é uma imagem](/P3/assets/kruskal.png)

* Árvore gerado mínima de Prim. 

![Isso é uma imagem](/P3/assets/prim.png)

* Árvore gerado mínima de Kurskal e Prim atuando em conjunto. 

![Isso é uma imagem](/P3/assets/primandkruskal.png)



