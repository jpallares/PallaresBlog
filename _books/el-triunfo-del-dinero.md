---
title: El triunfo del dinero
bookauthor: Niall Ferguson
date: 2022-12-30
header:
  teaser: https://covers.openlibrary.org/b/isbn/8483068133-L.jpg
quotes:
  - date: 2022-12-30
    chapter: 
    quote: Los incas no entendían la insaciable ansia de oro y plata que parecía poseer a los europeos. «Aunque toda la nieve de los Andes se convirtiera en oro, seguirían sin estar satisfechos», se quejaba Manco Cápac.10 Los incas no podían apreciar que, para Pizarro y sus hombres, la plata era algo más que un metal brillante y decorativo. Podía convertirse en dinero&#58; una unidad de cuenta, una reserva de valor; en otras palabras, poder fácilmente transportable.
  - date: 2022-12-30
    chapter: 
    quote: El «real de ocho» o «peso duro» español, que se basaba en el taler alemán (del que más tarde se derivaría el dólar estadounidense), se convirtió en la primera moneda realmente global del mundo, financiando no solo las prolongadas guerras que España libró en Europa, sino también el comercio, en rápida expansión, de Europa con Asia.
  - date: 2022-12-30
    chapter: 
    quote: En la época romana se fabricaron monedas con tres metales distintos&#58; el áureo (de oro), el denario (de plata) y el sestercio (de bronce), que se clasificaban en ese mismo orden en función de la escasez relativa de los metales en cuestión, aunque todas llevaban la efigie del emperador reinante en un lado y las legendarias figuras de Rómulo y Remo en el otro.
  - date: 2022-12-30
    chapter: 
    quote: la aportación más importante de Fibonacci fue la introducción del sistema de numeración indoarábigo. No solo dio a Europa el sistema decimal, que hace mucho más fácil que con los números romanos cualquier clase de cálculo; también mostró cómo este podía aplicarse a la contabilidad comercial, a las conversiones de moneda y —de manera fundamental— al cálculo del interés.
  - date: 2022-12-30
    chapter: 
    quote: En 1516, las autoridades venecianas destinaron una zona especial de la ciudad para los judíos, situada en el emplazamiento de una antigua fundición de hierro, que pasaría a conocerse como el ghetto nuovo (el actual término italiano getto —que en el siglo XIV se escribía gheto— significa literalmente «fundición», «fraguado»).
  - date: 2022-12-30
    chapter: 
    quote: Para cuando Pío II fue nombrado papa, en 1458, el hijo de Giovanni, Cosimo de’ Medici y el Estado florentino venían a ser prácticamente lo mismo. Como diría el propio papa&#58; «Las cuestiones políticas se deciden en su casa. El hombre que él elige ocupa el poder. […] Él es quien decide la paz y la guerra y controla las leyes. […] Él es rey en todo menos en el nombre».
  - date: 2022-12-30
    chapter: 
    quote: En conjunto, en vísperas de la Primera Guerra Mundial, los depósitos de residentes en bancos ingleses totalizaban casi 1.200 millones de libras, frente a un total de billetes en circulación de solo 45,5 millones de libras. El dinero estaba ahora principalmente en los bancos, fuera de la vista, aunque nunca fuera de la mente.
  - date: 2022-12-30
    chapter: 
    quote: a finales del siglo XVI y durante todo el XVII la Corona española se convirtió en una grave morosa, suspendiendo total o parcialmente los pagos a sus acreedores en 1557, 1560, 1575, 1596, 1607, 1627, 1647, 1652 y 1662.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
