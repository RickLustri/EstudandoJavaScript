> ### Tipos de Dados Primitivos
> - string
> - number
> - boolean
> - undefined
> - null

> ## String
> - O tipo `string` é utilizado para representar uma sequencia de caracteres elas podem conter letras, numeros, simbulos, espaços e outros caracteres
> - As `String` são criadas de 3 jeitos usando aspas simples (`' '`), usando aspas duplas (`" "`) ou usando crases (`` ` ` ``)
> - Você pode usar concatenação para juntar stings e interpolação para incluir valores de variaveis dentro da sting
> - Você pode utilizar aspas simples e duplas dentro de uma string utilizando (`\`), exemplo (`\' ou \"`)
> 
> ### Diferença entre elas:
> #### String com aspas simples: utilizada para uma sting simples e não permite interpolação de variavel.
> ##### **Exemplo:**
> ```javascript
> // Usando aspas simples:
> let nome = 'henrique';
> 
> // Usando interpolação de variavel:
> let dizerOla = 'Olá, ${nome}';
> console.log(dizerOla); // Saída: Olá, ${nome}
> // Obs: as aspas simples não indentifica ${nome} como uma variavel então ele apenas transforma tudo em sting... para que o exemplo acima funcione utilize concatenação
> 
> // Usando concatenação:
> let dizerOla = 'Olá, ' + nome;
> console.log(dizerOla); // Saída: Olá, henrique
> // Obs: usando concatenação você consegue juntar os 2 valores em uma unica sting
>
> // Usando aspas dentro da string:
> let fraseEntreAspas = 'Ela disse que o filme era \'incrível\'.'; // Exemplo com aspas simples
> console.log(fraseEntreAspas); // Saída: Ela disse que o filme era 'incrível'.
>
> let fraseEntreAspas = 'Ele descreveu a viagem como \"inesquecível\".'; // Exemplo com aspas duplas
> console.log(fraseEntreAspas); // Saída: Ele descreveu a viagem como "inesquecível".
> ```
> <hr>
>
> #### Sting com aspas duplas: assim como as aspas simples as aspas duplas segue o mesmo formato, são utilizadas para sting simples e não permite interpolação de variavel.
> ##### **Exemplo:**
> ```javascript
> // Usando aspas duplas:
> let cor = "Vermelho";
>
> // Usando interpolação de variavel:
> let frase = "Minha cor favorita é ${cor}";
> console.log(frase); // Saída: Minhca cor favorita é ${cor}
> // Obs: assim como as aspas simples as aspas duplas não indentifica ${cor} como uma variavel então ele apenas transforma tudo em sting... para que o exemplo acima funcione utilize concatenação
>
> // Usando concatenação:
> let frase = "Minha cor favorita é " + cor;
> console.log(dizerOla); // Saída: Minha cor favorita é Vermelho
> // Obs: usando concatenação você consegue juntar os 2 valores em uma unica sting
>
> // Usando aspas dentro da string:
> let fraseEntreAspas = "Ela mencionou que a reunião foi \'produtiva\'."; // Exemplo com aspas simples
> console.log(fraseEntreAspas); // Saída: Ela mencionou que a reunião foi 'produtiva'.
>
> let fraseEntreAspas = "Ele chamou o projeto de \"ambicioso\"."; // Exemplo com aspas duplas
> console.log(fraseEntreAspas); // Saída: Ele chamou o projeto de "ambicioso"
> ```
> <hr>
>
> #### String com crases: as string formadas por crases são chamadas de `template string` ou `template literal` sting com crases diferente das aspas simples ou duplas ela aceita interpolação de variavel e expressões dentro da string.
> ##### **Exemplo:**
> ```javascript
> let nome = "Henrique";
> let idade = 22;
> let cor = 'vermelho'; 
>
> // Usando template string para interpolação de variavel:
> let frase = `Olá meu nome é ${nome}, tenho ${idade} anos e minha cor favorita é ${cor}.`;
> console.log(frase); // Saída: Olá meu nome é Henrique, tenho 22 anos e minha cor favorita é vermelho.
>
> // Usando template string com multiplas linhas:
> let multiplasLinhas = `Essa
> frase está
> em varias
> linhas`
> console.log(multiplasLinhas);
> // Saída:
> // Essa
> // frase está
> // em varias
> // inhas
>
> let num1 = 9;
> let num2 = 1;
>
> // Usando expressões no template string:
> let somarNumeros = `A soma de ${num1} e ${num2} é: ${num1 + num2}`
> console.log(somarNumeros); // Saída: A soma de 9 e 1 é: 10
> ```

> ## Number
> - O tipo number é representado por valores numericos exemplo: inteiro, decimal, negativo e grande, ambos são do tipo `number`
> - ele tem suporte para notação exponencial par numero grande ou pequenos
> 
> ##### **Exemplos:**
> ```javascript
> // Usando numero inteiros:
> let numeroInteiro = 500;
>
> // Usando numero com ponto flutuante:
> let numeroDecimal = 1.99;
>
> // Usando numero negativo:
> let nuemroNegativo = -254;
>
> // Usando numeros grande:
> let numeroGrande = 3.99e6;
> // Representação: 3.99 × 10^6 = 3990000
> ```

> ## Boolean
> - O tipo boolean representa um valor logico que pode ser `true` ou `false`
>
> ##### **Exemplo:**
> ```javascript
> // Valor logico true:
> let carroLigado = true;
> console.log(carroLigado); // Saída: true
>
> // Valor logico false:
> let carroDesligado = false;
> console.log(carroDesligado); // Saída: false
> ```

> ## Undefined
> - O tipo undefined indica uma variavel que foi declarada sem um valor, `undefined` é atribuido por padrão nas variaveis não incializadas por um valor.
> 
> ##### **Exemplo:**
> ```javascript
> // Declarando uma variavel sem valor:
> let valorIndefinido;
> console.log(valorIndefinido); // Saída: undefined
>
> // Assim como as variaveis, funções tambem podem ter seu valor indefinido.
>
> // Declarando uma função sem valor:
> function semRetornoDeValor(){};
> semRetornoDeValor(); // Saída: undefined
> ```

> ## Null
> - O tipo null representa quando algo não vai ter um valor definido ou seja é um valor que vc pode atribuir a uma variavel para indicar que ela n tem valor.
>
> ##### **Exemplo:**
> ```javascript
> // Declarando uma variavel nula:
> let variavelSemValor = null;
> console.log(variavelSemValor); // Saída: null
>
> // Assim como as variaveis, objetos tambem pode ter seu valor como nulo.
>
> // Declarando um objeto nulo:
> let objeto = { carteira: null };
> console.log(objeto.carteira); // Saída: null
> ```

> ## Operador TypeOf
> - O operador typeof é usado para saber o tipo de dado de uma variavel ou expressão, ele retorna em uma string que indica o tipo do valor fornecido.
> ##### **Exemplo:**
> ```javascript
> // Para saber o tipo de dado retornado para a variavel utiliza-se a seguinte sintaxe
> typeOf valor;
>
> // exemplos:
> function saberTipo(value) {
>   console.log(typeof value);
> }
> 
> saberTipo("Ola");  // Saída: "string"
> 
> saberTipo(42);  // Saída: "number"
> 
> saberTipo(true); // Saída: "boolean"
> 
> saberTipo(undefined); // Saída: "undefined"
> 
> saberTipo(null); // Saída: "object"
> 
> saberTipo([1,2,3]);  // Saída: "object"
> 
> saberTipo({nome: 'henrique'}); // Saída: "object"
> 
> saberTipo(function(){}); // Saída: "function"
> ```