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

> ### HOISTING:
> > O que é?
> > - Hoisting é quando o JavaScript "sobe" as declarações de variáveis e funções para o topo do código antes de ele ser executado. Isso permite usar algo antes de declarar, mas com regras diferentes para var, let, const e funções.
> 
> #### Exemplo de hoisting em `var`:
> ```javascript
> // Criando a variavel 'nome' e acessando ela antes da declaração:
> 
> console.log(nome); // Saida: undefined
> var nome = "henrique"; // declarando e inicializando a variavel
> console.log(nome); // Saida: henrique
> 
> // Explicando como o JavaScript interpreta o codigo:
> 
> var nome; // ele apenas declara a variavel e eleva para o topo do escopo
> console.log(nome); // Saida: undefined
> nome = "henrique"; // ele inicia no local onde ela foi "originalmente declarada"
> console.log(nome); // Saida: henrique 
> 
>
>
> // A mesma coisa ocorre dentro de funções:
> 
> function chamarNome(){
>  console.log(nome); // Saida: undefined
>  var nome = "henrique"; // declarando e inicializando a variavel
>  console.log(nome); // Saida: henrique
> }
> chamarNome();
>
> // Explicando como o JavaScript interpreta o codigo:
> 
> function chamarNome(){
>  var nome; // ele apenas declara e eleva para o topo do escopo
>  console.log(nome); // Saida: undefined
>  nome = "henrique"; // ele inicia no local onde ela foi "originalmente declarada"
>  console.log(nome); // Saida: henrique
> }
> chamarNome()
> ```
>
> #### Exemplo de hoisting em `let`:
> ```javascript
> // Criando a variavel 'idade' e acessando ela antes da declaração:
> 
> console.log(idade); // Saida: ReferenceError: Não é possível acessar 'idade' antes da inicialização
> let idade = 22; // declarando e inicializando a variavel
> console.log(idade); // Saida: 22
>
> // Explicando como o JavaScript interpreta o codigo:
> 
> let idade; //  ele apenas declara e eleva para o topo do escopo
> console.log(idade); // Saida: ReferenceError: Não é possível acessar 'idade' antes da inicialização
> idade = 22; // ele inicia no local onde ela foi "originalmente declarada"
> console.log(idade); // Saida: 22
>
>
>
> // A mesma coisa ocorre dentro de uma função:
> 
> function chamarIdade(){
>  console.log(idade); // Saida: ReferenceError: Não é possível acessar 'idade' antes da inicialização
>  let idade = 22; // declara e inicializa a variavel
>  console.log(idade); // Saida: 22
> }
> chamarIdade();
>
> // Explicando como o JavaScript interpreta o codigo:
> 
> function chamarIdade(){
>  let idade; // ele apenas declara e eleva para o topo do escopo
>  console.log(idade); // Saida: ReferenceError: Não é possível acessar 'idade' antes da inicialização
>  idade = 22; // declara e inicializa a variavel
>  console.log(idade); // Saida: 22
> }
> chamarIdade();
> 
> // Com let diferente de var ele não aparece "undefined" mas sim um erro "ReferenceError" que refere-se a não pode acessar a variavel antes de inicializar
> ```
> 
> #### Exemplo de hoisting em `const`:
> ```javascript
> // Criando a variavel 'corFavorita' e acessando ela antes da declaração:
> 
> console.log(corFavorita); // Saida: ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
> const corFavorita = "red"; // declarando e inicializando a variavel
> console.log(corFavorita); // Saida: red
>
> // Explicando como o JavaScript interpreta o codigo:
> 
> const corFavorita; //  ele apenas declara e eleva para o topo do escopo
> console.log(corFavorita); // Saida: ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
> corFavorita = "red" // ele inicia no local onde ela foi "originalmente declarada"
> console.log(corFavorita); // Saida: red
>
>
>
> // A mesma coisa ocorre dentro de uma função:
> 
> function verCorFavorita(){
>  console.log(corFavorita); // Saida: ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
>  const corFavorita = "red"; // declara e inicializa a variavel
>  console.log(corFavorita); // Saida: red
> }
> verCorFavorita();
>
> // Explicando como o JavaScript interpreta o codigo:
> 
> function verCorFavorita(){
>  const corFavorita; // ele apenas declara e eleva para o topo do escopo
>  console.log(corFavorita); // Saida: ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
>  corFavorita = "red"; // declara e inicializa a variavel
>  console.log(corFavorita); // Saida: red
> }
> verCorFavorita();
>
> // Com const assim como o let ele exibe um erro "ReferenceError" que refere-se a não pode acessar a variavel antes de inicializar
>```
