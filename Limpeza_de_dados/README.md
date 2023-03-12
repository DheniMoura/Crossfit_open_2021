## Limpeza dos Dados

### 1 - Importar os dados para o ambiente de programação, utilizando a biblioteca Pandas;
Visualizar o dataset e verificar quais colunas estão em formato inadequado, como valores numéricos que estão salvos strings, por exemplo.

### 2 - Verificar a integridade dos dados, verificando missings (valores faltantes), dados duplicados ou dados inconsistentes; 
Verificar a necessidade de remover colunas cujos dados não fazem sentido.
Nesse caso, foram observadas algumas situações em que os dados parecem ter sido cadastrados equivocadamente, portanto não são dados pertinentes para análise.

### 3 - Tratar missings, removendo-os ou preenchendo-os conforme necessário; Tratar dados inconsistentes, removendo-os ou tratando conforme for conveniente;
Foram encontradas situações de dados faltantes. Dadas as características dos dados, optou-se por fazer o preenchimento dos campos.
Por exemplo, nas colunas referentes ao resultado de uma determinada prova em específico (como a 21.3 ou 21.2) o fato de não ter sido atribuído um valor, indica que o atleta não realizou a prova, portanto atribuiu-se, conforme conveniente, número de repetições zero, carga zero ou tempo nulo.
Na coluna de afiliação os missings foram tratados como "não afiliados", pois entende-se que se tratam de atletas que treinam em academias próprias ou não afiliada à <a href="https://www.crossfit.com/" target="_blank">Crossfit</a> porém que obtiveram o direito de validar suas provas em local licenciado.

1 - Processos necessários:
1.1 - renomear as colunas;
1.2 - separar a coluna referente ao peso e altura do atleta em duas colunas, uma para o peso (em kg) e outra emaltura (em cm);
1.3 - transformar a coluna referenta à idade do atleta em dado numérico;
1.4 - transformar em dado numérico as colunas '21.1 reps', '21.2 reps' e '21.3 time';
1.5 - transformar em numéricos os dados referentes ao peso levantado pelo atleta na quarta prova;
1.5.1 - as colunas '21.4' e 'weiht_lifted' referem-se à mesma informação (peso que o atleta levantou na quarta prova), analisar a possibilidade de remover uma das colunas;
1.6 - transformar em string no formato mm:ss (tempo - minutos:segundos) as colunas '21.1', '21.2' e '21.3';
FAZER 1.7 - preencher strings que estão faltando (como nome, país de origem, afiliação, etc).

### 4 - Verificar a qualidade dos dados após a limpeza, garantindo que os dados estão coerentes e corretos para serem analisados.
Verificando os dados após o processamento verificou que algumas inconsistencias permanecem, por exemplo há um dados de atleta que levantou 1.666Kg na prova 4, feito que podemos considerar impossível. Logo, a limpeza de dados realizada até esse momento serviu de grande aprendizado, mas ainda há um caminho a percorrer para que o trabalho seja realizado de forma consistente e confiável.