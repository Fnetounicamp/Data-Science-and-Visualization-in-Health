# Projeto 3 - Reproduzindo o Experimento de um Artigo Científico

O objetivo geral do projeto é reproduzir um experimento (total ou parcialmente) de um artigo científico. O tema do artigo deve estar relacionado a Ciência de Redes e Saúde.
Para encontrar artigos publicados com dados de redes, fez-se o uso do seguinte link:(https://icon.colorado.edu/#!/networks)[https://icon.colorado.edu/#!/networks)

A equipe teve a liberdade de adaptar e simplificar o experimento, conforme a disponibilidade dos dados, dos algoritmos e do grau de dificuldade na reprodução.

Para a reprodução do experimento, pode ser usada qualquer ferramenta/framework de processamento de redes complexas.

# 1. Apresentação
O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação Ciência e Visualização de Dados em Saúde, oferecida no primeiro semestre de 2022, na Unicamp.

|Nome  | RA | Especialização|
|--|--|--|
| Francisco Neto  | 263798  | Aluno especial| 
| Kátia Santana  | 233661  | Mestrado Ciências da Computação|
| Lukas da Rosa  | 183167  | Graduação Elétrica |

# 2. Referência bibliográfica do artigo lido
(https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1561585/)

https://www.hackerearth.com/practice/algorithms/graphs/minimum-spanning-tree/tutorial/

https://www.simplilearn.com/tutorials/data-structure-tutorial/kruskal-algorithm

Kruskal’s Algorithm for Minimum Spanning Forest, Maximilian P.L. Haslbeck, Peter Lammich, Julian Biendarra, December 14, 2021.

https://en.wikipedia.org/wiki/Prim%27s_algorithm

# 3. Breve descrição do artigo

O artigo apresenta um estudo de redes biológicas complexas e predição da função gênica que possibilitam métodos de alto rendimento - HTP - afim de detectar interações genéticas e proteicas. O estudo toma como base a genética da levedura Saccharomyces cerevisiae.

Foi utilizado um banco de dados abrangente de interações genéticas e proteicas com evidências experimentais associadas à levedura Saccharomyces cerevisiae, tendo cerca de pouco mais de 33 mil interações combinados com todos os conjuntos de dados  triagem de alto rendimento - HTP.

As pesquisas feitas pelos autores tiveram como fonte de busco o PubMed e rendeu 53.117 publicações que continham dados de interação em um ou mais genes e/ou proteínas de levedura em desenvolvimento. Um total de 5.434 das 5.726 proteínas atualmente previstas e são referidas pelo menos uma vez na literatura primária.


# 3.1. Resumo - Saccharomyces cerevisiae

Saccharomyces cerevisiae é uma espécie de levedura domesticada há pelo menos 3 mil anos e seu extensivo uso e considerável valor econômico decorrem do fato de que algumas cepas deste fungo unicelular são utilizadas em diversos processos industriais empregados na elaboração de produtos fermentados – como o etanol, e suas cepas são empregadas na alimentação humana e animal. Estudos mostram uma avaliação dos benefícios de sua aplicação na alimentação animal. A Figura abaixo ilustra uma amostra da levedura Saccharomyces cerevisiae.

![Isso é uma imagem](/P3/assets/levedura.jpg)

A cerca de uma década atrás, o genoma de Saccharomyces cerevisiae gerou dezenas de ferramentas genômicas funcionais para interrogação da função de genes e proteínas, incluindo microarrays de DNA para perfil de expressão gênica global e localização de fatores de ligação ao DNA e um conjunto abrangente de genes cepas de deleção para análise fenotípica. Após a descoberta do genoma, técnicas de triagem de alto rendimento (HTP) destinadas a identificar novos complexos de proteínas e redes de genes começaram a complementar as abordagens bioquímicas e genéticas convencionais.

Além de análises HTP de redes de interação de proteínas de levedura, mapas iniciais de dois híbridos de levedura foram gerados para o verme nematoide Caenorhabditis
elegans, a mosca da fruta Drosophila melanogaster e, mais recentemente, para humanos. Os vários conjuntos de dados gerados por essas técnicas começaram a revelar uma a rede global subjacente à complexidade celular.


# 3.2. Breve descrição do experimento/análise do artigo que foi replicado
Descreva brevemente a parte do artigo cujo experimento ou análise foi reproduzido. Explique o que foi usado como entrada e saída.

# 4. Dados usados como entrada
Dataset	Endereço na Web	Resumo descritivo
Título do Dataset	http://base1.org/	Breve resumo (duas ou três linhas) sobre o dataset.

# 5. Método

Na ciência da computação, o algoritmo de Prim (também conhecido como algoritmo de Jarník) é um algoritmo ganancioso que encontra uma árvore geradora mínima para um grafo não direcionado ponderado. Isso significa que ele encontra um subconjunto das arestas que forma uma árvore que inclui todos os vértices, onde o peso total de todas as arestas da árvore é minimizado. O algoritmo opera construindo esta árvore um vértice por vez, a partir de um vértice inicial arbitrário, a cada passo adicionando a conexão mais barata possível da árvore para outro vértice.

Como mencionado anteriormente, o algoritmo Kruskal é usado para gerar uma árvore geradora mínima para um determinado grafo. Mas, o que exatamente é uma árvore geradora mínima? Uma árvore geradora mínima é um subconjunto de um grafo com o mesmo número de vértices que o grafo e arestas igual ao número de vértices -1. Ele também tem um custo mínimo para a soma de todos os pesos das arestas em uma árvore geradora.   

O algoritmo de Kruskal ordena todas as arestas em ordem crescente de seus pesos de arestas e continua adicionando nós à árvore apenas se a aresta escolhida não formar nenhum ciclo. Além disso, ele escolhe a aresta com um custo mínimo no início e a aresta com um custo máximo no final. Assim, pode-se dizer que o algoritmo de Kruskal faz uma escolha localmente ótima, com a intenção de encontrar a solução ótima global. É por isso que é chamado de algoritmo ganancioso.



Método usado para a análise -- adaptações feitas, ferramentas utilizadas, abordagens de análise adotadas e respectivos algoritmos. Etapas do processo reproduzido.

# 6. Resultados
Apresente os resultados obtidos pela sua adaptação. Confronte os seus resultados com aqueles do artigo. Esta seção opcionalmente pode ser apresentada em conjunto com o método.
