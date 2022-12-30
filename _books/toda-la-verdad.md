---
title: Toda la verdad
bookauthor: Mike Tyson
date: 2022-12-30
header:
  teaser: https://covers.openlibrary.org/b/isbn/0007502524-L.jpg
quotes:
  - date: 2022-12-30
    chapter: 
    quote: —Puto maricón. No me pateaste el culo. Sólo me alcanzaste con un puñetazo a traición —dijo. —Ah, ¿así que te golpeé una vez y me bastó para fulminarte, hundiéndote un lado de la cara, rompiéndote dientes, costillas y lo demás?
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
