---
title: Bushido
bookauthor: Inazō Nitobe
date: 2023-03-11
header:
  teaser: https://covers.openlibrary.org/b/isbn/9781599869131-L.jpg
quotes:
  - date: 2023-03-11
    chapter: 
    quote: Siendo una minoría exclusiva y privilegiada que comprendía solo el 5 por ciento de la población, los samuráis promovieron la Restauración Meiji (1868), que sustituyó su autoridad militar por la imperial. Las diferencias de clase se eliminaron, pero los antiguos samuráis permanecieron a la vanguardia de la modernización de Japón, y algunos aspectos de su legado se conservaron o reinventaron en la creación de una nueva identidad nacional.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
