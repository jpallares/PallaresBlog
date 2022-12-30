---
title: Roma soy yo
bookauthor: Santiago Posteguillo
date: 2022-12-11
header:
  teaser: https://covers.openlibrary.org/b/isbn/8466671781-L.jpg
quotes:
  - date: 2022-12-03
    chapter: 
    quote: Sintió algo de dolor la primera vez. Poco. Él se mostró cuidadoso desde el principio. Le sorprendió que era muy distinto a hacerlo pagando, como había tenido ocasión de probar con alguna de las prostitutas de la propia Subura. Le sorprendió y le gustó esa sensación de entrega voluntaria de una mujer. No podía calibrar en aquel momento hasta qué punto la búsqueda de esa sensación a lo largo de su vida iba a influir en su existencia, en la de Roma y en la historia del mundo.
  - date: 2022-12-03
    chapter: 
    quote: —Nunca he estado con una egipcia de ningún tipo. —Se inclinó para besarla en la mejilla mientras le acariciaba el vientre con una mano—. Ni creo que lo esté nunca. Los dos rieron.
  - date: 2022-12-04
    chapter: 
    quote: Quizá pudiera decir algo que permitiera emitir un senatus consultum ultimum para ordenar su arresto y ejecución inmediata.
  - date: 2022-12-08
    chapter: 
    quote: Me desprecias porque me impongo con violencia. Me menosprecias porque te consideras más virtuoso que yo, pero hay algo de ti mismo, muchacho, que ni siquiera tú sabes y que yo sí veo. —Se le acercó hasta que su aliento, bien perfumado, envolvía la faz de César—. Lo que no sabes, lo que no eres capaz de intuir, es que tú eres como yo. Quizá aún no, pero tienes todos los mimbres para ser como yo y, si te dejo crecer, terminarás siendo como yo.
  - date: 2022-12-08
    chapter: 
    quote: —Eres demasiado magnánimo con todos, César —le dijo mientras le ponía la tela empapada en al frente—. Esa generosidad tuya para con todos será tu perdición un día.
  - date: 2022-12-08
    chapter: 
    quote: —En este juicio no se juzga sólo a Dolabela y sus crímenes, como he dicho. En este juicio se juzga mucho más. Y yo no soy sólo el abogado de los macedonios. Soy el abogado de Roma. Los abogados de su defensa han intentado hacernos creer que Dolabela es Roma, pero no es así. En este juicio, Roma no es Dolabela, Roma no sois vosotros, jueces. Roma y el pueblo de Roma están representados por mí. Y es que hoy, aquí y ahora, Roma soy yo. Alzó los brazos. La última clepsidra diluía sus gotas finales. El público inició una cerrada ovación.
  - date: 2022-12-09
    chapter: 
    quote: —¡Dolabela! —exclamó a continuación Sila volviéndose hacia su amigo—. Gracias, gracias, gracias por venir hasta aquí. Ya sé que implica una incomodidad enorme, pero esto es mil veces más seguro que Roma. Yo no moriré, como tantos, en una reyerta junto al foro, promovida por conjurados contra mi persona. Eso se lo dejo a otros, a los que cometen el error de fiarse de los senadores. —Y se echó a reír a mandíbula batiente.
  - date: 2022-12-10
    chapter: 
    quote: levantándose una vez más, cogió otro de esos frutos rojos y se lo llevó a la boca. —Conseguí los árboles en Cerasus. Llamaré estos frutos... cerasi.[55]
  - date: 2022-12-11
    chapter: 
    quote: —¡Tesalónica, hermana de Alejandro! ¡Quien camina por el muelle dijo que tu hermano está muerto! ¡Lo dijo alto y claro! ¡Desata sobre él y sus hombres la furia de tu rabia por tu hermano que vive y reina sobre todo y sobre todos! ¡Desata sobre él la rabia de toda Macedonia por sus crímenes e injusticias! ¡Desata sobre él la cólera de todos los dioses! ¡Arrástralo hasta el mismísimo Hades! El Tíber rugió como si mil gorgonas emergieran de sus aguas, como si Neptuno y todas las sirenas de todos los mares concentraran su furia en aquel río, en aquel punto exacto, en aquel momento. El Tíber se elevó sobre sí mismo y engulló aquel muelle con Dolabela y sus sicarios mientras el viejo senador aullaba palabras que ya nadie escuchaba&#58;
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
