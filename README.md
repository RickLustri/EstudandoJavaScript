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

![Diagrama Mermaid](/assets/image/variaveis.svg)

