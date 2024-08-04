<h1 align="center"> Estudando JavaScript</h1>

>![Diagrama Mermaid](/assets/image/introducaojs.svg)
>> ## O que é JavaScript?
>> JavaScript é uma linguagem de programação de alto nível, interpretada e orientada a objetos. É uma das principais tecnologias da web, juntamente com HTML e CSS. É amplamente utilizada para criar páginas web interativas, aplicativos web e servidores. JavaScript permite a manipulação dinâmica de conteúdo, controle de multimídia, animação de gráficos e muito mais.
>
><br>
> 
>> ## História do JavaScript
>> avaScript foi criado por Brendan Eich em 1995 enquanto trabalhava na Netscape. Desenvolvida em apenas dez dias, a linguagem foi inicialmente chamada de Mocha, depois LiveScript, e finalmente JavaScript. Seu objetivo era adicionar interatividade a páginas web. Em 1996, a Microsoft lançou o JScript, e para garantir a compatibilidade entre navegadores, JavaScript foi padronizado pela Ecma International como ECMAScript em 1997.\
Com o tempo, JavaScript evoluiu, tornando-se essencial para o desenvolvimento web, com o surgimento de bibliotecas e frameworks como [jQuery](https://jquery.com/), [Angular](https://angular.io/), [React](https://reactjs.org/), e [Vue.js](https://vuejs.org/), além da plataforma [Node.js](https://nodejs.org/), que permite a execução no lado do servidor. Hoje, JavaScript é amplamente utilizado e continua a evoluir, permanecendo crucial para experiências web dinâmicas.
>
><br>
>
>> ## Versões do JavaScript
>> JavaScript, inventado por Brendan Eich, alcançou o status de um padrão ECMA em 1997 e adotou o nome oficial ECMAScript. Esta linguagem evoluiu através de várias versões, nomeadamente [ES1](https://262.ecma-international.org/1.0/), [ES2](https://262.ecma-international.org/2.0/), [ES3](https://262.ecma-international.org/3.0/), [ES5](https://262.ecma-international.org/5.1/), e a transformadora [ES6](https://262.ecma-international.org/6.0/). Estas atualizações desempenharam um papel crucial na melhoria e padronização do JavaScript, tornando-o amplamente utilizado e valioso no campo em constante mudança do desenvolvimento web.
>
><br>
>
>> ## Como executar JavaScript?
>>
>>### # Executar JavaScript no Navegador
>>Os navegadores modernos possuem consoles de desenvolvedor onde você pode executar código JavaScript diretamente.
>>
>> #### Passos:
>> 1. Abra seu navegador (por exemplo, Chrome, Firefox, Edge).
>> 2. Pressione `F12` ou `Ctrl+Shift+I` (Windows/Linux) ou `Cmd+Opt+I` (Mac) para abrir as ferramentas de desenvolvedor.
>> 3. Vá para a aba "Console".
>> 4. Digite seu código JavaScript e pressione `Enter`.
>> 
>> ```javascript
>> Exemplo:
>>  console.log("Hello, World!");
>> ```
>>
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
>>
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

> ![Diagrama Mermaid](/assets/image/variaveis.svg)
>> ## Declarações de Variáveis 
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
>> ### Hoisting
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
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - var, let, const](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Grammar_and_types)
<br>
<hr>
<h3 align="center"> Não esqueça de sempre praticar; você não aprende a andar de bicicleta apenas olhando... essa frase não é sobre bicicleta.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/tipoDeDados.svg)
>> ## Tipos de Dados Primitivos
>> Em JavaScript, os dados primitivos são os blocos de construção fundamentais que não são objetos e não possuem métodos ou propriedades. Cada tipo primitivo representa um único valor básico e imutável. A seguir, vamos explorar cada um dos sete tipos de dados primitivos em JavaScript, juntamente com exemplos práticos para ilustrar suas características e usos.
> 
>> ### # String
>> O tipo `string` é utilizado para representar sequências de caracteres. Strings podem conter letras, números, símbolos, espaços e outros caracteres.
>> - Strings são criadas usando aspas simples (`'`), aspas duplas (`"`), ou crases (`` ` ``) para strings de template.
>> 
>> #### Exemplos:
>> ```javascript
>> let nome = "Henrique";
>> let corFavorita = 'Vermelho';
>> let frase = `Meu nome é ${nome} e minha cor favorita é ${corFavorita}`;
>> ```
>> - `nome` e `corFavorita` são strings simples.
>> - `frase` é uma string de template que permite interpolação de expressões.
>> 
>> #### # Diferença entre Aspas Simples, Duplas e Crases:
>> **Aspas Simples (`'`) e Duplas (`"`)**:\
>> Utilizadas para strings simples.\
>> Não permitem interpolação de variáveis.\
>> Necessário escape aspas simples e duplas dentro da string (`\'`, `\"`).
>> ```javascript
>> let saudacaoSimples = 'Olá, mundo!';
>> let saudacaoDuplas = "Olá, mundo!";
>> 
>> // Escaping aspas dentro da string
>> let fraseSimples = 'Ele disse: "Olá!"'; // Aspas duplas dentro de aspas simples
>> let fraseDuplas = "Ele disse: 'Olá!'"; // Aspas simples dentro de aspas duplas
>> let exemploEscapingSimples = 'Isso é uma aspa simples: \'';
>> let exemploEscapingDuplas = "Isso é uma aspa dupla: \"";
>> ```
>> **Crases (`` ` ``)**:\
>> Utilizadas para **template literals**.\
>> Permitem interpolação de variáveis e expressões (`${}`).\
>> Suportam strings multilinhas.
>> ```javascript
>> let nome = "Rick";
>> let saudacao = `Olá, ${nome}!`;
>> let multiline = `Esta é uma
>> string com
>> múltiplas linhas.`;
>> ```
>> #### # Comparação
>> **Aspas Simples e Duplas**:\
>> Uso intercambiável, ideal para strings simples.\
>> Não permitem interpolação direta.
>> 
>> **Crases**:\
>> Ideal para strings com interpolação de variáveis e multilinhas.\
>> Mais flexíveis e poderosas.
>> #### Exemplo Comparativo:
>> ```javascript
>> let nome = 'Henrique';
>> let saudacaoSimples = 'Olá, ' + nome + '!'; // usando concatenação
>> let saudacaoDupla = "Olá, " + nome + "!"; // usando concatenação
>> let saudacaoTemplate = `Olá, ${nome}!`;
>> ```
>
> <br>
>
>> ### # Number
>> O tipo `number` representa valores numéricos. JavaScript não diferencia entre inteiros e números de ponto flutuante; ambos são do tipo `number`.
>> - Pode representar números entre -2^53 + 1 e 2^53 - 1.
>> - Suporta notação exponencial para números grandes ou pequenos.
>> #### Exemplos:
>> ```javascript
>> let inteiro = 42;
>> let decimal = 3.14159;
>> let negativo = -7;
>> let grande = 1.23e5; // 1.23 * 10^5 = 123000
>> ```
>> - `inteiro`, `decimal`, `negativo` e `grande` são todos do tipo `number`.
>
> <br>
>
>> ### # Bigint
>> O tipo `bigint` é usado para representar inteiros que estão fora do limite seguro dos números do tipo `number`.
>> - Criado adicionando um `n` no final do número.
>> #### Exemplos:
>> ```javascript
>> let muitoGrande = 1234567890123456789012345678901234567890n;
>> let outroGrande = BigInt("9876543210987654321098765432109876543210");
>> ```
>> - `muitoGrande` e `outroGrande` são do tipo `bigint`.
>
> <br>
>
>> ### # Boolean
>> O tipo `boolean` representa um valor lógico que pode ser `true` ou `false`.
>> - Utilizado em condicionais e loops para controlar o fluxo do programa.
>> #### Exemplos:
>> ```javascript
>> let estaChovendo = true;
>> let estaEnsolarado = false;
>> ```
>> - `estaChovendo` é `true` e `estaEnsolarado` é `false`.
>
> <br>
> 
>> ### # Undefined
>> O tipo `undefined` indica que uma variável foi declarada, mas ainda não foi atribuída um valor.
>> - O valor padrão para variáveis não inicializadas.
>> #### Exemplos:
>> ```javascript
>> let valorIndefinido; // Declarando uma variavel sem valor.
>> console.log(valorIndefinido); // undefined
>> 
>> function naoRetornaNada() {}
>> console.log(naoRetornaNada()); // undefined
>> ```
>> - `valorIndefinido` é `undefined` porque não foi inicializado.
>> - A função `naoRetornaNada` retorna `undefined` porque não possui uma instrução `return`.
>> >OBS: Vamos aprender sobre funções mais adiante.
>
> <br>
> 
>> ### # Symbol
>> O tipo `symbol` é utilizado para criar valores únicos e imutáveis, comumente usados como identificadores de propriedades de objetos para evitar conflitos.
>> - Criado usando a função `Symbol`.
>> - Cada símbolo é único, mesmo se tiverem a mesma descrição.
>> #### Exemplos:
>> ```javascript
>> let simbolo1 = Symbol('descricao');
>> let simbolo2 = Symbol('descricao');
>> console.log(simbolo1 === simbolo2); // false
>> ```
>> - `simbolo1` e `simbolo2` são símbolos diferentes, mesmo com a mesma descrição.
>> #### Aplicação prática:
>> ```javascript
>> let usuario = {
>>   nome: "Henrique",
>>   [Symbol('id')]: 123 // 'id' é um identificador único que não conflita com outras propriedades
>> };
>> ```
>
> <br>
>
>> ### # Null
>> O tipo `null` representa a ausência intencional de qualquer valor de objeto.
>> - É um valor que você pode atribuir a uma variável para indicar que ela não tem valor.
>> #### Exemplos:
>> ```javascript
>> let valorNulo = null;
>> console.log(valorNulo); // null
>> 
>> let objeto = { chave: null };
>> console.log(objeto.chave); // null
>> ```
>> - `valorNulo` é `null`.
>> - `objeto.chave` é `null` indicando a ausência de um valor.
>
> <br>
>
>> ### # Recapitulando:
>> - **string**: Texto, como `"Olá, mundo!"` ou `'Henrique'`
>> - **number**: Números, como `42` ou `3.14`
>> - **bigint**: Números inteiros muito grandes, como `1234567890123456789012345678901234567890n`
>> - **boolean**: Valores lógicos `true` ou `false`
>> - **undefined**: Variável declarada, mas não inicializada, como `let valorIndefinido;`
>> - **symbol**: Valores únicos e imutáveis, como `Symbol('descricao')`
>> - **null**: Ausência intencional de valor, como `let valorNulo = null;`
>> 
>> Esses tipos de dados são fundamentais para manipular informações em JavaScript de forma eficiente e eficaz, e entender suas características e comportamentos é essencial para escrever códigos robustos e bem-estruturados.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Tipo de Dados](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Data_structures).
> <br>
> <br>
>
>> ## Operador TypeOf
>> O operador `typeof` em JavaScript é usado para determinar o tipo de dado de uma variável ou expressão. Ele retorna uma string indicando o tipo do valor fornecido. 
>> #### Aqui estão alguns exemplos de como ele funciona:
>> **Tipos Primitivos:**
>> ```javascript
>> typeof 42;  // "number"
>> typeof "Hello";  // "string"
>> typeof true;  // "boolean"
>> typeof undefined;  // "undefined"
>> typeof null;  // "object" (nota: isso é um erro histórico em JavaScript)
>> ```
>> **Objetos e Funções:**
>> ```javascript
>> typeof { key: 'value' };  // "object"
>> typeof [1, 2, 3];  // "object"
>> typeof function() {};  // "function"
>> ```
>> **Operadores Unários:**
>> ```javascript
>> typeof typeof 42;  // "string", pois typeof 42 retorna "number"
>> ```
>> ### Comportamento Importante:
>> - **Null:** Embora `typeof null` retorne `"object"`, isso é um erro histórico em JavaScript e não reflete o verdadeiro tipo de dado `null`.
>> - **Funções:** O `typeof` pode identificar funções como `"function"`, o que é útil para diferenciação em estruturas de controle ou manipulação de objetos.
>> ### Uso Prático:
>> O `typeof` é útil em situações onde você precisa verificar dinamicamente o tipo de dado antes de realizar operações específicas que variam de acordo com o tipo.
>> #### Por exemplo:
>> ```javascript
>> function printType(value) {
>>     console.log(typeof value);
>> }
>> 
>> printType(42);  // "number"
>> printType("Hello");  // "string"
>> printType({ key: 'value' });  // "object"
>> ```
>> Isso permite que seu código tome decisões com base no tipo de dado que está manipulando, melhorando a robustez e a flexibilidade das funções.
>> > ##### OBS: Você pode aprender mais lendo esse artigo:[MDN - Operador typeOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof)
> <br>
> <br>
>
>> ## Objetos
>> Objetos em JavaScript são coleções de propriedades, e uma propriedade é uma associação entre um nome (ou chave) e um valor. Um objeto pode ser visto como uma coleção de pares chave-valor. Aqui está um resumo de como definir e usar objetos em JavaScript, com base na referência fornecida do W3Schools.
>> 
>> ### # Definindo Objetos
>> Existem várias maneiras de definir um objeto em JavaScript:
>> #### Usando a notação literal usando `{...}`:
>> ```javascript
>> const pessoa = {
>>   primeiroNome: "Henrique",
>>   segundoNome: "Lustri",
>>   idade: 22,
>>   altura: 175
>> };
>> ```
>> Neste exemplo, `pessoa` é um objeto com quatro propriedades: `primeiroNome`, `segundoNome`, `idade`, e `altura`.
>> 
>> #### Usando o construtor `new Object()`:
>> ```javascript
>> const pessoa = new Object();
>> pessoa.primeiroNome = "Henrique";
>> pessoa.ultimoNome = "Lustri";
>> pessoa.idade = 22;
>> pessoa.altura = 175;
>> ```
>> Esta é uma abordagem mais longa e geralmente menos usada do que a notação literal.
>> 
>> ### # Acessando Propriedades
>> Você pode acessar as propriedades de um objeto usando a notação de ponto (`.`) ou a notação de colchetes (`[]`):
>> #### Notação de ponto:
>> ```javascript
>>  const pessoa = {
>>   primeiroNome: "Henrique",
>>   segundoNome: "Lustri",
>>   idade: 22,
>>   altura: 175
>> };
>> 
>> console.log(pessoa.primeiroNome); // Saida: Henrique
>> console.log(pessoa.segundoNome); // Saida: Lustri
>> ```
>> #### Notação de colchetes:
>> ```javascript
>>  const pessoa = {
>>   primeiroNome: "Henrique",
>>   segundoNome: "Lustri",
>>   idade: 22,
>>   altura: 175
>> };
>> 
>> console.log(pessoa["segundoNome"]); // Saida: Lustri
>> console.log(pessoa["idade"]); // Saida: 22
>> ```
>> 
>> ### # Métodos de Objetos
>> Objetos também podem conter métodos, que são funções associadas a objetos:
>> ```javascript
>> const pessoa = {
>>   primeiroNome: "Henrique",
>>   segundoNome: "Lustri",
>>   idade: 22,
>>   altura: 175,
>>   nomeCompleto: function() {
>>     return this.primeiroNome + " " + this.segundoNome;
>>   }
>> };
>> 
>> console.log(pessoa.nomeCompleto()); // Saida: Henrique Lustri
>> ```
>> No exemplo acima, `nomeCompleto` é um método do objeto `pessoa`. Ele retorna o nome completo ao concatenar `primeiroNome` e `segundoNome`.
>> 
>> ### # Modificando Objetos
>> Você pode adicionar, modificar ou deletar propriedades de um objeto após sua criação:
>> #### Adicionando novas propriedades:
>> ```javascript
>> pessoa.nacionalidade = "Brasileiro";
>> ```
>> #### Modificando propriedades existentes:
>> ```javascript
>> pessoa.idade = 23;
>> ```
>> #### Deletando propriedades:
>> ```javascript
>> delete pessoa.altura;
>> ```
>> 
>> #### Exemplo Completo:
>> Exemplo que reúne todos esses conceitos:
>> ```javascript
>> const carro = {
>>   marca: "Porsche",
>>   modelo: "911 Carrera GTS",
>>   ano: 2024,
>>   descricao: function() {
>>     return this.marca + " " + this.modelo + " " + this.ano;
>>   }
>> };
>> 
>> console.log(carro.descricao()); // Saida: Porsche 911 Carrera GTS 2024
>> carro.cor = "vermelho"; // Adiciona uma nova propriedade
>> carro.ano = 2021; // Modifica a propriedade existente
>> delete carro.modelo; // Deleta a propriedade
>> ```
>
> <br>
> 
>> ## Objetos embutidos (Built-in objects)
>> JavaScript oferece vários objetos integrados (built-in) que facilitam muitas operações comuns, sem a necessidade de criar tudo do zero. Esses objetos são parte da linguagem e estão disponíveis globalmente, o que significa que você pode usá-los diretamente em seu código.
>> ### # `String`
>> O objeto `String` é usado para representar e manipular sequências de caracteres. Strings são imutáveis, ou seja, uma vez criadas, não podem ser alteradas diretamente, mas você pode criar novas strings baseadas nas existentes.
>> #### Criação:
>> ```javascript
>> // Criando uma string usando uma notação literal
>> let texto = "Olá, Mundo!";
>> 
>> // Criando uma string usando o construtor String (não é comum)
>> let textoObj = new String("Olá, Mundo!");
>> ```
>> #### Propriedades e Métodos Comuns:
>> ```javascript
>> // Tamanho da string
>> console.log(texto.length); // 11
>> 
>> // Converte todos os caracteres para maiúsculas
>> console.log(texto.toUpperCase()); // "OLÁ, MUNDO!"
>> 
>> // Converte todos os caracteres para minúsculas
>> console.log(texto.toLowerCase()); // "olá, mundo!"
>> 
>> // Verifica se a string contém a palavra "Mundo"
>> console.log(texto.includes("Mundo")); // true
>> 
>> // Substitui a palavra "Mundo" por "JavaScript"
>> console.log(texto.replace("Mundo", "JavaScript")); // "Olá, JavaScript!"
>> 
>> // Retorna o caractere na posição 0 (primeiro caractere)
>> console.log(texto.charAt(0)); // "O"
>> 
>> // Extrai uma parte da string entre os índices 0 e 2 (não inclui o índice 2)
>> console.log(texto.substring(0, 2)); // "Olá"
>> 
>> // Exemplo:
>> // 0 - O
>> // 1 - l
>> // 2 - á
>> // 3 - ,
>> // 4 - ' '
>> // ... assim por diante ate mapear a string toda...
>> ```
>> 
>> ### # `Number`
>> O objeto `Number` é usado para representar e manipular números, incluindo inteiros e números de ponto flutuante. Ele inclui constantes e métodos úteis para trabalhar com números.
>> #### Criação:
>> ```javascript
>> // Criando um número usando uma notação literal
>> let numero = 123;
>> 
>> // Criando um número usando o construtor Number (não é comum)
>> let numeroObj = new Number(123);
>> ```
>> #### Propriedades e Métodos Comuns:
>> ```javascript
>> // Converte o número para uma string
>> console.log(numero.toString()); // "123"
>> 
>> // Formata o número para ter 2 casas decimais
>> console.log(numero.toFixed(2)); // "123.00"
>> 
>> // Verifica se o valor é um número inteiro
>> console.log(Number.isInteger(numero)); // true
>> 
>> // Verifica se o valor é NaN (Not-a-Number)
>> console.log(Number.isNaN(NaN)); // true
>> 
>> // Maior valor numérico representável
>> console.log(Number.MAX_VALUE); // 1.7976931348623157e+308
>> 
>> // Menor valor numérico representável
>> console.log(Number.MIN_VALUE); // 5e-324
>> ```
>> 
>> ### # `Math`
>> O objeto `Math` fornece propriedades e métodos para constantes e funções matemáticas. Todos os métodos e propriedades são estáticos.
>> #### Uso Comum:
>> ```javascript
>> // Valor de Pi (aproximado)
>> console.log(Math.PI); // 3.141592653589793
>> 
>> // Raiz quadrada de 16
>> console.log(Math.sqrt(16)); // 4
>> 
>> // Número aleatório entre 0 (inclusivo) e 1 (exclusivo)
>> console.log(Math.random()); // Pode ser qualquer valor entre 0 e 1
>> 
>> // Maior valor entre os números fornecidos
>> console.log(Math.max(10, 20, 30)); // 30
>> 
>> // Menor valor entre os números fornecidos
>> console.log(Math.min(10, 20, 30)); // 10
>> 
>> // Arredonda o número para baixo
>> console.log(Math.floor(1.7)); // 1
>> 
>> // Arredonda o número para cima
>> console.log(Math.ceil(1.2)); // 2
>> 
>> // Arredonda o número para o inteiro mais próximo
>> console.log(Math.round(1.5)); // 2
>> ```
>> 
>> ### # `Date`
>> O objeto `Date` é usado para trabalhar com datas e horas. Ele representa um ponto no tempo e fornece métodos para obter e manipular datas e horários.
>> #### Criação:
>> ```javascript
>> // Cria um objeto Date com a data e hora atuais
>> let dataAtual = new Date();
>> 
>> // Cria um objeto Date com uma data específica
>> let dataEspecifica = new Date('2024-07-19');
>> 
>> // Cria um objeto Date a partir de um número de milissegundos desde 1 de janeiro de 1970
>> let dataMilissegundos = new Date(1626652800000);
>> ```
>> #### Propriedades e Métodos Comuns:
>> ```javascript
>> // Obtém o ano da data atual
>> console.log(dataAtual.getFullYear()); // Ano atual (ex: 2024)
>> 
>> // Obtém o mês da data atual (0-11, onde 0 é janeiro e 11 é dezembro)
>> console.log(dataAtual.getMonth()); // Mês atual (ex: 6 para julho)
>> 
>> // Obtém o dia do mês
>> console.log(dataAtual.getDate()); // Dia do mês (ex: 19)
>> 
>> // Obtém o dia da semana (0-6, onde 0 é domingo e 6 é sábado)
>> console.log(dataAtual.getDay()); // Dia da semana (ex: 5 para sexta-feira)
>> 
>> // Obtém a hora atual
>> console.log(dataAtual.getHours()); // Hora atual (ex: 14 para 2 PM)
>> 
>> // Obtém os minutos atuais
>> console.log(dataAtual.getMinutes()); // Minutos atuais (ex: 30)
>> 
>> // Obtém os segundos atuais
>> console.log(dataAtual.getSeconds()); // Segundos atuais (ex: 45)
>> 
>> // Converte a data para uma string em formato legível
>> console.log(dataAtual.toLocaleDateString()); // Ex: "19/07/2024"
>> 
>> // Obtém o número de milissegundos desde 1 de janeiro de 1970
>> console.log(Date.now()); // Ex: 1626652800000
>> ```
>> 
>> ### # `Error`
>> O objeto `Error` é usado para representar um erro que ocorreu durante a execução de um script. É útil para lançar e capturar exceções.
>> #### Criação:
>> ```javascript
>> // Cria um novo objeto Error com uma mensagem personalizada
>> let erro = new Error("Algo deu errado!");
>> ```
>> #### Uso Comum:
>> ```javascript
>> try {
>>   // Lança o erro criado
>>   throw erro;
>> } catch (e) {
>>   // Captura o erro e exibe o nome e a mensagem do erro
>>   console.log(e.name); // "Error"
>>   console.log(e.message); // "Algo deu errado!"
>> }
>> ```
>> Existem tipos específicos de erros, como `TypeError`, `RangeError`, e `ReferenceError`, que fornecem informações mais detalhadas sobre o tipo de erro que ocorreu.
>> 
>> ### # `Function`
>> O objeto `Function` é usado para criar novas funções dinamicamente. Embora seja possível criar funções com `Function`, a maioria das funções é definida usando declarações ou expressões.
>> #### Criação:
>> ```javascript
>> // Cria uma nova função que soma dois números
>> let soma = new Function('a', 'b', 'return a + b');
>> 
>> // Chama a função e exibe o resultado
>> console.log(soma(2, 3)); // 5
>> ```
>> #### Uso Comum:
>> Normalmente, funções são definidas usando declarações de função ou expressões de função:
>> ```javascript
>> // Declaração de função
>> function minhaFuncao(a, b) {
>>   return a + b;
>> }
>> 
>> // Expressão de função
>> let minhaOutraFuncao = function(a, b) {
>>   return a + b;
>> };
>> 
>> // Chama as funções
>> console.log(minhaFuncao(2, 3)); // 5
>> console.log(minhaOutraFuncao(4, 5)); // 9
>> ```
>> 
>> ### # `Boolean`
>> O objeto `Boolean` é usado para representar um valor booleano (verdadeiro ou falso). Normalmente, os valores booleanos são usados diretamente sem a necessidade do construtor `Boolean`.
>> #### Criação:
>> ```javascript
>> // Cria um objeto Boolean com valor verdadeiro
>> let verdadeiro = new Boolean(true);
>> 
>> // Cria um objeto Boolean com valor falso
>> let falso = new Boolean(false);
>> ```
>> #### Uso Comum:
>> Normalmente, valores booleanos são usados diretamente:
>> ```javascript
>> // Declara variáveis booleanas diretamente
>> let isTrue = true;
>> let isFalse = false;
>> 
>> // Verifica o valor das variáveis booleanas
>> console.log(isTrue); // true
>> console.log(isFalse); // false
>> ```
>
> <br>
>
>> ## Prototypes
>> ### # O Que São Prototypes?
>> Em JavaScript, **prototypes** são um mecanismo que permite a criação de novos objetos a partir de outros objetos. Cada objeto tem uma referência interna para outro objeto chamado de prototype. Esta referência é acessível via `Object.getPrototypeOf(obj)` e `obj.__proto__` (embora o uso de `__proto__` seja desencorajado).
>> 
>> Quando você tenta acessar uma propriedade de um objeto, o JavaScript verifica primeiro se essa propriedade existe no próprio objeto. Se não encontrar, ele procura na cadeia de protótipos. Esta cadeia é uma sequência de objetos conectados por suas referências de prototype.
>> 
>> #### Exemplo de Prototypes:
>> ```javascript
>> // Definindo uma função construtora
>> function Pessoa(nome) {
>>     this.nome = nome; // Propriedade 'nome' definida diretamente no objeto
>> }
>> 
>> // Adicionando um método ao prototype de Pessoa
>> Pessoa.prototype.falarOla = function() {
>>     console.log(`Olá, meu nome é ${this.nome}`); // 'this.nome' acessa a propriedade do objeto
>> };
>> 
>> // Criando uma nova instância de Pessoa
>> const henrique = new Pessoa('Henrique');
>> 
>> // Chamando o método 'falarOla' da instância 'henrique'
>> henrique.falarOla(); // Saida: Olá, meu nome é Henrique
>> ```
>> #### Explicação do Exemplo:
>> 1. **Função Construtora:** `Pessoa` é uma função construtora que cria objetos com uma propriedade `nome`.
>> 2. **Método no Prototype:** O método `falarOla` é adicionado ao prototype da função `Pessoa`. Assim, todas as instâncias de `Pessoa` terão acesso a esse método.
>> 3. **Instância e Acesso ao Método:** Quando criamos `henrique` usando `new Pessoa('Henrique')`, ele herda o método `falarOla` do prototype. Isso permite que chamemos `henrique.falarOla()` e acesse a propriedade `nome` definida na instância.
>
> <br>
>
>> ## Prototypal Inheritance
>> #### O Que é Prototypal Inheritance?
>> **Prototypal Inheritance** é o modelo de herança em JavaScript onde objetos podem herdar diretamente de outros objetos. Em vez de definir uma classe base e subclasses, você pode criar um objeto a partir de outro objeto, permitindo que o novo objeto herde as propriedades e métodos do objeto original.
>> #### Exemplo de Prototypal Inheritance:
>> ```javascript
>> // Criando um objeto 'animal' com uma propriedade 'comem'
>> const animal = {
>>     comem: true // Todos os animais "comem"
>> };
>> 
>> // Criando um novo objeto 'coelho' que herda de 'animal'
>> const coelho = Object.create(animal); // 'coelho' herda de 'animal'
>> coelho.pular = true; // 'coelho' tem uma propriedade própria 'pular'
>> 
>> // Acessando propriedades do objeto 'coelho'
>> console.log(coelho.comem); // Saida: true (herdado de 'animal')
>> console.log(coelho.pular); // Saida: true (propriedade própria de 'coelho')
>> 
>> // Demonstrando a cadeia de protótipos
>> console.log(Object.getPrototypeOf(coelho) === animal); // Saida: true (verifica se 'animal' é o >> protótipo de 'coelho')
>> ```
>> #### Explicação do Exemplo:
>> 1. **Objeto Base:** `animal` é um objeto com uma propriedade `comem`. Esse objeto serve como protótipo.
>> 2. **Criação do Objeto Herdeiro:** Usamos `Object.create(animal)` para criar `coelho`. Este método cria um novo objeto que herda diretamente de `animal`.
>> 3. **Propriedades e Métodos:** `coelho` pode acessar a propriedade `comem` herdada de `animal`. Além disso, `coelho` tem uma propriedade própria chamada `pular`.
>> 4. **Verificação da Cadeia de Protótipos:** `Object.getPrototypeOf(coelho)` retorna o objeto de que `coelho` herda, que é `animal`. Isso confirma a cadeia de protótipos.
>
>> ### Conclusão:
>> - **Prototypes** em JavaScript permitem que objetos compartilhem métodos e propriedades, economizando memória e promovendo a reutilização de código.
>> - **Prototypal Inheritance** permite criar objetos que herdam diretamente de outros objetos, criando uma cadeia onde propriedades e métodos podem ser acessados e compartilhados entre objetos.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Objetos](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_objects) e [MDN - prototypes e prototypal inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
<br>
<hr>
<h3 align="center"> Não esqueça de sempre praticar; você não aprende a andar de skate apenas olhando... essa frase não é sobre skate.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/conversaoDeTipos.svg)
>> ## Conversão de Tipos (Type Casting)
>> **Type Casting** refere-se ao processo de transformar um valor de um tipo de dado para outro tipo. Em JavaScript, isso pode ser feito de forma explícita ou implícita.
>> ### # Conversão de tipo explícito (Explicit Type Casting)
>> **Explicit Type Casting** (ou casting explicit) ocorre quando você, como desenvolvedor, toma medidas específicas para converter um tipo de dado para outro. Isso é feito usando funções e métodos específicos para fazer a conversão.
>> #### Exemplos:
>> **Convertendo para Número:**
>> ```javascript
>> let texto = "123"; // Declaração de uma string com valor "123"
>> let numero = Number(texto); // Converte a string para número usando a função Number
>> console.log(numero); // 123 - Saída do número convertido
>> console.log(typeof numero); // "number" - Saída do tipo do valor convertido
>> ```
>> **Convertendo para String:**
>> ```javascript
>> let numero = 123; // Declaração de um número
>> let texto = String(numero); // Converte o número para string usando a função String
>> console.log(texto); // "123" - Saída da string convertida
>> console.log(typeof texto); // "string" - Saída do tipo do valor convertido
>> ```
>> **Convertendo para Booleano:**
>> ```javascript
>> let valor = 0; // Declaração de um número com valor 0
>> let bool = Boolean(valor); // Converte o número para booleano usando a função Boolean
>> console.log(bool); // false - Saída do booleano convertido
>> console.log(typeof bool); // "boolean" - Saída do tipo do valor convertido
>> ```
>
> <br>
>
>> ### # Conversão de tipo implícita (Implicit Type Casting)
>> **Implicit Type Casting** (ou casting implicit) ocorre quando o JavaScript automaticamente converte tipos de dados conforme necessário. Isso geralmente acontece em operações que envolvem diferentes tipos de dados.
>> #### Exemplos:
>> **Concatenação de Strings:**
>> ```javascript
>> let numero = 123; // Declaração de um número
>> let texto = "O número é " + numero; // Concatena número com string, convertendo implicitamente o número para string
>> console.log(texto); // "O número é 123" - Saída da string concatenada
>> console.log(typeof texto); // "string" - Saída do tipo do valor resultante
>> ```
>> **Operações Aritméticas:**
>> ```javascript
>> let texto = "5"; // Declaração de uma string com valor "5"
>> let numero = 10; // Declaração de um número com valor 10
>> let resultado = texto * numero; // Multiplica string por número, convertendo implicitamente a string para número
>> console.log(resultado); // 50 - Saída do resultado da multiplicação
>> console.log(typeof resultado); // "number" - Saída do tipo do valor resultante
>> ```
>> **Contexto Booleano:**
>> ```javascript
>> let valor = "Olá"; // Declaração de uma string com valor "hello"
>> if (valor) { // Converte a string para booleano implicitamente
>>     console.log("A string não está vazia!"); // "A string não está vazia!" - Saída caso a string seja verdadeira
>> }
>> ```
>
> <br>
>
>> ### # Conversão/coerção de tipo (Type Conversion/Coercion)
>> **Type Conversion** (ou **Type Coercion**) refere-se ao mesmo conceito de Type Casting, onde um tipo de dado é convertido em outro. Em JavaScript, a conversão de tipo pode ser:
>> - **Automática (implícita)**: Quando o JavaScript automaticamente converte o tipo de dado conforme necessário, como mostrado nos exemplos de casting implícito.
>> - **Manual (explícita)**: Quando o desenvolvedor usa métodos e funções específicas para converter os tipos de dados, como mostrado nos exemplos de casting explícito.
>> 
>> A conversão de tipo pode ocorrer em diferentes contextos, como em operações aritméticas, comparação de valores, e contextos booleanos.
>> #### Exemplos:
>> **Comparação de Valores:**
>> ```javascript
>> console.log("5" == 5); // true - Converte string para número implicitamente e compara os valores
>> console.log("5" === 5); // false - Sem conversão implícita, compara tipos diferentes (string e número)
>> ```
>> **Operações Aritméticas com Strings:**
>> ```javascript
>> let resultado = "10" - 2; // Converte string para número implicitamente e realiza a subtração
>> console.log(resultado); // 8 - Saída do resultado da subtração
>> console.log(typeof resultado); // "number" - Saída do tipo do valor resultante
>> ```
>> **Conversão em Contexto Booleano:**
>> ```javascript
>> let valor = ""; // Declaração de uma string vazia
>> if (valor) { // Converte a string vazia para false implicitamente
>>     console.log("Esta mensagem não será exibida");
>> } else {
>>     console.log("String está vazia"); // "String está vazia" - Saída caso a string seja falsa
>> }
>> ```
<br>
<hr>
<h3 align="center"> Não esqueça de sempre praticar; você não aprende a andar de patinete apenas olhando... essa frase não é sobre patinete.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/estruturaDeDados.svg)
>> ## Estruturas de Dados
>> As estruturas de dados são formas organizadas de armazenar e manipular informações em um computador. Elas são fundamentais para a eficiência dos algoritmos e do desempenho dos programas. Vamos explorar algumas das principais categorias de estruturas de dados em detalhes.
>> ### Coleções Indexadas (Indexed collections)
>> **Indexed collections** são estruturas de dados onde os elementos são acessados através de índices numéricos. Dois exemplos comuns são matrizes e matrizes tipadas.
>> ### # Matrizes (Arrays)
>> Uma **matriz** (ou array) é uma coleção de elementos, geralmente do mesmo tipo, armazenados em posições consecutivas na memória. Os elementos são acessados por índices, que começam em 0.
>> 
>> **Criação de um Array**:\
>> Você pode criar um array usando colchetes `[]` e separando os elementos por vírgulas.
>> ```javascript
>> let frutas = ["Maçã", "Banana", "Laranja"];
>> ```
>> **Acessando Elementos**:\
>> Os elementos são acessados usando o índice do array, que começa em 0.
>> ```javascript
>> console.log(frutas[0]); // Saída: Maçã
>> console.log(frutas[1]); // Saída: Banana
>> console.log(frutas[2]); // Saída: Laranja
>> ```
>> **Modificando Elementos**:\
>> Você pode modificar os elementos do array atribuindo novos valores aos índices correspondentes.
>> ```javascript
>> frutas[1] = "Morango";
>> console.log(frutas[1]); // Saída: Morango
>> ```
>> **Métodos Comuns**:\
>> Arrays vêm com diversos métodos embutidos para manipulação.
>> ```javascript
>> // Adiciona um elemento ao final
>> frutas.push("Uva");
>> console.log(frutas); // Saída: ["Maçã", "Morango", "Laranja", "Uva"]
>> 
>> // Remove o último elemento
>> frutas.pop();
>> console.log(frutas); // Saída: ["Maçã", "Morango", "Laranja"]
>> 
>> // Itera sobre os elementos
>> frutas.forEach(function(fruta) {
>>   console.log(fruta);
>> });
>> // Saída:
>> // Maçã
>> // Morango
>> // Laranja
>> 
>> // Adiciona um elemento ao início
>> frutas.unshift("Pera");
>> console.log(frutas); // Saída: ["Pera", "Maçã", "Morango", "Laranja"]
>> 
>> // Remove o primeiro elemento
>> frutas.shift();
>> console.log(frutas); // Saída: ["Maçã", "Morango", "Laranja"]
>> 
>> // Encontra o índice de um elemento
>> let indice = frutas.indexOf("Morango");
>> console.log(indice); // Saída: 1
>> 
>> // Remove um elemento específico
>> let indiceBanana = frutas.indexOf("Banana");
>> if (indiceBanana !== -1) {
>>   frutas.splice(indiceBanana, 1);
>> }
>> console.log(frutas); // Saída: ["Maçã", "Morango", "Laranja"]
>> 
>> // Copia uma parte do array
>> let algumasFrutas = frutas.slice(1, 3);
>> console.log(algumasFrutas); // Saída: ["Morango", "Laranja"]
>> 
>> // Mescla dois arrays
>> let maisFrutas = ["Abacaxi", "Manga"];
>> let todasFrutas = frutas.concat(maisFrutas);
>> console.log(todasFrutas); // Saída: ["Maçã", "Morango", "Laranja", "Abacaxi", "Manga"]
>> ```
>> 
>> ### # Matrizes Tipadas (Typed Arrays)
>> **Matrizes tipadas** são arrays que armazenam dados de um único tipo. Elas são úteis para operações de baixo nível e manipulação de grandes volumes de dados numéricos.
>> 
>> **Criação de um Typed Array**:\
>> Você cria um Typed Array usando construtores como `Int32Array`, `Float64Array`, etc.
>> ```javascript
>> let buffer = new ArrayBuffer(16); // Cria um buffer de 16 bytes
>> let int32View = new Int32Array(buffer); // Cria uma visão Int32Array sobre o buffer
>> 
>> int32View[0] = 42;
>> int32View[1] = 43;
>> 
>> console.log(int32View[0]); // Saída: 42
>> console.log(int32View[1]); // Saída: 43
>> ```
>> **Iterando sobre um Typed Array**:\
>> Você pode usar um loop para iterar sobre os elementos de um Typed Array.
>> ```javascript
>> for (let i = 0; i < int32View.length; i++) {
>>   console.log(int32View[i]);
>> }
>> // Saída:
>> // 42
>> // 43
>> // 0
>> // 0
>> ```
>
> <br>
>
>> ### Coleções Chaveadas (Keyed Collections)
>> **Keyed Collections** armazenam dados em pares chave-valor, permitindo acesso eficiente aos valores através de suas chaves.
>> ### # Map
>> Um **Map** é uma coleção de pares chave-valor onde as chaves podem ser de qualquer tipo.
>> 
>> **Criação de um Map**:\
>> Você cria um Map usando o construtor `Map`.
>> ```javascript
>> let mapa = new Map();
>> ```
>> **Adicionando e Acessando Elementos**:\
>> Use `set` para adicionar elementos e `get` para acessá-los.
>> ```javascript
>> mapa.set("nome", "Henrique");
>> mapa.set("idade", 22);
>> 
>> console.log(mapa.get("nome")); // Saída: Henrique
>> console.log(mapa.get("idade")); // Saída: 22
>> ```
>> **Verificando a Existência de uma Chave**:\
>> Use `has` para verificar se uma chave existe no Map.
>> ```javascript
>> console.log(mapa.has("nome")); // Saída: true
>> console.log(mapa.has("endereço")); // Saída: false
>> ```
>> **Removendo Elementos**:\
>> Use `delete` para remover um elemento por sua chave.
>> ```javascript
>> mapa.delete("idade");
>> console.log(mapa.has("idade")); // Saída: false
>> ```
>> **Iterando sobre um Map**:\
>> Você pode usar `forEach` ou `for...of` para iterar sobre os elementos do Map.
>> ```javascript
>> mapa.forEach((valor, chave) => {
>>   console.log(`${chave}: ${valor}`);
>> });
>> // Saída:
>> // nome: Henrique
>> 
>> for (let [chave, valor] of mapa) {
>>   console.log(`${chave}: ${valor}`);
>> }
>> // Saída:
>> // nome: Henrique
>> ```
>> 
>> ### # WeakMap
>> Um **WeakMap** é similar a um Map, mas só aceita objetos como chaves e não impede que esses objetos sejam coletados pelo garbage collector se não houver outras referências a eles.
>> 
>> **Criação de um WeakMap**:\
>> Use o construtor `WeakMap`.
>> ```javascript
>> let weakMap = new WeakMap();
>> ```
>> **Adicionando e Acessando Elementos**:\
>> Use `set` para adicionar elementos e `get` para acessá-los.
>> ```javascript
>> let obj = {nome: "Henrique"};
>> weakMap.set(obj, "algum valor");
>> 
>> console.log(weakMap.get(obj)); // Saída: algum valor
>> ```
>> **Garbage Collection**:\
Quando a referência ao objeto é removida, ele pode ser coletado pelo garbage collector.
>> ```javascript
>> obj = null; // O objeto agora é elegível para garbage collection
>> ```
>> 
>> ### # Set
>> Um **Set** é uma coleção de valores únicos, ou seja, não permite elementos duplicados.
>> 
>> **Criação de um Set**:\
>> Use o construtor `Set`.
>> ```javascript
>> let conjunto = new Set();
>> ```
>> **Adicionando Elementos**:\
>> Use `add` para adicionar elementos.
>> ```javascript
>> conjunto.add(1);
>> conjunto.add(2);
>> conjunto.add(2); // Ignorado, pois 2 já está no conjunto
>> ```
>> **Verificando a Existência de um Elemento**:\
>> Use `has` para verificar se um elemento existe no Set.
>> ```javascript
>> console.log(conjunto.has(1)); // Saída: true
>> console.log(conjunto.has(3)); // Saída: false
>> ```
>> **Removendo Elementos**:\
>> Use `delete` para remover um elemento.
>> ```javascript
>> conjunto.delete(1);
>> console.log(conjunto.has(1)); // Saída: false
>> ```
>> **Iterando sobre um Set**:\
>> Você pode usar `forEach` ou `for...of` para iterar sobre os elementos do Set.
>> ```javascript
>> conjunto.forEach((valor) => {
>>   console.log(valor);
>> });
>> // Saída:
>> // 2
>> 
>> for (let valor of conjunto) {
>>   console.log(valor);
>> }
>> // Saída:
>> // 2
>> ```
>> 
>> ### # WeakSet
>> Um **WeakSet** é similar a um Set, mas só armazena objetos e permite que esses objetos sejam coletados pelo garbage collector se não houver outras referências a eles.
>> 
>> **Criação de um WeakSet**:\
>> Use o construtor `WeakSet`.
>> ```javascript
>> let weakSet = new WeakSet();
>> ```
>> **Adicionando Elementos**:\
>> Use `add` para adicionar elementos.
>> ```javascript
>> let obj1 = {data: "dados"};
>> weakSet.add(obj1);
>> ```
>> **Garbage Collection**:\
>> Quando a referência ao objeto é removida, ele pode ser coletado pelo garbage collector.
>> ```javascript
>> obj1 = null; // O objeto agora é elegível para garbage collection
>> ```
>
> <br>
>
>> ### Dados Estruturados (Structured data)
>> **Structured data** são usados para representar e trocar dados de maneira estruturada e legível.
>> ### # JSON
>> **JSON** (JavaScript Object Notation) é um formato leve de troca de dados, fácil de ler e escrever para humanos e fácil de analisar e gerar para máquinas.
>> 
>> **Objeto JavaScript**:\
>> Um objeto em JavaScript pode ser convertido para JSON.
>> ```javascript
>> let pessoa = {
>>   nome: "Henrique",
>>   idade: 22,
>>   cidade: "São Paulo"
>> };
>> ```
>> **Conversão para JSON**:\
>> Use `JSON.stringify` para converter um objeto JavaScript para uma string JSON.
>> ```javascript
>> let json = JSON.stringify(pessoa);
>> console.log(json); // Saída: {"nome":"Henrique","idade":22,"cidade":"São Paulo"}
>> ```
>> **Conversão de JSON para Objeto**:\
>> Use `JSON.parse` para converter uma string JSON de volta para um objeto JavaScript.
>> ```javascript
>> let obj = JSON.parse(json);
>> console.log(obj.nome); // Saída: Henrique
>> ```
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Arrays](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array), [MDN - Typed Arrays](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Typed_arrays), [MDN - Map](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Map), [MDN - WeakMap](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/WeakMap), [MDN - Set](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Set), [MDN - WeakSet](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/WeakSet), [MDN - JSON](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/JSON)
<br>
<hr>
<h3 align="center"> Não esqueça de sempre praticar; você não aprende a programar apenas olhando... essa sim! essa frase é sobre programar.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/conparacaoDeIgualdade.svg)
>> ## Comparação de Igualdade
>> Comparações de igualdade são fundamentais em JavaScript para verificar se dois valores são iguais. Existem diferentes operadores e algoritmos para fazer essas comparações, cada um com suas particularidades. Vamos explorar os principais operadores de comparação de valor e os algoritmos de igualdade em detalhes.
>> ### # Operador de Comparação 
>> #### `==` (Igualdade)
>> O operador `==` compara dois valores para igualdade, realizando conversão de tipo (type coercion) se necessário. Isso significa que ele tenta converter os operandos para um tipo comum antes de compará-los.
>> ```javascript
>> console.log(1 == '1'); // true
>> // O valor numérico 1 é comparado com o valor da string '1'.
>> // A string é convertida para o número 1 antes da comparação, resultando em true.
>> 
>> console.log(true == 1); // true
>> // O valor booleano true é comparado com o valor númerico 1.
>> // true é convertido para 1 antes da comparação, resultando em true.
>> 
>> console.log(null == undefined); // true
>> // null e undefined são considerados iguais pelo operador ==
>> ```
>> #### `===` (Igualdade Estrita)
>> O operador `===` compara dois valores para igualdade sem realizar conversão de tipo. Ambos os valores e tipos devem ser iguais para que a comparação seja verdadeira.
>> ```javascript
>> console.log(1 === '1'); // false
>> // O valor numérico 1 é comparado com a string '1'.
>> // Como os tipos são diferentes (número e string), o resultado é false.
>> 
>> console.log(true === 1); // false
>> // O valor booleano true é comparado com o número 1.
>> // Como os tipos são diferentes (booleano e número), o resultado é false.
>> 
>> console.log(null === undefined); // false
>> // null e undefined têm tipos diferentes, resultando em false.
>> ```
>> #### `Object.is()`
>> O método `Object.is()` compara dois valores para igualdade. Ele é semelhante ao operador `===`, mas trata `NaN` como igual a `NaN` e diferencia `+0` de `-0`.
>> ```javascript
>> console.log(Object.is(1, 1)); // true
>> // Ambos os valores e tipos são iguais.
>> 
>> console.log(Object.is(NaN, NaN)); // true
>> // Diferente de `===`, `Object.is()` considera NaN igual a NaN.
>> 
>> console.log(Object.is(+0, -0)); // false
>> // `Object.is()` diferencia +0 e -0, ao contrário de `===`.
>> ```
>
> <br>
>
>> ### # Algoritmos de Igualdade
>> #### `LooselyEqual` (algoritmo de igualdade abstrata)
>> O algoritmo de igualdade abstrata é usado pelo operador `==` para comparar dois valores com coerção de tipo.\
>> #### Algumas das regras principais incluem:
>> - Se um valor é `null` e o outro é `undefined`, eles são iguais.
>> - Se um valor é um número e o outro é uma string, converta a string para número e compare.
>> - Se um valor é booleano, converta-o para número (`true` se torna `1`, `false` se torna `0`) e compare.
>> - Se um valor é um objeto e o outro é um tipo primitivo, converta o objeto para seu valor primitivo usando a função `toPrimitive`.
>> ```javascript
>> console.log('42' == 42); // true
>> // A string '42' é convertida para o número 42 antes da comparação, resultando em true.
>> 
>> console.log(true == 1); // true
>> // O booleano true é convertido para o número 1 antes da comparação, resultando em true.
>> 
>> console.log([1, 2] == '1,2'); // true
>> // O array [1, 2] é convertido para a string '1,2' antes da comparação, resultando em true.
>> 
>> console.log({} == '[object Object]'); // false
>> // O objeto {} não é convertido para a string '[object Object]', então a comparação resulta em false.
>> ```
>> #### `StrictlyEqual` (algoritmo de igualdade estrita)
>> Este algoritmo é usado pelo operador `===` e é mais simples, pois não realiza conversões de tipo. Ele apenas verifica se os dois valores são do mesmo tipo e valor.
>> #### Exemplo:
>> ```javascript
>> console.log('42' === 42); // false
>> // A string '42' e o número 42 são de tipos diferentes, então a comparação resulta em false.
>> 
>> console.log(true === 1); // false
>> // O booleano true e o número 1 são de tipos diferentes, então a comparação resulta em false.
>> 
>> console.log([1, 2] === '1,2'); // false
>> // O array [1, 2] e a string '1,2' são de tipos diferentes, então a comparação resulta em false.
>> 
>> console.log({} === {}); // false
>> // Cada objeto {} é uma instância diferente na memória, então a comparação resulta em false.
>> 
>> console.log(NaN === NaN); // false
>> // NaN nunca é igual a si mesmo, então a comparação resulta em false.
>> 
>> console.log(+0 === -0); // true
>> // 0 positivo e negativo são considerados iguais, então a comparação resulta em true.
>> 
>> console.log(Symbol('foo') === Symbol('foo')); // false
>> // Cada chamada a Symbol() cria um símbolo único, então a comparação resulta em false.
>> ```
>> #### `SameValueZero` (Mesmo valor que zero)
>> O algoritmo `SameValueZero` considera `NaN` igual a `NaN` e não diferencia entre `+0` e `-0`. É usado em algumas operações de array e objetos.
>> ```javascript
>> console.log(Object.is(NaN, NaN)); // true
>> // `Object.is()` usa o algoritmo `SameValueZero`, então NaN é igual a NaN.
>> 
>> console.log([+0].includes(-0)); // true
>> // O método `Array.prototype.includes` usa `SameValueZero`, então +0 é igual a -0.
>> ```
>> #### `SameValue` (Mesmo valor)
>> O algoritmo `SameValue` é similar ao `StrictEqual`, mas considera `NaN` igual a `NaN` e diferencia `+0` e `-0`.
>> ```javascript
>> console.log(Object.is(+0, -0)); // false
>> // `Object.is()` usa o algoritmo `SameValue`, diferenciando +0 e -0.
>> 
>> console.log(Object.is(NaN, NaN)); // true
>> // `SameValue` considera NaN igual a NaN.
>> ```
>> ### # Conclusão:
>> Entender os diferentes operadores de comparação e algoritmos de igualdade em JavaScript é essencial para escrever código correto e previsível. Saber quando usar `==`, `===` ou `Object.is()`, e como os algoritmos `LooselyEqual`, `StrictlyEqual`, `SameValueZero` e `SameValue` funcionam, ajuda a evitar bugs e comportamentos inesperados no código.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [w3schools - Comparações](https://www.w3schools.com/js/js_comparisons.asp) e [MDN - Comparação de Igualdade](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)
<br>
<hr>
<h3 align="center"> Não esqueça de sempre praticar; você não aprende a jogar bola apenas olhando... essa frase não é sobre jogar bola.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/loopsEiteracoes.svg)
>> ## loops e Iterações
>> ### # Loop "for"
>> O loop `for` é uma estrutura de repetição que permite executar um bloco de código um número específico de vezes. Ele é útil quando você sabe com antecedência quantas vezes deseja repetir uma operação.
>> #### Sintaxe:
>> ```javascript
>> for (inicialização; condição; incremento) {
>>   // Código a ser executado
>> }
>> ```
>> 
>> - **Inicialização:** Definição e inicialização de uma variável de controle (geralmente um contador).
>> - **Condição:** A condição que será verificada antes de cada iteração do loop. Se a condição for verdadeira, o bloco de código dentro do loop será executado.
>> - **Incremento:** Atualização da variável de controle após cada iteração.
>> #### Exemplo:
>> ```javascript
>> for (let i = 0; i < 5; i++) {
>>   console.log("O número é " + i);
>> }
>> ```
>> - `let i = 0;` - Inicializa a variável `i` com 0.
>> - `i < 5;` - O loop continua enquanto `i` for menor que 5.
>> - `i++;` - Incrementa `i` em 1 após cada iteração.
>> - Imprime os números de 0 a 4 no console.
>> 
>> ### # Declaração "for...of"
>> A declaração `for...of` é usada para iterar sobre objetos iteráveis (como arrays, strings, Map, Set, etc.), permitindo acessar diretamente os valores dos elementos.
>> #### Sintaxe:
>> ```javascript
>> for (const valor of iterável) {
>>   // Código a ser executado
>> }
>> ```
>> - `const valor` - Declara uma variável que armazena o valor do elemento atual.
>> - `iterável` - O objeto iterável (como um array) sobre o qual você está iterando.
>> #### Exemplo:
>> ```javascript
>> const array = ['a', 'b', 'c', 'd'];
>> for (const elemento of array) {
>>   console.log(elemento);
>> }
>> ```
>> - Itera sobre cada elemento do array `array`.
>> - Imprime `a`, `b`, `c` e `d` no console.
>> 
>> ### # Declaração "for...in"
>> A declaração `for...in` é usada para iterar sobre as propriedades enumeráveis de um objeto, permitindo acessar as chaves dessas propriedades.
>> #### Sintaxe:
>> ```javascript
>> for (const propriedade in objeto) {
>>   // Código a ser executado
>> }
>> ```
>> - `const propriedade` - Declara uma variável que armazena a chave da propriedade atual.
>> - `objeto` - O objeto cujas propriedades você está iterando.
>> #### Exemplo:
>> ```javascript
>> const objeto = {a: 1, b: 2, c: 3};
>> for (const chave in objeto) {
>>   console.log(`A chave é ${chave} e o valor é ${objeto[chave]}`);
>> }
>> ```
>> - Itera sobre cada chave do objeto `objeto`.
>> - Imprime `A chave é a e o valor é 1`, `A chave é b e o valor é 2`, e `A chave é c e o valor é 3` no console.
>
> <br>
>
>> ### # Loop "while"
>> O loop `while` executa um bloco de código enquanto uma condição especificada for verdadeira. É usado quando não se sabe antecipadamente quantas vezes o loop deve ser executado.
>> #### Sintaxe:
>> ```javascript
>> while (condição) {
>>   // Código a ser executado
>> }
>> ```
>> - `condição` - A condição que será verificada antes de cada iteração do loop. Se a condição for verdadeira, o bloco de código será executado.
>> #### Exemplo:
>> ```javascript
>> let contador = 0;
>> while (contador < 5) {
>>   console.log("O contador é " + contador);
>>   contador++;
>> }
>> ```
>> - Executa o loop enquanto `contador` for menor que 5.
>> - Incrementa `contador` em 1 após cada iteração.
>> - Imprime os números de 0 a 4 no console.
>> 
>> ### # Declaração "do...while"
>> O loop `do...while` é semelhante ao `while`, mas garante que o bloco de código seja executado pelo menos uma vez, pois a condição é verificada após a execução do bloco de código.
>> #### Sintaxe:
>> ```javascript
>> do {
>>   // Código a ser executado
>> } while (condição);
>> ```
>> - O bloco de código dentro do `do` será executado primeiro, independentemente da condição.
>> - A condição é verificada após a execução do bloco de código.
>> #### Exemplo:
>> ```javascript
>> let contador = 0;
>> do {
>>   console.log("O contador é " + contador);
>>   contador++;
>> } while (contador < 5);
>> ```
>> - Executa o bloco de código e depois verifica a condição.
>> - Isso garante que o código seja executado pelo menos uma vez, mesmo que a condição inicial não seja verdadeira.
>> - Imprime os números de 0 a 4 no console.
>
> <br>
>
>> ### # Break e Continue
>> As declarações `break` e `continue` são usadas para controlar o fluxo dos loops.
>> - **`break`:** Sai imediatamente do loop, interrompendo sua execução.
>> - **`continue`:** Pula a iteração atual e vai para a próxima iteração do loop.
>> #### Exemplo com `break`:
>> ```javascript
>> for (let i = 0; i < 10; i++) {
>>   if (i === 5) {
>>     break;
>>   }
>>   console.log(i);
>> }
>> ```
>> - O loop será interrompido quando `i` for igual a 5.
>> - O console mostrará `0, 1, 2, 3, 4`.
>> #### Exemplo com `continue`:
>> ```javascript
>> for (let i = 0; i < 10; i++) {
>>   if (i === 5) {
>>     continue;
>>   }
>>   console.log(i);
>> }
>> ```
>> - O loop pula a iteração quando `i` é igual a 5.
>> - O console mostrará `0, 1, 2, 3, 4, 6, 7, 8, 9`.
>> 
>> ### # Declarações Rotuladas
>> As declarações rotuladas são usadas para identificar um loop com um rótulo, permitindo que `break` e `continue` saiam de um loop específico, especialmente útil em loops aninhados.
>> #### Sintaxe:
>> ```javascript
>> rotulo: {
>>   // Código a ser executado
>> }
>> ```
>> #### Exemplo:
>> ```javascript
>> externo: for (let i = 0; i < 3; i++) {
>>   for (let j = 0; j < 3; j++) {
>>     if (i === 1 && j === 1) {
>>       break externo;
>>     }
>>     console.log(`i = ${i}, j = ${j}`);
>>   }
>> }
>> ```
>> - O loop externo será interrompido quando `i` for igual a 1 e `j` for igual a 1.
>> - O console mostrará `i = 0, j = 0`, `i = 0, j = 1`, `i = 0, j = 2`, `i = 1, j = 0`.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - loops e iterações](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)
<br>
<hr>
<h3 align="center"> Não esqueça de sempre praticar; Aprender nunca é demais, cada passo conta!</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/controleDeFluxo.svg)
>> ## Controle de Fluxo em JavaScript
>> O controle de fluxo determina a ordem na qual as instruções do seu código são executadas. Ele permite que você execute diferentes blocos de código dependendo das condições que você define. Vamos explorar os principais conceitos: condicionais e manipulação de exceções.
>> ### Condicionais
>> Os condicionais são estruturas que permitem executar diferentes blocos de código com base em uma condição. Os principais tipos de condicionais são `if`, `if...else`, `else if...else`, e `switch`.
>> ### # Sobre: `if`
>> A estrutura básica do `if` permite executar um bloco de código se uma condição for verdadeira.
>> ```javascript
>> let idade = 18; // Declarando uma variável idade com o valor 18
>> 
>> // Verificando se a idade é maior ou igual a 18
>> if (idade >= 18) {
>>     console.log("Você é maior de idade."); // Será exibido no console se a condição for verdadeira
>> }
>> // Saída: Você é maior de idade.
>> ```
>> Se `idade` é maior ou igual a 18, a mensagem "Você é maior de idade." é exibida no console.
>> ### # Sobre: `if...else`
>> O `if...else` permite executar um bloco de código se a condição for verdadeira e outro bloco se a condição for falsa.
>> ```javascript
>> let idade = 16; // Declarando uma variável idade com o valor 16
>> 
>> // Verificando se a idade é maior ou igual a 18
>> if (idade >= 18) {
>>     console.log("Você é maior de idade."); // Será exibido no console se a condição for verdadeira
>> } else {
>>     console.log("Você é menor de idade."); // Será exibido no console se a condição for falsa
>> }
>> // Saída: Você é menor de idade.
>> ```
>> Se `idade` for menor que 18, o bloco dentro do `else` será executado.
>> ### # Sobre: `else if...else`
>> O `else if...else` é útil quando você tem múltiplas condições a serem verificadas.
>> ```javascript
>> let nota = 85; // Declarando uma variável nota com o valor 85
>> 
>> // Verificando a faixa de valores da nota
>> if (nota >= 90) {
>>     console.log("Nota A"); // Será exibido se nota for maior ou igual a 90
>> } else if (nota >= 80) {
>>     console.log("Nota B"); // Será exibido se nota for maior ou igual a 80 e menor que 90
>> } else if (nota >= 70) {
>>     console.log("Nota C"); // Será exibido se nota for maior ou igual a 70 e menor que 80
>> } else {
>>     console.log("Nota abaixo de C"); // Será exibido se nota for menor que 70
>> }
>> // Saída: Nota B
>> ```
>> A primeira condição que for verdadeira determina qual bloco de código será executado. Neste caso, `nota` é 85, então "Nota B" é exibida.
>> ### # Sobre: `switch`
>> O `switch` é uma alternativa ao `if...else` quando você tem várias condições baseadas em uma única variável.
>> ```javascript
>> let dia = 3; // Declarando uma variável dia com o valor 3
>> 
>> // Verificando o valor da variável dia
>> switch (dia) {
>>     case 1:
>>         console.log("Domingo"); // Será exibido se dia for igual a 1
>>         break;
>>     case 2:
>>         console.log("Segunda-feira"); // Será exibido se dia for igual a 2
>>         break;
>>     case 3:
>>         console.log("Terça-feira"); // Será exibido se dia for igual a 3
>>         break;
>>     default:
>>         console.log("Dia inválido"); // Será exibido se dia não for igual a nenhum dos casos acima
>> }
>> // Saída: Terça-feira
>> ```
>> O `switch` compara o valor da variável `dia` com cada `case`. Quando encontra uma correspondência (3), o código dentro desse `case` é executado até encontrar um `break`.
>
> <br>
>
>> ### Manipulação de Exceções
>> A manipulação de exceções permite lidar com erros que ocorrem durante a execução do código. Os principais componentes são `throw`, `try`, `catch`, `finally`, e objetos de erro.
>> ### # Declaração `throw`
>> O `throw` é usado para lançar uma exceção quando você deseja sinalizar que algo deu errado.
>> ```javascript
>> // Função para verificar a idade
>> function verificarIdade(idade) {
>>     if (idade < 0) {
>>         throw new Error("Idade não pode ser negativa"); // Lançando um erro se a idade for negativa
>>     }
>>     console.log("Idade válida"); // Será exibido se a idade for válida
>> }
>> 
>> try {
>>     verificarIdade(-5); // Chamando a função com uma idade negativa
>> } catch (error) {
>>     console.log(error.message); // Capturando e exibindo a mensagem de erro
>> }
>> // Saída: Idade não pode ser negativa
>> ```
>> Se a `idade` for negativa, um erro é lançado com a mensagem "Idade não pode ser negativa". O bloco `try...catch` captura esse erro.
>> ### # Sobre: `try...catch`
>> O `try...catch` é usado para capturar e tratar erros que ocorrem dentro do bloco `try`.
>> ```javascript
>> try {
>>     let resultado = 10 / 0; // Tentativa de divisão por zero, mas não gera erro em JavaScript, apenas Infinity
>>     console.log(resultado); // Exibirá Infinity
>> } catch (error) {
>>     console.log("Ocorreu um erro: " + error.message); // Não será executado neste caso
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída: 
>> // Infinity
>> // Bloco finally executado.
>> ```
>> O código dentro do `try` é executado. Se um erro ocorrer, o bloco `catch` captura o erro e você pode tratá-lo conforme necessário. O `finally` é sempre executado, independentemente de um erro ocorrer ou não.
>> ### # Bloco `finally`
>> O bloco `finally` é opcional e é sempre executado após o bloco `try`, independentemente de um erro ter ocorrido ou não.
>> ```javascript
>> try {
>>     console.log("Tentando executar o código..."); // Exibindo uma mensagem
>>     throw new Error("Erro intencional"); // Lançando um erro intencionalmente
>> } catch (error) {
>>     console.log("Erro capturado: " + error.message); // Capturando e exibindo a mensagem de erro
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída:
>> // Tentando executar o código...
>> // Erro capturado: Erro intencional
>> // Bloco finally executado.
>> ```
>> O `finally` é útil para garantir que certas operações, como fechar arquivos ou liberar recursos, sejam sempre realizadas, independentemente de o código ter executado com sucesso ou ter lançado um erro.
>
> <br>
> 
>> ### Objetos de Erro (Error Objects)
>> Os objetos de erro são usados para criar instâncias de erros em JavaScript. Eles fornecem informações detalhadas sobre o erro ocorrido.
>> ### # Erro Padrão (Error)
>> ```javascript
>> try {
>>     throw new Error("Erro genérico"); // Lançando um erro genérico
>> } catch (error) {
>>     console.log("Nome do erro: " + error.name); // Exibindo o nome do erro
>>     console.log("Mensagem do erro: " + error.message); // Exibindo a mensagem do erro
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída:
>> // Nome do erro: Error
>> // Mensagem do erro: Erro genérico
>> // Bloco finally executado.
>> ```
>> `Error` é o tipo básico de erro em JavaScript. Ele é utilizado para criar erros genéricos. A mensagem do erro é "Erro genérico".
>> ### # Tipo de Erro (TypeError)
>> ```javascript
>> try {
>>     null.f(); // Tentativa de chamar um método em null, o que gera um TypeError
>> } catch (error) {
>>     console.log("Nome do erro: " + error.name); // Exibindo o nome do erro
>>     console.log("Mensagem do erro: " + error.message); // Exibindo a mensagem do erro
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída:
>> // Nome do erro: TypeError
>> // Mensagem do erro: Cannot read property 'f' of null
>> // Bloco finally executado.
>> ```
>> `TypeError` ocorre quando um valor é utilizado de uma maneira incompatível com seu tipo. Aqui, tenta-se acessar a propriedade `f` de `null`, que não é um objeto.
>> ### # Referência de Erro (ReferenceError)
>> ```javascript
>> try {
>>     console.log(x); // x não está definido, o que gera um ReferenceError
>> } catch (error) {
>>     console.log("Nome do erro: " + error.name); // Exibindo o nome do erro
>>     console.log("Mensagem do erro: " + error.message); // Exibindo a mensagem do erro
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída:
>> // Nome do erro: ReferenceError
>> // Mensagem do erro: x is not defined
>> // Bloco finally executado.
>> ```
>> `ReferenceError` ocorre quando se tenta acessar uma variável que não está definida. Aqui, `x` não foi declarado anteriormente.
>> ### # Faixa de Erro (RangeError)
>> ```javascript
>> try {
>>     let x = 1;
>>     x.toPrecision(500); // Tentativa de usar um valor fora do intervalo permitido, o que gera um RangeError
>> } catch (error) {
>>     console.log("Nome do erro: " + error.name); // Exibindo o nome do erro
>>     console.log("Mensagem do erro: " + error.message); // Exibindo a mensagem do erro
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída:
>> // Nome do erro: RangeError
>> // Mensagem do erro: toPrecision() argument must be between 1 and 100
>> // Bloco finally executado.
>> ```
>> `RangeError` ocorre quando um valor não está dentro do intervalo ou conjunto de valores permitidos. Aqui, o argumento para `toPrecision` está fora do intervalo aceitável (1 a 100).
>> ### # Sintaxe de Erro (SyntaxError)
>> ```javascript
>> try {
>>     eval('foo bar'); // Tentativa de executar uma sintaxe inválida, o que gera um SyntaxError
>> } catch (error) {
>>     console.log("Nome do erro: " + error.name); // Exibindo o nome do erro
>>     console.log("Mensagem do erro: " + error.message); // Exibindo a mensagem do erro
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída:
>> // Nome do erro: SyntaxError
>> // Mensagem do erro: Unexpected identifier
>> // Bloco finally executado.
>> ```
>> `SyntaxError` ocorre quando o código não é sintaticamente válido. Aqui, `eval` tenta executar um código que não é uma expressão JavaScript válida.
>> ### # URI de Erro (URIError)
>> ```javascript
>> try {
>>     decodeURIComponent('%'); // Tentativa de decodificar uma URI inválida, o que gera um URIError
>> } catch (error) {
>>     console.log("Nome do erro: " + error.name); // Exibindo o nome do erro
>>     console.log("Mensagem do erro: " + error.message); // Exibindo a mensagem do erro
>> } finally {
>>     console.log("Bloco finally executado."); // Será sempre executado
>> }
>> // Saída:
>> // Nome do erro: URIError
>> // Mensagem do erro: URI malformed
>> // Bloco finally executado.
>> ```
>> `URIError` ocorre quando as funções globais `encodeURI`, `decodeURI`, `encodeURIComponent`, ou `decodeURIComponent` recebem uma URI malformada. Aqui, `%` não é um componente válido.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - if...else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else), [MDN - switch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch), [MDN - try...catch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch), [MDN - Error Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error)
<br>
<hr>
<h3 align="center"> Não se esqueça de sempre praticar; você não aprende a tocar um instrumento apenas assistindo.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/expressoesOperadores.svg)
>> ## Expressões e Operadores
>> Em JavaScript, expressões são combinações de valores, variáveis e operadores que são avaliadas para produzir um resultado. Uma expressão pode ser tão simples quanto um número ou uma string, ou tão complexa quanto uma função invocada com argumentos e operadores aninhados.
>> 
>> Operadores são símbolos ou palavras-chave que indicam ao JavaScript para realizar operações específicas sobre os operandos. Eles permitem manipular dados e variáveis para realizar cálculos, comparar valores, executar operações lógicas, entre outras tarefas. Os operadores são fundamentais para construir expressões que compõem a lógica do código.
>> 
>> ### # Aqui estão algumas categorias principais de operadores:
>> **Operadores Aritméticos**: Realizam operações matemáticas básicas como adição, subtração, multiplicação, divisão e mais.\
>> **Operadores de Comparação**: Comparam valores e retornam um booleano (verdadeiro ou falso).\
>> **Operadores Lógicos**: Combinações de expressões booleanas.\
>> **Operadores Condicionais**: Avaliam uma condição e retornam um valor baseado na condição.\
>> **Operadores Unários**: Operam em um único operando para produzir um novo valor.\
>> **Operadores Bit a Bit**: Operam diretamente sobre os bits dos operandos.\
>> **Operadores de Atribuição**: Atribuem valores às variáveis e podem incluir operações aritméticas.
>> 
>> ### # Operadores Aritméticos
>> Os operadores aritméticos realizam operações matemáticas básicas, como adição, subtração, multiplicação, divisão e outras operações relacionadas. Eles são essenciais para manipular números e realizar cálculos dentro do código.
>> 
>> #### **Adição (`+`)**: Soma dois números.
>> ```javascript
>> let a = 5;
>> let b = 3;
>> console.log(a + b); // Saída: 8
>> // Aqui, `5 + 3` resulta em `8`.
>> ```
>> #### **Subtração (`-`)**: Subtrai o segundo número do primeiro.
>> ```javascript
>> console.log(a - b); // Saída: 2
>> // Aqui, `5 - 3` resulta em `2`.
>> ```
>> #### **Multiplicação (`*`)**: Multiplica dois números.
>> ```javascript
>> console.log(a * b); // Saída: 15
>> // Aqui, `5 * 3` resulta em `15`.
>> ```
>> #### **Divisão (`/`)**: Divide o primeiro número pelo segundo.
>> ```javascript
>> console.log(a / b); // Saída: 1.6667
>> // Aqui, `5 / 3` resulta em aproximadamente `1.6667`.
>> ```
>> #### **Módulo (`%`)**: Retorna o resto da divisão do primeiro número pelo segundo.
>> ```javascript
>> console.log(a % b); // Saída: 2
>> // Aqui, `5 % 3` resulta em `2` porque 5 dividido por 3 dá 1 com um resto de 2.
>> ```
>> #### **Exponenciação (`**`)**: Eleva o primeiro número à potência do segundo.
>> ```javascript
>> console.log(a ** b); // Saída: 125
>> // Aqui, `5 ** 3` (5 elevado a 3) resulta em `125`.
>> ```
>
> <br>
>
>> ### # **Operadores de Atribuição Aritmética**:
>> Os operadores de atribuição são usados para atribuir valores às variáveis. Eles podem incluir operações aritméticas junto com a atribuição, como adicionar e atualizar uma variável com um novo valor (+=, -=, *=).
>> 
>> #### **Atribuição de Adição (`+=`)**: Adiciona um valor à variável e a atualiza.
>> ```javascript
>> let x = 10;
>> x += 5; // Equivale a x = x + 5
>> console.log(x); // Saída: 15
>> // Aqui, `x` inicialmente vale `10`. `x += 5` faz `x` se tornar `15`.
>> ```
>> #### **Atribuição de Subtração (`-=`)**: Subtrai um valor da variável e a atualiza.
>> ```javascript
>> x -= 3; // Equivale a x = x - 3
>> console.log(x); // Saída: 12
>> // Aqui, `x` inicialmente vale `15`. `x -= 3` faz `x` se tornar `12`.
>> ```
>> #### **Atribuição de Multiplicação (`*=`)**: Multiplica a variável por um valor e a atualiza.
>> ```javascript
>> x *= 2; // Equivale a x = x * 2
>> console.log(x); // Saída: 24
>> // Aqui, `x` inicialmente vale `12`. `x *= 2` faz `x` se tornar `24`.
>> ```
>> #### **Atribuição de Divisão (`/=`)**: Divide a variável por um valor e a atualiza.
>> ```javascript
>> x /= 4; // Equivale a x = x / 4
>> console.log(x); // Saída: 6
>> // Aqui, `x` inicialmente vale `24`. `x /= 4` faz `x` se tornar `6`.
>> ```
>> #### **Atribuição de Módulo (`%=`)**: Calcula o módulo da variável por um valor e a atualiza.
>> ```javascript
>> x %= 4; // Equivale a x = x % 4
>> console.log(x); // Saída: 2
>> // Aqui, `x` inicialmente vale `6`. `x %= 4` faz `x` se tornar `2`.
>> ```
>> #### **Atribuição de Exponenciação (`**=`)**: Eleva a variável à potência de um valor e a atualiza.
>> ```javascript
>> x **= 2; // Equivale a x = x ** 2
>> console.log(x); // Saída: 4
>> // Aqui, `x` inicialmente vale `2`. `x **= 2` faz `x` se tornar `4`.
>> ```
>
> <br>
>
>> ### # Operadores de Comparação
>> Os operadores de comparação comparam dois valores e retornam um resultado booleano, true ou false, dependendo se a comparação é verdadeira ou falsa. Esses operadores são úteis para tomar decisões com base na comparação de valores.
>> 
>> #### **Maior que (`>`)**: Verifica se o valor à esquerda é maior que o valor à direita.
>> ```javascript
>> console.log(10 > 5); // Saída: true
>> // Aqui, `10 > 5` é verdadeiro, então a saída é `true`.
>> ```
>> #### **Menor que (`<`)**: Verifica se o valor à esquerda é menor que o valor à direita.
>> ```javascript
>> console.log(10 < 5); // Saída: false
>> // Aqui, `10 < 5` é falso, então a saída é `false`.
>> ```
>> #### **Maior ou igual a (`>=`)**: Verifica se o valor à esquerda é maior ou igual ao valor à direita.
>> ```javascript
>> console.log(10 >= 5); // Saída: true
>> // Aqui, `10 >= 5` é verdadeiro, então a saída é `true`.
>> ```
>> #### **Menor ou igual a (`<=`)**: Verifica se o valor à esquerda é menor ou igual ao valor à direita.
>> ```javascript
>> console.log(10 <= 5); // Saída: false
>> // Aqui, `10 <= 5` é falso, então a saída é `false`.
>> ```
>> #### **Igual a (`==`)**: Verifica se os valores são iguais, sem considerar o tipo.
>> ```javascript
>> console.log(5 == "5"); // Saída: true
>> // Aqui, `5 == "5"` é verdadeiro porque o operador `==` não verifica o tipo.
>> ```
>> #### **Estritamente igual a (`===`)**: Verifica se os valores e tipos são iguais.
>> ```javascript
>> console.log(5 === "5"); // Saída: false
>> // Aqui, `5 === "5"` é falso porque o tipo `number` não é igual ao tipo `string`.
>> ```
>> #### **Diferente de (`!=`)**: Verifica se os valores não são iguais, sem considerar o tipo.
>> ```javascript
>> console.log(5 != "5"); // Saída: false
>> // Aqui, `5 != "5"` é falso porque o operador `!=` não verifica o tipo.
>> ```
>> #### **Estritamente diferente de (`!==`)**: Verifica se os valores e tipos não são iguais.
>> ```javascript
>> console.log(5 !== "5"); // Saída: true
>> // Aqui, `5 !== "5"` é verdadeiro porque o tipo `number` não é igual ao tipo `string`.
>> ```
>
> <br>
>
>> ### # Operadores Lógicos
>> Os operadores lógicos permitem combinar várias expressões booleanas em uma única expressão complexa. Eles retornam um resultado booleano e são usados para testar múltiplas condições ao mesmo tempo.
>> 
>> #### **OR lógico (`||`)**: Retorna `true` se pelo menos uma das expressões for verdadeira.
>> ```javascript
>> console.log(true || false); // Saída: true
>> // Aqui, `true || false` é verdadeiro porque pelo menos uma das expressões é verdadeira.
>> ```
>> #### **AND lógico (`&&`)**: Retorna `true` somente se ambas as expressões forem verdadeiras.
>> ```javascript
>> console.log(true && false); // Saída: false
>> // Aqui, `true && false` é falso porque uma das expressões é falsa.
>> ```
>> #### **NOT lógico (`!`)**: Inverte o valor booleano da expressão.
>> ```javascript
>> console.log(!true); // Saída: false
>> // Aqui, `!true` inverte `true` para `false`.
>> ```
>> #### **Coalescência nula (`??`)**: Retorna o valor do lado esquerdo se ele não for `null` ou `undefined`; caso contrário, retorna o valor do lado direito.
>> ```javascript
>> let nome = null;
>> let saudacao = nome ?? "Visitante";
>> console.log(saudacao); // Saída: "Visitante"
>> // Aqui, `nome` é `null`, então `nome ?? "Visitante"` retorna `"Visitante"`.
>> ```
>
> <br>
>
>> ### Operadores Unários
>> Os operadores unários operam em um único operando para produzir um novo valor. Exemplos incluem incrementar (++) ou decrementar (--) um valor, e operadores lógicos como a negação (!).
>> 
>> #### **Incremento (`++`)**: Aumenta o valor da variável em 1.
>> ```javascript
>> let numero = 5;
>> numero++;
>> console.log(numero); // Saída: 6
>> // Aqui, `numero` inicialmente vale `5`. `numero++` faz `numero` se tornar `6`.
>> ```
>> #### **Decremento (`--`)**: Diminui o valor da variável em 1.
>> ```javascript
>> numero--;
>> console.log(numero); // Saída: 5
>> // Aqui, `numero` inicialmente vale `6`. `numero--` faz `numero` se tornar `5`.
>> ```
>
> <br>
> 
>> ### # Operadores Bit a Bit
>> Os operadores bit a bit operam diretamente sobre os bits dos operandos. Eles realizam operações a nível de bit, como AND, OR, XOR, e deslocamentos de bits, permitindo manipulações detalhadas dos dados binários.
>> 
>> #### **AND bit a bit (`&`)**: Realiza a operação AND em cada bit dos operandos.
>> ```javascript
>> console.log(5 & 3); // Saída: 1 (0101 & 0011 = 0001)
>> // Aqui, `5 & 3` compara os bits `0101` e `0011`, resultando em `0001`, que é `1` em decimal.
>> ```
>> #### **OR bit a bit (`|`)**: Realiza a operação OR em cada bit dos operandos.
>> ```javascript
>> console.log(5 | 3); // Saída: 7 (0101 | 0011 = 0111)
>> // Aqui, `5 | 3` compara os bits `0101` e `0011`, resultando em `0111`, que é `7` em decimal.
>> ```
>> #### **XOR bit a bit (`^`)**: Realiza a operação XOR em cada bit dos operandos.
>> ```javascript
>> console.log(5 ^ 3); // Saída: 6 (0101 ^ 0011 = 0110)
>> // Aqui, `5 ^ 3` compara os bits `0101` e `0011`, resultando em `0110`, que é `6` em decimal.
>> ```
>> #### **NOT bit a bit (`~`)**: Inverte todos os bits do operando.
>> ```javascript
>> console.log(~5); // Saída: -6 (inverte 0101 para 1010)
>> // Aqui, `~5` inverte os bits `0101` para `1010`, que é `-6` em decimal devido à representação de complemento de dois.
>> ```
>> #### **Deslocamento para a esquerda (`<<`)**: Desloca os bits do operando para a esquerda.
>> ```javascript
>> console.log(5 << 1); // Saída: 10 (0101 << 1 = 1010)
>> // Aqui, `5 << 1` desloca os bits `0101` para a esquerda por um bit, resultando em `1010`, que é `10` em decimal.
>> ```
>> #### **Deslocamento para a direita (`>>`)**: Desloca os bits do operando para a direita, mantendo o sinal.
>> ```javascript
>> console.log(5 >> 1); // Saída: 2 (0101 >> 1 = 0010)
>> // Aqui, `5 >> 1` desloca os bits `0101` para a direita por um bit, resultando em `0010`, que é `2` em decimal.
>> ```
>> #### **Deslocamento para a direita sem sinal (`>>>`)**: Desloca os bits do operando para a direita, preenchendo com zeros.
>> ```javascript
>> console.log(5 >>> 1); // Saída: 2 (0101 >>> 1 = 0010)
>> // Aqui, `5 >>> 1` desloca os bits `0101` para a direita por um bit, resultando em `0010`, que é `2` em decimal. A diferença para `>>` é que `>>>` não preserva o sinal.
>> ```
>
> <br>
>
>> ### # Operadores na String
>> Os operadores na string são usados principalmente para concatenar strings, unindo duas ou mais strings em uma única string. Isso é útil para construir mensagens dinâmicas, combinar variáveis de texto e manipular dados textuais.
>> 
>> #### **Concatenação (`+`)**: Junta duas ou mais strings.
>> ```javascript
>> let nome = "Henrique";
>> let saudacao = "Olá, " + nome + "!";
>> console.log(saudacao); // Saída: "Olá, Henrique!"
>> // Aqui, `"Olá, " + nome + "!"` concatena as strings `"Olá, "`, `nome` e `"!"`, resultando em `"Olá, Henrique!"`.
>> ```
>
> <br>
>
>> ### # Operadores Condicionais
>> Os operadores condicionais são usados para avaliar uma condição e retornar um valor baseado nessa condição. O operador condicional ternário é um exemplo comum.
>> 
>> #### Sintaxe:
>> ```javascript
>> condição ? valorCasoVerdadeiro : valorCasoFalso
>> ```
>> #### Exemplo:
>> ```javascript
>> let idade = 18;
>> let podeDirigir = idade >= 18 ? "Sim, pode dirigir." : "Não, não pode dirigir.";
>> console.log(podeDirigir); // Saída: Sim, pode dirigir.
>> ```
>> Neste exemplo, o operador condicional ? é usado para verificar se a idade é maior ou igual a 18. Se a condição for verdadeira (idade >= 18), o valor "Sim, pode dirigir." é retornado. Caso contrário, "Não, não pode dirigir." é retornado. O resultado é então exibido no console.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [W3S - Operators](https://www.w3schools.com/js/js_operators.asp), [W3S - Arithmetic](https://www.w3schools.com/js/js_arithmetic.asp), [W3S - Comparison and Logical Operators](https://www.w3schools.com/js/js_comparisons.asp), [W3S - Strings](https://www.w3schools.com/js/js_strings.asp)

<br>
<hr>
<h3 align="center"> Não se esqueça de sempre praticar; você não aprende a tocar um instrumento apenas assistindo.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/functions.svg)
>> ## 0. Functions (Funções)
>> As funções em JavaScript são blocos de código que realizam uma tarefa específica. Elas podem receber dados de entrada (parâmetros) e retornar um resultado. Funções ajudam a modularizar o código, tornando-o mais organizado e reutilizável.
>> ```javascript
>> // Definição de uma função chamada 'dizerOla' que recebe um parâmetro 'nome'
>> function dizerOla(nome) {
>>   // A função imprime uma mensagem de saudação no console
>>   console.log("Olá, " + nome);
>> }
>> 
>> // Chamada da função 'dizerOla' passando o argumento 'Henrique'
>> dizerOla("Henrique"); // Saída: Olá, Henrique
>> ```
>> ### # Parâmetros de função
>> Os parâmetros de função são variáveis listadas como parte da definição da função. Eles permitem que você passe informações para a função.
>> 
>> #### Parâmetros Padrão
>> Os parâmetros padrão permitem inicializar parâmetros com valores padrão se nenhum valor ou `undefined` for passado. Isso é útil para evitar erros quando a função é chamada sem todos os argumentos necessários.
>> ```javascript
>> // Definição da função 'dizerOla' com um parâmetro padrão 'nome' com valor "Sem Nome"
>> function dizerOla(nome = "Sem Nome") {
>>   // A função imprime uma mensagem de saudação no console
>>   console.log("Olá, " + name);
>> }
>> 
>> // Chamada da função 'dizerOla' sem passar argumentos
>> dizerOla(); // Saída: Olá, Sem Nome
>> 
>> // Chamada da função 'dizerOla' passando o argumento 'Henrique'
>> dizerOla("Henrique"); // Saída: Olá, Henrique
>> ```
>> #### Parâmetros Rest
>> Os parâmetros rest permitem representar um número indefinido de argumentos como um array. Isso é útil quando você não sabe de antemão quantos argumentos serão passados para a função.
>> ```javascript
>> // Definição da função 'somar' que usa parâmetros rest 'numbers'
>> function somar(...numbers) {
>>   // A função usa o método 'reduce' para somar todos os números passados
>>   return numbers.reduce((total, numero) => total + numero, 0);
>> }
>> 
>> // Chamada da função 'somar' passando múltiplos argumentos
>> console.log(somar(1, 2, 3)); // Saída: 6
>> console.log(somar(4, 5, 6, 7)); // Saída: 22
>> ```
>
> <br>
>
>> ### # Arrow Functions
>> Arrow functions são uma sintaxe curta para declarar funções. Elas são mais concisas e têm algumas diferenças de comportamento em comparação com funções tradicionais, especialmente no que diz respeito ao `this`.
>> ```javascript
>> // Definição de uma arrow function 'add' que recebe dois parâmetros 'a' e 'b'
>> const add = (a, b) => {
>>   // A função retorna a soma de 'a' e 'b'
>>   return a + b;
>> };
>> 
>> // Chamada da função 'add' passando dois argumentos
>> console.log(add(2, 3)); // Saída: 5
>> 
>> // Outra forma de definir uma arrow function que retorna implicitamente o resultado
>> const mult = (a, b) => a * b;
>> console.log(mult(4, 5)); // Saída: 20
>> ```
>
> <br>
>
>> ### # IIFEs (Immediately Invoked Function Expressions)
>> Uma IIFE é uma função que é executada imediatamente após sua definição. Isso é útil para criar um escopo local e evitar poluição do escopo global.
>> ```javascript
>> // Definição e invocação imediata de uma IIFE
>> (function() {
>>   // O código dentro da IIFE é executado imediatamente
>>   console.log("Isso é um IIFE");
>> })(); // Saída: Isso é um IIFE
>> 
>> // Outra forma de definir uma IIFE
>> (() => {
>>   console.log("Outro IIFE");
>> })(); // Saída: Outro IIFE
>> ```
>
> <br>
>
>> ### # Arguments object
>> O objeto `arguments` é uma variável local disponível dentro de todas as funções. Ele contém uma entrada para cada argumento passado para a função, permitindo acesso a todos os argumentos, mesmo que a função não os declare explicitamente.
>> ```javascript
>> // Definição da função 'multiplicar' que usa o objeto 'arguments'
>> function multiplicar() {
>>   // Inicializa a variável 'produto' com o valor 1
>>   let produto = 1;
>>   
>>   // Itera sobre os argumentos passados usando 'arguments.length'
>>   for (let i = 0; i < arguments.length; i++) {
>>     // Multiplica 'product' pelo argumento atual
>>     produto *= arguments[i];
>>   }
>>   
>>   // Retorna o resultado final
>>   return produto;
>> }
>> 
>> // Chamada da função 'multiplicar' passando múltiplos argumentos
>> console.log(multiplicar(2, 3, 4)); // Saída: 24
>> console.log(multiplicar(1, 2, 3, 4, 5)); // Saída: 120
>> ```
>
> <br>
>
>> ### # Escopo e function stack
>> O escopo refere-se ao contexto atual de execução, no qual valores e expressões são "visíveis" ou podem ser referenciados. A function stack (pilha de funções) é a pilha de execução de chamadas de funções.
>> 
>> #### Recursão
>> Recursão ocorre quando uma função chama a si mesma. É útil para resolver problemas que podem ser divididos em subproblemas menores do mesmo tipo.
>> ```javascript
>> // Definição da função 'factorial' que calcula o fatorial de um número 'n'
>> function factorial(n) {
>>   // Caso base: se 'n' for 0, retorna 1
>>   if (n === 0) return 1;
>>   
>>   // Chamada recursiva: multiplica 'n' pelo fatorial de 'n - 1'
>>   return n * factorial(n - 1);
>> }
>> 
>> // Chamada da função 'factorial' passando o argumento 5
>> console.log(factorial(5)); // Saída: 120 (5*4*3*2*1)
>> console.log(factorial(0)); // Saída: 1 (caso base)
>> ```
>> #### Lexical scoping
>> Lexical scoping significa que o escopo de uma variável é determinado pelo local onde ela é definida no código escrito. Funções aninhadas têm acesso às variáveis do escopo externo.
>> ```javascript
>> // Definição da função 'dizer'
>> function dizer() {
>>   // Declara a variável 'frase' no escopo da função 'dizer'
>>   let frase = "Ola, meu nome é Henrique";
>>   
>>   // Definição da função 'exibir' aninhada dentro de 'dizer'
>>   function exibir() {
>>     // A função 'exibir' tem acesso à variável 'frase' devido ao escopo léxico
>>     console.log(frase);
>>   }
>>   
>>   // Chamada da função 'exibit'
>>   exibir();
>> }
>> 
>> // Chamada da função 'dizer'
>> dizer(); // Saída: Olá, meu nome é Henrique
>> ```
>> #### Closures
>> Um closure é a combinação de uma função e o ambiente léxico no qual ela foi criada. Isso permite que a função acesse >> variáveis de seu escopo externo mesmo após o escopo externo ter sido executado.
>> ```javascript
>> // Definição da função 'makeCounter' que retorna uma função
>> function makeCounter() {
>>   // Declara a variável 'count' no escopo de 'makeCounter'
>>   let count = 0;
>>   
>>   // Retorna uma função anônima que incrementa e retorna 'count'
>>   return function() {
>>     count++;
>>     return count;
>>   };
>> }
>> 
>> // Chama a função 'makeCounter' e armazena o resultado na variável 'counter'
>> const counter = makeCounter();
>> 
>> // Chama a função 'counter' várias vezes
>> console.log(counter()); // Saída: 1
>> console.log(counter()); // Saída: 2
>> console.log(counter()); // Saída: 3
>> ```
>
> <br>
>
>> ### # Funções incorporadas
>> JavaScript possui várias funções incorporadas que fornecem funcionalidades comuns. Vamos ver alguns exemplos importantes.
>> #### Exemplo: `parseInt` e `parseFloat`
>> Essas funções analisam uma string e retornam um número inteiro ou de ponto flutuante, respectivamente.
>> ```javascript
>> // Usa 'parseInt' para converter uma string em um número inteiro
>> console.log(parseInt("10")); // Saída: 10
>> 
>> // Usa 'parseFloat' para converter uma string em um número de ponto flutuante
>> console.log(parseFloat("10.5")); // Saída: 10.5
>> 
>> // Exemplos com strings que contêm caracteres não numéricos
>> console.log(parseInt("10abc")); // Saída: 10
>> console.log(parseFloat("10.5abc")); // Saída: 10.5
>> ```
>> #### Exemplo: `setTimeout` e `setInterval`
>> `setTimeout` executa uma função após um período de tempo, e `setInterval` executa uma função repetidamente com um intervalo de tempo fixo entre as execuções.
>> ```javascript
>> // Usa 'setTimeout' para executar uma função após 1 segundo (1000 ms)
>> setTimeout(() => {
>>   console.log("Isso é executado após 1 segundo");
>> }, 1000); // Saída (após 1 segundo): Isso é executado após 1 segundo
>> 
>> // Usa 'setInterval' para executar uma função a cada 2 segundos (2000 ms)
>> const intervalId = setInterval(() => {
>>   console.log("Isso acontece a cada 2 segundos");
>> }, 2000); // Saída (a cada 2 segundos): Isso acontece a cada 2 segundos
>> 
>> // Para parar o intervalo após 7 segundos
>> setTimeout(() => {
>>   clearInterval(intervalId);
>>  
>> 
>>  console.log("Intervalo parado");
>> }, 7000); // Saída (após 7 segundos): Intervalo parado
>> ```
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
<br>
<hr>

>> ## Strict mode
>> O "modo estrito" (strict mode) em JavaScript é uma forma de optar por um comportamento mais restrito no seu código JavaScript, que visa a eliminar alguns erros silenciosos e "más práticas" de programação, além de fornecer mais segurança e melhorar a performance do código. Para ativar o modo estrito, basta adicionar a string `"use strict";` no início de um script ou de uma função.
>> ### # Ativação do Modo Estrito
>> Para ativar o modo estrito, insira `"use strict";` no início de um arquivo JavaScript ou dentro de uma função. 
>> #### Ativação Global
>> ```javascript
>> "use strict";
>> // Código JavaScript em modo estrito
>> ```
>> #### Ativação em Função
>> ```javascript
>> function exemplo() {
>>     "use strict";
>>     // Código JavaScript em modo estrito
>> }
>> ```
>> 
>> ### # Características e Restrições do Modo Estrito
>> 1. **Declaração de Variáveis**:\
>> No modo estrito, você deve declarar todas as variáveis usando `var`, `let` ou `const` antes de usá-las. Caso contrário, um erro será gerado.
>>    ```javascript
>>    "use strict";
>>    x = 3.14;  // ReferenceError: x is not defined
>>    ```
>> 2. **Escrita em Propriedades Não-Escrituráveis**:\
>> Propriedades que não podem ser modificadas (não-escrituráveis) não podem ser alteradas no modo estrito.
>>    ```javascript
>>    "use strict";
>>    const obj = {};
>>    Object.defineProperty(obj, 'x', { value: 42, writable: false });
>>    obj.x = 9;  // TypeError: Cannot assign to read-only property 'x'
>>    ```
>> 3. **Criação de Propriedades em Objetos Não-Extensíveis**:\
>> Novas propriedades não podem ser adicionadas a objetos que foram marcados como não-extensíveis.
>>    ```javascript
>>    "use strict";
>>    const obj = {};
>>    Object.preventExtensions(obj);
>>    obj.newProp = "value";  // TypeError: Cannot add property newProp, object is not extensible
>>    ```
>> 4. **Uso de `eval`**:\
>> No modo estrito, `eval` não cria ou modifica variáveis no escopo ao seu redor, isolando o código executado dentro de `eval`.
>>    ```javascript
>>    "use strict";
>>    eval("var x = 2;");
>>    console.log(x);  // ReferenceError: x is not defined
>>    ```
>> 5. **`this` em Funções**:\
>> Em funções no modo estrito, o valor de `this` será `undefined` se ele não for explicitamente configurado, enquanto que no modo não estrito `this` seria o objeto global (ou `window` no navegador).
>>    ```javascript
>>    "use strict";
>>    function func() {
>>        console.log(this);  // undefined
>>    }
>>    func();
>>    ```
>> 6. **Propriedades Duplicadas**:\
>> Objetos literais não podem ter propriedades com o mesmo nome.
>>    ```javascript
>>    "use strict";
>>    const obj = {
>>        prop: 1,
>>        prop: 2  // SyntaxError: Duplicate data property in object literal not allowed in strict mode
>>    };
>>    ```
>> 7. **Nomes de Parâmetros Duplicados**:\
>> Funções não podem ter parâmetros com nomes duplicados.
>>    ```javascript
>>    "use strict";
>>    function soma(a, a, b) {  // SyntaxError: Duplicate parameter name not allowed in this context
>>        return a + b;
>>    }
>>    ```
>> 8. **Literais Octais**:\
>> Literais octais (números base 8) são proibidos.
>>    ```javascript
>>    "use strict";
>>    const num = 010;  // SyntaxError: Octal literals are not allowed in strict mode
>>    ```
>> 9. **Proibição de `delete` em Variáveis**:\
>> O modo estrito não permite que variáveis, funções ou argumentos sejam excluídos.
>>    ```javascript
>>    "use strict";
>>    var x = 5;
>>    delete x;  // SyntaxError: Delete of an unqualified identifier in strict mode.
>>    ```
>> 10. **Palavras Reservadas para Futuro Uso**:\
>> Algumas palavras são reservadas para uso futuro e não podem ser usadas como nomes de variáveis no modo estrito.
>>     ```javascript
>>     "use strict";
>>     const implements = 5;  // SyntaxError: Unexpected strict mode reserved word
>>     ```
>> 
>> ### # Benefícios do Modo Estrito
>> 1. **Detecção de Erros**: O modo estrito ajuda a capturar erros comuns e evita armadilhas do JavaScript, tornando os erros mais visíveis e mais fáceis de corrigir.
>> 2. **Segurança**: Previne algumas práticas que podem levar a vulnerabilidades, como a criação acidental de variáveis globais.
>> 3. **Otimização**: Corrige erros que dificultam a otimização pelos motores JavaScript, ajudando a rodar o código de maneira mais eficiente.
>> #### Conclusão:
>> O modo estrito é uma maneira eficaz de melhorar a qualidade do seu código JavaScript, tornando-o mais seguro e menos propenso a erros. Adotar o modo estrito é uma prática recomendada, especialmente em projetos maiores ou ao trabalhar em equipe, para garantir que o código seja mais robusto e sustentável.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)

<br>
<hr>
<h3 align="center"> Não se esqueça de sempre praticar; você não aprende a tocar um instrumento apenas assistindo.</h3>
<hr>

> ![Diagrama Mermaid](/assets/image/thisEmJs.svg)
>> ## `this` no JavaScript
>> O `this` é uma palavra-chave importante no JavaScript que muitas vezes confunde os iniciantes. Ele se refere ao contexto de execução, ou seja, ao objeto que está atualmente executando o código. A maneira como o valor de `this` é determinado depende de como uma função é chamada. Vamos explorar detalhadamente os vários usos e comportamentos do `this`.
>> 
>> ### # `this` em Métodos de Objetos
>> Quando `this` é usado dentro de um método de um objeto, ele se refere ao próprio objeto que contém o método.
>> 
>> #### Exemplo:
>> Abaixo, `saudacao` é um método do objeto `pessoa`.\
>> Dentro do método `saudacao`, `this` se refere ao objeto `pessoa`.\
>> Portanto, `this.nome` acessa o valor `'Rick'` e `this.idade` acessa o valor `22`.
>> ```javascript
>> const pessoa = {
>>     nome: 'Rick',
>>     idade: 22,
>>     saudacao: function() {
>>         console.log(`Olá, meu nome é ${this.nome} e eu tenho ${this.idade} anos.`);
>>     }
>> };
>> pessoa.saudacao(); // Olá, meu nome é Rick e eu tenho 22 anos.
>> ```
>> #### Exemplo:
>> `detalhes` é um método do objeto `carro`.\
>> Dentro do método `detalhes`, `this` se refere ao objeto `carro`.\
>> Portanto, `this.marca` acessa o valor `'Toyota'` e `this.modelo` acessa o valor `'Corolla'`.
>> ```javascript
>> const carro = {
>>     marca: 'Toyota',
>>     modelo: 'Corolla',
>>     detalhes: function() {
>>         console.log(`Este carro é um ${this.marca} ${this.modelo}.`);
>>     }
>> };
>> 
>> carro.detalhes(); // Este carro é um Toyota Corolla.
>> ```
>> 
>> ### # `this` em Funções Normais
>> Quando `this` é usado em funções normais, seu valor depende de como a função é chamada. Se a função é chamada sem um contexto de objeto, `this` se refere ao objeto global (`window` no navegador, `global` no Node.js).
>> 
>> #### Exemplo:
>> `mostrarThis` é uma função normal.\
>> Como `mostrarThis` é chamada sem um objeto, `this` se refere ao objeto global.
>> ```javascript
>> function mostrarThis() {
>>     console.log(this);
>> }
>> 
>> mostrarThis(); // No navegador, isso será o objeto Window. No Node.js, será o objeto global.
>> ```
>> #### Exemplo:
>> `mostrarValor` é um método do objeto `obj`.\
>> Dentro de `mostrarValor`, `interna` é uma função normal.\
>> Quando `interna` é chamada, `this` se refere ao objeto global, onde `valor` não está definido, resultando em `undefined`.
>> ```javascript
>> const obj = {
>>     valor: 42,
>>     mostrarValor: function() {
>>         function interna() {
>>             console.log(this.valor);
>>         }
>>         interna();
>>     }
>> };
>> 
>> obj.mostrarValor(); // undefined
>> ```
>> 
>> ### # 'this' Sozinho
>> Quando `this` é usado sozinho fora de qualquer função, no contexto global, ele se refere ao objeto global.
>> 
>> #### Exemplo:
>> Fora de qualquer função, `this` se refere ao objeto global.
>> ```javascript
>> console.log(this); // No navegador, isso será o objeto Window. No Node.js, será o objeto global.
>> ```
>> #### Exemplo:
>> A função `globalThis` retorna `this`, que se refere ao objeto global quando a função é chamada no contexto global.
>> ```javascript
>> function globalThis() {
>>     return this;
>> }
>> 
>> console.log(globalThis() === window); // true no navegador
>> console.log(globalThis() === global); // true no Node.js
>> ```
>> 
>> ### # 'this' em Manipulação de Eventos
>> Em manipuladores de eventos, `this` se refere ao elemento HTML que recebeu o evento.
>> #### Exemplo:
>> O `this` dentro do manipulador de eventos se refere ao elemento `button` que foi clicado.
>> ```html
>> <button id="meuBotao">Clique aqui</button>
>> <script>
>> document.getElementById('meuBotao').addEventListener('click', function() {
>>     console.log(this); // <button id="meuBotao">Clique aqui</button>
>> });
>> </script>
>> ```
>> #### Exemplo:
>> O `this` dentro do manipulador de eventos se refere ao elemento `div` que foi clicado.\
>> A cor de fundo do `div` muda para amarelo quando clicado.
>> ```html
>> <div id="meuDiv">
>>     Clique aqui
>> </div>
>> <script>
>> document.getElementById('meuDiv').addEventListener('click', function() {
>>     this.style.backgroundColor = 'yellow';
>> });
>> </script>
>> ```
>> 
>> ### # 'this' em Arrow Functions
>> Arrow functions (funções de seta) não têm seu próprio `this`. Em vez disso, herdam o `this` do contexto onde foram definidas.
>> #### Exemplo:
>> `arrowFunc` é uma arrow function definida dentro do método `metodo`.\
>> `arrowFunc` herda o `this` do método `metodo`, que se refere ao objeto `objeto`.
>> ```javascript
>> const objeto = {
>>     valor: 10,
>>     metodo: function() {
>>         const arrowFunc = () => {
>>             console.log(this.valor);
>>         };
>>         arrowFunc(); // 10
>>     }
>> };
>> 
>> objeto.metodo();
>> ```
>> #### Exemplo:
>> A arrow function dentro do `setTimeout` herda o `this` do contexto da função `Comum`.\
>> Quando a função `Comum` é instanciada, `this` se refere à nova instância criada.
>> ```javascript
>> function Comum() {
>>     this.valor = 42;
>>     setTimeout(() => {
>>         console.log(this.valor); // 42
>>     }, 1000);
>> }
>> 
>> new Comum();
>> ```
>> 
>> ### # Function Borrowing
>> Function borrowing é a prática de usar métodos de um objeto em outro objeto.
>> #### Exemplo:
>> `pessoa1.saudacao` é emprestada para `pessoa2` usando `call`.\
>> O `this` dentro de `saudacao` se refere a `pessoa2` quando chamado com `call`.
>> ```javascript
>> const pessoa1 = {
>>     nome: 'Henrique',
>>     saudacao: function() {
>>         console.log(`Olá, eu sou ${this.nome}`);
>>     }
>> };
>> 
>> const pessoa2 = {
>>     nome: 'Rick'
>> };
>> 
>> pessoa1.saudacao.call(pessoa2); // Olá, eu sou Rick
>> ```
>> #### Exemplo:
>> `carro1.detalhes` é emprestada para `carro2` usando `apply`.\
>> O `this` dentro de `detalhes` se refere a `carro2` quando chamado com `apply`.
>> ```javascript
>> const carro1 = {
>>     marca: 'Honda',
>>     modelo: 'Civic',
>>     detalhes: function() {
>>         console.log(`Carro: ${this.marca} ${this.modelo}`);
>>     }
>> };
>> 
>> const carro2 = {
>>     marca: 'Ford',
>>     modelo: 'Mustang'
>> };
>> 
>> carro1.detalhes.apply(carro2); // Carro: Ford Mustang
>> ```
>> 
>> ### # Ligação Explícita
>> #### Call
>> O método `call` chama uma função com um determinado `this` e argumentos passados individualmente.
>> #### Exemplo:
>> `call` é usado para chamar `apresentar` com `this` definido como `null` e argumentos `'Rick'` e `22`.
>> ```javascript
>> function apresentar(nome, idade) {
>>     console.log(`Nome: ${nome}, Idade: ${idade}`);
>> }
>> 
>> apresentar.call(null, 'Alice', 25); // Nome: Rick, Idade: 22
>> ```
>> #### Exemplo:
>> `call` é usado para chamar `dizerNome` com `this` definido como `pessoa`.
>> ```javascript
>> const pessoa = {
>>     nome: 'Henrique'
>> };
>> 
>> function dizerNome() {
>>     console.log(this.nome);
>> }
>> 
>> dizerNome.call(pessoa); // Henrique
>> ```
>> 
>> #### Apply
>> O método `apply` é semelhante ao `call`, mas os argumentos são passados como um array.
>> #### Exemplo:
>> `apply` é usado para chamar `calcular` com `this` definido como `null` e argumentos `[1, 2, 3]`.
>> ```javascript
>> function calcular(a, b, c) {
>>     return a + b + c;
>> }
>> 
>> console.log(calcular.apply(null, [1, 2, 3])); // 6
>> ```
>> #### Exemplo:
>> `apply` é usado para chamar `dizerNomeEIdade` com `this` definido como `pessoa` e argumento `22`.
>> ```javascript
>> const pessoa = {
>>     nome: 'Rick Lustri'
>> };
>> 
>> function dizerNomeEIdade(idade) {
>>     console.log(`Nome: ${this.nome}, Idade: ${idade}`);
>> }
>> 
>> dizerNomeEIdade.apply(pessoa, [22]); // Nome: Rick Lustri, Idade: 22
>> ```
>> 
>> #### Bind
>> O método `bind` cria uma nova função que, quando chamada, tem seu `this` definido com um valor específico.
>> #### Exemplo:
>> ```javascript
>> const pessoa = {
>>     nome: 'Henrique'
>> };
>> 
>> function saudacao() {
>>     console.log(`Olá, ${this.nome}`);
>> }
>> 
>> const saudacaoHenrique = saudacao.bind(pessoa);
>> saudacaoHenrique(); // Olá, Henrique
>> ```
>> `bind` é usado para criar uma nova função `saudacaoHenrique` com `this` definido como `pessoa`.
>> #### Exemplo:
>> `bind` é usado para criar uma nova função `detalhesBMW` com `this` definido como `carro`.
>> ```javascript
>> const carro = {
>>     marca: 'BMW',
>>     modelo: 'X5'
>> };
>> 
>> function detalhesCarro() {
>>     console.log(`Marca: ${this.marca}, Modelo: ${this.modelo}`);
>> }
>> 
>> const detalhesBMW = detalhesCarro.bind(carro);
>> detalhesBMW(); // Marca: BMW, Modelo: X5
>> ```
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

<br>

> ![Diagrama Mermaid](/assets/image/asynchronous.svg)
>> ## Asynchronous
>> ### # `setTimeout`
>> #### O que é `setTimeout`?
>> `setTimeout` é uma função JavaScript que permite executar um pedaço de código ou uma função após um determinado período de tempo. Esse tempo é especificado em milissegundos. A função `setTimeout` é útil para atrasar a execução de uma ação ou tarefa.
>> #### Sintaxe
>> ```javascript
>> setTimeout(function, delay, ...arguments);
>> ```
>> `function`: A função que será executada após o tempo especificado.\
>> `delay`: O tempo em milissegundos após o qual a função será executada.\
>> `arguments`: Argumentos adicionais que podem ser passados para a função.
>> #### Exemplo:
>> ```javascript
>> // Função a ser executada
>> function falarOla(nome) {
>>     console.log(`Olá, ${nome}!`);
>> }
>> 
>> // Definindo o tempo de atraso em 2000 milissegundos (2 segundos)
>> const segundos = 2000;
>> 
>> // Chamando setTimeout para executar falarOla após 2 segundos
>> setTimeout(falarOla, segundos, "Henrique");
>> 
>> ```
>> 1. Definimos a função `falarOla` que aceita um parâmetro `nome`.
>> 2. Usamos `setTimeout` para chamar `falarOla` após 2 segundos (2000 milissegundos).
>> 3. O terceiro argumento `"Henrique"` é passado para a função `falarOla` quando ela for executada.
>> 4. Após 2 segundos, a mensagem `"Olá, Henrique!"` será exibida no console.
>> 
>> #### Cancelando um `setTimeout`
>> Você pode cancelar um `setTimeout` usando a função `clearTimeout`. Para isso, você precisa armazenar o ID do `setTimeout` em uma variável e então chamar `clearTimeout` com esse ID.
>> ```javascript
>> // Função a ser executada
>> function falarOla(nome) {
>>     console.log(`Olá, ${nome}!`);
>> }
>> 
>> // Definindo o tempo de atraso em 5000 milissegundos (5 segundos)
>> const segundos = 5000;
>> 
>> // Chamando setTimeout para executar falarOla após 5 segundos
>> const timeoutId = setTimeout(falarOla, segundos, "Rick");
>> 
>> // Cancelando o setTimeout antes que ele seja executado
>> clearTimeout(timeoutId);
>> ```
>> 1. Definimos a função `falarOla` que aceita um parâmetro `nome`.
>> 2. Usamos `setTimeout` para chamar `falarOla` após 5 segundos (5000 milissegundos).
>> 3. O `ID` retornado por `setTimeout` é armazenado na variável `timeoutId`.
>> 4. Chamamos `clearTimeout` com `timeoutId` para cancelar a execução de `falarOla`.
>> 5. Como resultado, a função `falarOla` não será executada e a mensagem `"Olá, Rick!"` não será exibida.
>> 
>> ### # `setInterval`
>> #### O que é `setInterval`?
>> `setInterval` é uma função JavaScript que permite executar repetidamente um pedaço de código ou uma função em intervalos de tempo regulares. O intervalo é especificado em milissegundos. A função `setInterval` é útil para executar tarefas periódicas.
>> #### Sintaxe
>> ```javascript
>> setInterval(function, delay, ...arguments);
>> ```
>> `function`: A função que será executada repetidamente.\
>> `delay`: O intervalo de tempo em milissegundos entre cada execução da função.\
>> `arguments`: Argumentos adicionais que podem ser passados para a função.
>> #### Exemplo:
>> ```javascript
>> // Função a ser executada
>> function mostrarHoraAtual() {
>>     const time = new Date();
>>     console.log(`Hora atual: ${time.toLocaleTimeString()}`);
>> }
>> 
>> // Definindo o intervalo em 1000 milissegundos (1 segundo)
>> const intervalo = 1000;
>> 
>> // Chamando setInterval para executar smostrarHoraAtual a cada 1 segundo
>> const intervalId = setInterval(mostrarHoraAtual, intervalo);
>> ```
>> 1. Definimos a função `mostrarHoraAtual` que exibe a hora atual no console.
>> 2. Usamos `setInterval` para chamar `mostrarHoraAtual` a cada 1 segundo (1000 milissegundos).
>> 3. O `ID` retornado por `setInterval` é armazenado na variável `intervalId`.
>> 4. A cada 1 segundo, a hora atual será exibida no console.
>> 
>> #### Cancelando um `setInterval`
>> Você pode cancelar um `setInterval` usando a função `clearInterval`. Para isso, você precisa armazenar o ID do `setInterval` em uma variável e então chamar `clearInterval` com esse ID.
>> ```javascript
>> // Função a ser executada
>> function mostrarHoraAtual() {
>>     const time = new Date();
>>     console.log(`Hora atual: ${time.toLocaleTimeString()}`);
>> }
>> 
>> // Definindo o intervalo em 1000 milissegundos (1 segundo)
>> const intervalo = 1000;
>> 
>> // Chamando setInterval para executar smostrarHoraAtual a cada 1 segundo
>> const intervalId = setInterval(mostrarHoraAtual, intervalo);
>> 
>> // Cancelando o setInterval após 5 segundos
>> setTimeout(() => clearInterval(intervalId), 5000);
>> 
>> ```
>> 1. Definimos a função `mostrarHoraAtual` que exibe a hora atual no console.
>> 2. Usamos `setInterval` para chamar `mostrarHoraAtual` a cada 1 segundo (1000 milissegundos).
>> 3. O `ID` retornado por `setInterval` é armazenado na variável `intervalId`.
>> 4. Usamos `setTimeout` para cancelar o `setInterval` após 5 segundos (5000 milissegundos).
>> 5. Como resultado, a função `mostrarHoraAtual` será executada 5 vezes antes de ser cancelada.
> 
><br>
>
>> ### # Event Loop
>> #### O que é o Event Loop?
>> O Event Loop é um mecanismo fundamental no JavaScript que permite a execução de código assíncrono. Ele monitora a pilha de chamadas (call stack) e a fila de mensagens (message queue) para garantir que o código assíncrono, como callbacks, seja executado quando a pilha de chamadas estiver vazia.
>> #### Componentes Principais
>> 1. **Call Stack (Pilha de Chamadas)**: Onde o código é executado. Cada vez que uma função é chamada, ela é adicionada à pilha. Quando a função termina sua execução, ela é removida da pilha.
>> 2. **Message Queue (Fila de Mensagens)**: Onde as mensagens (ou callbacks) aguardam para serem executadas. Cada mensagem é uma função que precisa ser processada.
>> 3. **Event Loop (Loop de Eventos)**: O Event Loop verifica continuamente se a pilha de chamadas está vazia. Se estiver, ele pega a primeira mensagem da fila de mensagens e a coloca na pilha de chamadas para ser executada.
>> 
>> #### Exemplo:
>> Vamos ver como o Event Loop funciona com um exemplo prático.
>> ```javascript
>> console.log('Start'); // 1. Adiciona 'Start' à pilha de chamadas e executa
>> 
>> setTimeout(() => {
>>     console.log('Callback 1'); // 4. Adiciona 'Callback 1' à fila de mensagens após 0 ms
>> }, 0);
>> 
>> console.log('Meio'); // 2. Adiciona 'Meio' à pilha de chamadas e executa
>> 
>> setTimeout(() => {
>>     console.log('Callback 2'); // 5. Adiciona 'Callback 2' à fila de mensagens após 1000 ms
>> }, 1000);
>> 
>> console.log('End'); // 3. Adiciona 'End' à pilha de chamadas e executa
>> 
>> 
>> // Ordem de execução esperada:
>> // 'Start'
>> // 'Meio'
>> // 'End'
>> // 'Callback 1'
>> // 'Callback 2'
>> ```
>> #### Explicação:
>> 1. `'Start'` é adicionado à pilha de chamadas e é imediatamente executado, exibindo `'Start'` no console.
>> 2. `setTimeout` é chamado com um atraso de 0 ms. A função de `callback` é colocada na fila de mensagens para ser executada depois que a pilha de chamadas estiver vazia.
>> 3. `'Meio'` é adicionado à pilha de chamadas e é imediatamente executado, exibindo `'Meio'` no console.
>> 4. Outro `setTimeout` é chamado com um atraso de 1000 ms. A função de `callback` é colocada na fila de mensagens para ser executada após 1 segundo.
>> 5. `'End'` é adicionado à pilha de chamadas e é imediatamente executado, exibindo `'End'` no console.
>> 6. Após a pilha de chamadas estar vazia, o Event Loop verifica a fila de mensagens e encontra `'Callback 1'`, que é então adicionado à pilha de chamadas e executado, exibindo `'Callback 1'` no console.
>> 7. Após 1 segundo, o Event Loop verifica novamente a fila de mensagens e encontra `'Callback 2'`, que é então adicionado à pilha de chamadas e executado, exibindo `'Callback 2'` no console.
>> 
>> #### Visualização do Event Loop
>> 1. **Call Stack (Pilha de Chamadas)**:
>>    - `console.log('Start')` -> `console.log('Meio')` -> `console.log('End')` -> `console.log('Callback 1')` -> `console.log('Callback 2')`
>> 
>> 2. **Message Queue (Fila de Mensagens)**:
>>    - Após `setTimeout(() => { console.log('Callback 1'); }, 0)`, a função de callback é colocada na fila de mensagens.
>>    - Após `setTimeout(() => { console.log('Callback 2'); }, 1000)`, a função de callback é colocada na fila de mensagens após 1 segundo.
>> 
>> 3. **Event Loop (Loop de Eventos)**:
>>    - Verifica continuamente se a pilha de chamadas está vazia.
>>    - Quando a pilha de chamadas está vazia, pega a próxima mensagem na fila de mensagens e a coloca na pilha de chamadas para ser executada.
>>  
>> #### Por que o Event Loop é Importante?
>> O Event Loop permite que o JavaScript seja não bloqueante e assíncrono, o que significa que ele pode lidar com múltiplas operações de I/O (entrada/saída) sem bloquear a execução do código. Isso é crucial para a construção de aplicações web eficientes e responsivas.
>
><br>
>
>> ### # Callbacks
>> #### O que são Callbacks?
>> Callbacks são funções passadas como argumentos para outras funções e são chamadas (ou "invocadas") dentro da função que as recebe. No JavaScript, os callbacks são frequentemente usados para operações assíncronas, como leitura de arquivos, consultas a bancos de dados, ou requisições HTTP.
>> #### Sintaxe
>> ```javascript
>> function doSomething(callback) {
>>     // Código assíncrono
>>     callback();
>> }
>> ```
>> #### Exemplo:
>> ```javascript
>> // Função que simula uma operação assíncrona usando setTimeout
>> function buscarDados(callback) {
>>     console.log('Buscando dados...');
>>     setTimeout(() => {
>>         const dados = { nome: 'Henrique', idade: 22 };
>>         callback(dados);
>>     }, 2000); // Simula um atraso de 2 segundos
>> }
>> 
>> // Função de callback que processa os dados
>> function processarDados(dados) {
>>     console.log('Informação recebida:', dados);
>> }
>> 
>> // Chamando a função assíncrona com o callback
>> buscarDados(processarDados);
>> ```
>> 1. Definimos a função `buscarDados` que aceita um `callback` como parâmetro.
>> 2. Dentro de `buscarDados`, usamos `setTimeout` para simular uma operação assíncrona com um atraso de 2 segundos.
>> 3. Após o atraso, a função de `callback` é chamada com os dados simulados.
>> 4. Definimos a função `processarDados` que aceita os dados como parâmetro e os exibe no console.
>> 5. Chamamos `buscarDados` e passamos `processarDados` como o callback.
>> 6. Após 2 segundos, a mensagem `'Informação recebida: { nome: "Henrique", idade: 22 }'` é exibida no console.
>> 
>> ### # Callback Hell
>> #### O que é Callback Hell?
>> Callback Hell é uma situação que ocorre quando vários callbacks aninhados são usados, resultando em código difícil de ler e manter. Isso geralmente acontece em operações assíncronas que dependem de várias etapas ou chamadas de função sequenciais.
>> #### Exemplo de Callback Hell
>> ```javascript
>> // Simulação de uma série de operações assíncronas dependentes
>> function step1(value, callback) {
>>     console.log('Step 1:', value);
>>     setTimeout(() => callback(value + 1), 1000); // Atraso de 1 segundo
>> }
>> 
>> function step2(value, callback) {
>>     console.log('Step 2:', value);
>>     setTimeout(() => callback(value + 1), 1000); // Atraso de 1 segundo
>> }
>> 
>> function step3(value, callback) {
>>     console.log('Step 3:', value);
>>     setTimeout(() => callback(value + 1), 1000); // Atraso de 1 segundo
>> }
>> 
>> // Executando as funções em sequência com callbacks aninhados
>> step1(0, (result1) => {
>>     step2(result1, (result2) => {
>>         step3(result2, (result3) => {
>>             console.log('Final result:', result3);
>>         });
>>     });
>> });
>> ```
>> 1. Definimos três funções assíncronas: `step1`, `step2` e `step3`, cada uma com um atraso de 1 segundo.
>> 2. Cada função exibe o valor atual e chama o `callback` com o valor incrementado em 1.
>> 3. Chamamos `step1` com o valor inicial 0 e um `callback` que chama `step2`.
>> 4. O `callback` de `step2` chama `step3` com o valor resultante de `step2`.
>> 5. O `callback` de `step3` exibe o resultado final no console.
>> 6. O código é difícil de ler devido ao aninhamento de callbacks.
>> 
>> #### Como Evitar Callback Hell
>> Existem várias maneiras de evitar o Callback Hell:
>> 
>> 1. **Modularizar Funções**: Separar funções em partes menores e reutilizáveis.
>> 2. **Promises**: Utilizar Promises para lidar com operações assíncronas de forma mais limpa.
>> 3. **Async/Await**: Usar `async` e `await` para escrever código assíncrono que se pareça com código síncrono.
>> 
>> #### Exemplo Usando Promises
>> ```javascript
>> // Convertendo funções para retornar Promises
>> function step1(value) {
>>     return new Promise((resolve) => {
>>         console.log('Step 1:', value);
>>         setTimeout(() => resolve(value + 1), 1000); // Atraso de 1 segundo
>>     });
>> }
>> 
>> function step2(value) {
>>     return new Promise((resolve) => {
>>         console.log('Step 2:', value);
>>         setTimeout(() => resolve(value + 1), 1000); // Atraso de 1 segundo
>>     });
>> }
>> 
>> function step3(value) {
>>     return new Promise((resolve) => {
>>         console.log('Step 3:', value);
>>         setTimeout(() => resolve(value + 1), 1000); // Atraso de 1 segundo
>>     });
>> }
>> 
>> // Encadeando Promises
>> step1(0)
>>     .then(step2)
>>     .then(step3)
>>     .then((result) => {
>>         console.log('Final result:', result);
>>     });
>> 
>> ```
>> 1. Convertendo `step1`, `step2` e `step3` para retornar Promises.
>> 2. Cada função retorna uma Promise que resolve com o valor incrementado em 1 após 1 segundo.
>> 3. Usamos `.then()` para encadear as Promises, tornando o código mais legível.
>> 4. O resultado final é exibido no console após todas as operações assíncronas serem concluídas.
>> 
>> #### Exemplo Usando Async/Await
>> ```javascript
>> // Funções assíncronas retornando Promises
>> function step1(value) {
>>     return new Promise((resolve) => {
>>         console.log('Step 1:', value);
>>         setTimeout(() => resolve(value + 1), 1000); // Atraso de 1 segundo
>>     });
>> }
>> 
>> function step2(value) {
>>     return new Promise((resolve) => {
>>         console.log('Step 2:', value);
>>         setTimeout(() => resolve(value + 1), 1000); // Atraso de 1 segundo
>>     });
>> }
>> 
>> function step3(value) {
>>     return new Promise((resolve) => {
>>         console.log('Step 3:', value);
>>         setTimeout(() => resolve(value + 1), 1000); // Atraso de 1 segundo
>>     });
>> }
>> 
>> // Função assíncrona usando async/await
>> async function executeSteps() {
>>     const result1 = await step1(0);
>>     const result2 = await step2(result1);
>>     const result3 = await step3(result2);
>>     console.log('Final result:', result3);
>> }
>> 
>> // Chamando a função assíncrona
>> executeSteps();
>> ```
>> 1. Usamos `async/await` para escrever código assíncrono de maneira mais legível.
>> 2. A função `executeSteps` é declarada como assíncrona com a palavra-chave `async`.
>> 3. Usamos `await` para esperar a resolução de cada Promise retornada por `step1`, `step2` e `step3`.
>> 4. O resultado final é exibido no console após todas as operações assíncronas serem concluídas.
>
> <br>
>
>> ### # Promises
>> #### O que são Promises?
>> Promises são objetos que representam a eventual conclusão (ou falha) de uma operação assíncrona e seu valor resultante. Uma Promise pode estar em um dos três estados:
>> - **Pending** (Pendente): Estado inicial, que ainda não foi resolvido ou rejeitado.
>> - **Fulfilled** (Resolvida): A operação assíncrona foi concluída com sucesso e a Promise tem um valor.
>> - **Rejected** (Rejeitada): A operação assíncrona falhou e a Promise tem um motivo pelo qual foi rejeitada.
>> #### Sintaxe
>> ```javascript
>> let promise = new Promise(function(resolve, reject) {
>>     // Código assíncrono
>>     if (/* operação bem-sucedida */) {
>>         resolve(value);
>>     } else {
>>         reject(error);
>>     }
>> });
>> ```
>> #### Exemplo:
>> Vamos ver como criar e usar Promises com um exemplo.
>> ```javascript
>> // Criando uma função que retorna uma Promise
>> function buscarDados() {
>>     return new Promise((resolve, reject) => {
>>         console.log('Buscando dados...');
>>         setTimeout(() => {
>>             const dados = { nome: 'Rick', idade: 22 };
>>             if (dados) {
>>                 resolve(dados); // Resolve a Promise com os dados
>>             } else {
>>                 reject('Error: Dados não encontrado'); // Rejeita a Promise com um erro
>>             }
>>         }, 2000); // Simula um atraso de 2 segundos
>>     });
>> }
>> 
>> // Usando a Promise
>> buscarDados()
>>     .then((dados) => {
>>         console.log('Dados recebidos', dados);
>>     })
>>     .catch((error) => {
>>         console.error(error);
>>     });
>> 
>> ```
>> 1. Criamos a função `buscarDados` que retorna uma Promise.
>> 2. Dentro da Promise, usamos `setTimeout` para simular uma operação assíncrona com um atraso de 2 segundos.
>> 3. Se os dados são encontrados, chamamos `resolve(dados)` para resolver a Promise.
>> 4. Se ocorrer um erro, chamamos `reject('Error: Dados não encontrado)` para rejeitar a Promise.
>> 5. Usamos `.then()` para manipular a resolução da Promise e exibir os dados recebidos no console.
>> 6. Usamos `.catch()` para manipular a rejeição da Promise e exibir o erro no console.
>> 
>> ### # Async/Await
>> #### O que são Async/Await?
>> `async` e `await` são palavras-chave do JavaScript que simplificam o trabalho com código assíncrono, permitindo que você escreva código assíncrono que parece síncrono. 
>> - **async**: Define uma função assíncrona que retorna uma Promise.
>> - **await**: Pausa a execução da função assíncrona até que a Promise seja resolvida ou rejeitada.
>> #### Sintaxe
>> ```javascript
>> async function myFunction() {
>>     let result = await somePromise;
>> }
>> ```
>> #### Exemplo:
>> Vamos ver como usar `async` e `await` para simplificar o exemplo anterior.
>> ```javascript
>> // Função assíncrona que retorna uma Promise
>> function buscarDados() {
>>     return new Promise((resolve, reject) => {
>>         console.log('Buscando dados...');
>>         setTimeout(() => {
>>             const dados = { nome: 'RickLustri', idade: 22 };
>>             if (dados) {
>>                 resolve(dados); // Resolve a Promise com os dados
>>             } else {
>>                 reject('Error: Dados não encontrado'); // Rejeita a Promise com um erro
>>             }
>>         }, 2000); // Simula um atraso de 2 segundos
>>     });
>> }
>> 
>> // Função assíncrona usando async/await
>> async function displayData() {
>>     try {
>>         const data = await buscarDados(); // Espera a resolução da Promise
>>         console.log('Data received:', data);
>>     } catch (error) {
>>         console.error(error); // Manipula a rejeição da Promise
>>     }
>> }
>> 
>> // Chamando a função assíncrona
>> displayData();
>> ```
>> 1. A função `buscarDados` permanece a mesma, retornando uma Promise.
>> 2. Definimos a função `displayData` como assíncrona usando a palavra-chave `async`.
>> 3. Dentro de `displayData`, usamos `await` para esperar a resolução da Promise retornada por `buscarDados`.
>> 4. Se a Promise for resolvida, os dados são exibidos no console.
>> 5. Usamos `try...catch` para manipular possíveis erros (rejeição da Promise).
>> 6. Chamamos `displayData` para executar o código assíncrono.
>> 
>> ### # Comparação entre Promises e Async/Await
>> #### Usando Promises
>> ```javascript
>> buscarDados()
>>     .then((dados) => {
>>         console.log('Dados encontrados:', dados);
>>     })
>>     .catch((error) => {
>>         console.error(error);
>>     });
>> ```
>> 
>> #### Usando Async/Await
>> ```javascript
>> async function displayData() {
>>     try {
>>         const dados = await buscarDados();
>>         console.log('Dados encotrados:', dados);
>>     } catch (error) {
>>         console.error(error);
>>     }
>> }
>> 
>> displayData();
>> ```
>> #### Vantagens do Async/Await
>> - **Leitura mais limpa e intuitiva**: Código assíncrono parece síncrono, facilitando a leitura e manutenção.
>> - **Menos aninhamento**: Evita o problema de "Promise chaining" (encadeamento de Promises) excessivo, tornando o código mais linear.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Promise](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Promise), [MDN - async/await](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/async_function), [MDN - Callback](https://developer.mozilla.org/pt-BR/docs/Glossary/Callback_function) e [MDN - Event loop](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Event_loop)
<br>
<hr>

> ![Diagrama Mermaid](/assets/image/sobreApi.svg)
>> ## Sobre API's
>> ### XMLHttpRequest
>> #### O que é XMLHttpRequest?
>> `XMLHttpRequest` é um objeto em JavaScript que permite fazer requisições HTTP para interagir com servidores. Ele pode ser usado para buscar dados de um servidor e atualizar partes de uma página web sem recarregar a página inteira. Isso é uma parte fundamental do AJAX (Asynchronous JavaScript and XML).
>> #### Criando um XMLHttpRequest
>> Para usar `XMLHttpRequest`, você primeiro precisa criar uma instância desse objeto:
>> ```javascript
>> let xhr = new XMLHttpRequest();
>> ```
>> ### # Métodos principais
>> Os métodos mais importantes do `XMLHttpRequest` são:
>> - `open(method, url, async)`: Inicializa a requisição. `method` é o método HTTP (GET, POST, etc.), `url` é o endpoint, e `async` define se a requisição será assíncrona (true) ou síncrona (false).
>> - `send(body)`: Envia a requisição. `body` é opcional e usado principalmente em requisições POST.
>> - `setRequestHeader(header, value)`: Define cabeçalhos HTTP adicionais.
>> ### # Eventos principais
>> - `onreadystatechange`: Evento disparado sempre que o `readyState` do `XMLHttpRequest` muda.
>> - `onload`: Evento disparado quando a requisição é completada com sucesso.
>> - `onerror`: Evento disparado quando ocorre um erro na requisição.
>> ### # Propriedades principais
>> - `readyState`: Retorna o estado atual da requisição. Os estados possíveis são:
>>   - `0`: Não inicializado
>>   - `1`: Conexão estabelecida
>>   - `2`: Requisição recebida
>>   - `3`: Processando requisição
>>   - `4`: Requisição concluída e a resposta está pronta
>> - `status`: Retorna o código de status HTTP da resposta (ex: 200 para sucesso).
>> - `responseText`: Retorna a resposta da requisição como uma string de texto.
>> - `responseXML`: Retorna a resposta da requisição como um documento XML.
>> ### # Requisição GET
>> Vamos fazer uma requisição GET para um API pública que retorna dados de usuários:
>> ```javascript
>> // Cria uma nova instância do XMLHttpRequest
>> let xhr = new XMLHttpRequest();
>> 
>> // Define o método e o URL para a requisição
>> xhr.open('GET', 'https://jsonplaceholder.typicode.com/users', true);
>> 
>> // Define o que fazer quando a resposta for carregada
>> xhr.onload = function() {
>>   if (xhr.status >= 200 && xhr.status < 300) {
>>     // Sucesso: parseia a resposta JSON
>>     let users = JSON.parse(xhr.responseText);
>>     console.log(users); // Exibe os dados dos usuários no console
>>   } else {
>>     // Se ocorreu um erro
>>     console.error('Erro na requisição:', xhr.statusText);
>>   }
>> };
>> 
>> // Define o que fazer se ocorrer um erro na requisição
>> xhr.onerror = function() {
>>   console.error('Erro na conexão');
>> };
>> 
>> // Envia a requisição
>> xhr.send();
>> ```
>> 
>> #### Explicação:
>> 1. **Criando o objeto**: `let xhr = new XMLHttpRequest();`
>>    - Cria uma nova instância de `XMLHttpRequest`.
>> 
>> 2. **Inicializando a requisição**: `xhr.open('GET', 'https://jsonplaceholder.typicode.com/users', true);`
>>    - Configura a requisição para usar o método GET e acessar a URL especificada. A requisição será assíncrona (true).
>> 
>> 3. **Configurando o evento onload**:
>>    - `xhr.onload` define uma função que será chamada quando a resposta for carregada com sucesso.
>>    - `if (xhr.status >= 200 && xhr.status < 300)` verifica se o status da resposta está no intervalo de sucesso (200–299).
>>    - `let users = JSON.parse(xhr.responseText);` converte a resposta JSON em um objeto JavaScript.
>>    - `console.log(users);` exibe os dados no console.
>> 
>> 4. **Configurando o evento onerror**:
>>    - `xhr.onerror` define uma função que será chamada se ocorrer um erro na requisição.
>> 
>> 5. **Enviando a requisição**: `xhr.send();`
>>    - Envia a requisição ao servidor.
>> 
>> ### # Requisição POST
>> Agora, vamos fazer uma requisição POST para enviar dados para o servidor:
>> ```javascript
>> // Cria uma nova instância do XMLHttpRequest
>> let xhr = new XMLHttpRequest();
>> 
>> // Define o método e o URL para a requisição
>> xhr.open('POST', 'https://jsonplaceholder.typicode.com/posts', true);
>> 
>> // Define o cabeçalho da requisição como JSON
>> xhr.setRequestHeader('Content-Type', 'application/json; charset=UTF-8');
>> 
>> // Define o que fazer quando a resposta for carregada
>> xhr.onload = function() {
>>   if (xhr.status >= 200 && xhr.status < 300) {
>>     // Sucesso: parseia a resposta JSON
>>     let response = JSON.parse(xhr.responseText);
>>     console.log(response); // Exibe a resposta no console
>>   } else {
>>     // Se ocorreu um erro
>>     console.error('Erro na requisição:', xhr.statusText);
>>   }
>> };
>> 
>> // Define o que fazer se ocorrer um erro na requisição
>> xhr.onerror = function() {
>>   console.error('Erro na conexão');
>> };
>> 
>> // Define os dados que serão enviados
>> let data = JSON.stringify({
>>   title: 'foo',
>>   body: 'bar',
>>   userId: 1
>> });
>> 
>> // Envia a requisição com os dados
>> xhr.send(data);
>> ```
>> #### Explicação:
>> 1. **Criando o objeto**: `let xhr = new XMLHttpRequest();`
>>    - Cria uma nova instância de `XMLHttpRequest`.
>> 
>> 2. **Inicializando a requisição**: `xhr.open('POST', 'https://jsonplaceholder.typicode.com/posts', true);`
>>    - Configura a requisição para usar o método POST e acessar a URL especificada. A requisição será assíncrona (true).
>> 
>> 3. **Definindo o cabeçalho da requisição**: `xhr.setRequestHeader('Content-Type', 'application/json; charset=UTF-8');`
>>    - Define que o corpo da requisição será JSON.
>> 
>> 4. **Configurando o evento onload**:
>>    - `xhr.onload` define uma função que será chamada quando a resposta for carregada com sucesso.
>>    - `if (xhr.status >= 200 && xhr.status < 300)` verifica se o status da resposta está no intervalo de sucesso (200–299).
>>    - `let response = JSON.parse(xhr.responseText);` converte a resposta JSON em um objeto JavaScript.
>>    - `console.log(response);` exibe os dados no console.
>> 
>> 5. **Configurando o evento onerror**:
>>    - `xhr.onerror` define uma função que será chamada se ocorrer um erro na requisição.
>> 
>> 6. **Definindo os dados**: `let data = JSON.stringify({ title: 'foo', body: 'bar', userId: 1 });`
>>    - Converte os dados em uma string JSON para serem enviados.
>> 
>> 7. **Enviando a requisição com os dados**: `xhr.send(data);`
>>    - Envia a requisição ao servidor com os dados JSON.
>> 
>> #### Conclusão:
>> O `XMLHttpRequest` é uma ferramenta poderosa para fazer requisições HTTP assíncronas e síncronas em JavaScript. No entanto, ele está sendo cada vez mais substituído pelo `fetch`, que oferece uma API mais moderna e simplificada para realizar operações semelhantes. Contudo, ainda é importante compreender `XMLHttpRequest`, pois é amplamente utilizado em muitas aplicações web existentes.
>
><br>
>
>> ###  Fetch
>> ### O que é Fetch API?
>> Fetch API é uma interface moderna que permite fazer requisições HTTP de forma mais simples e intuitiva do que o `XMLHttpRequest`. A Fetch API usa Promises, que facilitam o manuseio de requisições assíncronas.
>> ### # Como usar a Fetch API
>> A Fetch API é utilizada através da função global `fetch()`, que retorna uma Promise. Esta Promise resolve para o objeto `Response`, representando a resposta à requisição.
>> #### Sintaxe básica
>> A sintaxe básica do `fetch` é:
>> ```javascript
>> fetch(url, options)
>>   .then(response => {
>>     // Processa a resposta aqui
>>   })
>>   .catch(error => {
>>     // Lida com o erro aqui
>>   });
>> ```
>> ### # Requisição GET
>> Vamos fazer uma requisição GET para um API pública que retorna dados de usuários:
>> ```javascript
>> // URL da API
>> const url = 'https://jsonplaceholder.typicode.com/users';
>> 
>> // Fazendo a requisição GET
>> fetch(url)
>>   .then(response => {
>>     // Verifica se a resposta está ok (status 200-299)
>>     if (!response.ok) {
>>       throw new Error('Network response was not ok ' + response.statusText);
>>     }
>>     // Converte a resposta para JSON
>>     return response.json();
>>   })
>>   .then(data => {
>>     // Processa os dados
>>     console.log(data); // Exibe os dados no console
>>   })
>>   .catch(error => {
>>     // Lida com os erros
>>     console.error('There has been a problem with your fetch operation:', error);
>>   });
>> ```
>> #### Explicação:
>> 1. **Definindo a URL**: `const url = 'https://jsonplaceholder.typicode.com/users';`
>>    - Define a URL do endpoint da API.
>> 
>> 2. **Fazendo a requisição GET**: `fetch(url)`
>>    - Faz a requisição para a URL especificada.
>> 
>> 3. **Processando a resposta**:
>>    - `response.ok` verifica se a resposta foi bem-sucedida.
>>    - `response.json()` converte a resposta em JSON.
>> 
>> 4. **Manipulando os dados**: `console.log(data);`
>>    - Exibe os dados da resposta no console.
>> 
>> 5. **Lidando com erros**: `catch(error => { ... });`
>>    - Captura e exibe quaisquer erros que ocorram durante a requisição.
>> 
>> ### # Requisição POST
>> Vamos fazer uma requisição POST para enviar dados para o servidor:
>> ```javascript
>> // URL da API
>> const url = 'https://jsonplaceholder.typicode.com/posts';
>> 
>> // Dados a serem enviados
>> const data = {
>>   title: 'foo',
>>   body: 'bar',
>>   userId: 1
>> };
>> 
>> // Fazendo a requisição POST
>> fetch(url, {
>>   method: 'POST', // Método HTTP
>>   headers: {
>>     'Content-Type': 'application/json; charset=UTF-8' // Cabeçalhos HTTP
>>   },
>>   body: JSON.stringify(data) // Dados enviados no corpo da requisição
>> })
>>   .then(response => {
>>     // Verifica se a resposta está ok (status 200-299)
>>     if (!response.ok) {
>>       throw new Error('Network response was not ok ' + response.statusText);
>>     }
>>     // Converte a resposta para JSON
>>     return response.json();
>>   })
>>   .then(data => {
>>     // Processa os dados
>>     console.log(data); // Exibe a resposta no console
>>   })
>>   .catch(error => {
>>     // Lida com os erros
>>     console.error('There has been a problem with your fetch operation:', error);
>>   });
>> ```
>> #### Explicação:
>> 1. **Definindo a URL**: `const url = 'https://jsonplaceholder.typicode.com/posts';`
>>    - Define a URL do endpoint da API.
>> 
>> 2. **Definindo os dados**: `const data = { ... };`
>>    - Define os dados a serem enviados no corpo da requisição.
>> 
>> 3. **Fazendo a requisição POST**: `fetch(url, { method: 'POST', headers: { ... }, body: JSON.stringify(data) })`
>>    - Configura a requisição para usar o método POST, define os cabeçalhos e converte os dados para JSON.
>> 
>> 4. **Processando a resposta**:
>>    - `response.ok` verifica se a resposta foi bem-sucedida.
>>    - `response.json()` converte a resposta em JSON.
>> 
>> 5. **Manipulando os dados**: `console.log(data);`
>>    - Exibe os dados da resposta no console.
>> 
>> 6. **Lidando com erros**: `catch(error => { ... });`
>>    - Captura e exibe quaisquer erros que ocorram durante a requisição.
>> 
>> ### # Lidando com requisições e respostas
>> A Fetch simplifica a manipulação de respostas, especialmente no que diz respeito ao tratamento de diferentes tipos de dados (como JSON, texto, e até mesmo blobs).
>> #### # Requisição com autenticação
>> Algumas APIs exigem autenticação, que pode ser facilmente adicionada usando cabeçalhos.
>> ```javascript
>> // URL da API
>> const url = 'https://api.example.com/protected';
>> 
>> // Fazendo a requisição GET com autenticação
>> fetch(url, {
>>   method: 'GET',
>>   headers: {
>>     'Authorization': 'Bearer YOUR_ACCESS_TOKEN'
>>   }
>> })
>>   .then(response => {
>>     if (!response.ok) {
>>       throw new Error('Network response was not ok ' + response.statusText);
>>     }
>>     return response.json();
>>   })
>>   .then(data => {
>>     console.log(data);
>>   })
>>   .catch(error => {
>>     console.error('There has been a problem with your fetch operation:', error);
>>   });
>> ```
>> #### Explicação:
>> 1. **Definindo a URL**: `const url = 'https://api.example.com/protected';`
>>    - Define a URL do endpoint da API.
>> 
>> 2. **Fazendo a requisição GET com autenticação**: `fetch(url, { method: 'GET', headers: { 'Authorization': 'Bearer YOUR_ACCESS_TOKEN' } })`
>>    - Configura a requisição para usar o método GET e inclui o cabeçalho de autenticação.
>> 
>> 3. **Processando a resposta**:
>>    - `response.ok` verifica se a resposta foi bem-sucedida.
>>    - `response.json()` converte a resposta em JSON.
>> 
>> 4. **Manipulando os dados**: `console.log(data);`
>>    - Exibe os dados da resposta no console.
>> 
>> 5. **Lidando com erros**: `catch(error => { ... });`
>>    - Captura e exibe quaisquer erros que ocorram durante a requisição.
>> 
>> #### Conclusão
>> A Fetch API é uma maneira moderna e simplificada de fazer requisições HTTP em JavaScript. Ela oferece uma interface mais fácil de usar do que o `XMLHttpRequest` e permite um manuseio mais intuitivo de Promises, facilitando o trabalho com operações assíncronas. Através de exemplos comentados e detalhados, é possível entender como realizar diferentes tipos de requisições e como lidar com as respostas e possíveis erros.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) e [MDN - Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

<br>
<hr>

>> ## Classes
>> ### # O que são Classes em JavaScript?
>> Classes em JavaScript são uma forma moderna de criar objetos e implementar conceitos de Programação Orientada a Objetos (POO). Introduzidas no ECMAScript 6 (ES6), as classes fornecem uma sintaxe mais simples e familiar para desenvolvedores que vêm de outras linguagens orientadas a objetos, como Java ou C#. Embora JavaScript continue sendo uma linguagem baseada em protótipos, as classes oferecem uma maneira mais estruturada e legível de definir e herdar objetos.
>> 
>> #### Definindo uma Classe
>> Vamos definir uma classe simples chamada `Pessoa`. Uma classe em JavaScript é definida usando a palavra-chave `class`, seguida pelo nome da classe.
>> #### Exemplo Básico:
>> ```javascript
>> // Definindo a classe Pessoa
>> class Pessoa {
>>   // O método constructor é um método especial para criar e inicializar um objeto criado a partir de uma classe.
>>   constructor(nome, idade) {
>>     this.nome = nome; // Atribui o valor do argumento 'nome' à propriedade 'nome' do objeto
>>     this.idade = idade;   // Atribui o valor do argumento 'idade' à propriedade 'idade' do objeto
>>   }
>> 
>>   // Método de instância - estará disponível em todas as instâncias da classe
>>   apresentar() {
>>     console.log(`Olá, meu nome é ${this.nome} e eu tenho ${this.idade} anos.`);
>>   }
>> 
>>   // Método estático - disponível apenas na classe, não nas instâncias
>>   static especie() {
>>     console.log('Humana');
>>   }
>> }
>> 
>> // Criando uma instância da classe Pessoa
>> const pessoa1 = new Pessoa('Henrique', 22);
>> 
>> // Chamando o método de instância 'apresentar'
>> pessoa1.apresentar(); // Olá, meu nome é Henrique e eu tenho 22 anos.
>> 
>> // Chamando o método estático 'especie' diretamente na classe
>> Pessoa.especie(); // Humana
>> ```
>> #### Explicação:
>> 1. **Definição da Classe**: `class Pessoa` define uma nova classe chamada `Pessoa`.
>> 2. **Construtor**: `constructor(nome, idade)` é um método especial que inicializa novos objetos da classe. `this.nome` e `this.idade` são propriedades definidas com base nos argumentos passados ao construtor.
>> 3. **Método de Instância**: `apresentar()` é um método que pode ser chamado em qualquer instância da classe `Pessoa`.
>> 4. **Método Estático**: `static especie()` é um método que pode ser chamado diretamente na classe `Pessoa`, não em suas instâncias.
>> 5. **Instância da Classe**: `const pessoa1 = new Pessoa('Henrique', 22)` cria um novo objeto da classe `Pessoa`.
>> 6. **Chamando Métodos**: `pessoa1.apresentar()` chama o método `apresentar` na instância `pessoa1`. `Pessoa.especie()` chama o método estático `especie` na classe `Pessoa`.
>> 
>> ### # Herança
>> A herança permite que uma classe herde propriedades e métodos de outra classe, facilitando a reutilização de código e a criação de uma hierarquia de classes.
>> 
>> #### Exemplo de Herança
>> ```javascript
>> // Definindo uma classe chamada 'Funcionario' que herda da classe 'Pessoa'
>> class Funcionario extends Pessoa {
>>   constructor(nome, idade, meuTrabalho) {
>>     super(nome, idade); // Chama o construtor da classe pai (Pessoa)
>>     this.meuTrabalho = meuTrabalho; // Atribui o valor do argumento 'meuTrabalho' à propriedade 'meuTrabalho' do objeto
>>   }
>> 
>>   // Sobrescrevendo o método 'apresentar' da classe pai
>>   apresentar() {
>>     console.log(`Olá, meu nome é ${this.nome}, eu sou um(a) ${this.meuTrabalho} e eu tenho ${this.idade} anos.`);
>>   }
>> 
>>   // Método específico da classe 'Funcionario'
>>   trabalho() {
>>     console.log(`${this.nome} está trabalhando como ${this.meuTrabalho}.`);
>>   }
>> }
>> 
>> // Criando uma instância da classe 'Funcionario'
>> const funcionario1 = new Funcionario('Rick', 22, 'Desenvolvedor');
>> 
>> // Chamando o método de instância 'apresentar'
>> funcionario1.apresentar(); // Olá, meu nome é Rick, eu sou um(a) Desenvolvedor e eu tenho 22 anos.
>> 
>> // Chamando o método específico 'trabalho'
>> funcionario1.trabalho(); // Rick está trabalhando como Desenvolvedor.
>> ```
>> #### Explicação:
>> 1. **Definição da Classe Derivada**: `class Funcionario extends Pessoa` define uma nova classe `Funcionario` que herda da classe `Pessoa`.
>> 2. **Construtor**: `constructor(nome, idade, meuTrabalho)` inicializa a instância da classe `Funcionario`, chamando `super(nome, idade)` para herdar as propriedades `nome` e `idade` da classe `Pessoa`.
>> 3. **Método Sobrescrito**: `apresentar()` na classe `Funcionario` sobrescreve o método `apresentar` da classe `Pessoa`.
>> 4. **Novo Método**: `trabalho()` é um método específico da classe `Funcionario`.
>> 5. **Instância da Classe**: `const funcionario1 = new Funcionario('Rick', 22, 'Desenvolvedor')` cria um novo objeto da classe `Funcionario`.
>> 6. **Chamando Métodos**: `funcionario1.apresentar()` chama o método `apresentar` sobrescrito na instância `funcionario1`. `funcionario1.trabalho()` chama o método `trabalho` na instância `funcionario1`.
>> 
>> ### # Encapsulamento
>> O encapsulamento é uma prática de programação que esconde os detalhes internos de um objeto e expõe apenas o que é necessário. Em JavaScript, usamos `#` para declarar campos privados em classes.
>> 
>> #### Exemplo de Encapsulamento
>> ```javascript
>> // Definindo uma classe 'ContaBancaria' com campos privados
>> class ContaBancaria {
>>   // Campos privados são prefixados com #
>>   #saldo;
>> 
>>   constructor(dono, saldo) {
>>     this.dono = dono; // Atribui o valor do argumento 'dono' à propriedade 'dono' do objeto
>>     this.#saldo = saldo; // Inicializa o campo privado '#saldo' com o valor do argumento 'saldo'
>>   }
>> 
>>   // Método público para depositar dinheiro
>>   depositar(quantidade) {
>>     this.#saldo += quantidade;
>>     console.log(`${this.dono} depositou ${quantidade}. Saldo atual: ${this.#saldo}`);
>>   }
>> 
>>   // Método público para sacar dinheiro
>>   retirar(quantidade) {
>>     if (quantidade > this.#saldo) {
>>       console.log('Saldo insuficiente.');
>>     } else {
>>       this.#saldo -= quantidade;
>>       console.log(`${this.dono} sacou ${quantidade}. Saldo atual: ${this.#saldo}`);
>>     }
>>   }
>> 
>>   // Método público para verificar o saldo
>>   verificarSaldo() {
>>     console.log(`O saldo de ${this.dono} é ${this.#saldo}`);
>>   }
>> }
>> 
>> // Criando uma instância da classe ContaBancario
>> const conta = new ContaBancaria('Henrique', 1000);
>> 
>> // Interagindo com a conta bancária
>> conta.depositar(500); // Henrique depositou 500. Saldo atual: 1500
>> conta.retirar(200); // Henrique sacou 200. Saldo atual: 1300
>> conta.verificarSaldo(); // O saldo de Henrique é 1300
>> 
>> // Tentando acessar o campo privado '#saldo' diretamente (irá causar erro)
>> // console.log(conta.#saldo); // SyntaxError: Private field '#saldo' must be declared in an enclosing class
>> ```
>> #### Explicação:
>> 1. **Definição da Classe**: `class ContaBancaria` define uma nova classe chamada `ContaBancaria`.
>> 2. **Campos Privados**: `#saldo` é um campo privado, que não pode ser acessado diretamente fora da classe.
>> 3. **Construtor**: `constructor(dono, saldo)` inicializa a instância da classe com `dono` e `saldo`.
>> 4. **Métodos Públicos**: `depositar(quantidade)`, `retirar(quantidade)`, e `verificarSaldo()` são métodos públicos que interagem com o campo privado `#saldo`.
>> 5. **Instância da Classe**: `const conta = new ContaBancaria('Henrique', 1000)` cria um novo objeto da classe `ContaBancaria`.
>> 6. **Interagindo com a Instância**: `conta.depositar(500)` deposita dinheiro na conta. `conta.retirar(200)` saca dinheiro da conta. `conta.verificarSaldo()` verifica o saldo da conta.
>> 7. **Acesso Indevido**: `console.log(conta.#saldo)` tenta acessar o campo privado diretamente, o que resulta em um erro de sintaxe.
>> 
>> ### # Polimorfismo
>> O polimorfismo permite que métodos com o mesmo nome se comportem de maneira diferente em classes diferentes. No exemplo abaixo, o método `greet` se comporta de maneira diferente nas classes `Person` e `Employee`.
>> 
>> #### Exemplo de Polimorfismo
>> ```javascript
>> // Definindo a classe Programador que herda da classe Funcionario
>> class Programador extends Funcionario {
>>   constructor(nome, idade, meuTrabalho, departamento) {
>>     // Chama o construtor da classe pai (Funcionario)
>>     super(nome, idade, meuTrabalho);
>>     this.departamento = departamento; // Atribui o valor do argumento 'departamento' à propriedade 'departamento' do objeto
>>   }
>> 
>>   // Sobrescrevendo o método apresentar da classe pai
>>   apresentar() {
>>     console.log(`Olá, meu nome é ${this.nome}, eu sou um(a) ${this.meuTrabalho} do departamento de ${this.departamento} e eu tenho ${this.idade} anos.`);
>>   }
>> }
>> 
>> // Criando uma instância da classe Programador
>> const dev1 = new Programador('Rick', 22, 'Desenvolvedor', 'TI');
>> 
>> // Chamando o método de instância apresentar
>> dev1.apresentar();
>> 
>>  // Olá, meu nome é Rick, eu sou um(a) Desenvolvedor do departamento de TI e eu tenho 22 anos.
>> ```
>> #### Explicação:
>> 1. **Definição da Classe Derivada**: `class Programador extends Funcionario` define uma nova classe `Programador` que herda da classe `Funcionario`.
>> 2. **Construtor**: `constructor(nome, idade, meuTrabalho, departamento)` inicializa a instância da classe `Programador`, chamando `super(nome, idade, meuTrabalho)` para herdar as propriedades `nome`, `idade`, e `meuTrabalho` da classe `Funcionario`.
>> 3. **Método Sobrescrito**: `apresentar()` na classe `Programador` sobrescreve o método `apresentar` da classe `Funcionario`.
>> 4. **Instância da Classe**: `const dev1 = new Programador('Rick', 22, 'Desenvolvedor', 'TI')` cria um novo objeto da classe `Programador`.
>> 5. **Chamando Métodos**: `dev1.apresentar()` chama o método `apresentar` sobrescrito na instância `dev1`.
>> 
>> #### Conclusão
>> As classes em JavaScript fornecem uma maneira eficiente de criar e gerenciar objetos, promovendo a reutilização de código e a organização através de herança, encapsulamento e polimorfismo. Com a introdução de ES6, a sintaxe das classes tornou-se mais intuitiva e alinhada com outras linguagens de programação orientadas a objetos.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

<br>
<hr>


>> ## Introdução a Iterators
>> ### O que são Iterators?
>> Iterators são uma forma de acessar elementos de uma coleção (como arrays, strings ou objetos personalizados) de forma sequencial, sem expor a estrutura interna da coleção. Em JavaScript, um objeto é considerado um iterator se ele implementa um método chamado `next()`, que retorna um objeto com duas propriedades:
>> - `value`: O próximo valor na sequência.
>> - `done`: Um booleano indicando se a sequência terminou (`true`) ou não (`false`).
>> ### Exemplo de Iterator
>> Vamos criar um iterator simples para iterar sobre um array:
>> ```javascript
>> // Nosso array de exemplo
>> const array = [1, 2, 3, 4, 5];
>> 
>> // Função para criar um iterator para o array
>> function createIterator(arr) {
>>   let index = 0;
>>   return {
>>     next: function() {
>>       if (index < arr.length) {
>>         return { value: arr[index++], done: false };
>>       } else {
>>         return { value: undefined, done: true };
>>       }
>>     }
>>   };
>> }
>> 
>> // Criando o iterator
>> const iterator = createIterator(array);
>> 
>> console.log(iterator.next()); // { value: 1, done: false }
>> console.log(iterator.next()); // { value: 2, done: false }
>> console.log(iterator.next()); // { value: 3, done: false }
>> console.log(iterator.next()); // { value: 4, done: false }
>> console.log(iterator.next()); // { value: 5, done: false }
>> console.log(iterator.next()); // { value: undefined, done: true }
>> ```
>> Neste exemplo, a função `createIterator` cria um iterator para o array fornecido. Cada chamada para `next()` retorna o próximo valor do array até que todos os valores sejam retornados.
>
> <br>
> 
>> ## Introdução a Generators
>> ### O que são Generators?
>> Generators são uma forma mais poderosa e flexível de criar iterators em JavaScript. Um generator é uma função que pode ser pausada e retomada, e sua execução é controlada por meio do uso da palavra-chave `yield`. As funções geradoras são definidas usando a sintaxe `function*`.
>> ### Exemplo de Generator
>> Vamos criar um generator simples que produz valores de 1 a 5:
>> ```javascript
>> // Definindo uma função geradora
>> function* simpleGenerator() {
>>   yield 1;
>>   yield 2;
>>   yield 3;
>>   yield 4;
>>   yield 5;
>> }
>> 
>> // Criando um generator
>> const generator = simpleGenerator();
>> 
>> console.log(generator.next()); // { value: 1, done: false }
>> console.log(generator.next()); // { value: 2, done: false }
>> console.log(generator.next()); // { value: 3, done: false }
>> console.log(generator.next()); // { value: 4, done: false }
>> console.log(generator.next()); // { value: 5, done: false }
>> console.log(generator.next()); // { value: undefined, done: true }
>> ```
>> Neste exemplo, a função geradora `simpleGenerator` usa a palavra-chave `yield` para produzir valores. Cada chamada para `next()` retorna o próximo valor produzido pela função geradora.
>> 
>> ### # Usando Generators com Loop
>> Generators podem ser usados em loops para simplificar a iteração:
>> ```javascript
>> function* simpleGenerator() {
>>   yield 1;
>>   yield 2;
>>   yield 3;
>>   yield 4;
>>   yield 5;
>> }
>> 
>> // Criando um generator
>> const generator = simpleGenerator();
>> 
>> // Usando um loop for...of para iterar sobre os valores
>> for (const value of generator) {
>>   console.log(value); // 1, 2, 3, 4, 5
>> }
>> ```
>> Neste exemplo, o loop `for...of` itera automaticamente sobre os valores produzidos pelo generator.
>> 
>> ### # Usando Generators para Tarefas Complexas
>> Generators podem ser usados para implementar lógica mais complexa, como produção de uma sequência infinita de números:
>> ```javascript
>> function* infiniteSequence() {
>>   let i = 0;
>>   while (true) {
>>     yield i++;
>>   }
>> }
>> 
>> // Criando um generator
>> const generator = infiniteSequence();
>> 
>> // Pegando os primeiros 5 valores
>> console.log(generator.next().value); // 0
>> console.log(generator.next().value); // 1
>> console.log(generator.next().value); // 2
>> console.log(generator.next().value); // 3
>> console.log(generator.next().value); // 4
>> ```
>> Neste exemplo, o generator `infiniteSequence` continua produzindo valores indefinidamente.
>> 
>> ### Conclusão:
>> Iterators e Generators são ferramentas poderosas em JavaScript para manipular coleções de dados de forma eficiente e flexível. Iterators fornecem uma interface padrão para acessar elementos de uma coleção sequencialmente, enquanto Generators permitem criar iterators complexos com menos código e maior clareza.
>> ### Resumo dos Pontos Principais
>> - **Iterators**: Implementam um método `next()` para acessar elementos sequencialmente.
>> - **Generators**: Funções que podem ser pausadas e retomadas usando `yield`, facilitando a criação de iterators complexos.
>> > ##### OBS: Você pode aprender mais lendo esse artigo: [MDN - Iterators e Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_generators)
