---
title: OPEN&#58; Memorias
bookauthor: Andre Agassi
date: 2021-12-18
header:
  teaser: https://covers.openlibrary.org/b/isbn/9780307268198-L.jpg
quotes:
  - date: 2021-12-16
    quote: Por favor, que acabe todo esto. No estoy listo para que acabe.
  - date: 2021-12-16
    quote: estrella un revés contra la red. Juego para Agassi. Durante el cambio de campo, miro a Baghdatis, que se ha sentado. Craso error el suyo. Un error de juventud. Cuando uno tiene un calambre, no debe sentarse nunca. No hay que decirle nunca al cuerpo que es hora de descansar para después añadir&#58; «¡Era broma!». El cuerpo es como el gobierno, que dice&#58; «Tú haz lo que quieras, pero si te pillamos, no nos mientas». Así que no va a ser capaz de servir. No va a ser capaz de levantarse de esa silla.
  - date: 2021-12-16
    quote: Durante el cambio de campo, miro a Baghdatis, que se ha sentado. Craso error el suyo. Un error de juventud. Cuando uno tiene un calambre, no debe sentarse nunca. No hay que decirle nunca al cuerpo que es hora de descansar para después añadir&#58; «¡Era broma!». El cuerpo es como el gobierno, que dice&#58; «Tú haz lo que quieras, pero si te pillamos, no nos mientas». Así que no va a ser capaz de servir. No va a ser capaz de levantarse de esa silla.
  - date: 2021-12-18
    quote: Mi padre dice que, cuando boxeaba, siempre intentaba recibir el mejor golpe de su adversario. Un día, en la pista de tenis, me dice&#58; cuando sabes que acabas de recibir el mejor puñetazo de tu contrincante y sigues en pie, y el otro tipo lo sabe, acabas arrancándole el corazón. En tenis, dice, la regla es la misma. Ataca la fortaleza del rival. Si se le da bien el saque, anula su saque. Si su fuerte es la potencia, sé más potente que él. Si tiene un gran drive, si se vanagloria de su drive, ve a por su drive hasta que llegue a odiarlo.
  - date: 2021-12-18
    quote: dado que la mayoría de los tenistas se enorgullecen de su saque, mi padre me convierte en un experto en contragolpes, en un experto en restar el saque.
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
