<h1 align="center"> Estudando JavaScript</h1>

![Diagrama Mermaid](/assets/image/introducaojs.svg)

>> ### O que é JavaScript?
> JavaScript é uma linguagem de programação de alto nível, interpretada e orientada a objetos. É uma das principais tecnologias da web, juntamente com HTML e CSS. É amplamente utilizada para criar páginas web interativas, aplicativos web e servidores. JavaScript permite a manipulação dinâmica de conteúdo, controle de multimídia, animação de gráficos e muito mais.

>> ### História do JavaScript
> avaScript foi criado por Brendan Eich em 1995 enquanto trabalhava na Netscape. Desenvolvida em apenas dez dias, a linguagem foi inicialmente chamada de Mocha, depois LiveScript, e finalmente JavaScript. Seu objetivo era adicionar interatividade a páginas web. Em 1996, a Microsoft lançou o JScript, e para garantir a compatibilidade entre navegadores, JavaScript foi padronizado pela Ecma International como ECMAScript em 1997.\
Com o tempo, JavaScript evoluiu, tornando-se essencial para o desenvolvimento web, com o surgimento de bibliotecas e frameworks como [jQuery](https://jquery.com/), [Angular](https://angular.io/), [React](https://reactjs.org/), e [Vue.js](https://vuejs.org/), além da plataforma [Node.js](https://nodejs.org/), que permite a execução no lado do servidor. Hoje, JavaScript é amplamente utilizado e continua a evoluir, permanecendo crucial para experiências web dinâmicas.

>> ### Versões do JavaScript
> JavaScript, inventado por Brendan Eich, alcançou o status de um padrão ECMA em 1997 e adotou o nome oficial ECMAScript. Esta linguagem evoluiu através de várias versões, nomeadamente [ES1](https://262.ecma-international.org/1.0/), [ES2](https://262.ecma-international.org/2.0/), [ES3](https://262.ecma-international.org/3.0/), [ES5](https://262.ecma-international.org/5.1/), e a transformadora [ES6](https://262.ecma-international.org/6.0/). Estas atualizações desempenharam um papel crucial na melhoria e padronização do JavaScript, tornando-o amplamente utilizado e valioso no campo em constante mudança do desenvolvimento web.

>> ### Como executar JavaScript?
>
>>### # Executar JavaScript no Navegador
>>Os navegadores modernos possuem consoles de desenvolvedor onde você pode executar código JavaScript diretamente.
>>
>> Passos:
>> 1. Abra seu navegador (por exemplo, Chrome, Firefox, Edge).
>> 2. Pressione `F12` ou `Ctrl+Shift+I` (Windows/Linux) ou `Cmd+Opt+I` (Mac) para abrir as ferramentas de desenvolvedor.
>> 3. Vá para a aba "Console".
>> 4. Digite seu código JavaScript e pressione `Enter`.
>> 
>> ```javascript
>> Exemplo:
>>  console.log("Hello, World!");
>> ```
>
>>### # Executar JavaScript em um Arquivo HTML
>>Você pode inserir JavaScript diretamente em um arquivo HTML.
>> 
>> Passos:
>> 1. Crie um arquivo HTML com uma estrutura básica.
>> 2. Adicione a tag `<script>` onde deseja incluir seu código JavaScript.
>> 
>> 
>> ```html
>> Exemplo:
>>
>> <!DOCTYPE html>
>> <html lang="en">
>> <head>
>>      <meta charset="UTF-8">
>>      <meta name="viewport" content="width=device-width, initial-scale=1.0">
>>      <title>JavaScript Example</title>
>> </head>
>> <body>
>>      <h1>My First JavaScript</h1>
>>      <script>
>>          console.log("Hello, World!");
>>      </script>
>> </body>
>> </html>
>> ```
>> Abra este arquivo HTML no navegador e o JavaScript será executado automaticamente.
>
>> ### # Executar JavaScript com Node.js
>> Se você deseja executar JavaScript fora de um navegador, você pode usar Node.js.
>> 
>> Passos:
>> 1. [Instale o Node.js](https://nodejs.org/).
>> 2. Crie um arquivo JavaScript (por exemplo, `script.js`).
>> 3. Adicione seu código JavaScript ao arquivo.
>> 
>> ```javascript
>> Exemplo (`script.js`):
>>  console.log("Hello, World!");
>>  ``` 
>> 4. Abra o terminal ou prompt de comando.
>> 5. Navegue até o diretório onde seu arquivo JavaScript está localizado.
>> 6. Execute o arquivo usando o comando `node`.
>> ```sh
>>     node script.js
>> ```
<br>
<hr>
<br>

![Diagrama Mermaid](/assets/image/variaveis.svg)


>> ### Declarações de Variáveis
> 
>> ### # `Var`
>> **Declaração:**\
>> Você pode declarar uma variável usando `var` da seguinte maneira:
>> ```javascript
>> // Sintaxe:
>> var nomeDaVariavel = Valor;
>> 
>> // Exemplo:
>> var nome = "Rick Lustri";
>> ```
>> 
>> **Reatribuição:**\
>> Variáveis declaradas com `var` podem ser reatribuídas.
>> ```javascript
>> var nome = "Rick Lustri"; // declaração da variavel com o valor
>> console.log(nome); // Rick Lustri
>> 
>> nome = "Henrique Lustri"; // reatribuindo um valor para a variavel
>> console.log(nome); // Henrique Lustri
>> ```
>> 
>> **Re-declaração:**\
>> É possível re-declarar a mesma variável usando `var` sem causar erros. 
>> ```javascript
>> var nome = "Rick Lustri"; // declaração da variavel com o valor
>> var nome = "Henrique Lustri"; // declaração da variavel com o valor
>> console.log(nome); // Henrique Lustri
>> ```
>> 
>> ### Escopo
>> As variáveis declaradas com `var` têm escopo de função ou escopo global:
>> - **Escopo global**: Se uma variável for declarada fora de qualquer função, ela será visível em qualquer lugar no código.
>> - **Escopo de função**: Se uma variável for declarada dentro de uma função, ela será visível apenas dentro dessa função.
>> 
>> #### Exemplo de escopo global:
>> 
>> ```javascript
>> var nome = "Rick Lustri"; // nome está visível em qualquer lugar no código
>> 
>> function example() {
>>   console.log(nome); // Rick Lustri
>> }
>> console.log(nome); // Rick Lustri
>> ```
>> 
>> #### Exemplo de escopo de função:
>> 
>> ```javascript
>> function example() {
>>   var nome = "Rick Lustri"; // nome está visível apenas dentro desta função
>>   console.log(nome); // Rick Lustri
>> }
>> console.log(nome); // Erro: nome não está definido
>> ```
>> 
>>### Hoisting
>> Hoisting de `var` com declaração e inicialização
>> - **Inicialização com `undefined`**: A variável `var` é inicializada automaticamente com `undefined` durante o hoisting, mesmo que seu valor seja atribuído posteriormente no código.
>> 
>> #### Hoisting na declaração:
>> ```javascript
>> console.log(nome); // undefined
>> var nome = "Henrique";
>> console.log(nome); // Henrique
>> ```
>> Neste exemplo, o JavaScript interpreta o código da seguinte maneira durante a execução:
>> ```javascript
>> var nome; // declaração é elevada para o topo do escopo
>> console.log(nome); // undefined
>> nome = "Henrique"; // inicialização ocorre no local original
>> console.log(nome); // Henrique
>> ```
>> 
>> #### Hoisting dentro de uma função
>> Hoisting de `var` com declaração no escopo de função
>> - **Escopo de função**: As variáveis `var` têm escopo de função ou escopo global, o que pode levar a comportamentos inesperados se não forem compreendidos corretamente.
>> ```javascript
>> function example() {
>>   console.log(nome); // undefined
>>   var nome = "Rick";
>>   console.log(nome); // Rick
>> }
>> example();
>> ```
>> Dentro da função `example`, o código é interpretado da seguinte maneira:
>> ```javascript
>> function example() {
>>   var nome; // declaração é elevada para o topo da função
>>   console.log(nome); // undefined
>>   nome = "Rick"; // inicialização ocorre no local original
>>   console.log(y); // Rick
>> }
>> example();
>> ```
> <br>
>  
>> ### # `let`
>> **Declaração:**\
>> Você pode declarar uma variável usando `let` da seguinte maneira:
>> ```javascript
>> // Sintaxe:
>> let nomeDaVariavel = Valor;
>> 
>> // Exemplo:
>> let idade = 22;
>> ```
>> 
>> **Reatribuição:**\
>> Variáveis declaradas com `let` podem ser reatribuídas da mesma forma que `var`.
>> ```javascript
>> let idade = 22; // declaração da variavel com o valor
>> console.log(idade); // 22
>>
>> idade = 23; // reatribuindo um valor para a variavel
>> console.log(idade); // 23
>> ```
>> 
>> **Re-declaração:**\
>> Ao contrário de `var`, tentar re-declarar a mesma variável com `let` no mesmo escopo gera um erro.
>> ```javascript
>> let idade = 22; // declaração da variavel com o valor
>> let idade = 23; // Erro: variavel 'idade' ja foi declarada
>> console.log(idade); // 22
>> ```
>> 
>> ### Escopo
>> As variáveis declaradas com `let` têm escopo de bloco:
>> - **Escopo de bloco**: Uma variável declarada com `let` é visível apenas dentro do bloco onde foi declarada, seja um bloco de função, um bloco `if`, um loop `for`, etc.
>> 
>> #### Exemplo de escopo de bloco:
>> ```javascript
>> function example() {
>>     let idade = 22; // 'idade' está visível apenas dentro deste bloco `function`
>>     console.log(x); // 22
>> }
>> console.log(idade)); // Erro: 'idade' não está definida
>> ```
>> 
>> ### Hoisting
>> Hoisting de `let` com declaração
>> - **Erro `ReferenceError`**: Ao contrário de `var`, uma variável `let` não é inicializada com `undefined` durante o hoisting. Tentar acessá-la antes de sua declaração resulta em um erro `ReferenceError`.
>> #### Hoisting na declaração:
>> ```javascript
>> console.log(idade); // ReferenceError: Não é possível acessar 'idade' antes da inicialização
>> 
>> let idade = 22;
>> console.log(idade); // 22
>> ```
>> Com `let`, a variável não é inicializada com `undefined` durante o hoisting. Em vez disso, ocorre um erro `ReferenceError` se tentarmos acessar a variável antes de sua declaração.\
>> Durante a execução, o código é interpretado assim:
>> ```javascript
>> let idade; // declaração é elevada para o topo do escopo
>> console.log(idade); // ReferenceError: Não é possível acessar 'idade' antes da inicialização
>> 
>> idade = 22; // inicialização ocorre no local original
>> console.log(idade); // 22
>> ```
>> 
>> #### Hoisting dentro de uma função
>> Hoisting de `let` com declaração no escopo de função
>> - **Escopo de bloco**: `let` tem escopo de bloco, o que significa que é limitada ao bloco em que é declarada. Isso é útil para evitar problemas de vazamento de variáveis e colisões de nomes.
>> ```javascript
>> function example() {
>>   console.log(idade); // ReferenceError: Não é possível acessar 'idade' antes da inicialização
>> 
>>   let idade = 22;
>>   console.log(y); // 22
>> }
>> example();
>> ```
>> Dentro da função `example`, o código é interpretado da seguinte maneira:
>> ```javascript
>> function example() {
>>   let idade; // declaração é elevada para o topo da função
>>   console.log(idade); // ReferenceError: Não é possível acessar 'idade' antes da inicialização
>> 
>>   idade = 22; // inicialização ocorre no local original
>>   console.log(idade); // 22
>> }
>> example();
>> ```
> <br>
>
>> ### # `const`
>> **Declaração:**\
>> Você pode declarar uma variável constante usando `const` da seguinte maneira:
>> ```javascript
>> // Sintaxe:
>> const nomeDaVariavel = Valor;
>> 
>> // Exemplo:
>> const corFavorita = "Vermelho";
>> ```
>> 
>> **Reatribuição:**\
>> Ao contrário de `var` e `let`, variáveis declaradas com `const` não podem ser reatribuídas. Isso significa que seu valor inicial não pode ser alterado após a atribuição inicial.
>> 
>> #### Exemplo de tentativa de reatribuição:
>> ```javascript
>> const corFavorita = "Vermelho";
>> corFavorita = "Azul"; // Erro: Atribuição a variável constante.
>> console.log(corFavorita); // Vermelho
>> ```
>> 
>> **Re-declaração:**\
>> Assim como `let`, tentar re-declarar a mesma variável com `const` no mesmo escopo gera um erro.
>> ```javascript
>> const corFavorita = "Vermelho";
>> const corFavorita = "Roxo"; // Erro: variavel 'corFavorita' ja foi declarada
>> console.log(corFavorita); // Vermelho
>> ```
>> 
>> ### Escopo
>> As variáveis declaradas com `const` têm escopo de bloco:
>> - **Escopo de bloco**: Uma variável declarada com `const` é visível apenas dentro do bloco onde foi declarada, seja um bloco de função, um bloco `if`, um loop `for`, etc.
>> 
>> #### Exemplo de escopo de bloco:
>> ```javascript
>> function example() {
>>     const corFavorita = "Vermelho"; // corFavorita está visível apenas dentro deste bloco `function`
>>     console.log(corFavorita); // Vermelho
>> }
>> console.log(corFavorita); // Erro: corFavorita não está definida
>> ```
>> 
>> ### Hoisting 
>> Hoisting de `const` com declaração
>> - **Erro `ReferenceError`**: Semelhante a `let`, uma variável `const` não é inicializada durante o hoisting. Tentar acessá-la antes de sua declaração resulta em um erro `ReferenceError`.
>> - **Atribuição após inicialização**: Uma vez inicializada, uma variável `const` não pode ser reatribuída. Isso significa que seu valor não pode mudar depois de ser definido.
>> #### Hoisting na declaração:
>> ```javascript
>> console.log(corFavorita); // ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
>> 
>> const corFavorita = "Vermelho";
>> console.log(corFavorita); // Vermelho
>> ```
>> Com `const`, assim como `let`, a variável não é inicializada durante o hoisting. Tentar acessá-la antes de sua declaração resulta em um erro `ReferenceError`.\
>> Durante a execução, o código é interpretado assim:
>> ```javascript
>> const corFavorita; // declaração é elevada para o topo do escopo
>> console.log(corFavorita); // ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
>> 
>> corFavorita = "Vermelho"; // inicialização ocorre no local original
>> console.log(corFavorita); // Vermelho
>> ```
>> 
>> #### Hoisting dentro de uma função
>> Hoisting de `const` com declaração no escopo de função
>> - **Escopo de bloco**: `const` também possui escopo de bloco, o que é útil para limitar a visibilidade da variável ao bloco em que é declarada.
>> ```javascript
>> function example() {
>>   console.log(corFavorita); // ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
>> 
>>   const corFavorita = "Vermelho";
>>   console.log(corFavorita); // Vermelho
>> }
>> example();
>> ```
>> Dentro da função `example`, o código é interpretado da seguinte maneira:
>> ```javascript
>> function example() {
>>   const corFavorita; // declaração é elevada para o topo da função
>>   console.log(corFavorita); // ReferenceError: Não é possível acessar 'corFavorita' antes da inicialização
>> 
>>   corFavorita = "Vermelho"; // inicialização ocorre no local original
>>   console.log(corFavorita); // Vermelho
>> }
>> example();
>> ```
> <br>
>
>> ### Regras para Nomear Variáveis
>> Ao programar em JavaScript, é importante seguir regras específicas para nomear variáveis, garantindo clareza e evitando 
>> ### # Regras Importantes:
>> **Permitido**:\
>> Nomes de variáveis podem conter apenas letras, letras e números, `_` (sublinhado) e `$` (cifrão).
>> #### Por exemplo:
>> ```javascript
>> // Letras:
>> var abc; // É permitido
>> // Variáveis podem consistir apenas de letras.
>>  
>> // Letras e números:
>> var numero1 // É permitido
>> // Variáveis podem conter letras e números
>> 
>> // Sublinhado:
>> var com_sublinhado; // É permitido
>> var _sublinhado_; // É permitido (sublinhado no início e no final)
>> // Pode ser usado em qualquer posição no nome da variável.
>> 
>> // Cifrão:
>> var $cifrao; // É permitido
>> vat cifrao$; // É permitido (cifrão no início e no final, embora seja mais comum no final)
>> // Pode ser usado em qualquer posição no nome da variável.
>> ```
>> 
>> **Não permite:**\
>> Nomes de variáveis não podem começar com números, ter espaços dentro dos nomes ou usar palavras reservadas. 
>> #### Por exemplo:
>> ```javascript
>> // Letras e números:
>> var 1numero; // Não é permitido
>> 
>> // Espaços:
>> var meu nome; // Não é permitido
>> 
>> // Palavras reservadas:
>> var var; // Não é permitido
>> var let; // Não é permitido
>> var function; // Não é permitido
>> ```
>> 
>> ### # Como Nomear Variáveis:
>> **Seja Descritivo**: Escolha nomes que claramente descrevam o que a variável representa. 
>> #### Exemplo:
>> ```javascript
>> // É aceito, mas é ilegível caso outra pessoa pegue seu código para ler:
>> var x;
>> var y;
>> var z;
>> 
>> // O correto de se usar:
>> var nomeDeUsuario;
>> var idadeDoUsuario;
>> var diaDoMes;
>> ```
>> - Os exemplos mostram a diferença entre variáveis com nomes genéricos e variáveis com nomes descritivos.
>> - Utilize nomes descritivos como nomeDeUsuario, idadeDoUsuario e diaDoMes para facilitar a compreensão do código por outras pessoas que o lerem posteriormente.
>> 
>> ### Regra padrão em JavaScript
>> Em JavaScript, é recomendado seguir regras específicas ao nomear variáveis para garantir clareza e consistência no código. Uma das regras mais amplamente aceitas é o `camelCase`, que segue o padrão de iniciar com letra minúscula e usar maiúsculas para iniciar cada palavra subsequente no nome da variável.
>> ### # `camelCase`
>> No `camelCase`, a primeira letra da variável é minúscula, e cada palavra subsequente começa com letra maiúscula, sem espaços ou caracteres especiais entre as palavras.
>> #### Exemplos de uso correto:
>> ```javascript
>> // Exemplos de camelCase:
>> var meuNome; // Correto: primeira letra minúscula, iniciais de palavras subsequentes em maiúscula
>> var minhaIdade; // Correto: primeira letra minúscula, iniciais de palavras subsequentes em maiúscula
>> var nomeCompletoDoUsuario; // Exemplo mais descritivo usando camelCase
>> ```
<hr>
<h3 align="center"> Não esqueça de sempre praticar; você não aprende a andar de bicicleta apenas olhando... essa frase não é sobre bicicleta.</h3>
<hr>

![Diagrama Mermaid](/assets/image/tipoDeDados.svg)
