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

## Elementos inline, block e inline-block
Um elemento pode ocupar o espaço na tela de 3 maneiras diferentes. Ele pode ser block, inline ou inline-block.

## Posicionamento
Existe 5 tipos de posições:

* static(default);
* relative;
* fixed;
* absolute;
* sticky;

Para modificar o posicionamento se utiliza 'position: posicionamento'.

### static
É a posição padrão da página e não pode ser modificada.

### relative

<ul>
<li>Possui a posição relativa à posição normal.</li>
<li>Definir as propriedades top, right, bottom e left de um elemento relative fará com que ele seja ajustado para fora de sua posição normal.</li>
<li>Outros conteúdos não serão ajustados para caber em qualquer lacuna deixada pelo elemento.</li>
</ul>

### Absolute

Um elemento absoluto é removido do fluxo normal e terá sua posição relativa a página se o mesmo não estiver dentro de algum container com posição diferente de static.

Como ele é removido do fluxo normal, outros elementos preenchem a lacuna que ele deixou.

### Fixed
Um elemento com position: fixed; está posicionado em relação à janela de visualização, o que significa que sempre permanece no mesmo lugar, mesmo que a página seja rolada.

Como ele é removido do fluxo normal, outros elementos preenchem a lacuna que ele deixou.

### Sticky
Um elemento sticky alterna entre relative e fixed, dependendo da posição de rolagem.

Ele é posicionado relativo até que uma determinada posição de deslocamento seja encontrada na viewport, então ele "gruda" no lugar (como position:fixed).

#### Nota
<ul>
<li>O Internet Explorer não suporta posicionamento sticky.</li>
<li>O Safari requer um prefixo -webkit-.</li>
<li>Você também deve especificar pelo menos um entre top, right, bottom e left para que o posicionamento fixo funcione.</li>
</ul>

### Controle de empilhamento
Quando uma posição fica acima da outra e você quer decidir qual sobrepõe a outra você pode utilizar z-index para decidir qual irá aparecer primeiro.

## Links
 Os links possuem 4 diferentes estados, eles são:

<ul>
<li>a:link - um normal, link não visitado;</li>
<li>a:visited - um link que o usuário já visitou;</li>
<li>a:hover - o link quando o usuário para o mouse em cima;</li>
<li>a:active - o link quanto é clicado;</li>
</ul>

## Especificação de seletores
Tem momentos que você deseja fazer modificações específicas em lugares específicos, como um menu de links.

### Seletor do filho
Exemplo: 
    
    li>a

Só afeta os links diretamente dentro do li, se tiver por exemplo um <span><a href=""></a></span> o link não será modificado

### Seletor Descendente
Exemplo:

    p a

Afeta todos os descendentes &a> dentro do &lt;p>, portanto, diferente do filho, não importa se o &lt;a> estiver dentro de outro elemento, contando que o &lt;a> esteja dentro do &lt;p> o &lt;a> será modificado.

### Seletor de irmão
Exemplo:

    h1+p

Seleciona o primeiro elemento &lt;p> que esteja diretamente abaixo de h1 &lt;h1>

Se tiver qualquer tag entre eles, o &lt;p> não será modificado

### Irmão geral
Exemplo:

    h1~p

A diferença do seletor de irmão é que afetará todos os &lt;p> que estejam diretamente embaixo do &lt;h2>.

## Parallax
Parallax é um efeito visual usado para manipular a percepção do usuário no background.

Para adquiri-lo, costuma-se usar javascript, mas também é possível com CSS3

    height: 100%;
    O height do html, body, e dos containers das imagens tem que ser 100%;

    background-repeat: no-repeat;
    Para as imagens não se repetirem;

    background-size: cover;
    Para o background cobrir todo o container;

    background-position: center;
    Centralize a imagem no container;

    background-attachment: fixed;
    Deixar a imagem fixa, principal fator para o efeito parallax;
