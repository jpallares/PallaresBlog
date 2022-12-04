---
toc: true
toc_label: "Contents"
title: Calculadora de sueldo neto
tags: [sueldo, salario, neto, bruto, salary, calculator, net]
excerpt: Cómo funciona realmente el cálculo del IRPF, seguridad social, etc.
header:
  teaser: /images/tramos.jpg
lang: es
ref: sueldo-neto
---

**Esta es una actualización del artículo que publiqué el 04/07/2021**

Imagina que tienes una oferta de trabajo, un nuevo sueldo bruto anual que suena tentador, pero ¿Cúal es el neto mensual? ¿Cuál es la subida salarial exacta? Imagina que puedes comparar tu sueldo actual con el futuro simplemente arrastrando un slider, te traigo la solución:

:moneybag: [**Calculadora de sueldo neto**](https://tecalculo.com/calculadora-de-sueldo-neto){:target="\_blank"}

Si eres como yo, para calcular el sueldo neto a partir del bruto recurrías al [primer resultado de Google](https://cincodias.elpais.com/herramientas/calculadora-sueldo-neto/){:target="\_blank"}. Sin parar de hacer scroll arriba y abajo, refrescando la página que por cierto, es poco usable desde el móvil.

Y si querías hilar fino, te creas un Excel con la típica tabla de tramos y te lo calculas manual:

![Tramos IPRF Estatales](/images/tramos.jpg)

¿Ya está, no? Pues no no...para calcular bien el sueldo neto de verdad hay muchos más detalles a tener en cuenta.

Un día quise derrotar ese dragón y entender lo mejor posible como se calcula. Mientras investigaba he ido desarrollando esta [calculadora de sueldo neto](https://tecalculo.com/calculadora-de-sueldo-neto){:target="\_blank"} para validar lo que iba aprendiendo. Le faltan muchos casos y la UX es abominable pero he priorizado que sea cómodo de usar ~~y soy nefasto haciendo UX~~. Agárrate que vienen curvas.

## Conocimientos básicos primero 🧑‍🏫

Hay un especie de leyenda urbana que dice: _"Si te suben el sueldo y cambias de tramo puedes acabar cobrando menos"._ La he escuchado varias veces y explica muy bien que poca educación financiera hay en las escuelas, supongo que es más importante aprender que una persona separó los mares y multiplicó los panes...bueno, que me lío.

NO.

**Es imposible que una subida de tu sueldo implique ganar menos en neto**. Los tramos son acumulables. Ejemplo, imaginemos que Paco cobra 30000€ brutos al año:

Los primeros 12450€ tienen 19% de retención.
Lo que va entre 12450€ y 20200€, es decir, los siguientes 7750€ tienen el 24% de retención.
Finalmente, la diferencia entre 26095€ y 20200€ => 5895€ le retienen el 30%.

Siempre la primera parte del salario va a tener un retención mas baja y sube progresivamente en cada tramo. He intentado mostrar esto mediante gráficos en la [calculadora](https://tecalculo.com/calculadora-de-sueldo-neto){:target="\_blank"}, pruébala.

![Tramos explicados](/images/tramosExplicados.png)

## Gastos 🚗

Si has estado leyendo con atención, te habrás dado cuenta que la última resta no uso 30000€ y uso 26095€. Uno de los motivos son los gastos.

Hay un mínimo de gastos de 2000€, todos los calculos deben hacerse restando incialmente este valor del bruto, en el caso de Paco, tras restar los gastos nos quedan 28000€. Pero esta cifra aún no es 26095€, ¿qué falta? Seguridad Social.

## Seguridad Social 🏥

Aparte de los gastos, otro concepto a descontar antes de calcular el IRPF es la Seguridad Social. Esto debería ser facil, es el 6,35% pero con un matiz, [hay un mínimo y un máximo](https://www.campmanyabogados.com/blog/bases-cotizacion). El máximo se alcanza con 48841€ brutos anuales, todos los sueldos a partir de ahí pagan lo mismo. El mínimo\* es 12600€ brutos anuales.

A Paco le queda un pago a Seguridad Social de 1.905€ que si se lo restamos a 28000€ ya tenemos la cifra que he usado en el cálculo anterior. Vamos a ponerle nombre a todo.

## Base imponible

`Base imponible = Salario Bruto - Gastos - Seguridad Social`
`26095€ = 30000€ - 2000€ - 1905€`

## IRPF Estatal y Autónomico

Ahora si, con la base imponible ya podemos calcular el IRPF.

Las calculadoras online normalmente solo te muestran unos tramos de IRPF. Esos tramos son los estatales y aplican a todos excepto vascos y navarros. Lo que no solemos tener en cuenta es que cada autonomía tiene sus tramos, y en TODAS son diferentes. [Mira el desglose de los tramos IRPF de cada comunidad autónoma de España en la pestaña correspondiente](https://tecalculo.com/calculadora-de-sueldo-neto){:target="\_blank"}.

![Tramos IRPF de cada comunidad](/images/tramosComunidades.png)

La tabla Estatal típica solo aplica a españoles no residentes, si resides en territorio español, se usa la tabla de tu comunidad y la estatal (**con la mitad del porcentaje en cada tramo**). Fíjate en la imagen como los porcantajes estatales ahora son 9,5%, 12% y 15% en lugar de 19%, 24% y 30%.

![Tramos IRPF del estado y catalanes](/images/dosTramos.png)

Siguiendo el ejemplo de Paco, si viviera en Barcelona, tendríamos el siguiente IRPF:

- Estado - 2997€
- Cataluña - 3163,35€
- Total - 6160,35 (20,53%) (Estatal + Autónomico)

Si estas haciendo los cálculos por tu lado y no te cuadran los números es normal, mira el siguiente punto.

## Deducciones

Posiblemente te suene la cifra 5550€. Es el mínimo deducible. En el caso más común, persona soltera sin hijos etc., tiene ese mínimo deducible. Para deducirlo se aplican los tramos también. Es decir, para saber cuanto nos podemos deducir si vivimos en Cataluña tenemos que aplicar los tramos del estado y de la autonomía a la cifra a deducir. Ejemplo:

5.550€ está tanto en el primer tramo del Estado (hasta 12.450€) como de Cataluña (hasta 12.450€), por lo tanto se aplica el tipo del primer tramo:

- Estado 9,5% - 527,25€
- Cataluña 10,5% - 582,75€

A los impuestos totales del estado se les resta la deducción calculada, igual con la autonomía.

`IRPF = IRPF base imponible (tramos) - deducciones (tramos)`

Este es el caso estándar, las deducciones aumentan por cada hijo, por cada ancestro dependiente, etc. He recogido algunos de estos casos en la [calculadora de sueldo neto](https://tecalculo.com/calculadora-de-sueldo-neto){:target="\_blank"}, pero me quedan varios por añadir.

Imaginemos que Paco tiene gemelos, 2 hijos de menores de 3 años. Pues las deducciones aumentan hasta quedar:

- Estado 4,66% - 1035,5€
- Cataluña 5,2% - 1144,5€

El sueldo neto mensual con 12 pagas resultante es 2009,55€, que comparado con el sueldo sin hijos (1920,39€) resulta en 42,5€ más al mes por tener dos hijos menores de 3 años, no se si llega para los pañales.

He añadido en la calculadora este dato

![Beneficio deducción](/images/beneficioDeduccion.png)

*Ten en cuenta que estoy asumiendo que Paco hace una declaración individial, por lo tanto la deducción es del 50%. Si la hace conjunta (solo casados), obtiene el 100%, el doble de deducción que individual.*

## La fórmula :tada:

La fórmula final para el cálculo de tu sueldo neto es la siguiente:

`Salario Neto = Salario Bruto - Gastos - Seguridad Social - IRPF Estatal - IRPF Autonomico`

Con los matices ya comentados:

- El IRPF y sus deducciones se calculan sobre la base imponible y con los tramos correspondientes.
- Hay mínimo y máximo de Seguridad Social.

Espero haber aclarado un poco como funciona este cálculo, es importanto conocer esta información.

## Bonus tracks

A partir de aquí ya hablo de otros conceptos muy importantes a tener en cuenta cuando hablamos del sueldo.

## El tipo marginal

Paco hace un trabajo excelente y le dan un bonus extra de 2000€. ¿Cuánto recibirá en neto nuestro amigo? La tentación es calcular con el porcentaje de IRPF que paga del total del salario (16,83%). Pero es erróneo, como todo funciona por tramos, ese ingreso extra va directo al último tramo, el tramo marginal, que en este caso es de 30%. 15% estatal y 15% autonómico. Por la tanto el neto del bonus será 1400€. He añadido el tipo marginal en los detalles:

![Tramo marginal en los tramos IRPF](/images/tramoMarginalGrafico.png)

![Tramo marginal en los detalles](/images/tramoMarginalDetalles.png)

## Pagas extras

Cuando tenemos 14 pagas en lugar de 12. Las mal llamadas "pagas extras" son más grandes porque no se les reduce la seguridad social. La seguridad social es paga en 12 pagas siempre.

![Ejemplo de sueldo neto con 14 pagas](/images/pagaExtra.png)

## Comparar sueldo neto entre comunidades

Para poder ver la diferencia real entre comunidades he añadido un gráfico donde se puede ver cual sería el salario neto en cada comunidad y la diferencia con la comunidad seleccionado. Cuando tu bruto son 30000€ parece que Cataluña es casi la comunidad con mas carga impositiva. Madrid donde el sueldo neto sería superior.

![Comparar sueldo neto entre comunidades](/images/compararSueldoNetoComunidades.png)

## Siguientes pasos

- Añadir los deducciones que faltan.
- Añadir tickets restaurant, guardería, etc. como cotizan.
- Mejorar la UX.

#### Fuentes

- [Tablas de IRPF por comunidades autónomas](https://www.businessinsider.es/tablas-irpf-comunidades-autonomas-cuanto-pagas-renta-625415)
- [Cómo se cálcula el porcantaje de IRPF](https://ekuatio.com/como-se-calcula-el-porcentaje-de-irpf-en-la-nomina/)
- [Cálculo de rentenciones](https://www2.agenciatributaria.gob.es/wlpl/PRET-R170/index.zul)
- [Cuánto puedes desgravarte en la renta por tus hijos](https://www.finect.com/usuario/Josetrecet/articulos/hijos-declaracion-renta)
