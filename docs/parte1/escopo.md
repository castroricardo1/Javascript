# Escopo

### Escopo de Função

Variáveis declaradas dentro de funções não são acessadas fora das mesmas.

```js
function mostrarCarro() {
  var carro = 'Fusca';
  console.log(carro);
}

mostrarCarro(); // Fusca no console
console.log(carro); // Erro, carro is not defined
```
!!! info

    Escopo evita o conflito entre nomes.

### Variável Global (Erro)

Declarar variáveis sem a palavra chave `#!Javascript var`, `#!Javascript const` ou `#!Javascript let`, cria uma variável que pode ser acessar em qualquer escopo (global). Isso é um erro.

```js
function mostrarCarro() {
  carro = 'Fusca';
  console.log(carro);
}

mostrarCarro(); // Fusca
console.log(carro); // Fusca
```
!!! tip "Dica"

    `#!javascript use strict` impede isso.

### Escopo da Função (Pai)

Variáveis declaradas no escopo pai da função, conseguem ser acessadas pelas funções.

```js
var carro = 'Fusca';

function mostrarCarro() {
  var frase = `Meu carro é um ${carro}`;
  console.log(frase);
}

mostrarCarro(); // Meu carro é um Fusca
console.log(carro);  // Fusca
```

### Escopo de Bloco 

Variáveis criadas com `#!javascript var`, vazam o bloco. Por isso com a introdução do ES6 a melhor forma de declarmos uma variável é utilizando `#!javascript const` e `#!javascript let`, pois estas respeitam o escopo de bloco.

```js
if(true) {
  var carro = 'Fusca';
  console.log(carro);
}
console.log(carro); // Carro
```

### Var Vaza Bloco

Mesmo com a condição falsa, a variável ainda será declarada utilizando hoisting e o valor ficará como undefined.

```js
if(false) {
  var carro = 'Fusca';
  console.log(carro);
}
console.log(carro); // undefined
```

### Const e Let no Lugar de Var

A partir de agora vamos utilizar apenas `#!javascript const` e `#!javascript let` para declarmos variáveis.

```js
if(true) {
  const carro = 'Fusca';
  console.log(carro);
}
console.log(carro); // erro, carro is not defined
```

### { } Cria um Bloco

Chaves `{ }` criam um escopo de bloco, não confundir com a criação de objetos `= { }`

```js
{
  var carro = 'Fusca';
  const ano = 2018;
}
console.log(carro); // Carro
console.log(ano); // erro ano is not defined
```

### For Loop

Ao utilizar `#!javascript var` dentro de um `#!javascript for` loop, que é um bloco, o valor do variável utilizada irá `vazar` e existir fora do loop.

```js
for(var i = 0; i < 10; i++) {
  console.log(`Número ${i}`);
}
console.log(i); // 10
```

### For Loop com Let

Com o `#!javascript let` evitamos que o número vaze.

```js
for(let i = 0; i < 10; i++) {
  console.log(`Número ${i}`);
}
console.log(i); // i is not defined
```

### Const

Mantém o escopo no bloco, impede a redeclaração e impede a modificação do valor da variável, evitando bugs no código.

```js
const mes = 'Dezembro';
mes = 'Janeiro'; // erro, tentou modificar o valor
const semana; // erro, declarou sem valor

const data = {
  dia: 28,
  mes: 'Dezembro',
  ano: 2018,
}

data.dia = 29; // Funciona
data = 'Janeiro'; // erro
```

!!! info

    Variáveis com valores constantes devem utilizar o `#!javascript const`.

### Let

Mantém o escopo no bloco, impede a redeclaração, mas permite a modificação do valor da variável.
```js
let ano;
ano = 2018;
ano++;
console.log(ano); // 2019

let ano = 2020; // erro, redeclarou a variável
```
!!! tip "dica"

    Geralmente utilizamos o `#!javascript const`.















