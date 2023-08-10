# Informações importantes saber:

    # Quer aplicar alguma configuração ao passar o mouse em cima de algum elemento? utilize hover:

    .minhaClasse {
        // configurações
        transition: filter 0.2s;
    }

    .minhaClasse:hover {
        filter: brightness(0.9); // nesse exemplo é aplicado uma cor mais luminosa ao elemento 
        cursor: pointer; // muda a imagem cursor para uma mão apontado para sinalizar ao usuário que é apertável.

    }

    // outro exemplo que aprendi:

    minhaClasse:hover {
        transform: scale(1.1); // aumenta o elemento, invés de deixá-lo estático, ex: selecionar um filme na netflix
    }