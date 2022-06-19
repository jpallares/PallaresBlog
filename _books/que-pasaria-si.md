---
title: ¿Qué pasaría si…?
bookauthor: Randall Munroe
date: 2021-10-20
header:
  teaser: https://covers.openlibrary.org/b/isbn/9780544272996-L.jpg
quotes:
  - date: 2021-10-19
    quote: Munroe fue físico en la NASA antes de crear la web http&#58;//www.xkcd.com, que ha recibido más de un millón de visitas.
  - date: 2021-10-20
    quote: En el caso de un pequeño cargador de un smartphone, si no está caliente al tacto, está utilizando menos de un céntimo al año. Esto se cumple con casi cualquier aparato eléctrico
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
