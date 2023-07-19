# POSIÇÕES:
- Representa um conjunto de coordenadas 2D: top, right, bottom, left e center
- Usado para alguns tipos de propriedades como o background-position ou position.

- position: static / position: fixed é autoexplicativo.

- Quando o position = relative; o elemento daquele bloco de código se deslocará normalmente a partir de sua posição (através de right/top/left/bottom) sem afetar o posicionamento de outros elementos da página.

- Quando o position = absolute; é criado um novo "layer" diferente dos outros elementos da página e o elemento pode ser posicionado em qualquer posição a partir do seu ponto inicial, os elementos da página tomam seu lugar no layer inicial.

- Por default, os primeiros elementos declarados no HTML empilhará abaixo dos outros abaixo dele. se você deseja escolher a "ordem de prioridade" quem fica em cima de quem, use -> z-index: número (quanto maior, mais em cima fica)

.classeAleatoria {
    background-image : url(http://imagem.com)
    background-position: right 50px; (posição direita da imagem a 50px)
    position = relative;
    position = absolute;
    z-index = 2;
    z-index = 10 (pense em outro elemento com essa propriedade, ficaria acima desse com z-index = 2)
}

# FLEX -> MODELO FLEXIBLE BOX LAYOUT

- Primeiramente, as caixas podem ser em block ou inline, e a propriedade display: block/inline define como será posicionado, foi criado o atributo flex que permite que um elemento se comporte como um elemento de outra caixa pai. 

- No modelo de layout do Flexbox, os filhos de um contêiner flex podem ser dispostos em qualquer direção, e podem "flexibilizar" seus tamanhos, crescendo para preencher o espaço vazio ou diminuindo para evitar o transbordamento do elemento pai. 
 ______________________________
|   ________  PAI  ________    |
|  |_filho__|     |__filho_|   |
|______________________________|

.content {
    display: flex; -> DEFINE OS ITENS DA CAIXA COMO INLINE, UM AO LADO DO OUTRO.
}
- ao utilizar flex: 1/0/X px; irá mudar largura e altura das flex containers.

* Dica: se desejar flexionar seus itens, ajuste a altura de sua flexbox através da viewport, pois independente da
aba do usuário, a altura também se flexionará, "através de height: Número vh"

# FLEX DIRECTION
- Por default, todos os flexboxs são "flex-direction: row", ou seja, são exibidos em um linha horizontalmente, porém,
ao utilizar "flex-direction: column" mudará o conteúdo para ser exibido verticalmente por linhas.

# FLEX WRAP
- Quer que os itens caibam na linha até onde der e de acordo com o tamanho da janela jogue o resto do conteúdo para
outras linhas? use:

.content {
    flex-wrap: wrap;
}

QUER UM SHORTHAND (ATALHO) PARA USAR ESSAS PROPRIEDADES? use:
flex-flow: column wrap;


# Justify-content

- Se por exemplo alguém aumentar ou diminuir a janela da página, os elementos podem se "flexionar" para mudar de posição de acordo com a disposição da tela (parecido com o que tu viu na unity sobre diferentes resoluções apresentarem layouts diferentes e você deve administrar como os elementos serão posicionados considerando isso)

* Para ser flexionado a partir dos espaços entre os elementos inline (margin) use -> justify-content: space-between;
ou seja, a "margem" entre os elementos aumentará e diminuirá a partir da resolução da janela.

* O contrário de space-between, o que é flexionado é o espaço em volta e a margem dos itens permance o mesmo, utilize: justify-content: space-around;

_______________________________                     ________________________________________
|   ________  PAI  ________    |                    |         _______  PAI  _______         |
|  |_filho__|     |__filho_|   |      ----->        |        |_filho_|     |_filho_|        |
|______________________________|                    |_______________________________________|



* Para ser flexionado a partir do centro, ou seja os elementos ficam estaticos no centro e é o espaço em volta que muda utilize-> justify-content: center;

(no arquivo HTML tem uma tag com a classe "container" contendo as caixas que eu quero ter essa configuração)

.container  {
    display: flex;
    justify-content: space-between; /* calcula um espaço entre os itens através do tamanho da janela */
}

* justify-content: flex-end; para botar o conteúdo no final da linha.
* justify-content: space-evenly; para botar separar igualmente o espaçamento entre as flexbox.

OBS: também tem a propriedade gap que faz a mesma coisa:
    gap: 2% / gap: 2px;


# Exemplo sobre o assunto acima no arquivo de testes!!

# Align-items
- Controla o alinhamento dos itens no Eixo de Bloco dentro de sua grid area.

body {
    align-items: start/end/center;
}

# GRID
- Parece uma tabela ou a tela de um celular microsoft.

# 1º Você define os elementos dentro de um body em seu código HTML:

<body>
    <header>Algo acima</header> (conteúdo escrito)

    <main>Algo no centro</main>

    <aside>Algo abaixo</aside>

</body>

# 2º Você define onde estará posicionado cada um dos elementos e suas propriedades:

body {
    margin: 0;
    height: 100vh; (100% da viewport, área da tela)
    display: grid;
}

header {
    grid-area: header; (acima da "tabela")
}

main {
    grid-area: main; (meio da "tabela")
}

aside {
    grid-area: aside; (do lado da "tabela")
    grid-area: footer; (isso seria abaixo da "tabela")
}
         Browser
 __________________________
|                          |
|_________header___________|                        
|            |             |
|___main_____|__aside______|                          
|                          |
|_________footer___________|

# Podemos usar o Display Flex e Display Grid ao mesmo tempo:
(do mesmo exemplo acima)

header {
    grid-area: header;
    background-color: green;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 8px;
}

#  Order
- Para mudar a ordem dos items bote "order:" seguido de um número crescente onde o menor é o primeiro e o maior o último.