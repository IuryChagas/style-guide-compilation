<h1 align="center">
  Guia Basico de Estilo HTML e CSS
</h1>

Das pesquisas por convensões de padronização e organização de código surgiu a necessidade de documentar as preferências de escrita adotada por renomados e quase anonimos desenvolvedores ao redor da web. 

Este guia é bem simples e não tendo a pretenção de ser obrigatório, é apenas uma recomendação para desenvolver HTML e CSS da melhor maneira possível visando manter em todo o projeto um estilo único e consistente.

:octocat: Contribua, suas ideias e sugestões são bem-vindas.

## Tópicos:

1. **[HTML](#html)**
1. **[CSS](#css)**
1. **[Conclusão](#end)**

<a name="html"></a>
## 1. Formatação e Estilo no HTML

1. [DOCTYPE](#doctype)
1. [Capitalização](#capslock)
1. [Lang](#lang)
1. [UTF-8 encoding](#encoding)
1. [Indentação e Hierarquia](#indentation)
1. [Espaços Vazios](#whitespaces)
1. [Organizando os Atributos no HTML](#attributes)
1. [Aspas Duplas em Atribuições](#doublequotes)
1. [Tags de Auto-Fechamento](#void-elements)
1. [Viewport em Ação](#viewport)
1. [Protocolo HTTPS://](#https)
1. [Estrutura de Diretórios](#directory-structure)
___

O uso de uma formatação concisa torna mais fácil a leitura do seu HTML e possibilita que qualquer outro desenvolvedor se concentre no que você está dizendo e não em como você está dizendo.

<a name="doctype"></a>
#### 1.1```<!DOCTYPE html>``` como estrutura global

```!DOCTYPE``` é uma instrução para os browsers sobre a versão do html,
portanto essa declaração deve ser a primeira informação em seu html.

```html
<!doctype html>
<html>
  ...
</html>
```
<a name="capslock"></a>
#### 1.2 Capitalização - CAIXA ALTA e/ou caixa baixa?

Embora o HTML5 permite misturar letras MAIÚSCULAS e minúsculas, use somente "lowercase"

☑ *Código mais limpo*<br>
☑ *Facil digitar*<br>
☑ *Sem distrações na leitura*

```html
<!-- recomendado -->
<article class="article">
 <p>...</p>
</article>
```
```html
<!-- não recomendado -->
<ARTICLE Class="article">
  <p>...</p>
</article>
```
<a name="lang"></a>
#### 1.3 Use ```lang=" "``` para Especificar o Idioma:

Ao atribuir o idioma padrão do documento, você auxilia softwares de voz determinar quais pronuncias usar e a softwares de tradução quais regras utilizar.

```html
<!-- recomendado -->
<html lang="pt-br">
<head>
  ...
</head>
```
```html
<!-- não recomendado -->
<html>
<head>
  ...
</head>
```
<a name="encoding"></a>

#### 1.4 ```UTF-8``` Codificação de Caracteres:

Você deve garantir a renderização adequada do seu html e ao especificar a codificação utilizada, você evita que os caracteres do seu conteúdo sejam interpretados incorretamente. Com isso você garante legibilidade para humanos e maquinas, pois cadas vez mais softwares necessitam processar seus dados.

```html
<!-- recomendado -->
<head>
  <meta charset="utf-8">
   ...
</head>
```
```html
<!-- não recomendado -->
<head>
  <meta>
   ...
</head>
```
<a name="indentation"></a>
#### 1.5 Indentação de hierarquia:

Use soft-tabs com dois espaços.

```html
<!-- recomendado -->
<nav class="navbar">
  <ul class="nav">
    <li class="nav-item">
      <a class="nav-link">
```
```html
<!-- não recomendado -->
<nav class="navbar">
      <ul class="nav">
            <li class="nav-item">
                  <a class="nav-link">
```
_Para padronizar isso em qualquer editor/IDE, use o [editorconfig](http://editorconfig.org/)_

<a name="whitespaces"></a>
#### 1.6 Espaços Vazios:

Para manter seu código limpo e não sujar diffs no git, Remova todos os espaços desnecessários, principalmente os da direita.

```html
<!-- recomendado -->
<p>Lorem ipsum dolor sit amet, ...</p>
```
```html
<!-- não recomendado -->
<p>_ Lorem ipsum dolor sit amet, ...</p>_
```
<a name="attributes"></a>
#### 1.7 Organizando os Atributos no html:

Não há uma regra absoluta, apenas uma hierarquia para facilitar a leitura e manutenção.

1. `class`
1. `id`, `name`
1. `data-*`
1. `src`, `for`, `type`, `href`
1. `title`, `alt`
1. `aria-*`, `role`

```html
  <!-- Precisamos de exemplos... e essa é a hora de você contribuir! -->
  <!-- Seguindo a organização descrita acima, Crie um código ficticio ou -->
  <!-- /compartilhe um já existente que contenha a maioria destes atributos -->
```
<a name="doublequotes"></a>
#### 1.8 Aspas Duplas nos Atributos:

Sempre use "double quotes" ao inserir atributos em seu html.

```html
<!-- recomendado -->
<article class="article">
  <h1 class="main-title">...</h1>
</article>
```
```html
<!-- não recomendado -->
<article class='article'>
  <h1 class='main-title'>...</h1>
</article>
```
<a name="void-elements"></a>
#### 1.9 Tags de Auto-fechamento:

Recomenda-se não utilizar barra de fechamento ```/``` em elementos vazios.

Veja a lista de todas as tags de auto-fechamento.

```html
 1. <area>
 2. <base>
 3. <br>
 4. <col>
 5. <command>
 6. <embed>
 7. <hr>
 8. <img>
 9. <input>
10. <keygen>
11. <link>
12. <meta>
13. <param>
14. <source>
15. <track>
16. <wbr>
```
<a name="viewport"></a>
#### 1.10 Configure a área visível ao usuário (viewport)

A função da viewport é definir qual a área visível de uma página web. Essa área varia/se adapta de acordo com dispositivo.
Você deve incluir em todas as suas páginas web e certamente os usuários de smatphones agradecem:

```html
<!-- recomendado -->
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  ...
</head>
```
- com `viewport` [exemplo recomendado](https://www.w3schools.com/css/img_viewport2.png)

```html
<!-- não recomendado -->
<head>
  <meta charset="utf-8">
  ...
</head>
```
- sem `viewport` [exemplo não recomendado](https://www.w3schools.com/css/img_viewport1.png)

<a name="https"></a>
#### 1.11 HTTPS protocol

Proporcione aos usuários mais segurança, Use sempre que possível o protocolo `HTTPS` ao inserir links externos.

```html
  <!-- recomendado -->
  <link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">
  ...
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js" ></script>
```
```html
  <!-- não recomendado -->
  <link href="http://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">
  ...
  <script src="//ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js" ></script>
```
<a name="directory-structure"></a>
#### 1.12 Estrutura de Diretórios

Embora a estrutura de diretórios dependa exclusivamente do tipo de projeto, segue uma estrutura basica:

- _3 Diretórios:_ |`:css`| |`:img`| |`:js`|
- _5 Arquivos:_ `.html`
- _1 Arquivo:_ `.css`
- _3 Arquivos:_ `imgs`
- _2 Arquivos:_ `.js`

```html
.
├── index.html
├──:css
|  └── main.css
├──:img
|  ├── favicon.ico
│  ├── imagen.png
│  └── imagem.jpg
├──:js
│  ├── main.js
│  └── scripts.js
├── blog.html
├── projetos.html
├── sobre.html
└── contato.html
```
Depois de quase tudo explicado nos minimos detalhes, segue um resumo final:

```html
<!doctype html>
<html lang="pt-br">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="shortcut icon" href="img/favicon.ico">
  <link rel="stylesheet" href="css/main.css">
  <title>...</title>
</head>
<body>
  <main>
    ...
  </main>
  <script src="js/script.js"></script>
</body>
</html>
```
**[⬆ voltar ao topo](#--guia-basico-de-estilo-html-e-css)**

<a name="css"></a>
## 2. Formatação e Estilo no CSS

#### 2.1 [Como Nomear Seletores](#class-name-style)

  - [Classes Semânticas](#readable-classes)
  - [Hífens](#hyphens)
  - [Lowercase](#lowercase)
  - [Não use IDs, use Classes](#ids-classes)
  - [Seleção por aninhamento](#nesting-selection)

#### 2.2 [Como Montar uma Declaração](#declaration)

  - [Espaço ao abrir `{` e apos `:`](#add-space)
  - [Incluir `;` e alinhar fechamento `}`](#semicolon-closekey)
  - [Configurar soft-tabs para 2 espaços](#soft-tabs)
  - [Usando aspas duplas `""`](#doublequotes-css)
  - [Shortheand em propriedades](#shortheand)
  - [Abreviações em valores](#unit-reset)
  - [Seletores com as mesmas declarações](#declaration-single-line)
  - [Indentação no uso de prefixos](#prefixes-indentation)
  - [Valores muito extensos separados por `,`](#extensive-values)
  - [Ordens de declarção:](#declaration-order)
    - [Ordem Relacional](#relational-order)
    - [Alfabética](#alphabetical-order)

#### 2.3 [Como Organizar Blocos Declarativos](#organize-declarative-blocks)

  - [Manter uma propriedade/valor por linha](#property-per-line)
  - [Um espaço entre cada bloco declarativo](#space-between-blocks)
  - [Declarações com apenas uma propriedade/valor](#single-value-selectors)
  - [`@Media Queries` onde as queremos](#media-queries)

> O formato de código escolhido deve garantir que o código seja: fácil ler, fácil comentar, minimizar as chances de introduizir erros, e resultar em `diffs` e `blames` úteis.
~ Nicolas Gallagher

<a name="class-name-style"></a>
#### 2.1 Como Nomear Seletores

Nomear com base no que é, em vez de como se parece ou se comporta é o fundamento de um CSS bem arquitetado e manutenível.

<a name="readable-classes"></a>
Use nomes legiveis e que faça referência direta com o propósito/finalidade do elemento.

```css
/* recomendado */
  .class-name-example {
    ...
  }
```
```css
/* não recomendado */
  .Cname_exe {
    ...
  }
```
<a name="hyphens"></a>
Use "traço" hífen `-` ao inves de undeline `_`

```css
/* recomendado */
  .main-header {
    ...
  }
```
```css
/* não recomendado */
  .main_header {
    ...
  }
```
<a name="lowercase"></a>
lowercase, todo o código sempre em caixa baixa

```css
/* recomendado */
  .thumbnail {
    ...
  }
```
```css
/* não recomendado */
  .THUMBNAIL {
    ...
  }
 /* ou */
  .ThumbNail {
    ...
  }
```
<a name="ids-classes"></a>
Não use ids, use classes

```css
/* recomendado */
  .footer {
    ...
  }

  .aside {
    ...
  }
```
```css
/* não recomendado */
  #footer {
    ...
  }

  #aside {
    ...
  }
```
<a name="nesting-selection"></a>
Por motivos de performance, evite selecionar como base pela hierarquia, use com classe :v.
```css
/* recomendado */
  .navbar { ... }
  .nav { ... }
  .nav-item { ... }
  .nav-link { ... }
```
```css
/* não recomendado */
  .navbar ul { ... }
  .navbar ul li { ... }
  .navbar ul li a { ... }
```
*Thanks [@LFeh](https://github.com/LFeh), exemplo perfeito!*

<a name="declaration"></a>
#### 2.2 Como Montar uma Declaração

<a name="add-space"></a>
Adicione um espaço:

▸ Antes de abrir chave `{`,<br>
▸ Depois dos `:` da propriedade.

```css
/* recomendado */
  .article {
    padding: 1em;
  }
```
```css
/* não recomendado */
  .article{
    padding:1em;
  }
```
<a name="semicolon-closekey"></a>
Nunca esqueça de:

▸ Incluir `;` ao finalizar a declaração dos valores<br>
▸ Manter o fechamento da chave `}` em uma nova linha na mesma coluna do primeiro caractere do bloco declarativo.

```css
/* recomendado */
  .footer {
    margin: 10px;
  }
```
```css
/* não recomendado */
  .footer {
    margin: 10px
    }
```
<a name="soft-tabs"></a>
Configure seu editor para tabs com 2 espaços: use [editorconfig.org](http://editorconfig.org/ "EditorConfig helps developers define and maintain consistent coding styles between different editors and IDEs.")

```css
/* recomendado */
  .sotf-tabs {
    position: absolute;
    top: 0;
    left: 2em;
    width: 2em;
  }
```
```css
/* não recomendado */
  .sof-tabs {
       position: absolute;
       top: 0;
       left: 2em;
       width: 2em;
  }
```
```css
 /* não recomendado */
.sof-tabs {
position: absolute;
top: 0;
left: 2em;
width: 2em;
}
```
<a name="doublequotes-css"></a>
Para valores de propriedades que requerem cotações "aspas", Não use aspas simples`''`  mantenha `""`

```css
/* recomendado */
  .comments-area {
    font-family: "Arial Black", Arial, sans-serif;
  }

  .nav-item:after {
    content: "";
  }

  .selector[type="text"] {
    ...
    ...
  }
```
```css
/* não recomendado */
  .comments-area {
    font-family: 'Arial Black', Arial, sans-serif;
  }

  .nav-item:after {
    content: '';
  }
```
<a name="shortheand"></a>
Algumas propriedades permitem setar valores de outras propriedades simultaneamente seguindo uma regra de inserção conhecida como _**shorthand**_ "_Abreviações de propriedade_", Use sempre que possível

```css
/* recomendado */
  .title {
    font: 100%/1.6 palatino, georgia, serif;
    padding: 0 1em 2em;
    border-top: 0;
  }
```
```css
/* não recomendado */
 .title {
    font-family: palatino, georgia, serif;
    font-size: 100%;
    line-height: 1.6;
    padding-top: 0;
    padding-left: 1em;
    padding-right: 1em;
    padding-bottom: 2em;
    border-top-style: none;
  }
```
<a name="unit-reset"></a>
Zerando unidades de medidas, Não é necessário especificar o tipo de unidade que pretende zerar, economize bytes!

```css
/* recomendado */
  .title {
    border-top: 0;
    padding: 0 1em 0;
    opacity: .5;
  }
```
```css
/* não recomendado */
  .title {
    padding: 0px;
    margin: 0em;
    opacity: 0.5;
  }
```
Para valores em hexadecimal que permitem a notação de 3 caracteres use a forma mais sucinta.

```css
/* recomendado */
  .card {
    background-color: #ebc;
    color: #222;
  }
```
```css
/* não recomendado */
  .card {
    background-color: #eebbcc;
    color: #222222;
  }
```
```css
/* recomendado */
  .page-wrap {
    background-color: rgba(0,0,0,.5);
  }
```
```css
/* não recomendado */
  .page-wrap {
    background-color: rgba(0,0,0,0.5);
  }
```
<a name="declaration-single-line"></a>
Seletores que recebem os mesmos valores devem estar separados um em cada linha

```css
/* recomendado */
  .selector-a,
  .seletor-b,
  .seletor-c {
    width: 30%;
  }
```
```css
/* não recomendado */
  .selector-a, .seletor-b, .seletor-c {
    width: 30%;
  }
```
<a name="prefixes-indentation"></a>
  Com o intuito de facilitar na edição de multiplas linhas, propriedades que precisam de prefixos use da seguinte forma:
```css
/* recomendado */
  .element {
    -webkit-transform: rotate(-2deg);
       -moz-transform: rotate(-2deg);
        -ms-transform: rotate(-2deg);
         -o-transform: rotate(-2deg);
            transform: rotate(-2deg);
  }
```
```css
/* não recomendado */
  .element {
    -webkit-transform: rotate(-2deg);
    -moz-transform: rotate(-2deg);
    -ms-transform: rotate(-2deg);
    -o-transform: rotate(-2deg);
    transform: rotate(-2deg);
  }
```

<a name="extensive-values"></a>
Propriedades com especificações de valores muito extensos separados por `,` deveriam ser organizadas de maneira a melhorar legibilidade, segue uma sugestão simples.

```css
/* recomendado */
.selector {
  background-image:
    linear-gradient(#fff, #ccc),
    linear-gradient(#f3c, #4ec);
  box-shadow:
    1px 1px 1px #000,
    2px 2px 1px 1px #ccc inset;
  }
```
```css
/* não recomendado */
  .selector {
    background-image: linear-gradient(#fff, #ccc), linear-gradient(#f3c, #4ec);
    box-shadow: 1px 1px 1px #000, 2px 2px 1px 1px #ccc inset;
  }
```
<a name="declaration-order"></a>
Quanto a ordem das declarações, organize as propriedades agrupadas por ordem **relacional** ou por ordem **alfabetica**, defina um dos tipos e mantenha o padrão em todo o projeto

<a name="relational-order"></a>
**Propriedades Relacionadas**

```css
  .selector {
   /* Posicionamento */
    position: absolute;
    z-index: 10;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;

    /* Display & Box-Model */
    display: inline-block;
    overflow: hidden;
    box-sizing: border-box;
    width: 100px;
    height: 100px;
    padding: 10px;
    margin: 10px;

    /* Tipografia */
    font-family: sans-serif;
    font-size: 16px;
    line-height: 1.5;
    color: #333;
    text-align: center;

    /* Visual */
    background-color: #000;
    border: 10px solid #333;
    border-radius: 3px;

    /* Outros */
    opacity: 1;
  }
```
<a name="alphabetical-order"></a>
**Em ordem Alfabética**<br>
_obs: quando houver propriedades com prefixos, tais profixos devem ser ignorados, como exemplo abaixo no `border:`_

```css
  .selector {
    background: fuchsia;
    border: 1px solid;
   -webkit-border-radius: 4px;
      -moz-border-radius: 4px;
           border-radius: 4px;
    color: black;
    text-align: center;
    text-indent: 2em;
  }
```
<a name="organize-declarative-blocks"></a>
Como Organizar Blocos Declarativos

<a name="property-per-line"></a>
Mantenha uma única declaração propriedade/valor por linha

```css
/* recomendado */
  .button-darkblue {
    color: whitesmoke;
    background-color: darkblue;
  }

  .button-darkviolet {
    color: white;
    background-color: darkviolet;
  }
```
```css
/* não recomendado */
  .button-darkblue {
    width: 30%; color: whitesmoke; background-color: darkblue;
  }
  .button-darkviolet {
    width: 30%; color: white; background-color: darkviolet;
  }
```
<a name="space-between-blocks"></a>
Adicione um espaço entre cada bloco de declarativo

```css
/* recomendado */
  .marketing-header h1 {
    margin-top: 0;
    margin-bottom: 0;
    font-size: 42px;
    font-weight: 300;
  }

  .marketing-header .lead {
    max-width: 750px;
    margin: 10px auto 0;
    color: #586069;
  }

  .marketing-header .btn {
    padding: 12px 20px;
    margin-top: 15px;
    font-size: 18px;
    font-weight: normal;
    border-radius: 6px;
  }

  .marketing-section {
    position: relative;
    padding: 80px 0;
    font-size: 16px;
    line-height: 1.5;
    text-align: center;
    border-bottom: 1px solid #e5e5e5;
  }
```
```css
/* não recomendado */
  .marketing-header h1 {
    margin-top: 0;
    margin-bottom: 0;
    font-size: 42px;
    font-weight: 300;
  }
  .marketing-header .lead {
    max-width: 750px;
    margin: 10px auto 0;
    color: #586069;
  }
  .marketing-header .btn {
    padding: 12px 20px;
    margin-top: 15px;
    font-size: 18px;
    font-weight: normal;
    border-radius: 6px;
  }
  .marketing-section {
    position: relative;
    padding-top: 80px;
    padding-bottom: 80px;
    font-size: 16px;
    line-height: 1.5;
    text-align: center;
    border-bottom: 1px solid #e5e5e5;
  }
```
<a name="single-value-selectors"></a>
Matenha as declarações de *propriedade/valor único* em apenas uma linha

```css
/* recomendado */
  .button-darkblue { background-color: darkblue; }
  .button-darkgrey { background-color: darkgrey; }
```
```css
/* não recomendado */
  .button-darkblue {
    background-color: darkblue;
  }

  .button-darkviolet {
    background-color: darkviolet;
  }
```
<a name="media-queries"></a>
Agrupe as `@media queries` junto aos respectivos blocos declarativos a que manipulam, não as coloque em arquivo separado ou ao fim do arquivo principal.

```css
/* recomendado */
  .element { ... }
  .element-avatar { ... }
  .element-selected { ... }

  @media (min-width: 480px) {
    .element { ...}
    .element-avatar { ... }
    .element-selected { ... }
  }
```
<p align="center"> Todo o css do projeto pronto? ok! Minifique seu código, Sempre!</p>

- Use algum automatizador de tarefas como [Gulp](https://gulpjs.com/ "Automate and enhance your workflow")
- Bate e pronto, coisa rápida. use [CSS Minifier](https://cssminifier.com/ "Minify your CSS")
**<p align="center"> Todo o css do projeto pronto? ok! Minifique seu código, Sempre!</p>**

- Use algum automatizador de tarefas como [Gulp](https://gulpjs.com/ "Automate and enhance your workflow")
- Bate e pronto, coisa rápida. use [CSS Minifier](https://cssminifier.com/ "Minify your CSS")

<a name="end"></a>
<h2 align="center">Conclusão</h2>

 Embora gambiarras sejam a forma mais genial de expressar a criatividade, use-a em último recurso, pois o objetivo do código em produção é manter eficiencia e gerenciabilidade.

**Continue o aprendizado:**

- Arquitetura CSS:
  - [Semantic Class Names](https://maintainablecss.com/chapters/semantics/ "MaintainableCSS - Semantics ")<br>
  - [Naming CSS Stuff Is Really Hard](https://seesparkbox.com/foundry/naming_css_stuff_is_really_hard "Naming CSS by Ethan Muller")<br>
