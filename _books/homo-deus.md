---
title: Homo Deus
bookauthor: Yuval Noah Harari
date: 2019-05-19
header:
  teaser: https://covers.openlibrary.org/b/isbn/0062464345-L.jpg
quotes:
  - date: 2019-05-19
    quote: En Perú, Guatemala, Filipinas y Albania (países en vías de desarrollo con pobreza e inestabilidad política), cada año se suicida una de cada 100.000 personas. En países ricos y pacíficos como Suiza, Francia, Japón y Nueva Zelanda, anualmente se quitan la vida 25 de cada 100.000 personas.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
