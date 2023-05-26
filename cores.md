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