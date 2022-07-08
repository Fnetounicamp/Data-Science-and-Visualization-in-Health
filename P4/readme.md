# Projeto 4 – Classificação de lesões de substância branca no Lúpu

**Atividade**

O objetivo geral do projeto é, a partir de uma classificador treinado para diferenciar lesões isquêmicas e desmielinizantes, identificar qual a etiologia mais provável das lesões presentes em pacientes de Lúpus Eritematoso Sistêmico (SLE).

O conjunto de dados de lesões de pacientes de SLE estão na pasta compartilhada.

# 1. Apresentação
O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação Ciência e Visualização de Dados em Saúde, oferecida no primeiro semestre de 2022, na Unicamp.

|Nome  | RA | Especialização|
|--|--|--|
| Francisco Neto  | 263798  | Aluno especial| 

# 2. Introdução

O Lúpus Eritematoso Sistêmico (LES ou apenas lúpus) é uma doença inflamatória crônica de origem autoimune, cujos sintomas podem surgir em diversos órgãos. São reconhecidos dois tipos principais de lúpus: o **cutâneo**, que se manifesta apenas com manchas na pele (geralmente avermelhadas ou eritematosas e daí o nome lúpus eritematoso), principalmente nas áreas que ficam expostas à luz solar (rosto, orelhas, colo (“V” do decote) e nos braços) e o **sistêmico**, no qual um ou mais órgãos internos são acometidos. 

Neste trabalho é abordado o lúpus sistêmico. Neste caso, as lesões na substância branca do cérebro podem causar um déficit funcional significativo. A figura 1 ilustra como é o Lúpus no cérebro. 

![Isso é uma imagem](/P4/assets/foto01.png)

Assim, o intuito é que seja respondida a seguinte questão de pesquisa: Lúpus são mais semelhantes ao Lúpus de substância branca desmielinizante ou isquêmico, qual a etiologia mais provável das lesões presentes em pacientes de Lúpus Eritematoso Sistêmico? 

# 3. Ferramentas
As ferramentas utilizadas para o desenvolvimento deste trabalho foram:

- Notebook google colab
- Google drive
- Google search

# 4. Preparo e uso dos dados
Pipeline de pré-processamento dos dados.

- Corte das imagens para que todas tenham o mesmo tamanho (150x150)
- Nas imagens de treinamento foram utilizadas funções de modificam a imagem quanto a posição dos pixels de forma horizontal e verticalmente com uma dada probabilidade - 50% - (RandomHorizontalFlip([p]) e RandomVerticalFlip([p])). Assim é possível obter mais imagens para treinamentos. 
- Após foram retirados os atributos, como mínimo e máximo; média; mediana; desvio padrão, de cada um dos conjuntos de imagens (Treinamento, Validação e Teste). 

# 5. Metodologia

- A arquitetura ResNet-18 foi configurada para ser usade de forma pré-treinada.
- Os parâmetros do algoritmo de otimização que apresentou melhores resultados foram a taxa de aprendizagem igual a 0.0001 e fator de momentum igual a 0.9.
- Para taxa de decaimento foi usado um período de 20 com um fator multiplicativo de 0.1.
O que resultou nos parâmetros mostrados na Figura 2. 

![Isso é uma imagem](/P4/assets/foto02.png)

As métricas do modelo de treinamento podem ser visualizados na Figura 3. Nela, é possível verificar que o treinamento teve um aproveitamento de 92.86%. 

![Isso é uma imagem](/P4/assets/foto03.png)

![Isso é uma imagem](/P4/assets/foto04.png)

# 6. Resultados e Discussão

Esta seção deve apresentar o resultado de predição das lesões de LES usando o classificador treinado. Também deve tentar explicar quais os atributos relevantes usados na classificação obtida

apresente os resultados de forma quantitativa e qualitativa
tenha em mente que quem irá ler o relatório é uma equipe multidisciplinar. Descreva questões técnicas, mas também a intuição por trás delas.

# 7. Conclusão

Para ter bom modelo de classificação de de lesões em imagens médicas, é necessário que se tenha um conhecimento multidiciplinar que auxilia na escolhas dos parâmetros mais adequados para tal classificação. O uso destes parâmetros ajudam as Redes Neurais Convolucionais - CNN - a ter um dataset de treinamento muito melhor e, consequentemente, uma melhor predição das lesões.



Destacar os principais desafios enfrentados: Por não ser da área de computação, tive um pouco de dificuldade em acompanhar o andamento e desenvolvimento das atividades, principalmente áquelas que necessitaram de maior profundidade na área da computação. Tive que me dedicar a algun cursos paralelos para ajudar no andamento das atividades. Mesmo assim, por ter um tempo, relativamente, baixo para estudos, o desenvolvimento das atividades P3 e P4 foram mais desafiadoras.

Principais lições aprendidas: Apesar da dificuldade em acompanhar o andamento da turma, consegui ter uma boa noção de como funcionam os algoritmos de Deep Learning, como as imagens médicas são tratadas e o quão importante é a evolução desta tecnologia e disciplina para auxiliar na área da saúde.

Como trabalho Futuro, tendo mais tempo para desenvolvimento e aprendizagem, coloco um aprofundamento no tema de imagens médicas para conseguir parâmetros mais interessantes e que tenham mais informações relevantes a serem extraídas das imagens.

# 8. Referências
- https://pytorch.org/vision/stable/transforms.html
- https://pytorch.org/docs/stable/generated/torch.optim.SGD.html
- https://www.mathworks.com/help/deeplearning/ref/resnet18.html
- https://pytorch.org/docs/stable/generated/torch.optim.lr_scheduler.StepLR.html
- L.Rittner. Data Science and Visualization in Health. Classificação de WML baseado em etiologia. Junho,2022.


