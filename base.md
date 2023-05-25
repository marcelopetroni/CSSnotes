# BASE CSS ROCKEATSEAT

- Comentários: começam com '/*' e terminam com o inverso: '*/'
- Para conectar CSS com HTML, botar diretamente o código css na tag <style></style> dentro do head do HTML ou :
criar um arquivo css e no HTML, no head, adicionar a tag:
<link rel="stylesheet" type="text/css" href="teste.css" (referência do arquivo css)>

- Esqueleto: 

Elemento {
        propriedade: valor; (não esquecer ponto e vírgula)
        propriedade: valor;
        propriedade: valor;
}

# Seletores:
- ' * ' : o asterístico (global) indica todos os elementos (h1, p, etc)

        * {
                margin: 0; (espaçamento por fora)
        }

- quer alterar um elemento específico e não todas as ocorrências dele?
pode ser especificado através das tags <div id = "x"> </div> designando um nome no html e especificando ela no css por '#'
# Exemplo:

HTML:
<div id = "nome">
    <h1>Título</h1>
</div>

CSS:
#nome {
    width: 200px; (largura do título especificado)
}

- Ou também usar a designação class no HTML para modificar algo e ".nomeClass:" no CSS:
HTML:
<div class = "m-40">
    <h1>Título</h1>
</div>

CSS:
.m-40 {
    margin: 40px;
}

# É possível especificar mais de um elemento no mesmo bloco no css:
h1, h2 {
    width: 200px; (largura do título especificado)
}