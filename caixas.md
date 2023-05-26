# Box Model
- são caixas retangulares,  com propriedades de uma caixa 2D (2 dimensões):

Propriedades da caixa
- Tamanho (largura x altura) → width | height
    OBS IMPORTANTE: a altura e a largura estão relacionadas ao conteúdo da caixa e não o tamanho dela em si
    como assim? se eu tiver um texto "Texto aqui" ele definirá o tamanho da caixa a partir desse texto,
    porém a propriedade "padding" definirá como um todo adicionando pixels em volta do conteúdo.

- Conteúdo → content
- Bordas → border
- Preenchimento interno → padding (entre o conteúdo e a borda)
- Espaços fora da caixa → margin


Por padrão o navegador vai calcular o tamanho da caixa pelo content-box e vai somar com os outros boxes, no exemplo abaixo no lugar de 100px (width) a caixa vai ficar com uma largura de 140px. Para que isso não aconteça, é possível mudar qual vai ser a referência para o calculo do tamanho da caixa adicionando a propriedade box-sizing: border-box.

div {
   width: 100px; 
   height: 100px;
   border: 1px solid red;
   margin: 10%;
   padding 0 20px (20 pixels para cada lado, se quiser adiconar espaço em apenas um lado use: padding-left/right)
#  box-sizing: border-box (adicionando isso, invés dacaixa ter 140px de largura, terá 100px e ainda haverá o espaçamento
#  de 20px entre o conteúdo da caixa, nesse caso, o texto)
}

Antes de adicionar propriedade padding:
 __________
|texto aqui|
|__________|    
<---100px--->

Depois de adicionar propriedade padding:
 ______________________________
|<- 20px ->texto aqui<- 20px ->|
|______________________________|  
<-------------140px------------>

Depois da propriedade box-sizing: border-box:
 ______________________________
|<- 20px ->texto aqui<- 20px ->|
|______________________________|  
<-------------100px------------>

(ficaria do tamnho do primeiro exemplo com o espaçamento entre o conteúdo e a borda)

FAZENDO ISSO JÁ DEIXA REGISTRADO ESSA PROPRIEDADE PARA TODAS AS CAIXAS DO CÓDIGO:
* {
   box-sizing: border-box;
}

# Display-block-inline
- as caixas podem ser em block ou inline, ou seja, se separa de outra caixa/componente de forma diferente:
- BLOCK: Ocupa toda a linha, colocando o próximo elemento abaixo desse, width e height são respeitados
#  exemplos: <p> <div> <section>, todos os headings <h1> <h2>...

- INLINE: Os elementos ficam ao lado do outro e não empurram outros elementos para baixo, width e height não funcionam
  somente valores horizontais como margin funcionam.
#  exemplos: <a> <strong> <span> <em>

Block: ____________________
      |_____conteúdo_______|
       ____________________
      |_____conteúdo_______|

Inline:  __    __
        |  |  |  |              
        |  |  |  |   
        |  |  |  |   
        |__|  |__|   

- você pode escolher o estilo de caixa também pela propriedade: display: inline;
                                                             ou display: block;

# Margin
Geralmente usamos uma forma abreviada (shorthand) para escrever o margin. Esse formato segue o sentido horário iniciando pelo top, seguindo para right, bottom e left.

margin: 12px 16px 10px 4px; // TOP = 12px | RIGHT = 16px | BOTTOM = 10px | LEFT = 4px 
margin: 12px 16px 0; // TOP = 12px | RIGHT = 16px | BOTTOM = 0px | LEFT = 16px 
margin: 8px 16px; // TOP = 8px | RIGHT = 16px | BOTTOM = 8px | LEFT = 16px 
margin: 8px; // TOP = 8px | RIGHT = 8px | BOTTOM = 8px | LEFT = 8px 

Valores permitidos para o margin: <length> (px), <percentage> (%), auto (cálculo automatizado da margin)

# margin collapsing: Quando o top se junta ao bottom.
exemplo em block:

div {
   margin-bottom: 15px;             
}                             
div {
   margin-top: 10px;
}
- nesse exemplo, a margem em block será de 15px apenas e não 25px(10+25), pois ele considera o maior,
  porém, se fosse em inline, os valores de margem seriam somados:

div {
   display: inline;
   margin-right: 15px;
}
div {
   display: inline;
   margin-left: 10px;
}
- A margem final seria 25px (15 + 10)


# PADDING
- Segue o mesmo esquema da margin (bottom, top, left, right), o padding é o preenchimento interno da caixa.
- O padding pode ter valores (values) de comprimento (px, em, rem) ou de porcentagem (%).

# BORDER-OUTLINE
- São as bordas da caixa, todo o em volta dela.
- Você pode atribuir -> border: <border-style> | <border-width> | <border-color>

tipos de style para a borda: solid (mais comum) | dotted | dashed | double | groove | ridge | inset | outset

CUIDADO! ao botar uma largura, você soma os px com o tamanho da caixa.
Para continuar com o tamanho definido da caixa, use box-sizing: border-box;

# E o outline?
O outline é muito semelhante ao border, mas difere em 4 sentidos:
Não modifica o tamanho da caixa, pois não é parte do Box Model
Poderá ser diferente de retangular
Não permite ajuste individuais
Mais usado pelo user agent para acessibilidade
