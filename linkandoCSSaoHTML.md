# LINK ENTRE CSS E HTML:

os principais:
- por meio de "class = nome" no HTML e .nome {} no CSS
- por meio de "id = algo" no HTML e #algo {} no CSS
- também é possível atribuir valores no css a diversos class, ids, afins:

#algumID, .algumClass {

}

# Quer que a cor mude ao passar o mouse em cima?
- use ": hover":

#algumID: hover {
    color red;
}

#  Quer acessar um item específico de um blocono CSS? 

<body>
  <ul>
    <li>Item 1</li>
    <ul>
      <li>Item 2</li>
    </ul>
  </ul>
</body>

body > ul > li {
	color: blue;
}

" > " entre dois seletores seleciona somente o elemento que é filho direto do pai
- é tipo acessar uma pasta dentro de outra.

h1 + p {
	color: red;
}
" + " para acessar o elemento ao lado direito que é irmão direto.

