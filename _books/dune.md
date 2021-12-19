---
title: Dune
bookauthor: Frank Herbert
date: 2021-09-11
header:
  teaser: https://covers.openlibrary.org/b/isbn/9780425036983-L.jpg
quotes:
  - date: 2021-08-23
    quote: —El rey vuelve a estar ahogado
  - date: 2021-08-27
    quote: Paul tuvo aún una última visión de Idaho de pie ante un racimo de uniformes Harkonnen... sus gestos eran aún firmes y controlados, pero su rizada cabellera negra estaba marcada por una mortal flor escarlata. Después la puerta se cerró, y Kynes la atrancó.
  - date: 2021-08-28
    quote: —El miedo mata la mente. El miedo es la pequeña muerte que conduce a la destrucción total. Afrontaré mi miedo. Permitiré que pase sobre mí y a través de mi. Y cuando haya pasado, giraré mi ojo interior para escrutar su camino. Allá donde haya pasado el miedo ya no habrá nada. Sólo estaré yo.
  - date: 2021-08-28
    quote: Los instrumentos del poder deben estar siempre afilados y a punto. Poder y miedo... afilados y a punto.
  - date: 2021-08-31
    quote: —Arrakis es un planeta de un solo cultivo —dijo su padre—. Un solo cultivo. Esto mantiene a una clase dominante, que vive como siempre han vivido las clases dominantes, aplastando bajo ellas a una masa semihumana de medio esclavos que sobreviven de lo que ellas desechan. Son esas masas y esos desechos los que ocupan nuestra atención. Tienen mucho más valor del que nunca se ha sospechado.
  - date: 2021-09-01
    quote: Los Fremen eran supremos en aquella cualidad que los antiguos llamaban «spannungsbogen»... que es la demora que se impone uno mismo entre el deseo de algo y el acto de conseguirlo.
  - date: 2021-09-04
    quote: Una hipno-ligazón en la psique de Feyd-Rautha y su hijo en mi seno... y podremos irnos.
  - date: 2021-09-06
    quote: ¡La bruja está viva!, pensó Gurney. ¡Está viva, aquella sobre la que juré vengarme! Y es obvio que el Duque Paul ignora qué clase de criatura le ha dado a luz. ¡La diablesa!
  - date: 2021-09-11
    quote: Allí estaba la consciencia racial que había ya experimentado, con su terrible finalidad.
  - date: 2021-09-11
    quote: había visto a Fenring en las tramas de su presciencia. Fenring era uno de aquellos que hubiera-podido-ser, un potencial Kwisatz Haderach, malogrado por una mancha en su esquema genético... un eunuco, cuyo talento estaba concentrado furtivamente, secretamente.
  - date: 2021-09-11
    quote: —Te juro —murmuró— que no necesitarás ningún título. Aquella mujer será mi esposa y tú tan sólo una concubina porque esto es un asunto político y debemos sellar la paz y aliarnos con las Grandes Casas del Landsraad. Las formalidades serán respetadas. Pero aquella princesa no obtendrá de mí más que el nombre. Ningún hijo, ninguna caricia, ninguna mirada, ningún instante de deseo. —Dices eso ahora —murmuró Chani. Miró a la rubia princesa a través de la estancia. —¿Tan poco conoces a mi hijo? —susurró Jessica—. Mira a esa princesa inmóvil, allí, tan orgullosa y segura de si misma. Dicen que tiene pretensiones literarias. Esperemos que puedan llenar su existencia, porque va a tener muy poca cosa más. —Se le escapó una amarga sonrisa—. Piensa en ello, Chani&#58; esa princesa tendrá el nombre, pero será mucho menos que una concubina... nunca conocerá un momento de ternura por parte del hombre al que estará unida. Mientras que a nosotras, Chani, nosotras que arrastramos el nombre de concubinas... la historia nos llamará esposas. FIN
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
