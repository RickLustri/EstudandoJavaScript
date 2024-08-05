> #### Atualmente temos 3 jeitos diferentes de declarar uma variavel:
> - você pode usar a palavra-chave: `var`, `let`, `const`
> 
> #### Cada uma delas tem suas diferenças:
> - `var`, pode ser redeclarada, pode reatribuir seu valor e tem escopo global e dentro de função ela se torna escopo de bloco
> - `let`, não pode ser redeclarada, pode reatribuir seu valor e tem escopo de bloco
> - `const`, não pode ser redeclarada, não pode reatribuir seu valor e tem escopo de bloco

> ### SINTAXE: 
> ```javascript
> var nomDaVariavel = valor;
> 
> let nomDaVariavel = valor;
> 
> const nomDaVariavel = valor;
> ```
> 
> #### Exemplo `var`:
> ```javascript
> var nome = "Rick"; // Aqui declaramos uma variavel com o valor Rick
> console.log(nome) // Saida: Rick
> 
> nome = "Henrique"; // aqui reatibuimos o valor da variavel para Henrique
> console.log(nome) // Saida: Henrique
> 
> var nome = "RickLustri"; // aqui redeclaramos a variavel com o nome RickLustri
> console.log(nome) // Saida: RickLustri
> 
> // Obs: em var é permitido redeclarar a variavel e reatribuir o valor sem cometer algum tipo de erro
> ```
> 
> #### Exemplo `let`:
> ```javascript
> let idade = 22; // aqui declara com um valor numero 22
> console.log(idade) // Saida: 22
> 
> idade = 23; // Reatribuiu o valor para 23
> console.log(idade) // Saida: 23
> /*
> // erro:
> let idade = 24; // Isso causaria um erro
> console.log(idade); // Erro: variavel "idade" ja foi declarada 
> 
> Obs: em let não é permitido redeclarar a variavel isso pode retornar um error
> */
> ```
> 
> #### Exemplo `const`:
> ```javascript
> const corFavorita = "Vermelho"; // aqui declarei a variavel "corFavorita" com o valor "Vermelho"
> console.log(corFavorita); // Saida: Vermelho
> /*
> // erro:
> corFavorita = "Roxo"; // Isso causaria um erro
> console.log(corFavorita); // Saida: erro: essa variavel é uma constante
> 
> // erro:
> const corFavorita = "Roxo"; // Isso causaria um erro
> console.log(corFavorita); // Saida: erro: a variavel "corFavorita" ja foi declarada
> 
> Obs: em const não é permitido redeclarar a variavel e nem reatribuir o valor caso contrario ele retornaria um erro
> */
> ```

> ### ESCOPO:
> 
> #### # `var`: dependendo de onde for declarada ela pode ter escopo global ou se declarada dentro de funções ela se torna escopo de bloco
> 
> #### Exemplo:
> ```javascript
> // Declarando a variavel no escopo global
> var variavelGlobal = "Eu estou aqui";
> 
> // Testando dentro do bloco:
> {
>   console.log(variavelGlobal) // Saída: Eu estou aqui
> }
> 
> // Testando dentro de funções:
> function testandoVariavel(){
>   console.log(variavelGlobal) // Saída: Eu estou aqui
> }
> 
> // Testando no global:
> console.log(variavelGlobal) // Saída: Eu estou aqui
> ```
> 
> #### # `let`: tem escopo de bloco então onde ela for declarada ela não consegue ser acessada de todo lugar
> 
> #### Exemplo:
> ```javascript
> // Testando dentro de bloco:
> {
>   // Declarando a variavel no escopo de bloco:
>   let variavelBloco = "Eu estou aqui"
>   console.log(variavelBloco) // Saída: Eu estou aqui
> }
> 
> // Testando dentro de funções:
> function testandoVariavel(){
>   console.log(variavelBloco) // Erro: 'variavelBloco' não está definida
> }
> 
> // Testando no global:
> console.log(variavelBloco) // Erro: 'variavelBloco' não está definida
> ```
> 
> #### # `const`: tem escopo de bloco então onde ela for declarada ela não pode ser acessada fora desse bloco
> 
> #### Exemplo:
> ```javascript
> // Testando dentro de bloco:
> {
>   // Declarando a variavel no escopo de bloco:
>   const variavelBloco = "Eu estou aqui"
>   console.log(variavelBloco) // Saída: Eu estou aqui
> }
> 
> // Testando dentro de funções:
> function testandoVariavel(){
>   console.log(variavelBloco) // Erro: 'variavelBloco' não está definida
> }
> 
> // Testando no global:
> console.log(variavelBloco) // Erro: 'variavelBloco' não está definida
> ```