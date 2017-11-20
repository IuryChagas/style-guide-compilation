<h1 align="center">
  Guia Basico de Estilo HTML e CSS
</h1>

Das pesquisas por convensões de padronização e organização de código surgiu a necessidade de documentar as preferências de escrita adotada por renomados e quase anonimos desenvolvedores ao redor da web. 

Este guia é bem simples e não tendo a pretenção de ser obrigatório, é apenas uma recomendação para desenvolver HTML e CSS da melhor maneira possível visando manter em todo o projeto um estilo único e consistente.

:octocat: Contribua, suas ideias e sugestões são bem-vindas.

## Tópicos:

1. **[HTML](#html)**
1. **[CSS](#css)**

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

1. [ID e Nomeação de Classes](#classnaming)
1. [Seletores de Tipos](#typeselectors)
1. [Regras de Formatação](#formattingrules)

> O formato de código escolhido deve garantir que o código seja: fácil ler, fácil comentar, minimizar as chances de introduizir erros, e resultar em `diffs` e `blames` úteis.
~ Nicolas Gallagher

<a name="classnaming"></a>
#### 2.1 Nomeação de Classes, IDs

Use nomes legiveis sempre em caixa baixa e que faça referência direta com o propósito/finalidade do elemento.

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
<a name="typeselectors"></a>
#### 2.2 Seletores

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

<a name="#formattingrules"></a>
#### 2.3 Formatação, Regras e Sintaxe

Seletores que recebem os mesmos valores devem estar separados um em cada linha
```css
/* recomendado */
  .selector-a,
  .seletor-b,
  .seletor-c {
    ...
}
```
```css
/* não recomendado */
  .selector-a, .seletor-b, .seletor-c {
   ...
}
```
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