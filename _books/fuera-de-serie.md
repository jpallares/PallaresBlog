---
title: Fuera de serie
bookauthor: Malcolm Gladwell
date: 2022-05-07
header:
  teaser: https://covers.openlibrary.org/b/olid/OL23157209M-L.jpg
quotes:
  - date: 2022-04-26
    quote: trasplantar la cultura campesina de la Italia meridional a las colinas de Pensilvania oriental, los rosetinos habían creado una poderosa estructura social de protección capaz de aislarlos de las presiones del mundo moderno. Estaban sanos por ser de donde eran, por el mundo que habían creado para sí en su pequeña comunidad de las colinas.
  - date: 2022-04-26
    quote: Vieron cómo los rosetinos se visitaban unos a otros, se paraban a charlar en italiano por la calle o cocinaban para sus vecinos en los patios traseros. Aprendieron el ámbito de los clanes familiares que formaban la base de la estructura social. Observaron cuántas casas tenían tres generaciones viviendo bajo el mismo techo, y el respeto que infundían los viejos patriarcas.
  - date: 2022-05-01
    quote: en cualquier equipo de la elite del hockey —la flor y nata—, el 40 por ciento de los jugadores habrá nacido entre enero y marzo; el 30 por ciento, entre abril y junio; el 20 por ciento, entre julio y septiembre; y el 10 por ciento, entre octubre y diciembre.
  - date: 2022-05-01
    quote: Pero la mayor parte de los padres, se barrunta uno, piensan que cualquier desventaja que un niño más joven afronte en el jardín de infancia acabará por diluirse, ¿no? Pues no. Pasa como con el hockey, que persiste la pequeña ventaja inicial que el niño nacido en la primera mitad del año tiene sobre el niño nacido en la segunda. Encierra a los niños en una dinámica de logro contra frustración, de estímulo contra desaliento, que se prolonga sin cesar durante años.
  - date: 2022-05-07
    quote: Sus investigaciones sugieren que una vez que un músico ha demostrado capacidad suficiente para ingresar en una academia superior de música, lo que distingue a un intérprete virtuoso de otro mediocre es el esfuerzo que cada uno dedica a practicar. Y eso no es todo&#58; los que están en la misma cumbre no es que trabajen un poco o bastante más que todos los demás. Trabajan mucho… mucho más.
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
