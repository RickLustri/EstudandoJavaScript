<h1 align="center"> Estudando JavaScript</h1>

![Diagrama Mermaid](/assets/image/introducaojs.svg)

>> ## O que é JavaScript?
>> JavaScript é uma linguagem de programação de alto nível, interpretada e orientada a objetos. É uma das principais tecnologias da web, juntamente com HTML e CSS. É amplamente utilizada para criar páginas web interativas, aplicativos web e servidores. JavaScript permite a manipulação dinâmica de conteúdo, controle de multimídia, animação de gráficos e muito mais.
>
>> 
>> ## História do JavaScript
>> avaScript foi criado por Brendan Eich em 1995 enquanto trabalhava na Netscape. Desenvolvida em apenas dez dias, a linguagem foi inicialmente chamada de Mocha, depois LiveScript, e finalmente JavaScript. Seu objetivo era adicionar interatividade a páginas web. Em 1996, a Microsoft lançou o JScript, e para garantir a compatibilidade entre navegadores, JavaScript foi padronizado pela Ecma International como ECMAScript em 1997.\
Com o tempo, JavaScript evoluiu, tornando-se essencial para o desenvolvimento web, com o surgimento de bibliotecas e frameworks como [jQuery](https://jquery.com/), [Angular](https://angular.io/), [React](https://reactjs.org/), e [Vue.js](https://vuejs.org/), além da plataforma [Node.js](https://nodejs.org/), que permite a execução no lado do servidor. Hoje, JavaScript é amplamente utilizado e continua a evoluir, permanecendo crucial para experiências web dinâmicas.
>
>> ## Versões do JavaScript
>> JavaScript, inventado por Brendan Eich, alcançou o status de um padrão ECMA em 1997 e adotou o nome oficial ECMAScript. Esta linguagem evoluiu através de várias versões, nomeadamente [ES1](https://262.ecma-international.org/1.0/), [ES2](https://262.ecma-international.org/2.0/), [ES3](https://262.ecma-international.org/3.0/), [ES5](https://262.ecma-international.org/5.1/), e a transformadora [ES6](https://262.ecma-international.org/6.0/). Estas atualizações desempenharam um papel crucial na melhoria e padronização do JavaScript, tornando-o amplamente utilizado e valioso no campo em constante mudança do desenvolvimento web.
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

![Diagrama Mermaid](/assets/image/variaveis.svg)


>> ## Declarações de Variáveis
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

![Diagrama Mermaid](/assets/image/tipoDeDados.svg)

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

![Diagrama Mermaid](/assets/image/conversaoDeTipos.svg)

>> ## Conversão de Tipos
>>> # LOADING....
