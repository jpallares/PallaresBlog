---
title: Baby-led weaning
bookauthor: Begoña Prats
date: 2024-03-24
header:
  teaser: https://ia800505.us.archive.org/view_archive.php?archive=/35/items/l_covers_0014/l_covers_0014_16.zip&file=0014167022-L.jpg
quotes:
  - date: 2024-03-21
    chapter: 
    quote: Además, la OMS (Organización Mundial de la Salud) y la AEPED recomiendan la lactancia materna (o en su defecto, la lactancia artificial) en exclusiva hasta los seis meses y de manera complementaria al menos hasta los dos años.
  - date: 2024-03-21
    chapter: 
    quote: Tomar cualquier otro alimento, incluso agua o infusiones, hará que su pequeño estómago quede lleno y no haya espacio para lo que realmente le hará crecer&#58; la preciada leche.
  - date: 2024-03-21
    chapter: 
    quote: No lo conocen, no lo echarán de menos. Mucha gente os dirá cosas como que un bebé necesita azúcar para el desarrollo del cerebro (¡azúcar no!; glucosa, presente hasta en las verduras), que por una vez no pasa nada, que tarde o temprano tendrá que ir a un cumpleaños y ahí se pondrá morao… Bueno, pues no, no podemos aislarlo del mundo, pero al inculcarle hábitos saludables, en muchas ocasiones preferirá una fruta a cualquier dulce. Doy fe.
  - date: 2024-03-21
    chapter: 
    quote: Hay que entender que igual que nuestros hijos no necesitan sal para aderezar los alimentos, no necesitan azúcar. No lo conocen, no lo echarán de menos. Mucha gente os dirá cosas como que un bebé necesita azúcar para el desarrollo del cerebro (¡azúcar no!; glucosa, presente hasta en las verduras), que por una vez no pasa nada, que tarde o temprano tendrá que ir a un cumpleaños y ahí se pondrá morao… Bueno, pues no, no podemos aislarlo del mundo, pero al inculcarle hábitos saludables, en muchas ocasiones preferirá una fruta a cualquier dulce. Doy fe.
  - date: 2024-03-24
    chapter: 
    quote: Le ofreceremos alimentos saludables adecuados. Nada excesivamente duro, pequeño o redondo como manzana o zanahoria cruda, frutos secos y uvas o cerezas enteras.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
