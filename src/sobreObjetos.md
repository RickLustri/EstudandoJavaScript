> #### Em javascript para definir um objeto você pode utilizar chaves e existem 2 modos de declarar um objeto, primeiro é você usar chaves `{...}` e o segundo vc utiliza construtor `new Object()`
> ##### **Exemplo:**
> ```javascript
> // Sintaxe de objeto é:
> nomeDoObjeto = { propriedade: 'valor' }
> 
> // Exemplo usando chaves:
> const cardapio = {
>   prato1: "Macarrão",
>   prato2: "Sopa",
>   prato3: "Ovo frito"
> };
> 
> // Exemplo usando new Object():
> const cardapio = new Object();
> cardapio.prato1 = "Macarrão";
> cardapio.prato2 = "Sopa";
> cardapio.prato3 = "Ovo frito";
> ```
> #### Para acessar uma propriedade de algun dos objetos basta colocar o nome do objeto ponto e sua propriedade
> ##### **Exemplo:**
> ```javascript
> // Usaremos o exemplo acima para poder puxar as propriedades
> 
> // Puxando a propriedade "prato1" do objeto:
> console.log(cardapio.prato1); // Saída: Macarrão
> 
> // Você pode tambem utilizar [] para puxar as propriedades
> 
> // Puxando a propriedade "prato3" do objeto:
> console.log(cardapio["prato3"])
> ```
> #### Você pode usar metodos dentro dos objeto que sãoo basicamente funções integradas dentro do objeto
> ##### **Exemplo:**
> ```javascript
> const personagem = {
>   nome: "rkzin",
>   poder: "telepatia",
>   level: "100",
>   apresentacao: function (){
>     return "Personagem: " + this.nome + ", " + "Poder: " + this.poder + ", " + "level: " + this.level
>   }
> }
> 
> console.log(personagem.apresentacao()); // Saída: Personagem: rkzin, Poder: telepatia, level: 100
> ```
> #### Você pode alterar os valores do objeto
> ##### **Exemplo:**
> ```javascript
> const carro = {
>   marca: "Porsche",
>   modelo: "911",
>   ano: 2024,
>   descricao: function(){
>     return `Marca do carro: ${this.marca} do modelo ${this.modelo} do ano ${this.ano}`
>   }
> }
> console.log(carro.descricao()); // Saída: Marca do carro: Porsche do modelo 911 do ano 2024
> 
> // Você pode alterar ou adicionar propriedades:
> 
> // Exemplo:
> carro.cor = "Preto"; //  Adicionei a propriedade cor ao objeto
> 
> carro.ano = 2023; // Alterei o valor da propriedade do objeto
> 
> // Pode tambem deletar as propriedade do objeto:
> delete carro.modelo; // Propriedade deletada
> 
> // Veja como ficaria no log:
> console.log(carro.cor) // Saída: Preto
> console.log(carro.modelo) // Saída: undefined (lembrando que deletamos a propriedade do objeto)
> console.log(carro.descricao()); // Saída: Marca do carro: Porsche do modelo undefined do ano 2024
> ```

