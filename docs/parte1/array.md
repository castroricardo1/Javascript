# Array e Loops

### Array

É um grupo de valores geralmente relacionados. Servem para guardarmos diferentes valores em uma única variável.

```js
var videoGames = ['Switch', 'PS4', 'XBox'];

videoGames[0] // Switch
videoGames[2] // Xbox
```
!!! info

    Acesse um elemento da array utilizando `[n]`

### Métodos e Propriedade de um Array

```js
var videoGames = ['Switch', 'PS4', 'XBox'];

videoGames.pop(); // Remove o último item e retorna ele
videoGames.push('3DS'); // Adiciona ao final da array
videoGames.length; // 3
```
!!! info

    Existem diversos outros métodos, como `#!javascript map`, `#!javascript reduce`, `#!javascript forEach` e mais que veremos mais à frente

### Loop For

Fazem algo repetidamente até que uma condição seja atingida.

```js
for (var numero = 0; numero < 10; numero++) {
  console.log(numero);
}
// Retorna de 0 a 9 no console
```
!!! info

    O for loop possui 3 partes, `início`, `condição` e `incremento`

### Loop While

```js
var i = 0;
while (i < 10) {
  console.log(i);
  i++;
}
// Retorna de 0 a 9 no console
```
!note 

    O loop for é o mais comum

### Arrays e Loops 

```js
var videoGames = ['Switch', 'PS4', 'XBox', '3DS'];
for (var i = 0; i < videoGames.length; i++) {
  console.log(videoGames[i]);
}
```

### Break

O loop irá parar caso encontro e palavra `break`

```js
var videoGames = ['Switch', 'PS4', 'XBox', '3DS'];
for (var i = 0; i < videoGames.length; i++) {
  console.log(videoGames[i]);
  if(videoGames[i] === 'PS4') {
    break;
  }
}
```

### For Each
forEach é um método que executa uma função para cada item do Array. É uma forma mais simples de utilizarmos um loop com arrays (ou array-like)


```js
var videoGames = ['Switch', 'PS4', 'XBox', '3DS'];
videoGames.forEach(function(item) {
  console.log(item);
});
// O argumento item será atribuído dinamicamente
```

!!! info 

    Podemos passar os seguintes parâmetros `item`, `index` e `array`







