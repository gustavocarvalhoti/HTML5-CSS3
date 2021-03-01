## Instalar Ubuntu
``
sudo apt-get install ruby
``

## Instalar Ubuntu
````
sass estilos.scss:estilos.css               <- Compilar SASS
sass --watch estilos.scss:estilos.css       <- Verifica e compila
sudo apt install ruby-full rubygems autogen autoconf libtool make
sudo gem install sass                       <- Install sass
````

## Sobre
````
Sass - estilos.scss
*********************************************************************************************
Mixin - utilizado para não repetir codigo no css
@mixin borda-arredondada {                  <- Definir
    -webkit-border-radius: 0.3em;
}

.plano_button {                             <- Utilizar
    @include borda-arredondada;
}

Mixin que recebe valor
@mixin borda-arredondada($raio) {                  <- Definir
    -webkit-border-radius: $raio;
}

.plano_button {                                     <- Utilizar
    @include borda-arredondada(0.5em);
}

O sass respeita a hierarquia de componentes, pode colocar um dentro do outro
.menu-principal {
    button {
        &:hover { <- Pega o pai dele, nesse exemplo o button
            text-decoration: underline;
        }
    }
}

Place holder, ele coloca no inicio do CSS e agrupa - Ele não recebe valor
%sombra-padrao {                                        <- Definir
    -webkit-bom-shadow: 0 2px 6.65px 0.35px rgba(0, 0, 0, 0.3);
    box-shadow: 0 2px 6.65px 0.35px rgba(0, 0, 0, 0.3);
}       
.plano_button {                                         <- Utilizar
    @extend %sombra-padrao;
}
Agrupa assim: 
.destaque button, .plano button {
    -webkit-bom-shadow: 0 2px 6.65px 0.35px rgba(0, 0, 0, 0.3);
    box-shadow: 0 2px 6.65px 0.35px rgba(0, 0, 0, 0.3);
}

Variáveis ->
$ponto-de-quebra: 950px;                                <- Definir
@media (max-width: $ponto-de-quebra) {                  <- Utilizar
    .container {
        width: 905;
    }
}

Midia Query em Variável ->
$mq-mobile: "(max-width: 980px)";                           <- Definir
@media #{$mq-mobile} {}                                     <- Utilizar

Function ->
@function get-largura($mult){                               <- Definir
    @return $mult * 16;
}
.plano {                                                    <- Utilizar
    width: round(get-largura(18.5));                        <- Round - Arredonda o valor
}

Compass - Framework CSS com muitas coisas prontas
*********************************************************************************************
Ele faz comentários automaticos no scss

Less - estilos.less
*********************************************************************************************                              
lessc nome-do-arquivo.less nome-do-arquivo.css              <- compilar o LESS

@cor-padrao: red;                                           <- Variável
div {
    background-color: @cor-padrao;
}
@mobile: ~"max-width: 980px";                               <- Definir
@media @mobile {                                            <- Utilizar
    height: auto;
}

Mixin
.borda-arredondada(@raio-da-borda: 0.3em) {                 <- Definir, default 0.3em
    border-radius: @raio-da-borda;
}
.plano button {                                             <- Utilizar
    .borda-arredondada(5px);
}

Place holder - Ele agrupa
.plano button {                                             <- Utilizar
    &:extend(.borda-arredondada);
}
````