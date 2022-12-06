#forEach e Arrow Function

### forEach

Constantemente vamos selecionar uma lista de itens do dom. A melhor forma para interagirmos com os mesmos é utilizando o método forEach.

```js
const imgs = document.querySelectorAll('img');

imgs.forEach(function(item){
  console.log(item);
});
```

### Parâmetros do forEach

O primeiro parâmetro é o callback, ou seja, a função que será ativada a cada item. Esse função pode receber três parâmetros: valorAtual, index e array;

```js
const imgs = document.querySelectorAll('img');

imgs.forEach(function(valorAtual, index, array){
  console.log(item); // o item atual no loop
  console.log(index); // o número do index
  console.log(array); // a Array completa
});
```

### forEach e Array

forEach é um método de Array, alguns objetos array-like possuem este método. Caso não possua, o ideal é transformá-los em uma array.

```js
const titulos = document.getElementsByClassName('titulo');
const titulosArray = Array.from(titulos);

titulosArray.forEach(function(item){
  console.log(item);
});
```

### Arrow Function

Sintaxe curta em relação a `function expression`. Basta remover a palavra chave function e adicionar a fat arrow `=>` após os argumentos.

```js
const imgs = document.querySelectorAll('img');

imgs.forEach((item) => {
  console.log(item);
});
```

### Parâmetros e Parênteses

```js
const imgs = document.querySelectorAll('img');

// parâmetro único não precisa de parênteses
imgs.forEach(item => {
  console.log(item);
});

// multiplos parâmetros precisam de parênteses
imgs.forEach((item, index) => {
  console.log(item, index);
});

// sem parâmetro precisa dos parênteses, mesmo vazio
let i = 0;
imgs.forEach(() => {
  console.log(i++);
});
```

### Return 

É possível omitir as chaves ` {} ` para uma função que retorna uma linha.

```js
const imgs = document.querySelectorAll('img');

imgs.forEach(item => 
  console.log(item)
);

imgs.forEach(item => console.log(item));
```

!!! warning

    Não é permitido fechar a linha com ` ; `

    



