---
title: Trilogía de la fundación
bookauthor: Isaac Asimov
date: 2022-04-20
header:
  teaser: https://covers.openlibrary.org/b/olid/OL32351593M-L.jpg
quotes:
  - date: 2022-02-23
    quote: es el que ha dispuesto el exilio, ¿por qué? ¿Es que ya
  - date: 2022-03-20
    quote: No me dejaron nada, porque había contribuido a expulsar a un gobernador rebelde y privado a un almirante de su gloria.
  - date: 2022-04-08
    quote: —¡Por la Galaxia! Déjeme contarlo a mi manera, pequeña criatura ofensiva. No hable por mi boca ni replique a cada frase mía o saldré de aquí inmediatamente y dejaré que todo se derrumbe a su alrededor. Recuerde, incalificable necio, que la Fundación perdurará porque así ha de ser, pero si yo salgo ahora mismo de aquí, usted no perdurará.
  - date: 2022-04-11
    quote: —Quiero decir que es fácil para él inspirar, por ejemplo, en un general, la emoción de completa lealtad al Mulo y de completa fe en la victoria del Mulo. Sus generales están controlados emocionalmente. No pueden traicionarle, no pueden flaquear... y el control es permanente. Sus enemigos más inteligentes se convierten en sus más fieles subordinados. El señor guerrero de Kalgan le entregó su planeta y se convirtió en virrey de la Fundación.
  - date: 2022-04-11
    quote: La Segunda Fundación era un mundo de científicos mentales. Era la imagen reflejada de nuestro mundo. La psicología, y no la física, predominaba. —Y triunfalmente—&#58;
  - date: 2022-04-14
    quote: »El segundo es que desconocíamos sus defectos físicos, en particular el que usted consideraba tan importante y por el que adoptó el nombre de Mulo. No previmos que no era simplemente un mutante, sino además un mutante estéril, y que padecía una distorsión psíquica debido a su complejo de inferioridad. Sólo adivinamos la megalomanía, y no una intensa paranoia psicopática al mismo tiempo.
  - date: 2022-04-17
    quote: —Bien, si algún día se va a casar, mátelo. Me refiero a su novio. —Miró gravemente a los ojos del otro—. Hablo en serio. La vida no puede contener un horror más grande que vivir con la persona que será cuando tenga veinte años. No es mi intención ofenderle, naturalmente. —No me ha ofendido. Creo que sé a qué se refiere.
  - date: 2022-04-20
    quote: Huía de una mujer frágil que la había ayudado a escapar, de una criatura que la había cargado de dinero y joyas, que había arriesgado su vida para salvarla. Huía de una persona de la cual sabía, con absoluta certeza, que era una mujer de la Segunda Fundación.
  - date: 2022-04-20
    quote: Por razones desconocidas para los miembros de la Galaxia, el Tiempo Medio Intergaláctico define su unidad fundamental, el segundo, como el tiempo que la luz emplea en recorrer 299.776 kilómetros. Por otro lado, 86.400 segundos son arbitrariamente igualados a un Día Medio Intergaláctico; y 365 de esos días, a un Año Medio Intergaláctico. ¿Por qué 299.776, 86.400 o 365?
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
