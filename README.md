<H1> Questões corrigidas da P2 de Computação 1 </H1>
<p> Luiz Carlos Aguiar Carrion </p>

<H2> Comentários sobre a Q1 </H2>
<p> A questão em si não foi trabalhosa, o único erro foi por falta de atenção. Na linha 44, acabei confundindo uma palavra e, em vez de colocar arq_linhas, escrevi lista_linhas. Ao consertar esse erro, o programa rodou sem nenhum outro aviso de erro. A lógica utilizada foi:</p>

<p><b> Letra a)</b> Utilizei a estratégia do split para conseguir separar a data corretamente, em seguida salvei cada valor em uma variável. Por fim adicionei cada uma delas ao dicionário data_d, e retornei o mesmo para a main.</p>

<p><b> Letra b)</b> Para essa questão, eu primeiro verifiquei o tamanho da string. Como "SIM" e"NAO" possuem, ambos, 3 letras, caso tivesse um len de 4, teria um "\n". Para me livrar desse caractere, copiei o dado somente até o terceiro caractere. Por fim, verifiquei somente a primeira letra dele. Caso fosse S, seria SIM, logo true. Caso N, seria NAO, logo false. </p>

<p><b> Letra c)</b> Essa foi a mais simples, simplesmente usei um split para separar nos dois pontos e retornei a lista gerada. </p>

<p><b> Letra d)</b> Nada muito complexo tambem, utilizei o seek para colocar o ponteiro de volta no início do arquivo e usei o readlines para gerar a lista com todas as linhas.</p>

<p><b> Letra e)</b> Por fim, a letra e foi simplesmente aplicar todas as outras funções desenvolvidas anteriormente. Criei uma lista chamada pessoas, na qual guardei todos os dicionários. Ao abrir o arquivo (utilizei um arquivo de teste, assumindo que ele já exista) usei o le_linhas para pegar as informações. Criei um dicionário para servir de base para todos os outros. Depois só fui preenchendo ele com as infprmações do arquivo texto, em conjunto com as funções criadas.</p>

<H2> Comentários sobre a Q2 </H2>
<p> A segunda questão foi relativamente simples. O único detalhe que me passou despercebido foi a parte dos ponteiros da matriz. Por não ter feito uma cópia dela, a matriz final e a inicial estavam apontando para o mesmo endereço de memória. Logo, na hora de imprimir as duas para comparar os resultados, elas eram iguais. Para resolver isso, importei uma biblioteca chamada copy e utilizei a função deepcopy. Sem essa função, não teriamos uma cópia completamente independete, visto que a matriz é uma lista de listas, logo utilizar o comando list() não seria suficiente. A lógica foi essa: a função recebe a matriz e imediatamente cria uma cópia dela. Após isso, ela trabalha somente com a cópia. Primeiro, calculamos o valor da determinante e avaliamos se é diferente de 0. Caso não seja o programa retorna imediamente None. Caso seja, ele continua o passo a passo de criar a inversa e depois multiplica os resultados encontrados. No fim ela retorna a matriz nova. </p>

<H2> Comentários sobre a Q3 </H2>
<p> A 3 não precisou ser corrigida pois estava completamente correta. A ideia pensada foi: vamos supor que tenhamos 2 retângulos, A e B. as coordenadas de A são: bottom left = (xAi,yAi) top right = (xAf, yAf) já as de B são: bottom left = (xBi, yBi) e top right = (xBf, yBf). Para verificar se existe ou não colisão, precisamos que todas as seguintes condições sejam atendidas. Se pelo menos uma não for, então não há colisão: xAi < xBf; xAf > xBi; yAi < yBf; yAf > yBi. Se por algum motivo o início de algum retângulo for maior que o final do outro, chegamos a conclusão que a colisão não existe. Mas só porque o início e o fim em um eixo são compatíveis não significa que tem colisão, é necessário que sejam compatíveis no outro eixo também, por isso utilizamos o and. </p>

<H2> Comentários sobre a Q4 </H2>
<p> Os comandos utilizados foram os mesmos para fazer esse repositório: git add -A, git commit -m "" e o git push --set-upstream origin master. (o último comando está assim para garantir que os dados a serem commitados no repositório da nuvem sejam da branch master). </p>
