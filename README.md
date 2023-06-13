# Análise de Dados Exploratória no estado do Amazonas sobre a Síndrome Respiratória Aguda Grave no ano de 2023.


![Capa do Projeto](https://dive.sc.gov.br/images/doencas%20e%20agravos/Doen%C3%A7as%20Definitivas/Banners-SRAG-736x378px.png)

# Sobre o Projeto
As infecções respiratórias são doenças com alta incidência e prevalência na população mundial, sendo a terceira causa de mortes em 2007 (REFERENCIA https://scielosp.org/pdf/rsp/2022.v56/52/pt) . Complicações decorrentes destas infecções, como os quadros de Síndrome Respiratória Aguda Grava (SRAG) levam a necessidade de internação hospitalar e possuem elevada mortalidade (REFERENCIA Hui DSC, Zumla A. Severe acute respiratory syndrome: historical, epidemiologic, and clinical features. Infect Dis Clin North Am 2019; 33 (4): 869-89. https://doi.org/10.1016/j.idc.2019.07.001).  

A alta capacidade de mutação dos vírus causadores destas infecções e as altas taxas de transmissão preocupa autoridades mundiais de saúde e o monitoramento dos dados epidemiológicos se torna de extrema importância afim de planejamento de políticas públicas de promoção da saúde e prevenção de doenças. (referencia https://www.scielo.br/j/rbepid/a/KQ5swCNJ6WrDGjyvq8ypQbd/?lang=pt). 

Em março de 2020, foi decretado pela Organização Mundial de Saúde (OMS), devido o agravamento das notificações em território mundial, estado de pandemia em decorrência da COVID-19, causada pelo vírus SARS-CoV-2, direcionando todos os países a adotarem medidas preventivas, afim de mitigar o alastramento e o colapso dos sistemas de saúde (Referencia https://www.scielo.br/j/rbepid/a/KQ5swCNJ6WrDGjyvq8ypQbd/?lang=pt). 

A partir de tal cenário, o Ministério da Saúde (MS), incorporou o monitoramento de sintomas decorrentes da COVID-19 a vigilância da Síndrome Respiratória Aguda Grave (SRAG), já em monitoramento desde a pandemia de Influenza A (H1N1), ocorrido em 2009.

Mesmo após decretado o fim da pandemia pela OMS, buscou-se entender neste estudo dados epidemiológicos das notificações de Síndrome Respiratória Aguda Grave (SRAG) no Brasil no ano de 2023, utilizando os dados disponibilizados pelo Departamento de Informática do SUS (DATA SUS), divulgados pelo Ministério da Saúde (MS). 

# Índice/Sumário

* [Introdução](#sobre-o-projeto)
* [Objetivos](#objetivos)
* [Metodologia](#metodologia)
* [Autores](#autores)
* [Licença](#licença)
* [Referencias](#referencias)


# Objetivos
Para este estudo, buscou-se entender o perfil das notificações de SRAG no Brasil entre janeiro de 2023 e março do mesmo ano, através de uma análise exploratória de dados (Exploratory Data Analysis - EDA), do conjunto de dados SRAG 2021 a 2023 - Banco de Dados de Síndrome Respiratória Aguda Grave - incluindo dados da COVID-19, disponível em 2023. Serão respondidas ao longo deste estudo as seguintes questões:
a)	Qual a média de idade dos pacientes?
b)	Os pacientes em questão receberam as vacinas contra Influenza e COVID-19?
c)	Qual a taxa de internação dos casos notificados?
d)	Qual a taxa de mortalidade dos casos notificados?
e)	Ao longo do protocolo de atendimento, qual o diagnóstico destes pacientes?

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
|TP_IDADE | Classificação do intervalo de dias entre o nascimento do paciente e a data de notificação dos primeiros sintomas | 1-Dia  2-Mês  3-Ano |
|CS_GESTANT |Informar se paciente está gestante | 1-1º Trimestre. 2-2º Trimestre. 3-3º Trimestre. 4-Idade Gestacional Ignorada. 5-Não. 6-Não se aplica. 9-Ignorado. |
|CS_RACA | Raça/cor do paciente | 1-Branca. 2-Preta.  3-Amarela.  4-Parda.  5-Indígena.  9-Ignorado. |
|CS_ESCOL_N |	Nível de escolaridade do paciente | 0-Sem escolaridade/ Analfabeto. 1-Fundamental 1º ciclo (1ª a 5ª série). 2-Fundamental 2º ciclo (6ª a 9ª série). 3- Médio (1º ao 3º ano). 4-Superior. 5-Não se aplica. 9-Ignorado |
| CS_ZONA | Zona geográfica da residência do paciente | 1-Urbana. 2-Rural. 3-Periurbana.  9-Ignorado|
| NOSOCOMIAL	 | Informa se SRAG foi adquirida em internação hospitalar | 1-Sim. 2-Não. 9-Ignorado |
| AVE_SUINO |	Informa se paciente trabalha com aves ou suínos  |1-Sim. 2-Não. 9-Ignorado |
| FEBRE	 | Paciente apresentou febre |	1-Sim. 2-Não. 9-Ignorado |
| TOSSE	 | Paciente apresentou tosse |	1-Sim. 2-Não. 9-Ignorado |
| GARGANTA|	Paciente apresentou dor de garganta |	1-Sim. 2-Não. 9-Ignorado |
| DISPNEIA | Paciente apresentou dispneia  |1-Sim. 2-Não. 9-Ignorado |
| DESC_RESP |	Paciente apresentou desconforto respiratório |	1-Sim. 2-Não. 9-Ignorado |
| SATURAÇÃO |  Paciente apresentou saturação igual ou menor que 95% | 1-Sim. 2-Não. 9-Ignorado |
| DIARREIA | Paciente apresentou diarreia |  1-Sim. 2-Não. 9-Ignorado |
| VOMITO | Paciente apresentou vômito | 1-Sim. 2-Não. 9-Ignorado |		
| OUTRO_SIN |	Informa se paciente apresentou outro sintoma | 1-Sim. 2-Não. 9-Ignorado |
| OUTRO_DES |	Lista outros sintomas do paciente |	
| FATOR_RISC |	Paciente apresenta fator de risco | 1-Sim. 2-Não. 9-Ignorado |
| PUERPERA | Pacientes com até 45 dias pós parto | 1-Sim. 2-Não. 9-Ignorado |
| CARDIOPATI |	Paciente possui doença cardiovascular | 1-Sim. 2-Não. 9-Ignorado |
| HEMATOLOGI | Paciente possui doença hematológica | 1-Sim. 2-Não. 9-Ignorado |
| SIND_DOWN | Paciente possui doença Síndrome de Down | 1-Sim. 2-Não. 9-Ignorado |
| HEPATICA | Paciente possui doença hepática | 1-Sim. 2-Não. 9-Ignorado |
| ASMA | Paciente possui asma	 | 1-Sim. 2-Não. 9-Ignorado |
| DIABETES | Paciente possui Diabetes mellitus | 1-Sim. 2-Não. 9-Ignorado |
| NEUROLOGIC	| Paciente possui doença neurológica |	1-Sim. 2-Não. 9-Ignorado |
| PNEUMOPATI	| Paciente possui outras pneumopatias | 1-Sim. 2-Não. 9-Ignorado |
| IMUNODEPRE | Paciente possui imunodeficiência/imunodepressão |	1-Sim. 2-Não. 9-Ignorado |
| RENAL | Paciente possui doença renal	 | 1-Sim. 2-Não. 9-Ignorado |
| OBESIDADE |	Paciente possui obesidade | 1-Sim. 2-Não. 9-Ignorado |
| OUT_MORBI | Paciente possui outros fatores de risco | 1-Sim. 2-Não. 9-Ignorado |
| MORB_DESC | Lista outros fatores de risco do paciente |	
| VACINA_COV | Informa se o paciente recebeu vacina COVID-19 | 1-Sim. 2-Não. 9-Ignorado |
| DOSE_1_COV | Data de aplicação da 1º dose da vacina COVID-19 |	
| DOSE_2_COV | Data de aplicação da 2º dose da vacina COVID-19 |	
| DOSE_REF | Data de reforço da vacina COVID-19 |	
| DOSE_2REF |	Data da 2º dose de reforço da vacina COVID-19	|
| VACINA | Informa se paciente recebeu vacina contra gripe na última campanha | 1-Sim. 2-Não. 9-Ignorado |
| DT_UT_DOSE | Data da última vacina da gripe que o paciente tomou |	
| ANTIVIRAL |	Paciente fez uso de antiviral durante o tratamento | 1-Sim. 2-Não. 9-Ignorado |
| HOSPITAL |	Informa se o paciente foi internado | 1-Sim. 2-Não. 9-Ignorado |
| DT_INTERNA	Data da internação do paciente	
| UTI |	Informa se o paciente foi internado na UTI | 1-Sim. 2-Não. 9-Ignorado |
| DT_ENTUTI |	Data da entrada do paciente na UTI |	
| DT_SAIDUTI |	Data da saída do paciente na UTI|	
| SUPORT_VEN | Paciente fez uso de suporte ventilatório |	1-Sim, invasivo. 2-Sim, não invasivo. 3-Não. 9-Ignorado |
| PCR_RESUL	| Resultado de teste RT-PCR |	1-Detectável. 2-Não Detectável. 3-Inconclusivo. 4-Não Realizado. 5-Aguardando Resultado. 9-Ignorado |
| POS_PCRFLU |	Informa se RT-PCR foi positivo para Influenza |	1-Sim. 2-Não. 9-Ignorado |
| CLASSI_FIN |	Diagnóstico final do caso |	1-SRAG por influenza. 2-SRAG por outro vírus respiratório. 3-SRAG por outro agente etiológico, qual:. 4-SRAG não especificado, 5-SRAG por covid-19 |
| EVOLUCAO |	Evolução do caso |	1-Cura. 2-Óbito. 3- Óbito por outras causas.  9-Ignorado | 


# Autores

[Thaina Leal](https://github.com/Thaina-Leal)

# Licença

Este projeto está licenciado sob a Licença MIT,  consulte o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

# Referencias
[Dicionário de Dados](https://s3.sa-east-1.amazonaws.com/ckan.saude.gov.br/SRAG/pdfs/Dicionario_de_Dados_SRAG_Hospitalizado_19.09.2022.pdf)

[DataSUS](https://opendatasus.saude.gov.br/dataset/srag-2021-a-2023)
