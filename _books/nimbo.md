---
title: Nimbo
bookauthor: Neal Shusterman
date: 2024-10-11
header:
  teaser: 
quotes:
  - date: 2024-10-02
    chapter: 
    quote: Entonces, ella sonrió. No se trataba de su sonrisa habitual, sino de algo mucho más amplio y mucho más aterrador. Mucho más seductor. —Vamos a matar a un par de segadoras.
  - date: 2024-10-10
    chapter: 
    quote: La suerte es para los perdedores. Tú tienes a la historia de tu lado. Tienes la presencia. La autoridad. Eres la Gran Dama de la Muerte. —Y entonces añadió—&#58; Su excelencia. Marie no pudo reprimir la sonrisa. Aquella chica, a la que ni siquiera quería como protegida en un principio, se había convertido en su mayor defensora. En su mejor amiga.
  - date: 2024-10-11
    chapter: 
    quote: En mi Barcelona natal, los tonistas son mucho más problemáticos que aquí. Suelen atacar a los segadores, lo que nos obliga a cribarlos. Mi cuota siempre estaba repleta de tonistas a los que no deseaba cribar y que me impedían tomar mis propias decisiones. Fue uno de los motivos por los que me vine a Midmérica, aunque, últimamente, me pregunto si no llegaré a arrepentirme de esa elección.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
