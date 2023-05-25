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

