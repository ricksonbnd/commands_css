# RESUMO CSS

O CSS não é uma linguagem de programação, é uma linguagem de estilo que pode adicionar várias caracteristicas a linguagem de html, criar animações e dar identidade visual desejada a uma página.

O [codepen.io](https://codepen.io) codepen.io é um site onde podemos estudar, buscar códigos interessantes adiquirir inspirações sobre CSS.

## TIPOS DE CSS

**CSS INLINE** é quando trabalhamos no código CSS utilizando o atributo style dentro das tags HTML dentro de cada elemento. É util para modificar elementos especificos. O css inline tem prioridade a outros tipos de `style`s.

**CSS INTERNO** é quando o`<style>` está dentro da tag `head`. **Exemplo:** `<style> h1 {background: blue; color: white;}</style>` Assim todos elementos dentro da tags `<h1>` teram as propriedades, atributos e valores definidos por esse style.

**CSS EXTERNO** é criado um arquivo com extesão .css com todos as propriedade e atributos desejados para abrir num arquivo html referenciando através da tag `<link>`

Por conveção os **CSS EXTERNOS** são colocados dentro dos diretorios /assets/css.

### SELETORES

Os seletores devem estar dentro da tag `<style>`.

Lista por ordem de **PRIORIDADE** (depende também da ordem escrita dentro de `<style>`)

1. **Seletor por ID** busca pelo ID "único" de um elemento. Exemplo: `#idName {background: blue; color: white;}`, assim todos elementos com `id="texto-de-boas-vindas"` iram responder a esse seletor.
1. **Seletor por Atributo** iram responder apenas os elemetos que tiverem o atributo em questão. Exemplo: `[atributoName] {background: blue; color: white;}` irá mudar todos elementos que tiverem `atributoName` como atributo. Também é possivel buscar um atributo com o valor definido como por exemplo: [atributoName="valorName"] {background: blue; color: white;}
1. **Seletor por Classe** busca elementos pela classe seleciona, diferente do **seletor por ID**, responde a vários elementos dentro de um documento html. Os elementos podem ter mais de uma classe. Exemplo: `.className {background: blue; color: white;}`
1. **Seletor de tags** busca elementos por uma tag html. Exemplo: `div {background: blue; color: white;}`, assim todos elementos `<div>` iram responder a esse seletor.
1. **Seletor por Universal** serve para mudar TODO o documento html, o refencial é o `*` Exemplo: `* {background: blue; color: white;}`

### COMBINADORES

Tendo mente da esquerda para direita: Pai > filho > neto ...

1. **Combinador de descendencia *(espaço)*** serve para selecionar os filhos de um seletor, por exemplo podemos selecionar apenas uma lista especifica dentro de outras lista. Exemplo `li li {background: blue; color: white;}`. funciona da mesma maneira para outros seletores como: `.atributoName li {background: blue; color: white;}` que seleciona apenas a lista dentro dos atributos `atributoName`.
1. **Combinador filho *(>)*** serve para selecionar **FILHOS DIRETOS** de um seletor. Exemplo `.atributoName > li {background: blue; color: white;}` assim iram mudar os elementos da `li` que são filhos diretos do `.atributoName`.
1. **Combinador irmão adjacente *(+)*** seleciona o **PRIMEIRO IRMÃO DIRETO** adjacente ao pai. Exemplo `.atributoName + li {background: blue; color: white;}` assim seleciona a primeira lista (li) ao lado do elemento `atributoName`. Vale lembrar que desconcidera netos e demais decendetes. Podemos visualizar também tendo o mesmo nível de indentação do `atributoName`.
1. **Combinador irmão em geral *(+)*** seleciona o **~TODOS OS IRMÃO DIRETOS** adjacente ao pai. Exemplo `.atributoName + li {background: blue; color: white;}` assim seleciona todas as lista (li) ao lado do elemento `atributoName`.

### PROPRIEDAS E VALORES

A propriedade é uma caracteristica de um elemento HTML.

O valor é o que define o resultado junto com a propriedade seja exibina no navegador?

Uma propriedade termina com `:` com espera de um valor.
Um valor vem após uma propriedade e termina `;`. Como exemplo temos: `background: red;`

### PROPRIEDADES

1. `background:` define uma cor para o fundo de um elemento.
1. `color:` define uma cor para fonte de um elemento.
1. `width` largura, precisa da unidade de medida(px, %, etc).
    1. `min-width` a largura é definida pelo tamanho do contéudo, até o **minimo** de largura atribuida.
    1. `max-width` a largura é definida pelo tamanho do contéudo, até o **máximo** de largura atribuida.
1. `height` altura, precisa da unidade de medida(px, %, etc).
    1. `min-width` a altura é definida pelo tamanho do contéudo, até o **minimo** de altura atribuida.
    1. `max-heigth` a altura é definida pelo tamanho do contéudo, até o **máximo** de altura atribuida.
1. `margin` é usada para criar um espaçamento em volta das bordas do nosso elemento. Pode usar apenas um valor para definir o espaçamento para todos os lados. Ou definir 4 valores cada área em sentido hórario. Exemplo: `margin: 10px 20px 30px 40px`
    1. `margin-top` é usado para criar uma margem na parte superior do elemento, precisa da unidade de medida. Ex: `margin: 10px`
    1. `margin-right` é usado para criar uma margem na parte direita do elemento, precisa da unidade de medida. Ex: `margin: 20px`
    1. `margin-bottom` é usado para criar uma margem na parte inferior do elemento, precisa da unidade de medida. Ex: `margin: 30px`
    1. `margin-left` é usado para criar uma margem na parte esquerda do elemento, precisa da unidade de medida. Ex: `margin: 40px`
    1. `margin: auto` é usado para centralizar o elemento na página.
1. `padding` faz um espaçamento na parte interior do objeto com o contéudo. Possui a mesma analogia da propriedade `margin` como `padding-top, padding-left`, etc.

### ATRIBUTOS

1. `rel=""` atributo do `<link>` para definir tipo de link.

#### CORES

Cores prédefinidas

   1. `color: corName;` defina uma cor com o nome de cores prédefinidas (black, white, red, etc).
   1. `color: rgb(redValue,greenValue,blueValue)` define a cor conforme os valores de `red`,`green` e `blue`de `0 a 255`. Exemplo para cor vermelha: `color: rgb(255,0,0)`. Pode-se usar os valores como `%`.
   1. `color: rgba(redValue,greenValue,blueValue,alphaValue)` define cor rgb com adicição do alpha (transparencia). Alpha varia de `0 a 1`.
   1. `color: #000000` onde os 2 primeiros digitos são referentes a valores para `red`,  os intermediarios para `green` e os dois ultimos para `blue`.
   1. `color: hsl(hueValue,saturationValue,lightnessValue)` define com `hueValue de 0 a 360`. `saturationValue e lightnessValue` pode ser usado em %.

### OBJECT

#### OBJECT-FIT

Serve para definir como uma imagem se comporta num container, por padrão o valor de `object-fit` padrão é `fill`.

1. `object-fit: fill` redimensiona a imagem para conter **TODO** espaço do conteiner. Pode distorcer a imagem.
1. `object-fill: contain` redimensiona para a imagem couber dentro do conteiner sem cortar nenhuma parte e distorcer a imagem. Pode sobrar espaço do conteiner vazio.
1. `object-fill: cover` redimensiona a imagem para utilizar **TODO** espaço do container, mas **SEM** distorcer a imagem.
1. `object-fill: none` não redimensiona a imagem, utiliza a resolução padrão converme couber no conteiner. Pode sobrar espaço ou faltar partes da imagem.
1. `object-fill: scale-down` seleciona entre as configurações `contain` e `nome` que prejudique **MENOS** a imagem.

#### OBJECT-POSITION

Serve para definir as posição de um objeto(imagem) dentro de um container.
`object-position: horizontalValue, verticalValue;` determina as cordenadas para X e Y, necessita de uma unidade de medina nos valores. Exemplo: `object-position: 50px, 50px;` define a visualização centralizado dos 50, 50 da imagem. `object-position: left, top;` Define a visualização principal da esquerda superior da imagem.

### BACKGROUND

`background: url(image) /position/size/repeat/attachment/origin/clip/color;`

Exemple:

    background: url(https://imageseila.png) top center / 200px 200px no-repeat fixed padding-box content-box red;

#### BACKGROUND-IMAGE

Serve para definnir ou alterar fundo dos elementos. Para templats acesse: [porjects.verou.me/css3patterns/](porjects.verou.me/css3patterns/).

Exemplos:

1. `background-image: url(localImage);`
1. `background-image: linear-gradient (color1,color2);`
1. `background-image: radial-gradient (color1,color2);`

#### BACKGROUND-SIZE

1. `background-size: auto;` a imagem se ajusta automaticamente no elemento.
1. `background-size: cover;` a imagem se ajusta para ocupar todo fundo do elemento. Pode perder qualidade.
1. `background-size: contain;` a imagem se ajusta para todo contéudo da imagem esteje no elemento, mesmo que sobre espaço vazios no elemento.
1. `background-size: tamanhoValue;` pode definir um tamanho ou uma % para imagem, pode gerar repetições.

#### BACKGROUND-REPEAT

`background-repeat: repeat;` define repetições de imagem em espaços vazios nos elementos.
`background-repeat: repeat-x;` define repetições de imagem em espaços vazios nos elementos no eixo X.
`background-repeat: repeat-y;` define repetições de imagem em espaços vazios nos elementos no eixo Y.

#### BACKGROUND-ATTACHMENT

Define o comportamento das imagens de fundo com o scrolls do mouse.

`background-attachment: fixed;` o contéudo é fixo dentro do elemento, mas a imagem é movel com a página.
`background-attachment: scroll;` a imagem  é fixa e o contéudo é movél com a rolagem da página.
`background-attachment: local;` a imagem e o contéudo é movel com a rolagem da página.

#### BACKGROUND-POSITION

`background-position: horizontalValue, verticalValue;` posiciona uma imagem no elemento.

#### BACKGROUND-ORIGIN

Define o ponto de origem de uma imagem. `padding-box` é valor padrão da propriedade.

`background-origin: padding-box;` valor padrão da propriedade. Define o ponto de origem no canto superior esquerdo do espaçamento interno. Cobre a área q o padding ocupa.
`background-origin: border-box;` Define o ponto de origem no canto superior esquerdo do contéudo externo. Ocupa a área da borda.
`background-origin: content-box;` Define o ponto de origem no canto superior esquerdo do contéudo interno. Não ocupa a área do padding.

#### BACKGROUND-CLIP

Define se como o fundo preenche a área do elemento.

`background-clip: text;` preenche apenas a área de texto, o texto precisa ser definido como `color: transparent;`. Necessita `webkit-background-clip: text;` para o chrome interpretar o efeito.
`background-clip: padding-box;` valor padrão da propriedade. Define como preenchimento a área de padding mas não a área de bordas.
`background-clip: border-box;`  Define como preenchimento até a área das bordas do contéudo interno do elemento.
`background-clip: content-box;` Define como preenchimento somente o contéudo interno do elemento. Não opreenche a área do padding.

#### BACKGROUND-MERGEMODDE

Define como imagem e cor de fundo dos elementos misturam entre si.

1. `background-blend-mode: hard-light`
1. `background-blend-mode: soft-light`
1. `background-blend-mode: luminosity`
1. `background-blend-mode: overlay`
1. etc

São efeitos gráficos que alteram a cor.

### VALORES

Entende-se como valores reservadas:

1. `auto` define valores automaticos o elemento conter os contéudos dentro.
1. `initial` define como o valor padrão inicial.
1. `inherit` define como valor o valor herdado do pai do elemento.
1. `top` define como valor area superior.
1. `botton` define como valor area inferior.
1. `left` define como valor area esquerda.
1. `right` define como valor area direita.

### CSS COMMANDS

`<link>` serve para definir um arquivo externo. Sendo útil para linkar um arquivo .css com o HTML.
