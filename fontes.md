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

