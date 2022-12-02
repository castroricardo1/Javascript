# Objetos

Conjunto de variáveis e funções, que são chamadas de propriedades e métodos.

```js
var pessoa = {
  nome: 'André',
  idade: 28,
  profissao: 'Designer',
  possuiFaculdade: true,
}

pessoa.nome; // 'André'
pessoa.possuiFaculdade; // true
```
!!! note

    Propriedades e métodos consistem em nome (chave) e valor

### Métodos

É uma propriedade que possui uma função no local do seu valor.

```js
var quadrado = {
  lados: 4,
  area: function(lado) {
    return lado * lado;
  },
  perimetro: function(lado) {
    return this.lados * lado;
  },
}

quadrado.lados; // 4
quadrado.area(5); // 25
quadrado.perimetro(5); // 20
```

Abreviação de `#!javascript area:function () {}` para `#!javascript area () {}`, no ES6+

```js
var quadrado = {
  lados: 4,
  area(lado) {
    return lado * lado;
  },
  perimetro(lado) {
    return this.lados * lado;
  },
}
```

### Organizar Código

Objetos servem para organizar o código em pequenas partes reutilizáveis.

```js
Math.PI; // 3.14
Math.random(); // número aleatório

var pi = Math.PI;
console.log(pi); // 3.14
``` 
!!! tip "Dica"

    `#!javascript Math` é um objeto nativo de JavaScript. Já percebeu que `#!javascript console` é um objeto e `#!javascript log()` um método?

### Criar um Objeto

Um objeto é criado utilizando as chaves `{ }`

```js
var carro = {};
var pessoa = {};

console.log(typeof carro); // 'object'
```

### Dot Notation Get

Acesse propriedades de um objeto utilizando o ponto `.`

```js
var menu = {
  width: 800,
  height: 50,
  backgroundColor: '#84E',
}

var bg = menu.backgroundColor; // '#84E'
``` 

### Dot Notation Set

Substitua o valor de uma propriedade utilizando `.` e o `=` após o nome da mesma.

```js
var menu = {
  width: 800,
  height: 50,
  backgroundColor: '#84E',
}

menu.backgroundColor = '#000';
console.log(menu.backgroundColor); // '#000'
``` 

### Adicionar Propriedades e Métodos

Basta adicionar um novo nome e definir o valor.

```js
var menu = {
  width: 800,
}

menu.height = 50;
menu.position = 'fixed';
``` 

### Palavra-Chave This

`This` irá fazer uma referência ao próprio objeto.

```js
var height = 120;
var menu = {
  width: 800,
  height: 50,
  metadeHeight() {
    return this.height / 2;
  }
}

menu.metadeHeight(); // 25
// sem o this, seria 60
```
!!! info

    This irá retornar o próprio objeto

### Protótipo e Herença

O objeto herda propriedades e métodos do objeto que foi utilizado para criar o mesmo.

```js
var menu = {
  width: 800,
}

menu.hasOwnProperty('width') // true
menu.hasOwnProperty('height') // false
```
!!! info

    hasOwnProperty é um método de Object

### Tudo é objeto

Strings, Números, Boolean, Objetos e mais, possuem propriedades e métodos. Por isso são objetos.

```js
var nome = 'André';

nome.length; // 5
nome.charAt(1); // 'n'
nome.replace('ré', 'rei'); // 'Andrei'
nome; // 'André'
```
!!! info

    Uma string herda propriedades e métodos do construtor `#!javascript String()`

### Números

```js
var altura = 1.8;

altura.toString(); // '1.8'
altura.toFixed(); // '2'
```

!!! tip "Dica"

    Por um breve momento o número é envolvido em um Objeto (coerção), tendo acesso assim as suas propriedades e métodos

### Funções

```js
function areaQuadrado(lado) {
  return lado * lado;
}

areaQuadrado.toString();
//"function areaQuadrado(lado) {
//  return lado * lado;
//}"

areaQuadrado.length; // 1
```

### Elementos do DOM

```html
<a class="btn">Clique</a>
```

```js
var btn = document.querySelector('.btn');

btn.classList.add('azul') // adiciona a classe azul
btn.innerText; // 'Clique'
btn.addEventListener('click', function() {
  console.log('Clicou')
})
```
!!! info

    Praticamente todos os efeitos com JS são feitos utilizando propriedades e métodos de objetos do DOM.





