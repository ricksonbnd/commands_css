# RESUMO CSS

O CSS não é uma linguagem de programação, é uma linguagem de estilo que pode adicionar várias caracteristicas a linguagem de html, criar animações e dar identidade visual desejada a uma página.

O [codepen.io](https://codepen.io) codepen.io é um site onde podemos estudar, buscar códigos interessantes adiquirir inspirações sobre CSS.

## TIPOS DE CSS

**CSS INLINE** é quando trabalhamos no código CSS utilizando o atributo style dentro das tags HTML dentro de cada elemento. É util para modificar elementos especificos. O css inline tem prioridade a outros tipos de `style`s.

**CSS INTERNO** é quando o`<style>` está dentro da tag `head`. **Exemplo:** `<style> h1 {background: blue; color: white;}</style>` Assim todos elementos dentro da tags `<h1>` teram as propriedades, atributos e valores definidos por esse style.

**CSS EXTERNO** é criado um arquivo com extesão .css com todos as propriedade e atributos desejados para abrir num arquivo html referenciando através da tag `<link>`

Por conveção os **CSS EXTERNOS** são colocados dentro dos diretorios /assets/css.

### PROPRIEDAS E VALORES

A propriedade é uma caracteristica de um elemento HTML.

O valor é o que define o resultado junto com a propriedade seja exibina no navegador?

Uma propriedade termina com `:` com espera de um valor.
Um valor vem após uma propriedade e termina `;`. Como exemplo temos: `background: red;`

### CSS COMMANDS

`<link>` serve para definir um arquivo externo. Sendo útil para linkar um arquivo .css com o HTML.

### PROPRIEDADES

`background:` define uma cor para o fundo de um elemento.
`color:` define uma cor para fonte de um elemento.

### ATRIBUTOS

`rel=""` atributo do `<link>` para definir tipo de link.
