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

fator mais determinante é stress


# 2.2. Ferramentas
As ferramentas utilizadas para desenvolvimento deste projeto foram:
- Notebook Jupyter
- Binder
- Orange
	
# 2.3. Data
Os dados utilizados para este projeto respeita as possíveis implicações éticas. São dados originais gerados para dois cenários e disponibilizados pelo synthea o que garante a reprodutibilidade do processo.

Para treinamento do modelo e teste de predição, os dados utilizados foram retirados de dois cenários de dados (scenario01 e scenario02) disponíveis [neste endereço](https://github.com/santanche/lab2learn/tree/master/data/synthea).

# 3. Metodologia



> Abordagem adotada pelo projeto na predição.
> Justificar as escolhas e (opcionalmente) apresentar fundamentos teóricos.
> 
# 3.1. Bases Adotadas para o Estudo
![Isso é uma imagem](tela1.png)
Em ambos os cenários (scenario01 e scenario02), foram utilizados as bases de dados mostradas na imagem acima. 

# 4. Resultados Obtidos
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


# 5. Evolução do Projeto
Seção opcional se houver histórico de mudanças e evolução relevantes. Relate aqui a evolução do projeto: possíveis problemas enfrentados e possíveis mudanças de trajetória. Relatar o processo para se alcançar os resultados é tão importante quanto os resultados.

# 6. Discussão

Fazer um breve debate sobre os resultados alcançados. Aqui pode ser feita a análise dos possíveis motivos que certos resultados foram alcançados. Por exemplo:

por que seu modelo alcançou (ou não) um bom resultado?
por que o modelo de um cenário não se desempenhou bem em outro?
A discussão dos resultados também pode ser feita opcionalmente na seção de Resultados, na medida em que os resultados são apresentados. Aspectos importantes a serem discutidos: É possível tirar conclusões dos resultados? Quais? Há indicações de direções para estudo? São necessários trabalhos mais profundos?

# 7. Conclusão
Destacar as principais conclusões obtidas no desenvolvimento do projeto.

Destacar os principais desafios enfrentados.

Principais lições aprendidas.

Trabalhos Futuros:

o que poderia ser melhorado se houvesse mais tempo?

# 8. Referências Bibliográficas

* https://www.hospitalproncor.com.br/post/avc-derrame-cerebral#:~:text=O%20AVC%20(CID%2010%20%2D%20I64,Acidente%20Vascular%20Encef%C3%A1lico%20(AVE)
* https://www.infoescola.com/doencas/acidente-vascular-cerebral-avc-derrame/
* https://github.com/santanche/lab2learn/blob/master/sql/synthea/synthea-prognostics.ipynb
* https://www.findacode.com/snomed/
* https://www.findacode.com/snomed/230690007--cerebrovascular-accident.html?hl=230690007
* https://synthea.mitre.org/
* https://github.com/synthetichealth/synthea


