TIPOS NUMÉRICOS

<integer> - número inteiro como -10 ou 223
<number> (double) - número decimal como -2.4, 64 ou 0.234
<dimension> - é um <number> com uma unidade junto: 90deg, 2s, 8px
<percentage> - representa uma fração de outro número: 50%

UNIDADES COMUNS

<length> - é um dos mais usados no CSS e representa um valor de distância: px (pixel), em, vw
<angle> - representa um ângulo: deg, rad, turn
<time> - representa um tempo: s, ms
<resolution> - representa resoluções para dispositivos: dpi

# Distâncias absolutas <length>

São fixas e não alteram seu valor.

| Unidade  | Nome                | Equivalência         |
|----------|---------------------|----------------------|
| cm       | Centímetros         | 1cm = 96px/2.54      | 
| in       | Inches (polegadas)  | 1in = 2.54cm = 96px  | 
| px       | Pixels              | 1px = 1/96th of 1in  |
*o mais comum e mais utilizado é o px

*não é recomendado usar cm

# Distâncias relativas

São relativas a um outro valor, pode ser o elemento pai, ou root, ou o tamanho da tela.
Benefício: Maior adaptação aos diferentes tipos de tela.

| Unidade  | Relativo a                                    |
|----------|-----------------------------------------------|
| em       | Tamanho da font do elemento pai               |
| rem      | Tamanho da font do elemento raiz (root/html)  |
(os dois usados para multiplicar o tamanho da fonte atual)

| vw       | 1% da viewport wid                            |  
| vh       | 1% da viewport height                         |
(porcentagem de largura e altura da tela)

Normalmente o tamanho da font padrão do navegador é de 16px e para mudar esse valor temos que fazer a alteração no root ou no elemento html.

:root {
	font-size: 18px;
}

/* OU */

html {
	font-size: 18px;
}
O viewport é a parte da tela que está sendo exibida. No caso dos navegadores web, é o que é exibido na janela/tela do documento. Conteúdos que estão fora do viewport só serão exibidos quando feito um scroll da área de visualização.

# PORCENTAGEM:
- Exemplo de uso: pode mudar o tamanho da fonte padrão por meio de porcentagem

html {
    font-size: 50%;
}
- se a fonte padrão tem 16 pixels, fazendo esse comando, você a muda para 8px

# POSIÇÕES:
- Representa um conjunto de coordenadas 2D: top, right, bottom, left e center
- Usado para alguns tipos de propriedades como o background-position ou position. (verificar arquivo posicoes)

.classeAleatoria {
    background-image : url(http://imagem.com)
    background-position: right 50px; (posição direita da imagem a 50px)
    position = relative;
}

# Uso prático da função calc() para posicionar uma imagem:
body {
    height: 100vh; (altura da visualização da tela)
    margin: 0 (espaçamento em volta da imagem)
}

.classeAleatoria {
#   height: calc(100% - 40px) --> aqui foi posicionado a imagem em 100% da altura da tela menos 40 pixels
    ou seja, a imagem comportará quase todo o espaço da tela menos uma quantidade de 40 pixels abaixo.

    width: 100% -> porcentagem da largura
    background-image : url(http://imagem.com) -> a imagem escolhida, também utilizando uma função, a url()
}

# Uso de texto:
.classeAleatoria {
	content: "Isso é uma string";
    color: white; --> isso é um identificador
}