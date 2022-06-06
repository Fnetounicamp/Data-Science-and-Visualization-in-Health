
## Reproduzindo o Experimento de um Artigo Científico

# 1. Equipe

|Nome  | RA | Especialização|
|--|--|--|
| Francisco Neto  | 263798  | Mestrado Ciências da Computação| Aluno especial
| Kátia Santana  | 233661  | Mestrado Ciências da Computação|
| Lukas da Rosa  | 183167  | Graduação Elétrica |

# 2. Contextualização da Proposta 



# 2.1. Resumo artigo
1. Estabelecer se um prognóstico de mortalidade após um AVC está relacionado à utilização ou não de plano de saúde pelo paciente;
2. Estabelecer se a raça de determinado paciente interfere na possibilidade do mesmo ter um AVC;
3. Estabelecer se pacientes que tiveram maiores gastos hospitalares, tiveram mais chance de sobreviver após um AVC;
4. Verificar se houve sintoma de dor de cabeça antes da ocorrência do AVC e morte.

# 2.2. Metodologia do artigo
As ferramentas utilizadas para desenvolvimento deste projeto foram:
- Notebook Jupyter
- Binder
- Orange

# 2.3. Metodologia proposta
A metodologia escolhida para predição foi verificar se existe uma relação entre o paciente ter ou não um plano de saúde e isso estar associado a ter maior ou menor chance de morte. Também foi verificada a questão de raças entre os pacientes, a fim de analisar se este fator têm influência no AVC. 

Outro fator verificado foi relacionado à entrada de pacientes no hospital com sintoma de dores de cabeça antes destes pacientes darem entrada com AVC. Por fim, verificou-se a probabilidade de pacientes internados com dores de cabeça proguedirem esta situação de morte por AVC. 

# 2.3. Resultados

![Isso é uma imagem](/P2/assets/datafluxo.png)

Em ambos os cenários (scenario01 e scenario02), foram utilizados as bases de dados mostradas na imagem acima. 

# 3. Discussão
Para obtenção do modelo foram utilizados os dois cenários já comentados anteriormente, selecionando os campos mais relevantes para nossa análise, como gênero, raça, etnia, datas das últimas consultas de cada paciente, datas de mortes e a identificação de cada um. Foi utilizada uma proporção fixa de dados de 66%, uma regressão logística com pré-processamento padrão. Também fez-se uso do método de aprendizado conjunto através do Random Forest Regression.

Como resultado, o modelo não alcançou um bom fator desejado devido aos parâmetros escolhidos para predição de mortalidade para estes cenários, visto que os parâmetros escolhidos tiveram poucas ocorrências dentro da base de dados mediante à doença selecionada.

Outro fator que auxiliou na ineficácia dos resultados foi a inexperiência do grupo com o software de aprendizado de máquina - Orange. Estes fatores dificultaram na implementação dos inputs e targets a serem analisados e uso mais eficaz da plataforma. 

# Referências Bibliográficas

1. Hospital Proncor. (2021). AVC (derrame cerebral): conheça os sintomas, causas e sequelas | Hospital Proncor.[Online]. Available: https://www.hospitalproncor.com.br/post/avc-derrame-cerebral
2. Info Escila. (2019). Acidente Vascular Cerebral (AVC). [Online]. Available: https://www.infoescola.com/doencas/acidente-vascular-cerebral-avc-derrame/
3. SyntheticMass. (2022). HL7 FHIR API. [Online]. Available: https://synthea.mitre.org/fhir-api
4. Synthetichealth. (2022). SyntheaTM Patient Generator. [Online]. Available: https://github.com/synthetichealth/synthea
5. Synthea Case Study. (2022). Synthea-prognostics. [Online]. Available: https://github.com/santanche/lab2learn/blob/master/sql/synthea/synthea-prognostics.ipynb
6. Find-a-code. (2022). Cerebrovascular accident. [Online]. Available: https://www.findacode.com/snomed/230690007--cerebrovascular-accident.html?hl=230690007


