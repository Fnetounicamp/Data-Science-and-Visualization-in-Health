## Projeto 3 - Reproduzindo o Experimento de um Artigo Científico

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

# 3. Resumo
Escreva um breve do artigo (com as suas palavras, não deve ser copiado texto do artigo).

# 3.1 Breve descrição do experimento/análise do artigo que foi replicado
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
