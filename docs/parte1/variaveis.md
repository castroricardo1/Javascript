# Variáveis

Reponsável por guardar dados na memória

!!! note "Tipos de variáveis"

    Inicia com a palavra `#!javascript var`, `#!javascript let` ou `#!javascript const`.

* var: Não se utiliza mais hoje em dia
* let: Declarar variáveis com escopo de bloco
* Const: Declarar variáveis com const mantêm seus valores

``` js
var nome = 'André';
let idade = 28;
const possuiFaculdade = true;
```

### Sintaxe
Palavra chave `#!javascript var`, `#!javascript let` ou `#!javascript const`, sinal de igual e o valor

!!! example "Exemplo"
  
    ``` js
    var nome = 'André';
    ```



### Evitar repetições

``` js
var preco = 20;
var totalComprado = 5;
var precoTotal = preco * totalComprado;
```

Para evitar a repetição como no caso acima, podemos separar as variáveis por vírgula

```js
var nome = 'André',
    idade = 28,
    possuiFaculdade = true;
```

Podemos declarar a variável e não atribuir o valor inicialmente

``` js
var precoAplicativo;
// retorna undefined
```

### Nome

* Os nomes podem iniciar com $, _ , ou letras.
  
    * *Podem conter números mas não iniciar com eles*

* Case Sensitive
  
    * *nome é diferente de Nome*  

* Não utilizar palavras reservadas

    * [https://www.w3schools.com/js/js_reserved.asp](https://www.w3schools.com/js/js_reserved.asp)

* Camel Case

    * É comum nomearmos assim: abrirModal


### Nome

``` js
// Inválido
var §nome;
var function;
var 1possuiFaculdade;

// Válido
var $selecionar;
var _nome;
var possuiFaculdadeNoExterior;
```

### Declarar

!!! failure "Erro ao tentar utilizar uma variável que não foi declarada"

    ``` js
    console.log(nome);
    // retorna nome is not defined
    ```

### Hoisting 

São movidas para cima do código, porém o valor atribuído não é movido

```js
console.log(nome);
var nome = 'André';
// Retorna undefined

var profissao = 'Designer';
console.log(profissao);
// Retornar Designer
```

### Mudar o valor atribuído

É possível mudar os valores atribuídos a variáveis declaradas com `#!javascript var` e `#!javascript let`. Porém não é possível modificar valores declarados com `#!javascript const`.

```js
var idade = 28;
idade = 29;

let preco = 50;
preco = 25;

const possuiFaculdade = true;
possuiFaculdade = false;
// Retorna um erro
```

### 7 Tipos de Dados

Todos são primitivos exceto os objetos.

```js
var nome = 'André'; // String
var idade = 28; // Number
var possuiFaculdade = true; // Boolean
var time; // Undefined
var comida = null; // Null
var simbolo = Symbol() // Symbol
var novoObjeto = {} // Object
```

!!! note "Nota"

    Primitivos são dados imutáveis

### Veriicar tipo de dado (typeof)

```js
var nome = 'André';
console.log(typeof nome);
// retorna string
```

!!! note "Nota"

    `#!javascript typeof null` retorna object

### String

Você pode somar uma string e assim concatenar as palavras

```js
var nome = 'André';
var sobrenome = 'Rafael';
var nomeCompleto = nome + ' ' + sobrenome;
```

Você pode somar números com strings, o resultado é sempre uma **string**

```js
var gols = 1000;
var frase = 'Romário fez ' + gols + ' gols';
```

### Aspas Duplas, Simples e Template Strig

```js
'JavaScript é "super" fácil';
"JavaScript é 'super' fácil";
"JavaScript é \"super\" fácil";
`JavaScript é "super" fácil"`;
"JavaScript é "super" fácil"; // Inválido
```

!!! tip "Dica"

    Não necessariamente precisamos atribuir valores a uma variável

### Template String

```js
var gols = 1000;
var frase1 = 'Romário fez ' + gols + ' gols';
var frase2 = `Romário fez ${gols} gols`; // Utilizando Template String
```

!!! info 

    Você deve passar expressões / variáveis dentro de `#!javascript ${}`
