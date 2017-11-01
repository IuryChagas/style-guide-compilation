<h3>:clipboard:</h3>

# Guia Básico de Estilo HTML e CSS

Das pesquisas por convensões de padronização e organização de código surgiu a necessidade de documentar as preferências de escrita adotada por renomados e quase anonimos desenvolvedores ao redor da web. 

Este guia é bem simples e não tendo a pretenção de ser obrigatório, é apenas uma recomendação para desenvolver HTML e CSS da melhor maneira possível visando manter em todo o projeto um estilo único e consistente.

:octocat: Contribua, suas ideias e sugestões são bem-vindas.

## Formatação e Estilo no HTML

1. [DOCTYPE](#doctype)
1. [Capitalização](#capslock)
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

- :heavy_check_mark: *Código mais Limpo*
- :heavy_check_mark: *Facil Digitar*
- :heavy_check_mark: *Sem Distrações na Leitura*

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