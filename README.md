<h3>:clipboard:</h3>

# Guia Básico de Estilo HTML e CSS

Das pesquisas por convensões de padronização e organização de código surgiu a necessidade de documentar as preferências de escrita adotada por renomados e quase anonimos desenvolvedores ao redor da web. 

Este guia é bem simples e não tendo a pretenção de ser obrigatório, é apenas uma recomendação para desenvolver HTML e CSS da melhor maneira possível visando manter em todo o projeto um estilo único e consistente.

:octocat: Contribua, suas ideias e sugestões são bem-vindas.

## Formatação e Estilo no HTML

1. [DOCTYPE](#doctype)
1. [Capitalização](#capslock)
1. [Lang](#lang)
1. [UTF-8 encoding](#encoding)
1. [Indentação e Hierarquia](#indentation)
___

O uso de uma formatação concisa torna mais fácil a leitura do seu HTML e possibilita que qualquer outro desenvolvedor se concentre no que você está dizendo e não em como você está dizendo.

<a name="doctype"></a>
#### 1°```<!DOCTYPE html>``` como estrutura global

```!DOCTYPE``` é uma instrução para os browsers sobre a versão do html,
portanto essa declaração deve ser a primeira informação em seu html.

```html
<!doctype html>
<html>
  ...
</html>
```
<a name="capslock"></a>
#### 2°	Capitalização - CAIXA ALTA e/ou caixa baixa?

Embora o HTML5 permite misturar letras MAIÚSCULAS e minúsculas, use somente "lowercase"

- [x] *Código mais limpo*
- [x] *Facil digitar*
- [x] *Sem distrações na leitura*

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
#### 3°	Use ```lang=" "``` para Especificar o Idioma:

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

#### 4° ```UTF-8``` Codificação de Caracteres:

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
#### 5° Indentação de hierarquia:

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