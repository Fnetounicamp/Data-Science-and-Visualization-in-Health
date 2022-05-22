## Projeto Prognóstico: predição de mortalidade

# 1. Apresentação do projeto
O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação Ciência e Visualização de Dados em Saúde, oferecida no primeiro semestre de 2022, na Unicamp.

|Nome  | RA | Especialização|
|--|--|--|
| Francisco Neto  | 263798  | Mestando Aluno Especial|
| Kátia Santana  | 233661  | Mestando Ciências da Computação|
| Lukas da Rosa  | 183167  | Graduação Elétrica |

# 2. Contextualização da Proposta

Este projeto tem como objetivo geral gerar um modelo de prognóstico para realizar a predição de mortalidade de pacientes sintéticos gerados em cenários fictícios de acordo com a base de dados do synthea.
 
 Através desta base de dados foram escolhidos dados relacionados aos diretamente aos pacientes **patients.csv**, consultas dos pacientes com os médicos **encounters.csv**, as condições dos pacientes **conditions.csv** e os dados de planos de saúde de cada paciente **careplans.csv**.  

O foco desta predição está relacionada ao Acidente Vascular Cerebral - AVC. De acordo com o Hospital Proncor, AVC (CID 10 - I64) é o entupimento ou rompimento dos vasos que levam sangue ao cérebro, provocando a paralisia da região afetada no cérebro. Também é chamado de acidente vascular cerebral, derrame cerebral ou Acidente Vascular Encefálico (AVE). 
	
Dependendo da causa do AVC ele pode ser hemorrágico ou isquêmico: 

O AVC isquêmico é o derrame com obstrução da artéria o que impede a passagem de oxigênio para as células cerebrais o que ocasiona sua morte. Essa condição é chamada de isquemia cardíaca. A obstrução da artéria pode acontecer por um trombo, que é um coágulo de sangue que se forma na parede do vaso sanguíneo; ou por um êmbolo, que nada mais é do que um trombo que se desloca pela corrente sanguínea até ficar preso em um vaso sanguíneo menor que sua extensão.

O AVC hemorrágico é o derrame com rompimento de um vaso cerebral, ocorrendo um sangramento (hemorragia) em algum ponto do sistema nervoso.
A hemorragia pode acontecer no interior do tecido cerebral (AVC hemorrágico intraparenquimatoso), que é o mais comum e responsável por 15% de todos os casos de AVC. Contudo, o sangramento também pode ocorrer perto da superfície cerebral, entre o cérebro e a meninge, conhecido como AVC hemorrágico subaracnóideo.

![Isso é uma imagem](https://www.infoescola.com/wp-content/uploads/2008/03/acidente-vascular-cerebral-384907717.jpg)

Apesar do AVC hemorrágico não ser tão comum quanto o isquêmico, pode causar a morte mais frequentemente do que acidentes vasculares cerebrais isquêmicos.

# 2.1. Hipóteses 
1. estabelecer se todos os pacientes deste banco de dados possuem planos de saúde;
2. verificar se há distinção de raças em pessoas que tiveram AVC;
3. estabelecer se pacientes que tiveram maiores gastos hospitalares, tiveram mais chances de viver por mais tempo;
4. verificar se houve sintoma de dor de cabeça forte antes da ocorrência do AVC e morte;

# 2.2. Ferramentas
As ferramentas utilizadas para desenvolvimento deste projeto foram:
- Notebook Jupyter
- Binder
- Orange

# 3. Metodologia
A metodologia escolhida para predição foi verificar se existe uma relação entre o paciente ter ou não um plano de saúde e ter maior ou menor chance de morte. Também foi verificado a questão de raças entre os pacientes, afim de analisar se este fator têm influência no AVC. 

Outro fator verificado foi relacionado à entrada de pacientes no hospital com sintoma de dores de cabeça antes destes pacientes darem entrada com AVC. Por fim, verificaou-se a probabilidade de pacientes internados com dores de cabeça proguedirem esta situação de morte por AVC. 


> Abordagem adotada pelo projeto na predição.
> Justificar as escolhas e (opcionalmente) apresentar fundamentos teóricos.

# 3.1. Bases Adotadas para o Estudo

![Isso é uma imagem](/assets/datafluxo.png)

Em ambos os cenários (scenario01 e scenario02), foram utilizados as bases de dados mostradas na imagem acima. 

# 4. Resultados e Discusão
Esta seção pode opcionalmente ser apresentada em conjunto com a metodologia, intercalando método e resultados.

Descreva etapas para obtenção do modelo, incluindo tratamento de dados, se houve.

Apresente o seu modelo de predição e resultados alcançados. Para cada modelo, apresente no mínimo:

quais os dados sobre o paciente que serão usados para a predição;
qual a abordagem/modelo adotado;
resultados do preditor (apresente da forma mais rica possível, usando tabelas e gráficos - métricas e curva ROC são bem vindos);
breve discussão sobre os resultados obtidos.
Nesta seção, lembre-se das sugestões de análise:

analisar diferentes composições de treinamento e análise do modelo:
um modelo treinado/validado no cenário 1 e testado no cenário 2 e vice-versa;
um modelo treinado e validado com os dados dos dois cenários;
nos modelos dos dois itens anteriores:
houve diferença de resultados?
como analisar e interpretar as diferenças?
testar diferentes composições de dados sobre o paciente para a predição (por exemplo, quantidade diversificadas de número de itens).


Fazer um breve debate sobre os resultados alcançados. Aqui pode ser feita a análise dos possíveis motivos que certos resultados foram alcançados. Por exemplo:

por que seu modelo alcançou (ou não) um bom resultado?
por que o modelo de um cenário não se desempenhou bem em outro?
A discussão dos resultados também pode ser feita opcionalmente na seção de Resultados, na medida em que os resultados são apresentados. Aspectos importantes a serem discutidos: É possível tirar conclusões dos resultados? Quais? Há indicações de direções para estudo? São necessários trabalhos mais profundos?

# 5. Evolução do Projeto
Durante o desenvolvimento do projeto houveram algumas mudanças que alteraram o andamento do projeto, como por exemplo, a escolha da doença a ter seu prognóstico de mortalidade. No primeiro momento foi escolhida a Neutropenia Febril para que, de serta forma, dar uma continuidade ao projeto anterior - P1 - Dados Tabulares. Porém, não houve dados suficientes, dentro desta base de dados, que pudessem ser utilizados para predição. Assim, foi escolhida uma nova doença, que neste caso foi o Acidente Vascular Cerebral. 


# 6. Conclusão
Após processamentos e análises feitas pela equipe, foi verificado que, para o Acidente Vascular Cerebral - AVC, o sintoma mais predominante entre os pacientes com esta doença é o **stress**, visto que todos os pacientes com AVC e que deram entrada na emergência ou no atendimento urgente tiveram este sintoma em consultas anteriores. Para fins de comparação, foi verificado se pacientes que deram entrada na emergência ou no atendimento urgente com sintoma de dores de cabeça e tiveram AVC, neste cenário, nenhum dos pacientes veio a óbito. 

Outro ponto averiguado pela equipe foi se a questão racial tinha algum impacto relacionado ao AVC. Neste cenário, não foi possível dar andamento com a predição pois o número de pacientes com AVC era predominante branco, com um percentual muito baixo de negros e apenas um asiático. 

Para trabalhos futuros, ficou definido pelo grupo que a doença escolhida para predição não foi a melhor, visto que o número de incidências foi pequeno. Sendo assim, ficou acordado que, para os dados disponibilizados pelo Synthea atualmente, a escolha por uma doença de origem respiratória seria mais vantajoso de se obter melhores resultados, visto que existem mais dados, em diferentes bases de dados relacionados às doenças respiratórias. 

Trabalhos Futuros:

o que poderia ser melhorado se houvesse mais tempo?

# Referências Bibliográficas

1. Hospital Proncor. (2021). AVC (derrame cerebral): conheça os sintomas, causas e sequelas | Hospital Proncor.[Online]. Available: https://www.hospitalproncor.com.br/post/avc-derrame-cerebral
2. Info Escila. (2019). Acidente Vascular Cerebral (AVC). [Online]. Available: https://www.infoescola.com/doencas/acidente-vascular-cerebral-avc-derrame/
3. SyntheticMass. (2022). HL7 FHIR API. [Online]. Available: https://synthea.mitre.org/fhir-api
4. Synthetichealth. (2022). SyntheaTM Patient Generator. [Online]. Available: https://github.com/synthetichealth/synthea
5. Synthea Case Study. (2022). Synthea-prognostics. [Online]. Available: https://github.com/santanche/lab2learn/blob/master/sql/synthea/synthea-prognostics.ipynb
6. Find-a-code. (2022). Cerebrovascular accident. [Online]. Available: https://www.findacode.com/snomed/230690007--cerebrovascular-accident.html?hl=230690007


