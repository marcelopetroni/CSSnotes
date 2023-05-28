# CORES
- Usamos CSS para alterar cores do nosso documento.
- Pode ser usado: palavra-chave (blue, transparent), funções: rgb, rgba, hsl, hsla, etc

# Tipos
background-color (para caixas), color (para textos), border-color (para caixas), etc

div {
    color: blue/red/pink/currentcolor..etc;
}

# RGB → Red, Green e Blue
- O alpha representa a transparência da cor.
- hexadecimal -> color: #090 // RED, GREEN, BLUE (de 0-9)

div {
    color: rgb(34, 12, 64, 0.6) // 0-255, o último representa a transparência.
}

# HSL → Hue - Saturation - Lightness
div {
    color: hsl(180, 100%, 50%, 60%) // 1º elemento: hue -> um círculo 360º de cores RGB (0º RED, 120º GREEN, 240º BLUE)
                                    // 2º elemento: saturação -> intensidade das cores. 0% -> branco
                                    // 3º elemento: lightness -> intensidade de brilho. 100% -> branco
                                    // 4º elemento: transparência que nem a função rgb.
}

color: inheritr; // Herda a cor do elemento anterior 
color: initial; // Volta a sua cor inicial 
color: unset; // Pega a cor do contexto

# BACKGROUND COLOR

# A propriedade background-color define a cor de fundo do elemento selecionado.
    background-color: blue;

# Para adicionar uma imagem como background podemos usar a propriedade background-image.
    background-image: url(link);

# Por padrão a imagem vai se repetir e podemos modificar essa opção usando a propriedade background-repeat.
    background-repeat: repeat-x; // a imagem se repete apenas no eixo x
    background-repeat: repeat-y; // a imagem se repete apenas no eixo y
    background-repeat: no-repeat; // a imagem não se repete

# background-position podemos mudar a posição da imagem do background.
    background-position: right/left/center; // escolhe a posição da imagem

# Para mudar o tamanho da imagem do background usamos a propriedade background-size.
    background-size: cover (se estica)/contain/40%/50px

# A propriedade background-origin é quem define o ponto de origem de uma imagem específica.
    background-origin: border-box;     // Começa a partir da borda
    background-origin: padding-box;    // Começa a partir do padding
    background-origin: content-box;    // Começa depois da borda

# O background-clip define se imagem/cor iniciam debaixo de sua área de borda, preenchimento ou conteúdo.
    background-clip: border-box;
    background-clip: padding-box;
    background-clip: content-box;
    background-clip: text;

# A propriedade background-attachment determina se a posição da imagem vai ser fixa ou se vai rolar junto com o conteúdo.
    background-attachment: scroll; // padrão
    background-attachment: fixed;  // fica parado no mesmo background ao rolar a página
    background-attachment: local;

# Podemos usar o shorthand background para definir todos os valores do background:
    escrever apenas "background: " e todas as propriedades acima, com exceção do size que precisa botar uma barra antes de botar o valor desejado.

    main {
        background: blue center url(link) / 50px content-box;
    }

# linear-gradient() é a função usada para criar gradient linear com o CSS.
    main {
        background: linear-gradient(45deg, red, yellow);
        background: radial-gradient(rgba(255, 255, 255, 0), rgba(255, 0, 0, 0.2)) // faz de forma circular o gradiente
    }
- é possível adicionar multiplos backgrounds aplicando vírgula.
