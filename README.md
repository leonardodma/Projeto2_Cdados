# Projeto2_Cdados - 2020.1 

### Integrantes: 
* Andresa Bicudo
* Gabriel Yamashita 
* Leonardo Malta

### Objetivo:
O objetivo desse projeto é, através dos modelos de classificação escolhidos, poder estimar qual seria o ganhador da Premiere League. Aproveitando que o campeonato não terá continuidade (logo, pelo menos), vamos tentar adivinhar o vencedor.

### Métodos:
Para o projeto, utilizamos muitas funções, contidas em outras bibliotecas.
Algumas destas foram: sklearn, seaborn, statsmodels.api, numpy, matplotlib.pyplot e pandas.

### Processo:
- Primeiramente, baixamos o arquivo Excel que continha os dados dos jogos entre os times participantes no período 2007 - 2018. O transformamos em uma tabela de dados pandas para podermos utilizá-lo;
- Em seguida, criamos uma nova coluna para o arquivo que continha os resultados das partidas em questão. Os números 0, 1 e 2 representavam respectivamente: a vitória do time local, o empate ou a vitória do time visitante;
- Filtramos as colunas que já não seriam necessárias para o processo, principalmente depois de termos criado a coluna Resultado, que indicava bem quem tinha sucedido . Tais como: time local e time visitante (por serem palavras), ID da partida (por não interferir no processo), Pontuações dos times local e visitante (por estarem contidas na coluna 'Resultado"), o ano do jogo (por não ser relevante no momento) e o resultado;
- Separamos a coluna "Resultado" em uma outra variável, porque seria mais fácil trabalhar com ela assim depois, já que é a nossa base de comparação com as outras variáveis;
- Colocamos em uma outra variável os nomes times locais e visitantes;
- Fizemos um heatmap para ver qual a correlação que os features tinham com os times locais (que jogavam no estádio que já estavam acostumados);
- Calculamos o variance inflation (fator de inflação de variância) para descobrir quais features tem uma multicolinearidade alta (valor maior de 5), portanto são muito parecidos.
- A partir do variance inflation, selecionamos as variáveis que de fato seriam relevantes e as utilizamos em alguns dos modelos de classificação.

### Classificadores:

##### Tentativa 1:
- É referente ao uso de todos os dados

##### Tentativa 2: 
- É referente ao uso das variáveis "relevantes"

#### Random Forest:
- É um método de Regressão baseado em várias árvores de probabilidade. 
Cada uma delas faz as probabilidades separadamente usando ordens diferentes entre suas variáveis. 
Com isso, caso apresente algum erro, ele será minimizado.
Esse método é uma técnica de "bagging", já que as árvores funcionam paralelamente e não interferem umas nas outras.

#### Regressão Multinominal:
- A Regressão Multinomial é usada para relacionar uma variável nominal dependente (nesse caso, resultado de um jogo) e outras variáveis independentes (número de passes, time adversário, estádio).

#### Regressão Naive Bayes Multinominal:
- 

#### K-Nearest Neighbors:
- Esse método assume que os fatores que estão mais relacionados são os que estão mais perto em distância e os utiliza para calcular o resultado final.

#### Gradient Boosting:
- Boosting é uma técnica usada para montar diversas árvores modificadas dos dados. Cada árvore recebe um peso no processo, a partir de alguns cálculos feitos.
