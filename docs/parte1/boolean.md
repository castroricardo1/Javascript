# Boolean e Condicionais

### Boolean

Existem dois valores booleanos `#!javascript false` ou `#!javascript true`

```js
var possuiGraduacao = true;
var possuiDoutorado = false;
```

### Condicionais If e Else

Verificar se uma expressão é verdadeira com `#!javascript if`, caso o contrário o `#!javascript else` será ativado.

```js
var possuiGraduacao = true;

if(possuiGraduacao) {
  console.log('Possui graduação');
} else {
  console.log('Não possui graduação');
}
// retorna Possui Graduação e não executa o else
```
!!! info "Informação"

    O valor dentro dos parênteses sempre será avaliado em `#!javascript false` ou `#!javascript true`.

### Condicional Else If

Se o `#!javascript if` não for verdadeiro, ele testa o `#!javascript else if`

```js
var possuiGraduacao = true;
var possuiDoutorado = false;

if(possuiDoutorado) {
  console.log('Possui graduação e doutorado');
} else if(possuiGraduacao) {
  console.log('Possui graduação, mas não possui doutorado');
} else {
  console.log('Não possui graduação');
}
// retorna Possui Graduação, mas não possui doutorado
```

### Switch

Com o `#!javascript switch` você pode verificar se uma variável é igual à diferentes valores utilizando o `#!javascript case`. Caso ela seja igual, você pode fazer alguma coisa e utilizar a palavra chave `#!javascript break` para cancelar a continuação. O valor de dafult ocorrerá caso nenhuma das anteriores seja verdadeira.

```js
var corFavorita = 'Azul';

switch (corFavorita) {
  case 'Azul':
    console.log('Olhe para o céu.');
    break;
  case 'Vermelho':
    console.log('Olhe para rosas.');
    break;
  case 'Amarelo':
    console.log('Olhe para o sol.');
    break;
  default:
    console.log('Feche os olhos');
}
```

### Truthy e Falsy

Existem valores que retornam `#!javascript true` e outros que retornam `#!javascript false` quando verificados em uma expressão booleana.

```js
// Falsy
if(false)
if(0) // ou -0
if(NaN)
if(null)
if(undefined)
if('') // ou "" ou ``
``` 
!!! info 

    Todo o resto é truthy

### Truthy

```js
// Truthy
if(true)
if(1)
if(' ')
if('andre')
if(-5)
if({})
```

### Operador Lógico de Negação (!)

O operador `#!javascript !` nega uma operação booleana. Ou seja, `#!javascript !true` é a igual a `#!javascript false` 

```js
// Truthy
if(!true) // false
if(!1) // false
if(!'') // true
if(!undefined) // true
if(!!' ') // true
if(!!'') // false
```
!!! tip "Dica"

    Pode utilizar o `#!javascript !!` para verificar se uma expressão é Truthy ou Falsy

### Operadores de Comparaçao

Vão sempre retornar um valor booleano

```js
10 > 5; // true
5 > 10; // false
20 < 10; // false
10 <= 10 // true
10 >= 11 // false
```

### Operadores de Comparaçao

O `#!javascript ==` faz uma comparação não tão estrita e o `#!javascript ===` faz uma comparação estrita, ou seja, o tipo de dado deve ser o mesmo quando usamos `#!javascript ===`

```js
10 == '10'; // true
10 == 10; // true
10 === '10'; // false
10 === 10 // true
10 != 15 // true
10 != '10' // false
10 !== '10' // true
```

### Operadores Lógicos &&

`#!javascript &&` Compara se uma expressão `#!javascript e` outra é verdadeira

```js
true && true; // true
true && false; // false
false && true; // false
'Gato' && 'Cão'; // 'Cão'
(5 - 5) && (5 + 5); // 0
'Gato' && false; // false
(5 >= 5) && (3 < 6); // true
```

!!! info 

    Se ambos os valores forem true ele irá retornar o último valor verificado se algum valor for false ele irá retornar o mesmo e não irá continuar a verificar o próximo

### Operadores Lógicos ||

`#!javascript ||` Compara se uma expressão `ou` outra é verdadeira
```js
true || true; // true
true || false; // true
false || true; // true
'Gato' || 'Cão'; // 'Gato'
(5 - 5) || (5 + 5); // 10
'Gato' || false; // Gato
(5 >= 5) || (3 < 6); // true
```
!!! info 

    Retorna o primeiro valor true que encontrar