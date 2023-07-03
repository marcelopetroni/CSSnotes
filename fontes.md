# Fontes
- Define o tipo de fonte por: font-family
- Tem ordem de prioridade, você bota o tipo de fonte, ex: Arial, e se não achar, pula pra próxima opção, veja:

p {
    font-family: Arial-14 (primeira tentativa de fonte), Times (segunda), serif (terceira);
}

- nesse caso, a fonte "Arial-14" deve estar no computador
- serif seria os traços que botam abaixo/aos lados/ect de por exemplo o número 1, só que em letras.

# Peso fonte
- Define o quão negrito uma fonte deve ser renderizada.
- Valores: normal | bold | bolder | lighter | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900
- Dependendo da família da fonte não conseguimos utilizar todos os pesos de fonte.

p {
    font-weight: bold;
}

# Estilo da fonte
- Valores: normal | italic | oblique

p {
    font-style: italic;
}

# Fonte size
- Tamanho da fonte.
p {
    font-size: 12px;
}

# OBS IMPORTANTE:
- Nem todas as fontes vão estar no computador do seu cliente, import suas fontes no seu programa através de:
@font-face
@import
link (maneira mais rápida, melhor usar no HTML)

# Font-variant
- Usado quando quiser mudar as letras minusculas para um estilo maisculo so que menor.
Smallcaps replaces lowercase letters with small caps - uppercase-like, yet tiny, small capital letters.

p {
    font-variant: small-caps;
}

# Font-stretch
- Alarga ou estreita a fonte (seu tamanho horizontalmente)
- Aceita palavras-chaves como: expanded, condensed, normal
- Aceita porcentagens de 50% a 200%

p {
    font-stretch: 50%;
}

# ESPAÇAMENTO
- Muda o espaçamento entre as letras/palavras/linhas/etc.
- Letter spacing para letras e Word-spacing para palavras.
- Line-height é o espaçamento entre linhas de um texto.
- text-transform, transformação do texto:
Valores podem ser: none | capitalize | uppercase | lowercase | full-width | full-size-kana

p {
    letter-spacing: 4px;
    word-spacing: 4px;
    line-height: 1.5;
    text-transform: uppercase;
}

# DECORAÇÕES
- Aparência decorativa de um texto
line: underline | overline (Linha no meio do texto, cortando) | line-through
- Pode escolher uma cor botando em seguida.

h1 {
	text-decoration: underline blue;
}

# Alinhamento do texto
- Alinhamento de um texto
- Valores: start | end | left | right | center | justify | match-parent

p {
    text-align: center;
}

# Text-shadow
- Sombra aplicada a um texto (no estilo placa de hollywood com uma sombra)

p {
  text-shadow: 1px 1px 1px red,
	       2px 2px 1px green; /* offset-x | offset-y | blur-radius | color */
}

# OBS IMPORTANTE:
- É possível usar todas essas propriedades juntas em apenas uma: font

p {
    font: italic normal bold normal 3em/1.5 Helvetica, Arial, sans-serif;
}