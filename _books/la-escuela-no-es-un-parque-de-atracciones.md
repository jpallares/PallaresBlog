---
title: La escuela no es un parque de atracciones
bookauthor: Gregorio Luri
date: 2023-09-05
header:
  teaser: https://covers.openlibrary.org/b/isbn/8434435691-L.jpg
quotes:
  - date: 2023-09-05
    chapter: 
    quote: ¿Cómo se alcanza a discriminar entre lo que es fiable y lo que no lo es? ¿Acaso con la ayuda de McDonald’s? Se aprende exactamente del mismo modo en que se aprende a discriminar entre buena y mala música, buena y mala literatura, bueno y mal cine, etcétera&#58; habituando el paladar. Hay que tener una cierta convivencia y aprecio por la verdad para aprender a sospechar cuándo te están dando gato por liebre. Pero hoy, hasta el director de Educación de la Fundación Santillana declara sin reparo alguno en un periódico que «transmitir la verdad ya no corresponde a la escuela».
  - date: 2023-09-05
    chapter: 
    quote: Por una parte, un sabio de origen humilde le está diciendo al sucesor de los faraones egipcios que «si quiere saber geometría, tiene que seguir el mismo duro camino que los demás mortales». Pero, por otra, está diciéndoles a los plebeyos que tienen la geometría a su alcance si quieren someterse al rigor de sus procedimientos.
  - date: 2023-09-05
    chapter: 
    quote: La actual accesibilidad a la información, en lugar de permitirnos prescindir del conocimiento, lo hace más necesario que nunca. La información se hace inteligible cuando es filtrada por nuestro conocimiento previo y se integra en el contexto de lo que ya sabemos. Nunca fue tan fácil acceder a la información, pero nunca ha sido más importante aprender a filtrarla para convertirla en conocimiento valioso. Nunca ha sido más importante la referencia significativa del texto al contexto.
  - date: 2023-09-05
    chapter: 
    quote: La actual accesibilidad a la información, en lugar de permitirnos prescindir del conocimiento, lo hace más necesario que nunca. La información se hace inteligible cuando es filtrada por nuestro conocimiento previo y se integra en el contexto de lo que ya sabemos. Nunca fue tan fácil acceder a la información, pero nunca ha sido más importante aprender a filtrarla para convertirla en conocimiento valioso. Nunca ha sido más importante la referencia significativa del texto al contexto. La información puede caer de la nube, el conocimiento no; el conocimiento es información procesada por conocimientos previos, rumiada en la memoria de trabajo y retenida en la memoria a largo plazo. Lo que ya sabemos condiciona nuestro interés. El conocimiento previo es tan activo que modela nuestra percepción, nos empuja a buscar unas informaciones en lugar de otras y ordena por su significado y relevancia lo que hayamos encontrado. Cuanto más reducido sea el conocimiento previo, más desorganizada será nuestra percepción y nuestra búsqueda y menos comprensible será lo encontrado.
  - date: 2023-09-05
    chapter: 
    quote: Wexler va más allá y defiende que un país que comprendiera la relación existente entre el conocimiento y el dominio de la lectoescritura se avergonzaría de la vacuidad de los programas escolares actuales y exigiría más historia, más ciencia, más arte y música y todo aquello que permitiera devolver a los maestros de primaria su lugar legítimo como guías para el mundo. Yo no soy tan optimista como Wexler, visto que
  - date: 2023-09-05
    chapter: 
    quote: Wexler va más allá y defiende que un país que comprendiera la relación existente entre el conocimiento y el dominio de la lectoescritura se avergonzaría de la vacuidad de los programas escolares actuales y exigiría más historia, más ciencia, más arte y música y todo aquello que permitiera devolver a los maestros de primaria su lugar legítimo como guías para el mundo.
  - date: 2023-09-05
    chapter: 
    quote: Los profesores desconfían mucho, y estoy convencido de que con toda razón, de los teóricos que no han pisado una clase en su vida. Dice Navarra&#58; «Es el comentario que más se escucha entre compañeros&#58; “Esto es inaplicable. Se ve que este no ha dado clase nunca”. Hay un abismo enorme entre el ideal que dibujan los materiales que llegan a los centros y la realidad cotidiana». La experiencia educativa debería ser el encuentro de la realidad con el laboratorio, no de la idealidad con su imposibilidad. Hablemos de los estigmatizados deberes. ¿No parece razonable pedirle al que va retrasado en una carrera que acelere si quiere alcanzar a los que van en cabeza? Pues hay pedagogos que nos vienen a decir que lo que tenemos que hacer es impedir que nadie llegue en cabeza.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
