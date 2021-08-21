---
title: El Hombre Mas Rico De Babilonia
bookauthor: Clason, George S.
date: 2021-06-25
quotes:
  - date: 2021-06-25
    quote: ¿Cómo puedes llamarte a ti mismo un hombre libre cuando tu debilidad te llevó a esto? Si un hombre tiene en su interior el alma de un esclavo, ¿no se convertirá en uno, no importa cómo nazca, ya que el agua busca su nivel? Si un hombre tiene en su interior el alma de un hombre libre, ¿no será respetado y honrado en su propia ciudad a pesar de su desgracia?
  - date: 2021-06-25
    quote: el alma de un hombre libre ve la vida como una serie de problemas a resolver y los resuelve, mientras que el alma de un esclavo
---
## *{{page.bookauthor}}*

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
