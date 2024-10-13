---
title: Siega
bookauthor: Neal Shusterman
date: 2024-09-19
header:
  teaser: 
quotes:
  - date: 2024-08-30
    chapter: 
    quote: reconozco que he reiniciado el contador cuatro veces. Mi edad natural ronda los ciento ochenta años, aunque he olvidado el número exacto. En los últimos tiempos he elegido esta apariencia venerable porque he descubierto que aquellos a los que cribo encuentran consuelo en ella. —Entonces se rió—. Me toman por alguien sabio.
  - date: 2024-09-10
    chapter: 
    quote: El mayor logro de la raza humana no fue conquistar la muerte, sino acabar con el Gobierno. En la época en que la red digital del mundo se llamaba la nube, la gente creía que darle demasiado poder a una inteligencia artificial sería una idea muy mala. Abundaban las historias aleccionadoras en todo tipo de medios. Las máquinas siempre eran el enemigo. Pero entonces la nube evolucionó para convertirse en el Nimbo al adquirir consciencia de sí misma o algo similar, y ocurrió todo lo contrario de lo que temía la gente&#58; el Nimbo no se hizo con el poder. En su lugar, fueron los humanos los que llegaron a darse cuenta de que estaba mucho más preparada que los políticos para gestionarlo todo.
  - date: 2024-09-11
    chapter: 
    quote: Está de viaje de ida o de vuelta a casa? —preguntó la mujer que tenía a su lado, en el 15A. No había 15B; el concepto del asiento B, en el que uno debía sentarse entre otros dos pasajeros, se había eliminado junto con otros detalles desagradables, como las enfermedades y el Gobierno.
  - date: 2024-09-11
    chapter: 
    quote: Aprendieron los movimientos básicos del bokator viuda negra, una versión letal de la milenaria arte marcial camboyana desarrollada específicamente para la Guadaña. Los dejaba exhaustos, aunque nunca habían sido tan fuertes.
  - date: 2024-09-13
    chapter: 
    quote: Entonces anunciaban su histórico patrono, el personaje célebre de la historia cuyo nombre adoptaban. El cónclave aplaudía tras cada anuncio y, así, aceptó a los segadores Goodall, Schrödinger y Colbert en la Guadaña midmericana.
  - date: 2024-09-14
    chapter: 
    quote: Lo que significaba que, en algún punto de su memoria, acechaba una grabación de los movimientos de Faraday el día en que había acabado con su vida. Citra sabía que realizar el seguimiento de dichos movimientos quizá fuera una tarea inútil, pero ¿y si el segador no había decidido cribarse?
  - date: 2024-09-19
    chapter: 
    quote: chico dejó que su entrenamiento tomara el control. «Soy el verdugo», se dijo. Y, en aquel momento, lo era&#58; un verdugo, un arma mortífera. Chomsky y Rand se defendieron, pero por muy buenos que fueran, no eran rivales para un verdugo tan preciso como él. La hoja de Rowan le dejó un profundo corte a Rand y ella le quitó la espada de la mano de una certera patada de bokator. Rowan respondió con otra aún más efectiva que le rompió la columna. Chomsky le prendió fuego a un brazo usando el lanzallamas, pero el chico rodó por el suelo para apagarlo. Después cogió la maza de entonar que había junto al altar y la dejó caer sobre el segador novato como si del martillo de Thor se tratara, machacándolo una y otra vez como si diera la hora, hasta que el coadjutor le cogió la mano para detenerlo. —Ya basta, hijo. Está muerto. Rowan soltó la maza. Sólo entonces se permitió bajar la guardia.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
