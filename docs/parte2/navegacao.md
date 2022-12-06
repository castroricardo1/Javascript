### Navegação por Tabs

# Adicionar Classe para Manipulação

A ideia de navegação por tabs, é ter uma lista de itens que controla a visualização de uma lista de conteúdo. Cada item da lista possui um conteúdo relacionado ao mesmo.

```html
<!-- Primeiro, adicionar classes que irão
facilitar a manipulação dos elementos -->
<ul class="animais-lista js-tabmenu">
  ...
</ul>
<div class="animais-descricao js-tabcontent">
  ...
</div>
```

### Selecionar os Itens

```js
const tabMenu = document.querySelectorAll('.js-tabmenu li');
const tabContent = document.querySelectorAll('.js-tabmenu section');
```

### Função Callback

Recebe index como parâmetro para ativar a tab. Sempre que ativar, remove a classe ativo de todos os outros elementos.

```js

function activeTab(index) {
  tabContent.forEach((content) => {
    content.classList.remove('ativo');
  });
  tabContent[index].classList.add('ativo');
}
```

### Adicionar Evento

```js
tabMenu.forEach((itemMenu, index) => {
  itemMenu.addEventListener('click', () => {
    activeTab(index);
  });
});
```

Adicionar a classe ativo ao primeiro elemento e adicionar a classe js ao html. Assim identificamos se o JavaScript está habilitado ou não.

```html
<!-- No head do borwser -->
<script>document.documentElement.className += ' js';</script>
```

```js
// Verificar se existe elemento em tabContent e tabMenu
if(tabContent.length && tabMenu.length) {
  tabContent[0].classList.add('ativo');
  ...
}
```

### Animação com CSS

Animação simples com css, sai de display none para display block.

```css
.js .js-tabcontent section {
  display: none;
}

.js-tabcontent section.ativo {
  display: block !important;
  animation: show .5s forwards;
}

@keyframes show {
  from {
    opacity: 0;
    transform: translate3d(-30px, 0, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0px, 0, 0);
  }
}
```
!!! info

    Lembre-se, o display none remove o texto até dos leitores de tela (acessibilidade)



