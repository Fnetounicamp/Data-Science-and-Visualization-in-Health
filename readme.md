## Projeto Prognóstico: predição de mortalidade

# 1. Apresentação do projeto
O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação Ciência e Visualização de Dados em Saúde, oferecida no primeiro semestre de 2022, na Unicamp.

|Nome  | RA | Especialização|
|--|--|--|
| Francisco Neto  | 263798  | Mestrado Ciências da Computação| Aluno especial
| Kátia Santana  | 233661  | Mestrado Ciências da Computação|
| Lukas da Rosa  | 183167  | Graduação Elétrica |

# 2. Contextualização da Proposta

Este projeto tem como objetivo gerar um modelo de prognóstico para realizar a predição de mortalidade de pacientes sintéticos gerados em cenários fictícios de acordo com a base de dados do synthea.
 
 Através desta base de dados foram escolhidos dados relacionados:
  1. A pacientes - disponíveis na base de dados **patients.csv**;
  2. Às consultas dos pacientes com os médicos - disponíveis na base de dados  **encounters.csv**;
  3. Às condições dos pacientes - disponíveis na base de dados **conditions.csv** e;
  4. Aos dados de planos de saúde de cada paciente - disponíveis na base de dados **careplans.csv**.  

O foco desta predição está relacionada ao Acidente Vascular Cerebral - AVC. De acordo com o Hospital Proncor, AVC (CID 10 - I64) é o entupimento ou rompimento dos vasos que levam sangue ao cérebro, provocando a paralisia da região afetada no cérebro. Também é chamado de derrame cerebral ou Acidente Vascular Encefálico (AVE). 
	
Dependendo da causa do AVC ele pode ser hemorrágico ou isquêmico: 

O AVC isquêmico é o derrame com obstrução da artéria o que impede a passagem de oxigênio para as células cerebrais o que ocasiona sua morte. Essa condição é chamada de isquemia cardíaca. A obstrução da artéria pode acontecer por um trombo, que é um coágulo de sangue que se forma na parede do vaso sanguíneo; ou por um êmbolo, que nada mais é do que um trombo que se desloca pela corrente sanguínea até ficar preso em um vaso sanguíneo menor que sua extensão.

O AVC hemorrágico é o derrame com rompimento de um vaso cerebral, ocorrendo um sangramento (hemorragia) em algum ponto do sistema nervoso.
A hemorragia pode acontecer no interior do tecido cerebral (AVC hemorrágico intraparenquimatoso), que é o mais comum e responsável por 15% de todos os casos de AVC. Contudo, o sangramento também pode ocorrer perto da superfície cerebral, entre o cérebro e a meninge, conhecido como AVC hemorrágico subaracnóideo.

![Isso é uma imagem](https://www.infoescola.com/wp-content/uploads/2008/03/acidente-vascular-cerebral-384907717.jpg)

Apesar do AVC hemorrágico não ser tão comum quanto o isquêmico, pode causar a morte mais frequentemente do que acidentes vasculares cerebrais isquêmicos.

# 2.1. Hipóteses 
1. Estabelecer se um prognóstico de mortalidade após um AVC está relacionado à utilização ou não de plano de saúde pelo paciente;
2. Estabelecer se a raça de determinado paciente interfere na possibilidade do mesmo ter um AVC;
3. Estabelecer se pacientes que tiveram maiores gastos hospitalares, tiveram mais chance de sobreviver após um AVC;
4. Verificar se houve sintoma de dor de cabeça antes da ocorrência do AVC e morte.

# 2.2. Ferramentas
As ferramentas utilizadas para desenvolvimento deste projeto foram:
- Notebook Jupyter
- Binder
- Orange

# 3. Metodologia
A metodologia escolhida para predição foi verificar se existe uma relação entre o paciente ter ou não um plano de saúde e isso estar associado a ter maior ou menor chance de morte. Também foi verificada a questão de raças entre os pacientes, a fim de analisar se este fator têm influência no AVC. 

Outro fator verificado foi relacionado à entrada de pacientes no hospital com sintoma de dores de cabeça antes destes pacientes darem entrada com AVC. Por fim, verificou-se a probabilidade de pacientes internados com dores de cabeça proguedirem esta situação de morte por AVC. 

# 3.1. Bases Adotadas para o Estudo

![Isso é uma imagem](/assets/datafluxo.png)

Em ambos os cenários (scenario01 e scenario02), foram utilizados as bases de dados mostradas na imagem acima. 

# 4. Resultados e Discussão
Para obtenção do modelo foram utilizados os dois cenários já comentados anteriormente, selecionando os campos mais relevantes para nossa análise, como gênero, raça, etnia, datas das últimas consultas de cada paciente, datas de mortes e a identificação de cada um. Foi utilizada uma proporção fixa de dados de 66%, uma regressão logística com pré-processamento padrão. Também fez-se uso do método de aprendizado conjunto através do Random Forest Regression.

Como resultado, o modelo não alcançou um bom fator desejado devido aos parâmetros escolhidos para predição de mortalidade para estes cenários, visto que os parâmetros escolhidos tiveram poucas ocorrências dentro da base de dados mediante à doença selecionada.

Outro fator que auxiliou na ineficácia dos resultados foi a inexperiência do grupo com o software de aprendizado de máquina - Orange. Estes fatores dificultaram na implementação dos inputs e targets a serem analisados e uso mais eficaz da plataforma. 

# 5. Evolução do Projeto
Durante o desenvolvimento do projeto houveram algumas mudanças que alteraram o objeto de pesquisa do projeto, como por exemplo, a escolha da doença a ter seu prognóstico de mortalidade. No primeiro momento foi escolhida a Neutropenia Febril para, de certa forma, dar uma continuidade ao projeto anterior - P1 - Dados Tabulares. Porém, não houveram dados suficientes na base de dados que pudessem ser utilizados para predição. Assim, foi escolhida uma nova doença, que neste caso foi o Acidente Vascular Cerebral. 
# 6. Resultados Obtidos

**Métricas - Resultados obtidos através dos dados do cenário 01:**
![Isso é uma imagem](/assets/MetricasCenario01.png)

**Matriz de Confusão 01:**

![Isso é uma imagem](/assets/MatrizCenario01.png)

**Curva ROC cenário 01:**	
![Isso é uma imagem](/assets/LR_&_RF_scenario01.png)

**Métricas - Resultados obtidos através dos dados do cenário 02:**
![Isso é uma imagem](/assets/MetricasCenario02.png)

**Matriz de Confusão 02:**

![Isso é uma imagem](/assets/MatrizCenario02.png)

**Curva ROC cenário 02:**
![Isso é uma imagem](/assets/LR_&_RF_scenario02.png)

**Métricas - Resultados obtidos através de uma combinação de dados dos cenários 01 e 02:**
![Isso é uma imagem](/assets/MetricasCenario0102.png)

**Matriz de Confusão - combinação de dados dos cenários 01 e 02:**

![Isso é uma imagem](/assets/MatrizCenario0102.png)

**Curva ROC Combinando os cenários 01 e 02:**
![Isso é uma imagem](/assets/LR_&_RF_cross_validated.png)


# 7. Conclusão
Após processamentos e análises feitas pela equipe, foi verificado que, para o Acidente Vascular Cerebral - AVC, o sintoma mais predominante entre os pacientes com esta doença é o **stress**, visto que todos os pacientes com AVC e que deram entrada na emergência ou no atendimento urgente tiveram este sintoma em consultas anteriores. Para fins de comparação, foi verificado se pacientes que deram entrada na emergência ou no atendimento urgente com sintoma de dores de cabeça e tiveram AVC, neste cenário, nenhum dos pacientes veio a óbito. 

Outro ponto averiguado pela equipe foi se a questão racial tinha algum impacto relacionado ao AVC. Neste cenário, não foi possível dar andamento com a predição pois o número de pacientes com AVC era predominante branco, com um percentual muito baixo de negros e asiáticos. Também foi verificado se o gasto com planos de saúde dos pacientes afetaram a mortalidade dos pacientes com AVC. Como resultados, constatou que, tanto para pacientes que tiveram altos gastos, quanto para pacientes com gastos menores, não houve diferença no resultado final. 

Para trabalhos futuros, ficou definido pelo grupo que a doença escolhida para predição não foi a melhor, visto que o número de incidências foi pequeno. Sendo assim, ficou acordado que, para os dados disponibilizados pelo Synthea atualmente, a escolha por uma doença de origem respiratória seria mais vantajosa de se obter melhores resultados, visto que existem mais dados, em diferentes bases de dados relacionados às doenças respiratórias. 

Caso houvesse maior tempo para discorrer sobre o assunto, seria interessante conseguir aprofundar mais nas ferramentas utilizadas com o intuito de extrair mais informações relevantes para os resultados do desenvolvimento do projeto. 

# Referências Bibliográficas

1. Hospital Proncor. (2021). AVC (derrame cerebral): conheça os sintomas, causas e sequelas | Hospital Proncor.[Online]. Available: https://www.hospitalproncor.com.br/post/avc-derrame-cerebral
2. Info Escila. (2019). Acidente Vascular Cerebral (AVC). [Online]. Available: https://www.infoescola.com/doencas/acidente-vascular-cerebral-avc-derrame/
3. SyntheticMass. (2022). HL7 FHIR API. [Online]. Available: https://synthea.mitre.org/fhir-api
4. Synthetichealth. (2022). SyntheaTM Patient Generator. [Online]. Available: https://github.com/synthetichealth/synthea
5. Synthea Case Study. (2022). Synthea-prognostics. [Online]. Available: https://github.com/santanche/lab2learn/blob/master/sql/synthea/synthea-prognostics.ipynb
6. Find-a-code. (2022). Cerebrovascular accident. [Online]. Available: https://www.findacode.com/snomed/230690007--cerebrovascular-accident.html?hl=230690007


