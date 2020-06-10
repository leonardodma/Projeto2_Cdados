# Projeto2_Cdados - 2020.1 

### Integrantes: 
* Andresa Bicudo
* Gabriel Yamashita 
* Leonardo Malta

### Objetivo:
O objetivo desse projeto é, através dos modelos de classificação escolhidos, poder estimar qual seria o ganhador da Premiere League. Aproveitando que o campeonato não terá continuidade (logo, pelo menos), vamos tentar adivinhar o vencedor.

### Processo:
- Primeiramente, baixamos o arquivo Excel que continha os dados dos jogos entre os times participantes no período 2007 - 2018. O transformamos em uma tabela de dados pandas para podermos utilizá-lo;
- Em seguida, criamos uma nova coluna para o arquivo que continha os resultados das partidas em questão. Os números 0, 1 e 2 representavam respectivamente: a vitória do time local, o empate ou a vitória do time visitante;
- Filtramos as colunas que já não seriam necessárias para o processo, principalmente depois de termos criado a coluna Resultado, que indicava bem quem tinha sucedido . Tais como: time local e time visitante (por serem palavras), ID da partida (por não interferir no processo), Pontuações dos times local e visitante (por estarem contidas na coluna 'Resultado"), o ano do jogo (por não ser relevante no momento) e o resultado;
- Separamos a coluna em uma outra variável, porque seria mais fácil trabalhar com ela separadamente depois, já que é a nossa base de comparação com as outras variáveis;
- 
