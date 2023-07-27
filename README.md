# CSS3 Intermediário e Avançado

## Estilo de Caixa

height: Altura;

width: Largura;

padding: Espaçamento interno;

margin: Espaçamento Externo;

Margin/padding podem ser feitas com -top,bottom... ou colocar tudo junto em sentido horário.

### Collapse
Se um objeto estiver por exemplo com uma margin-bottom de 10px e houver outro objeto embaixo dele com uma margin-top de 5px, a distância entre eles será de 10px pois o que irá valer é a maior margin, isso se chama collapse.

## Elementos Flutuantes
Uma propriedade flutuante é usada para posicionar e formatar um conteúdo, como deixar uma imagem flutuando à esquerda de um texto em um contêiner.

A propriedade float pode ter um dos seguintes valores: left, right, none(default) e inherit(O elemento herda o valor float do seu parente).

Um elemento flutuante sai do fluxo normal do documento, podendo ficar dentro de outros elementos.

Os elementos flutuantes ficam no mesmo fluxo, então eles se afetam no posicionamento. 

Exemplo: eles ficariam um do lado do outro

Elementos flutuantes mudam de posição com o tamanho da página.

Um texto fica envolta do conteúdo, se você não quiser isso você pode utilizar o atributo clear.

### Clear
A propriedade clear específica o que acontece com o elemento próximo ao elemento flutuante.

A propriedade clear pode ter esses valores: 

* none(default);
* left(ignora elementos flutuantes a esquerda);
* right(ignora elementos flutuantes a direita);
* both(ignora elementos flutuantes de ambos os lados);
* inherit(O elemento herda o valor clear do seu parente);

Quanto você usar elementos flutuantes dentro de outros containers(divs) que tenham, por exemplo um background, ele não irá aparecer, sendo necessário por uma div clear vazia junto com os elementos.