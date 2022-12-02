# Números e Operadores

### Números

```js
var idade = 28;
var gols = 1000;
var pi = 3.14; // ponto para decimal
var exp = 2e10; // 20000000000
```

### Operadores Aritméticos

```js
var soma = 100 + 50; // 150
var subtracao = 100 - 50; // 50
var multiplicacao = 100 * 2; // 200
var divisao = 100 / 2; // 50
var expoente = 2 ** 4; // 16
var modulo = 14 % 5; // 4
```

!!! note "Lembrando"

    A símbolo de soma `#!javascript +` em strings serve para concatenar

### Operadores Aritméticos (Strings)

```js
var soma = '100' + 50; // 10050
var subtracao = '100' - 50; // 50
var multiplicacao = '100' * '2'; // 200
var divisao = 'Comprei 10' / 2; // NaN (Not a Number)
```
!!! tip "Dica"

    É possível verificar se uma variável é NaN ou não com a função `#!javascript isNan()`

### A ordem importa

Começa por multiplicação e divisão, depois por soma e subtração

```js
var total1 = 20 + 5 * 2; // 30
var total2 = (20 + 5) * 2; // 50
var total3 = 20 / 2 * 5; // 50
var total4 = 10 + 10 * 2 + 20 / 2; // 40
```
!!!note "Nota"

    Parênteses para priorizar uma expressão

### Operadores Aritméticos 

```js
var incremento = 5;
console.log(incremento++); // 5
console.log(incremento); // 6

var incremento2 = 5;
console.log(++incremento2); // 6
console.log(incremento2); // 6
```
!!! note "Nota"

    Mesma coisa para o decremento `#!javascript --x`

O `#!javascript +`e `#!javascript -` tenta transformar o valor seguinte em número

```js
var frase = 'Isso é um teste';
+frase; // NaN
-frase; // NaN

var idade = '28';
+idade; // 28 (número)
-idade; // -28 (número)
console.log(+idade + 5); // 33 

var possuiFaculdade = true;
console.log(+possuiFaculdade); // 1
```
!!! note "Nota"

    O `#!javascript -` antes de um número o torna negativo

[Guia completo de operadores](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_Operators)


