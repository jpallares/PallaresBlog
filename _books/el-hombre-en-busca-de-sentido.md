---
title: El hombre en busca de sentido
bookauthor: Victor Frankl
date: 2021-04-27
header:
  teaser: https://covers.openlibrary.org/b/isbn/067166736X-L.jpg
quotes:
  - date: 2021-04-17
    quote: hayan creído), sino que cuenta esa otra multitud de pequeños tormentos. En otras palabras, pretende dar respuesta a la siguiente pregunta&#58; ¿Cómo incidía la vida diaria de un campo de concentración en la mente del prisionero medio? Muchos de los sucesos que aquí se describen no tuvieron lugar en los grandes y famosos campos, sino en los más pequeños, que es donde se produjo la mayor experiencia del exterminio. Tampoco es un libro sobre el sufrimiento y la muerte de grandes héroes y mártires, ni sobre los preeminentes «capos» —prisioneros que actuaban como especie de administradores y tenían privilegios especiales— o los prisioneros de renombre. Es decir, no se refiere tanto a los sufrimientos de los poderosos, cuanto a los sacrificios, crucifixión y muerte de la gran legión de víctimas desconocidas y olvidadas, pues era a estos prisioneros normales y corrientes, que no llevaban ninguna marca distintiva en sus mangas, a quienes los «capos» realmente despreciaban. Mientras estos prisioneros comunes tenían muy poco o nada que llevarse a
  - date: 2021-04-20
    quote: al hombre se le puede arrebatar todo salvo una cosa&#58; la última de las libertades humanas —la elección de la actitud personal ante un conjunto de circunstancias— para decidir su propio camino.
  - date: 2021-04-27
    quote: Sólo muy lentamente se podía devolver a aquellos hombres a la verdad lisa y llana de que nadie tenía derecho a obrar mal, ni aun cuando a él le hubieran hecho daño.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
