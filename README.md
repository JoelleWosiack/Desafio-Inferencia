# Desafio de Inferência

## Depressão e Hábitos Saudáveis
<br>
O transtorno depressivo representa um grande problema de saúde pública e é apontado como uma das principais causas de doenças e debilitações segundo a Organização Mundial da Saúde (OMS). A depressão resulta de uma interação complexa de fatores sociais, psicológicos e biológicos e, embora o acesso a diagnósticos e tratamentos esteja aumentando, muitos ainda não possuem acesso ao controle adequado dos sintomas depressivos.
<br>
Para garantir um estilo de vida saudável, a OMS recomenda a prática regular de exercícios, bem como a adoção de uma dieta saudável rica em alimentos in natura e com reduzido teor de gordura saturada, sal e açúcares refinados.
<br>
Neste desafio, utilizaremos dados de uma pesquisa realizada anualmente nos Estados Unidos para avaliar (1) qual o perfil de indivíduos (adultos maiores de 18 anos) com sintomas depressivos nos EUA no período de 2005-2006, e (2) se hábitos saudáveis de alimentação e atividade física estão associados a menores índices de depressão nesta população.
<br>

## Aspectos da análise

<br>
1. Qual o tipo de estudo está sendo empregado pelo NHANES? experimental ou observacional?
<br>
2. Discuta as possíveis fontes de viés presentes na análise
<br>
3. A partir da análise realizada, podemos afirmar que hábitos saudáveis possuem um efeito causal na prevenção de depressão?
<br>
4. Quais são as fraquezas das análises realizadas? O que pode ser feito para melhorar?
<br>
5. Quais outras variáveis/informações poderiam ter sido coletadas para esta análise?
<br>

## Informações das bases

<br>

## National Health and Nutrition Examination Survey

<br>
O National Health and Nutrition Examination Survey (NHANES) é uma pesquisa anual conduzida pelo National Center for Health Statistics (NCHS) do Centro de Controle e Prevenção de Doenças (Centers for Disease Control - CDC) para avaliar a saúde e nutrição de adultos e crianças dos Estados Unidos. Dados coletados incluem questões demográficas, socioeconômicas, dietéticas e relacionadas à saúde, com o componente de exame contendo medidas médicas, odontológicas, fisiológicas e exames laboratoriais.
<br>
A pesquisa examina uma amostra de cerca de 5.000 pessoas a cada ano, selecionada à partir de amostragem complexa a fim de selecionar uma amostra representativa da população civil não institucionalizada dos EUA. Sendo assim, as análises utilizando este estudo devem ser realizadas utilizando técnicas e ferramentas que levem em conta a amostragem complexa.
<br>
Neste desafio, no entanto, iremos assumir que os dados foram obtidos usando uma amostra aleatória da população de interesse e utilizaremos técnicas e ferramentas de análise usuais para amostras aleatórias para fins didáticos.
<br>

## Patient Health Questionnaire-9 (PHQ-9)

<br>
O Patient Health Questionnaire-9 (PHQ-9) é um instrumento utilizado para avaliar o grau de depressão em pacientes. O questionário consiste de 9 itens em que os respondentes indicam a frequência (0 = “nenhuma vez”, 1 = “menos de uma semana”, 2 = “uma semana ou mais” e 3 = “quase todos os dias”) de sintomas de depressão nas duas últimas semanas.
<br>
O PHQ-9 inclui os seguintes itens para a pergunta “Nas últimas 2 semanas, com que frequência você ficou incomodado por algum dos problemas a seguir?” (0 = “nenhuma vez”, 1 = “menos de uma semana”, 2 = “uma semana ou mais” e 3 = “quase todos os dias”):
<br>
1 - Pouco interesse ou pouco prazer em fazer as coisas
<br>
2 - Se sentiu para baixo, deprimido(a) ou sem perspectiva
<br>
3 - Dificuldade para pegar no sono ou permanecer dormindo ou dormiu mais do que o costume
<br>
4 - Se sentiu cansado(a) ou com pouca energia
<br>
5 - Falta de apetite ou comeu demais
<br>
6 - Se sentiu mal consigo mesmo(a) ou achou que é um fracasso ou que decepcionou sua família ou a você mesmo(a)
<br>
7 - Dificuldade para se concentrar nas coisas (como ler o jornal ou ver televisão)
<br>
8 - Teve lentidão para se movimentar ou falar (a ponto de outras pessoas perceberem), ou ao contrário, esteve tão agitado(a) que você ficava andando de um lado para o outro mais do que costume
<br>
9 - Pensou em se ferir de alguma maneira ou que seria melhor estar morto(a)
<br>
O escore total é calculado à partir da soma dos itens 1-9 e varia de 0 a 27, em que maiores valores do escore indicam maiores frequências de sintomas de depressão. Aqueles com pontuação maior ou igual a 5 para o escore total de PHQ-9 são considerados como tendo sintomas leves (5-9), moderados (10-14), moderadamente severos (15-19) e severos de depressão (>= 20).
<br>

## Healthy Eating Index - (HEI)

<br>
O Healthy Eating Index (HEI) é uma medida de qualidade da dieta baseado nas orientações dietéticas do governo federal americano (Dietary Guidelines for Americans). O HEI utiliza diferentes grupos alimentares para o cálculo do escore, variando de 0 a 100, em que maiores valores do escore refletem dietas mais próximas das orientações alimentares em vigor.
<br>
O índice é composto por 13 componentes baseados nos grupos alimentares descritos nas recomendações dietéticas. Detalhes dos valores máximos e interpretações estão descritos no link abaixo:
<br>
https://storage.googleapis.com/tera-originals/desafio-inferencia/download.png
<br>

## Physical Activity Guidelines for Americans (PAGA)

<br>
O Physical Activity Guidelines for Americans (PAG) é emitido pelo Departamento de Saúde e Serviços Humanos (U.S. Department of Health and Human Services (HHS)) e possui recomendações de atividades físicas. Este documento é utilizado em conjunto com as orientações dietéticas para americanos (Dietary Guidelines for Americans) para promover a importância de ser fisicamente ativo e seguir uma dieta saudável.
<br>
O PAGA recomenda que adultos se engajem em pelo menos 150 minutos de atividades aeróbicas de intensidade moderada ou 75 minutos de atividades aeróbicas de intensidade vigorosa semanalmente. A partir dos dados coletados do NHANES, é possível calcular o número de minutos de atividades físicas, definido como a total minutos semannais de atividades físicas moderadas + 2*(total minutos de atividades aeróbicas vigorosas).


<br>

## Informações da análise

<br>
Roteiro para o Desafio
<br>
1 - Bases de dados
<br>
Segue os seguintes bancos de dados em formato csv:
<br>
DEMO_PHQ.csv: banco de dados contendo 5334 observações de adultos pesquisados no NHANES 2005-2006.
<br>
PAG_HEI.csv: banco de dados contendo 9424 observações de crianças e adultos pesquisados no NHANES 2005-2006.
<br>
2 - Tratamento de dados
<br>
1. Faça a leitura dos bancos de dados e faça o tratamento que julgar necessário para as variáveis (exemplo: tratamento das categorias 7 = “Se recusou a responder” e 9 = “Não sabe”).
<br>
2. Em seguida, combine os dois bancos de dados fornecidos, utilizando a variável SEQN como chave única. O banco de dados final deve conter 5334 observações dos adultos respondentes do NHANES.
<br>
3. Crie a variável phq9 - escore Patient Health Questionnaire-9 como a soma das variáveis DPQ010 a DPQ090
<br>
4. Crie a variável phq_grp - grupo de sintomas de depressão que assume 0 (“sem sintomas”) se phq9 < 5, 1 (“sintomas leves”) se 5 <= phq9 < 10, 2 (“sintomas moderados”) se 10 <= phq9 < 15, 3 (“sintomas moderadamente severos”) se 15 <= phq9 < 19 e 4 (“sintomas severos”) se phq9 >= 20
<br>
3 - EDA: Análise Univariada
<br>
1. Faça uma análise univariada de todas as variáveis da análise.
<br>
2. Julgue como proceder com os casos faltantes nas variáveis
<br>
3. Re-agrupe ou re-codifique as variáveis que julgar necessário
<br>
4 - EDA: Análise Bivariada
<br>
1. Faça uma análise bivariada de sintomas de depressão (phq9 ou phq_grp) com as características demográficas. Descreva o perfil com maiores incidências de sintomas de depressão.
<br>
2. Faça uma análise bivariada de características demográficas x hábitos saudáveis. Qual perfil possui hábitos mais saudáveis?
<br>
3. Faça uma análise bivariada de sintomas de depressão (phq9 ou phq_grp) com os hábitos saudáveis (variáveis de atividade física e healthy eating index). O que podemos observar?
<br>
5 - Testes de hipóteses
<br>
1. Faça o(s) teste(s) de hipóteses adequado(s) para avaliar a significância estatística das diferenças nas características demográficas apontadas na análise bivariada. Quais são as características apresentam diferenças estatisticamente significativas para a frequência de sintomas de depressão?
<br>
2. Faça o(s) teste(s) de hipóteses adequado(s) para avaliar se existe associação entre hábitos saudáveis e sintomas de depressão.
