# CAIXA:
- Quase tudo terá caixas no css, além de cores, posicionamento, bordas, etc.

HTML:
<h1>Título</h1>

CSS:
h1 {
    border: 1px (a finura da borda em volta) solid red; (cor escolhida para o contorno)
    margin (espaçamento por fora da caixa): 200px; (pixels)
    padding (preenchimento por dentro): 60px;
}

# MUDAR FONTE DA LETRA:
HTML:
- dentro do head usar a tag link:
<link rel="stylesheet" href="url">

CSS:
Dentro da designação da caixa/elemento que deseja mudar, citar a fonte por:
h1 {
    font-family: 'NomeDaFonte';
}
- Ou apenas dentro do css botar "@import" + link da fonte, mas não é recomendado, pois é mais lento que a tag link.

# Prioridade de leitura do código: modificações de estilo lida de baixo para cima
# Ou seja, o código mais embaixo é considerado para um mesmo elemento
# Ordem de prioridade: 
-> Código HTML, modificação dentro de alguma tag <h1 style = "red"> 
-> tag <style> </style>
-> tag <link> </link>
-> Código CSS de baixo para cima (o mais embaixo é o considerado)


# Algumas regras relacionadas ao comportamento do CSS:
@import serve para incluir um CSS externo.
@media são regras condicionais para vários dispositivos.
@font-face é para colocar fontes externas.
@keyframes serve para as animations do CSS.

# Junção de propriedades:
- Imagine que você necessita adicionar várias propriedades a um elemento, invés de citar cada característica,
é possível adicionar tudo que você precisa em uma linha (shorthand): 

/* background properties */
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;

#   (Background shorthand)
#   background: #000 url(images/bg.gif) no-repeat left top;

/* font properties */
    font-style: italic;
    font-weight: bold;
    font-size: .8em;
    line-height: 1.2;
    font-family: Arial, sans-serif;

#   (Font shorthand)
#   font: bold italic .8em/1.2 Arial, sans-serif;

# FUNÇÕES:
Um tipo de valor existente no CSS, é estruturado com um nome escolhido seguido de abre e fecha parênteses.
- usado para reaproveitamento de código.

Recebe um argumento, que são seus valores, dentro do parenteses.

Um exemplo de função é:

color: nomeCor(255,0,100);