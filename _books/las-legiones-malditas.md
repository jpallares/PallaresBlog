---
title: Las legiones malditas
bookauthor: Santiago Posteguillo
date: 2017-10-07
header:
  teaser: https://covers.openlibrary.org/b/isbn/9788466637688-L.jpg
quotes:
  - date: 2017-10-07
    quote: Aquél cuyos oídos están tan cerrados a la verdad hasta el punto que no puede escucharla de boca de un amigo, puede darse por perdido.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
