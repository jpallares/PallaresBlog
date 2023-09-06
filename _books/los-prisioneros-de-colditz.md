---
title: Los prisioneros de Colditz
bookauthor: Ben Macintyre
date: 2023-04-22
header:
  teaser: 
quotes:
  - date: 2023-04-15
    chapter: 
    quote: Un total de ciento cuatro prisioneros habían tratado de huir en cuarenta y nueve intentos, pero solo lo habían logrado quince. Los franceses iban en cabeza con diez triunfos, seguidos de los neerlandeses con cuatro y los polacos con uno. Los británicos y los belgas eran los últimos, ya que no habían logrado una sola fuga. Unos treinta y cinco prisioneros británicos habían intentado escapar, pero solo dos habían rebasado los muros del castillo y ninguno había conseguido salir.
  - date: 2023-04-16
    chapter: 
    quote: La guerra siempre consigue encontrar empleos útiles a personas que en tiempos de paz serían tachadas de raras e inadaptadas.
  - date: 2023-04-22
    chapter: 
    quote: El grand cru de Farr era el Chateau Colditz, un vino espumoso semiseco creado mediante el méthode champenoise, ideado en 1863 por Veuve Clicquot, la gran dama del champán.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
