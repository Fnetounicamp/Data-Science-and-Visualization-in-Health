## Projeto Prognóstico: predição de mortalidade

# Apresentação do projeto
O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação Ciência e Visualização de Dados em Saúde, oferecida no primeiro semestre de 2022, na Unicamp.

|Nome  | RA | Especialização|
|--|--|--|
| Francisco Neto  | 263798  | Mestando Aluno Especial|
| Kátia Santana  | 233661  | XXX|
| Lukas da Rosa  | 183167  | XXX|

## Contextualização da Proposta

  Este projeto tem como objetivo geral gerar um modelo de prognóstico para realizar a predição de mortalidade de pacientes sintéticos gerados em cenários fictícios de acordo com a base de dados do synthea.
	Através desta base de dados foram escolhidos dados relacionados aos diretamente aos pacientes **patients.csv**, consultas dos pacientes com os médicos **encounters.csv**, as condições dos pacientes **conditions.csv** e os dados de planos de saúde de cada paciente **careplans.csv**.  

# Ferramentas
	As ferramentas utilizadas para desenvolvimento deste projeto foram:
	- Notebook Jupyter
	- Binder
	- Orange
	
# Data
  Os dados utilizados para este projeto respeita as possíveis implicações éticas. São dados originais gerados para dois cenários e disponibilizados pelo synthea o que garante a reprodutibilidade do processo.
  
# Notebooks         
  [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Fnetounicamp/p2prognostico/HEAD)

## Metodologia
	
> Abordagem adotada pelo projeto na predição.
> Justificar as escolhas e (opcionalmente) apresentar fundamentos teóricos.
> 
# Bases Adotadas para o Estudo
scenario01
scenario02

## Resultados Obtidos
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


## Evolução do Projeto
Seção opcional se houver histórico de mudanças e evolução relevantes. Relate aqui a evolução do projeto: possíveis problemas enfrentados e possíveis mudanças de trajetória. Relatar o processo para se alcançar os resultados é tão importante quanto os resultados.

## Discussão

Fazer um breve debate sobre os resultados alcançados. Aqui pode ser feita a análise dos possíveis motivos que certos resultados foram alcançados. Por exemplo:

por que seu modelo alcançou (ou não) um bom resultado?
por que o modelo de um cenário não se desempenhou bem em outro?
A discussão dos resultados também pode ser feita opcionalmente na seção de Resultados, na medida em que os resultados são apresentados. Aspectos importantes a serem discutidos: É possível tirar conclusões dos resultados? Quais? Há indicações de direções para estudo? São necessários trabalhos mais profundos?

## Conclusão
Destacar as principais conclusões obtidas no desenvolvimento do projeto.

Destacar os principais desafios enfrentados.

Principais lições aprendidas.

Trabalhos Futuros:

o que poderia ser melhorado se houvesse mais tempo?

## Referências Bibliográficas

* https://github.com/santanche/lab2learn/blob/master/sql/synthea/synthea-prognostics.ipynb
* https://www.findacode.com/snomed/
* https://www.findacode.com/snomed/230690007--cerebrovascular-accident.html?hl=230690007
* https://synthea.mitre.org/
* https://github.com/synthetichealth/synthea


