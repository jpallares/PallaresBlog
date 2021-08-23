---
title: El Cisne Negro
bookauthor: Nassim Taleb
date: 2017-05-26
header:
  teaser: https://covers.openlibrary.org/b/openlibrary/OL15168636W-L.jpg
quotes:
  - date: 2017-05-10
    quote: De aquí que la misma condición que nos hace simplificar nos empuja a pensar que el mundo es menos aleatorio de lo que realmente es. Y el Cisne Negro
  - date: 2017-05-26
    quote: Es verdad que no cabe esperar mucho de psicólogos como los de 1965, pero parece que estos resultados se repiten en todas las disciplinas.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
