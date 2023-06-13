# Análise de Dados Exploratória no estado do Amazonas sobre a Síndrome Respiratória Aguda Grave no ano de 2023.


![Capa do Projeto](https://dive.sc.gov.br/images/doencas%20e%20agravos/Doen%C3%A7as%20Definitivas/Banners-SRAG-736x378px.png)

# Sobre o Projeto
As infecções respiratórias são doenças com alta incidência e prevalência na população mundial, sendo a terceira causa de mortes em 2007 (REFERENCIA https://scielosp.org/pdf/rsp/2022.v56/52/pt) . Complicações decorrentes destas infecções, como os quadros de Síndrome Respiratória Aguda Grava (SRAG) levam a necessidade de internação hospitalar e possuem elevada mortalidade (REFERENCIA Hui DSC, Zumla A. Severe acute respiratory syndrome: historical, epidemiologic, and clinical features. Infect Dis Clin North Am 2019; 33 (4): 869-89. https://doi.org/10.1016/j.idc.2019.07.001).  

A alta capacidade de mutação dos vírus causadores destas infecções e as altas taxas de transmissão preocupa autoridades mundiais de saúde e o monitoramento dos dados epidemiológicos se torna de extrema importância afim de planejamento de políticas públicas de promoção da saúde e prevenção de doenças. (referencia https://www.scielo.br/j/rbepid/a/KQ5swCNJ6WrDGjyvq8ypQbd/?lang=pt). 

Em março de 2020, foi decretado pela Organização Mundial de Saúde (OMS), devido o agravamento das notificações em território mundial, estado de pandemia em decorrência da COVID-19, causada pelo vírus SARS-CoV-2, direcionando todos os países a adotarem medidas preventivas, afim de mitigar o alastramento e o colapso dos sistemas de saúde (Referencia https://www.scielo.br/j/rbepid/a/KQ5swCNJ6WrDGjyvq8ypQbd/?lang=pt). 

A partir de tal cenário, o Ministério da Saúde (MS), incorporou o monitoramento de sintomas decorrentes da COVID-19 a vigilância da Síndrome Respiratória Aguda Grave (SRAG), já em monitoramento desde a pandemia de Influenza A (H1N1), ocorrido em 2009.

Mesmo após decretado o fim da pandemia pela OMS, buscou-se entender neste estudo dados epidemiológicos das notificações de Síndrome Respiratória Aguda Grave (SRAG) no Brasil no ano de 2023, utilizando os dados disponibilizados pelo Departamento de Informática do SUS (DATA SUS), divulgados pelo Ministério da Saúde (MS). 

# Índice/Sumário

* [Sobre o Projeto](#sobre-o-projeto)
* [Objetivos](#objetivos)
* [Metodologia](#metodologia)
* [Autores](#autores)
* [Licença](#licença)
* [Referencias](#referencias)


# Objetivos
<p>Para este estudo, buscou-se entender o perfil das notificações de SRAG no Brasil entre janeiro de 2023 e março do mesmo ano, através de uma análise exploratória de dados (Exploratory Data Analysis - EDA), do conjunto de dados SRAG 2021 a 2023 - Banco de Dados de Síndrome Respiratória Aguda Grave - incluindo dados da COVID-19, disponível em 2023. Serão respondidas ao longo deste estudo as seguintes questões: </p>
<p>a)	Qual a média de idade dos pacientes? </p>
<p>b)	Os pacientes em questão receberam as vacinas contra Influenza e COVID-19? </p>
<p>c)	Qual a taxa de internação dos casos notificados? </p>
<p>d)	Qual a taxa de mortalidade dos casos notificados? </p>
<p>e)	Ao longo do protocolo de atendimento, qual o diagnóstico destes pacientes?</p>

# Metodologia
Ao obter o banco de dados de Síndrome respiratória aguda grave, foram localizadas as categorias abaixo.
| Coluna | Descrição | Categoria |
| :----         |     :----:      |          :-----: |
| DT_SIN_PRI |	Data dos primeiros sintomas| 	
|SG_UF_NOT |	Unidade Federativa da notificação |	
|ID_MUNICIP OU CO_MUN_NOT | Município da notificação |
|CS_SEXO | Sexo do paciente |
|DT_NASC | Data de Nascimento do paciente |	
|NU_IDADE_N | Idade do paciente |	
|TP_IDADE | Classificação do intervalo de dias entre o nascimento do paciente e a data de notificação dos primeiros sintomas | <p>1-Dia</p> <p> 2-Mês </p> <p> 3-Ano</p> |
|CS_GESTANT |Informar se paciente está gestante |<p> 1-1º Trimestre </p><p> 2-2º Trimestre</p><p> 3-3º Trimestre</p><p> 4-Idade Gestacional Ignorada</p><p> 5-Não</p><p>6-Não se aplica</p><p> 9-Ignorado</p> |
|CS_RACA | Raça/cor do paciente | <p>1-Branca</p><p> 2-Preta</p><p>  3-Amarela</p><p>  4-Parda</p><p>  5-Indígena</p><p>  9-Ignorado</p> |
|CS_ESCOL_N |	Nível de escolaridade do paciente | </p>0-Sem escolaridade/ Analfabeto </p><p> 1-Fundamental 1º ciclo (1ª a 5ª série) </p><p>  2-Fundamental 2º ciclo (6ª a 9ª série)</p><p> 3- Médio (1º ao 3º ano)</p><p> 4-Superior</p><p> 5-Não se aplica</p><p> 9-Ignorado </p> |
| CS_ZONA | Zona geográfica da residência do paciente |<p> 1-Urbana </p><p>2-Rural </p><p>3-Periurbana </p> <p> 9-Ignorado </p>|
| NOSOCOMIAL	 | Informa se SRAG foi adquirida em internação hospitalar | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p>|
| AVE_SUINO |	Informa se paciente trabalha com aves ou suínos  |	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| FEBRE	 | Paciente apresentou febre |		<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| TOSSE	 | Paciente apresentou tosse |		<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| GARGANTA|	Paciente apresentou dor de garganta |		<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DISPNEIA | Paciente apresentou dispneia  |	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DESC_RESP |	Paciente apresentou desconforto respiratório |		<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| SATURAÇÃO |  Paciente apresentou saturação igual ou menor que 95% | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DIARREIA | Paciente apresentou diarreia |  	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| VOMITO | Paciente apresentou vômito | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |		
| OUTRO_SIN |	Informa se paciente apresentou outro sintoma |	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| OUTRO_DES |	Lista outros sintomas do paciente |	
| FATOR_RISC |	Paciente apresenta fator de risco | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| PUERPERA | Pacientes com até 45 dias pós parto | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| CARDIOPATI |	Paciente possui doença cardiovascular | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| HEMATOLOGI | Paciente possui doença hematológica | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| SIND_DOWN | Paciente possui doença Síndrome de Down | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| HEPATICA | Paciente possui doença hepática | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| ASMA | Paciente possui asma	 | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DIABETES | Paciente possui Diabetes mellitus | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| NEUROLOGIC	| Paciente possui doença neurológica |		<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| PNEUMOPATI	| Paciente possui outras pneumopatias | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| IMUNODEPRE | Paciente possui imunodeficiência/imunodepressão |		<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| RENAL | Paciente possui doença renal	 | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| OBESIDADE |	Paciente possui obesidade | 1	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| OUT_MORBI | Paciente possui outros fatores de risco | 1-	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| MORB_DESC | Lista outros fatores de risco do paciente |	
| VACINA_COV | Informa se o paciente recebeu vacina COVID-19 | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DOSE_1_COV | Data de aplicação da 1º dose da vacina COVID-19 |	
| DOSE_2_COV | Data de aplicação da 2º dose da vacina COVID-19 |	
| DOSE_REF | Data de reforço da vacina COVID-19 |	
| DOSE_2REF |	Data da 2º dose de reforço da vacina COVID-19	|
| VACINA | Informa se paciente recebeu vacina contra gripe na última campanha |	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DT_UT_DOSE | Data da última vacina da gripe que o paciente tomou |	
| ANTIVIRAL |	Paciente fez uso de antiviral durante o tratamento | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| HOSPITAL |	Informa se o paciente foi internado | 	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DT_INTERNA	Data da internação do paciente	
| UTI |	Informa se o paciente foi internado na UTI |	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| DT_ENTUTI |	Data da entrada do paciente na UTI |	
| DT_SAIDUTI |	Data da saída do paciente na UTI|	
| SUPORT_VEN | Paciente fez uso de suporte ventilatório |	 <p>1-Sim, invasivo  </p>  <p>2-Sim, não invasivo </p>  <p> 3-Não. 9-Ignorado </p> |
| PCR_RESUL	| Resultado de teste RT-PCR |		<p>1-Detectável </p> 	<p>2-Não Detectável </p> 	<p>3-Inconclusivo </p> 	<p>4-Não Realizado </p> 	<p>5-Aguardando Resultado. 	<p>9-Ignorado  </p> |
| POS_PCRFLU |	Informa se RT-PCR foi positivo para Influenza |	<p>1-Sim </p> <p> 2-Não </p> <p> 9-Ignorado </p> |
| CLASSI_FIN |	Diagnóstico final do caso |	<p>1-SRAG por influenza </p> <p>2-SRAG por outro vírus respiratório </p> <p>3-SRAG por outro agente etiológico, qual:</p><p> 4-SRAG não especificado </p> <p> 5-SRAG por covid-19 </p> |
| EVOLUCAO |	Evolução do caso |	<p>1-Cura </p> <p> 2-Óbito </p> <p>3- Óbito por outras causas </p> <p> 9-Ignorado </p>| 


# Autores

[Thaina Leal](https://github.com/Thaina-Leal)

# Licença

Este projeto está licenciado sob a Licença MIT,  consulte o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

# Referencias
[Dicionário de Dados](https://s3.sa-east-1.amazonaws.com/ckan.saude.gov.br/SRAG/pdfs/Dicionario_de_Dados_SRAG_Hospitalizado_19.09.2022.pdf)

[DataSUS](https://opendatasus.saude.gov.br/dataset/srag-2021-a-2023)
