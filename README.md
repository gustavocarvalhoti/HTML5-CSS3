# HTML5 (Versão 5 - 2015) e CSS3 (Versão 3 - 2012)

## Tags que nunca lembro.

````
<strong>    Algo importante
<em>        Para dar enfâse, itálico
<header>    Primeira informação a ser apresentada, cabeçalho
<main>      Conteúdo principal
<footer>    Rodapé
<fieldset><legend>  Utilizada em formulários, paginas-teste/form.html
<section>   Para um bloco onde o conteúdo tenha o mesmo significado, o mesmo sentido
````

## Propriedades CSS que nunca lembro.

````
text-transform: uppercase;
font-weight: bold;
text-decoration: none;          <- Remove sublinhado link
box-sizing: border-box;         <- Para utilizar o espaçamento definitivo
background: url("./imagens/background.png");   <- Duplica até preencher toda a tela
````

## Outras dicas.

````
**********************************************************************************************************************************
#Reset
Reseta os arquivos de css default do navegador para utilizar somento os que inserimos
<link rel="stylesheet" href="reset.css">  <- Eric Meyer
OU
http://necolas.github.io/normalize.css/
<- O Normalize não apenas remove o estilo padrão do navegador como também define alguns estilos úteis,
como tamanhos de fontes para cabeçalhos e estilos de fontes para elementos <em> e <strong>

**********************************************************************************************************************************
#Tags
<blockquote>  - Citação
<nav>         - Indica regiões da página que contêm links de navegação
<main>        - Conteúdo principal da página
<header>      - Cabeçalho da página ou de uma região dela
<footer>      - Mesma ideia da tag <header> para o rodapé
<aside>       - Conteúdo auxiliar ao conteúdo principal, como links relacionados ao conteúdo
<article>     - Conteúdo que, por si só, já tem um sentido completo, como um post de um blog ou uma notícia
<section>     - Parte/seção de uma página ou texto
<article>     - Artigo

**********************************************************************************************************************************
#Caracteres especiais por meio das entidades
&euro;:   €
&yen;:    ¥
&pound;:  £
&reg;:    ®
&hearts;: ♥
&lt;:     <
&gt;>     >

**********************************************************************************************************************************
#Assumir o valor do Pai
<ul><li><a href="#">Link 1</a></li></ul>
ul { color: pink;}
ul li a { color: inherit; }

**********************************************************************************************************************************
#Altera o css da tag
h1, h2 {
  font-family: "Open Sans Condensed", "Arial", sans-serif;
}

#Bordas
border: 10px solid #C2CCCA;
solid, dotted, dashed, double, groove, ridge, inset, outset
#Tamanho 250px considerando as bordas
blockquote {
    padding: 16px;
    margin: 0;
    border: 10px solid #C2CCCA;
    width: 250px;
    box-sizing: border-box;
}

line-height: 1.5; -> Aumenta o tamanho da linha em relação ao texto,
se a fonte tiver o tamanho de 20 pixels, a linha terá o tamanho de 30 pixels.

**********************************************************************************************************************************
# Tamanhos - Medidas relativas
px      - Pixel da tela
%       - Porcentagem da font (Ele pega do pai do elemento "Container")
1.25rem - 1.25 * tamanho da fonte do navegador
30ch    - 30 caracteres

rem: tem como padrão a fonte do navegador;
em: tem como padrão a fonte do elemento pai; Posso colocar 1em, 2em (Relativo ao tamanho da fonte)
ch: tem como base a largura do caractere zero da fonte usada;

No font-size de preferência para porcentagem por causa da opção de tamanho de fonte do navegador.
.titulo-principal {
  padding: 1.25rem;
  font-size: 300%;
}

#Exemplo de uso do em - Padrão a fonte do elemento pai
p {
    font-size: 20px;
    margin: 1em;
}

#Exemplo de uso do rem - Tamanho da fonte do Navegador
#Ele pega o tamanho de fonte do elemento html ou se não houver tamanho de fonte definido neste elemento, o tamanho de fonte padrão do navegador.
html { font-size: 25px; }
p { margin: 1rem; }

#Vinculando o tamanho relativamente
.blog {
  background-color: #999;
  color: #FFF;
  border-bottom: .5em solid #851944;
  position: relative;
}
.inicio-post {
  background-color: #FFFFFF;
  /*Relativo a página do navegador ou o primeiro pai que tem um position*/
  position: absolute;
  color: red;
  top: 3em;
  right: 3em;
  height: 6em;
  padding: 1em;
}
<section class="secao-inicio blog">
  <h2>Blog</h2>
  <small>Últimos posts</small>
  <ol>
    <li>
      <a href="blog.html">O essencial de design responsivo</a>
      <p class="inicio-post">
        Paragrafo inicio do post
      </p>
    </li>
    <li>
      <a href="blog.html">Por que fazer páginas acessíveis?</a>
    </li>
    <li>
      <a href="blog.html">JavaScript não obstrusivo</a>
    </li>
  </ol>
  <a class="botao-index" href="blog.html">Veja mais</a>
</section>

**********************************************************************************************************************************
#Exemplo de positions TOP
<header class="titulo-principal">
  <img class="foto-home" src="../img/eu.jpg" alt="Foto de Gustavo Carvalho da Silva">
  <h1> Gustavo Carvalho da Silva</h1>
  <p class="subtitulo-principal">Desenvolvedor web</p>
  <ul>
    <li class="palavra-home eficiencia">Eficiência</li>
    <li class="palavra-home boas-praticas">Boas práticas</li>
    <li class="palavra-home codigo-limpo">Código limpo</li>
    <li class="palavra-home css3">CSS3</li>
    <li class="palavra-home html5">HTML5</li>
    <li class="palavra-home javascript">JavaScript</li>
    <li class="palavra-home acessibilidade">Acessibilidade</li>
    <li class="palavra-home responsivo">Responsivo</li>
    <li class="palavra-home otimizacoes">Otimizações</li>
    <li class="palavra-home agilidade">Agilidade</li>
    <li class="palavra-home design">Design</li>
  </ul>
</header>

/*Define a referência para as posições*/
header {
  position: relative;
}
.palavra-home {
  position: absolute;
  font-family: "Shadows Into Light", cursive;
  font-weight: bold;
  color: #D5447E;
}
.eficiencia {
  top: 20%;
  left: 75%;
}
.boas-praticas {
  top: 70%;
  left: 20%;
}

**********************************************************************************************************************************
#Border radius - Arredondamento da borda
border-radius: 100px 50px 0 100px;

**********************************************************************************************************************************
#Sombras e opacidade
#Sombra no testo
h1 {
    text-transform: uppercase;
    font-size: 3em;
    text-shadow: 5px 5px #000;
}

#Sombra na imagem
.foto-home {
  height: 200px;
  box-shadow: 0 0 1em #000;
}

#Sombra interna e externa
box-shadow: 0 0 1em #000, inset 0 0 .5em #FFF;

#Podemos separa por virgula para colocar duas
#direita + baixo, esquerda + alto
box-shadow: 10px 10px black, -10px -10px orange;

#5 Bordas - Precisa aumentar o tamanho 4,8,12...
box-shadow: 0 0 0 4px black,
            0 0 0 8px blue,
            0 0 0 12px black,
            0 0 0 16px blue,
            0 0 0 20px black;

#Deixa transparente*/
.acessibilidade {
  opacity: .3;
}
background-color: rgba(0, 0, 0, 0.8);

**********************************************************************************************************************************
#Efeito modal
.modal-top {
  width: calc(50% - 10px);
  height: 300px;
  margin: 0 auto;
  background-color: rebeccapurple;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 9999;
  padding: 10% 3%;
  text-align: center;
  font-size: 2em;
  box-shadow: 0px 0px 0px 9999px rgba(0, 0, 0, 0.75);
}
<div class="modal-top">
  OI
</div>

**********************************************************************************************************************************
#Gradientes - Efeito de escurecimento
.titulo-principal {
  position: relative;
  background-image: linear-gradient(to bottom, #F00, #000);
}
#Da esquerda para a direita descendo
background-image: linear-gradient(to bottom right, white, red, black);
#Da esquerda para a direita
background-image: linear-gradient(to right, white, red, black);
#Gradual
background-image: linear-gradient(to bottom, black, blue 80%, brown);
#Radial
background-image: radial-gradient(yellow, red);

**********************************************************************************************************************************
#Conhecendo outros seletores do CSS - Selecionar os elementos para aplicar estilos neles
#Do segundo li para baixo
li ~ li {
  background-color: blue;
}
#Do terceiro li para baixo
li ~ li ~ li{
  background-color: red;
}

#O primeiro paragrafo após uma img será purple (Se tiver div não funciona)
img + p {
  color: purple;
}

#Todos os paragrafos dentro da div
div > p {
  color: red;
}

#Todos os paragrafos dentro da div
div > p + p {
  color: yellow;
}

#Todos os ha dentro da div e o <p> após a div é aqua
div > h1 + p {
  color: aqua;
}

#Conseguimos selecionar por qualquer outro atributo usando essa sintaxe
<a href="http://www.alura.com.br">
[href="http://www.alura.com.br"] { <- Especifico
  border: black 1px dashed;
}
[src$=".jpg"] { <- Selecionar todas as imagens com a extensão .jpg
  border: black 1px dashed;
}
[href^="http://"] { <- Se quisermos selecionar todos os links que começam com http://
border: black 1px dashed;
}

#Altera a primeira letra do paragrafo dentro do container
.container > p::first-letter {
    font-size: 200%;
    font-weight: bold;
    color: #3C1D3D;
    text-shadow: 1px 1px #000;
}

**********************************************************************************************************************************
#Pseudoclasses    - O vavegador coloca
:nth-child(odd)   - linhas ímpares;
:nth-child(even)  - linhas pares;
:nth-child(3)     - terceira linha;
:first-child      - primeira linha;
:last-child       - última linha.
tr:nth-child(odd) {
  background-color: red;
}

**********************************************************************************************************************************
#Focar nesse e apagar os outros
.citacao-bio:hover {
  box-shadow: 0 0 0 99999px rgba(0,0,0,.8);
}

**********************************************************************************************************************************
#Pattern
<input pattern="[A-Za-z0-9]*">
<input pattern="[A-Za-z0-9]{8,}">

**********************************************************************************************************************************
#Cálculos com CSS
.navegacao-site {
    width: calc(0.9 * 300px);
}

**********************************************************************************************************************************
#Coloca uma imagem antes do input
label[for="nome"] {
    position: relative;
}

label[for="nome"]:after {
    content: "";
    background-color: #666;
    background-repeat: no-repeat;
    background-image: [o destino da imagem aqui]
    background-size: 50% 50%;
    width: 2em;
    height: 2em;
    background-position: center;
    position: absolute;
    top: 100%;
    left:0;
}

#nome {
    width: calc(100% - 2em);
    position: relative;
    left: 2em;
}

**********************************************************************************************************************************
#Transições e animações
.citacao-bio {
  /*transition: 1s;*/
  /*transition: transform 1s;*/
  /*Transforma e depois de 2s mostra a sombra*/
  /*ease-in   - remove a suavização do inicio*/
  /*ease-out  - remove a suavização do final*/
  transition: transform 1s linear, box-shadow 2s ease-in;
  /*Começar com um atraso*/
  transition-delay: 0s, 1s;
}
h1 {
  animation: aparece 2s;
}
#Da um apelido para ele
@keyframes aparece {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

**********************************************************************************************************************************
#Flexbox - Controle atraves do pai
.container {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
display: flex: ativa o flexbox no elemento;
align-items: distribui verticalmente os elementos dentro de um container flex;
justify-content: distribuir os elementos espaçadamente dentro do container;
flex-direction: permite inverter o align-items;
order: muda a ordem dos elementos;
flex: indica a proporção do tamanho dos elementos. Ele é um atalho para mais três propriedades:
flex-grow: determina quanto o elemento deve crescer;
flex-shrink: determina quanto o elemento deve diminuir;
flex-basis: determina o tamanho mínimo do elemento.

**********************************************************************************************************************************
Utilizando a ultima versão disponível do HTML, nesse caso o 5, 
colocar em UPPERCASE. Ela não fecha. Verificar abaixo:
<!DOCTYPE html>

Tem os caracteres mais utilizados, arrumando a acentuação.
<html lang="pt-br"> <meta charset="UTF-8">
    
<head>      Informações que passamos para o navegador
<body>      Informações que queremos exibir para o usuário

Podemos representar a cor vermelha com o nome red, 
o hexadecimal #FF0000 e o RGB rgb(255,0,0).

### inline block
Block  - Pegar o tamanho inteiro da linha
Inline - Uma imagem deixa ter outros conteudos ao lado
Inline Block - Bloqueia uma parte só e aceita outra parte. Lembra muito o display flex
Exemplo em: paginas-teste/inline-block.html

### Position Relative, verificar paginas-teste/inline-block.html
position: relative; /*Muda a partir do ponto inicial e coloca na frente de uma imagem absoluta*/
top: 20px;          /*Add mais 10 px do ponto aonde ele deveria estar*/

### Position Absolute, sai do contexto e pode alinhar sem interferir os outros
img {
    position: absolute;
    top: 0;
    right: 0;
}


### Quando estiver em cima do item
.container-heroes img:hover {
    background-color: burlywood;
}
### Quando estiver clicando no item
.container-heroes img:active {
    background-color: #3C1D3D;
}
````

## Links

https://unicode-table.com/pt/ <br/>
http://mobileinputtypes.com/ <br/>
https://fonts.google.com/ <br/>
https://blog.alura.com.br/criando-componentes-css-com-padrao-bem/ <br/>
https://cssgridgarden.com/ <br/>