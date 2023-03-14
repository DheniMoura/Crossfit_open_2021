## Limpeza dos Dados

### 1 - Importar os dados para o ambiente de programação, utilizando a biblioteca Pandas
Visualizar o dataset e verificar quais colunas estão em formato inadequado, como valores numéricos que estão salvos strings, por exemplo.

### 2 - Visualizar os Dados
Verificar a integridade dos dados, verificando missings (valores faltantes), dados duplicados ou dados inconsistentes; 
Verificar a necessidade de remover colunas cujos dados não fazem sentido.
Nesse caso, foram observadas algumas situações em que os dados parecem ter sido cadastrados equivocadamente, portanto não são dados pertinentes para análise.

### 3 - Tratar colunas
Processos realizados:

##### 3.1. Renomear as colunas;<br>
##### 3.2. Separar a coluna referente ao peso e altura do atleta em duas colunas, uma para o peso (em kg) e outra para altura (em cm);<br>
##### 3.3. Transformar a coluna referente à idade do atleta em dado numérico;<br>
##### 3.4. Transformar em dado numérico as colunas '21.1 reps', '21.2 reps' e '21.3 time'; bem como transformar em string no formato mm:ss (tempo - minutos:segundos) as colunas '21.1', '21.2' e '21.3'; -> Dada a natureza das provas e dos dados, optou-se por manter apenas a posição do atleta em cada prova. A motivação vem do fato de que as provas que são realizadas com tempo máximo (provas do tipo 'for time') irão armazenar dado de tempo para o atleta que terminar antes do time cap, e a mesa coluna armazena o número de repetições realizadas dentro do tempo máximo, caso o atleta não tenha conseguido terminar toda a tarefa antes do fim do tempo determinado. A decisão de manter a posição do atleta na prova visa preservar a variação do desempenho do atleta nas provas sem elevar o nível de complexidade do processo de limpeza dos dados;<br>
##### 3.5. Transformar em numéricos os dados referentes ao peso levantado pelo atleta na quarta prova (‘21.4’);<br>

### 4 - Preenchendo missings
Preencher strings que estão faltando (como nome, país de origem, afiliação, etc)
Foram encontradas situações de dados faltantes. Dadas as características dos dados, optou-se por fazer o preenchimento dos campos.
Por exemplo, nas colunas referentes ao resultado de uma determinada prova em específico (como a 21.3 ou 21.2) o fato de não ter sido atribuído um valor, indica que o atleta não realizou a prova, portanto atribuiu-se, conforme conveniente, valor zero.
Na coluna de afiliação os missings foram tratados como "não afiliados", pois entende-se que se tratam de atletas que treinam em academias próprias ou não afiliada à <a href="https://www.crossfit.com/" target="_blank">Crossfit</a> porém que obtiveram o direito de validar suas provas em local licenciado.

##### 4.1. Convertendo dados categóricos;

### 5 - Verificando a qualidade dos dados
Verificar a qualidade dos dados após a limpeza, garantindo que os dados estão coerentes e corretos para serem analisados.
Neste caso através da visualização dos dados constatamos que temos o necessário para iniciar uma análise exploratória dos dados.
