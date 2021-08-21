---
title: Net salary calculator
layout: post
tags: [sueldo, salario, neto, bruto, salary, calculator, net]
excerpt: Personal income taxes in Spain explained
lang: en
ref: sueldo-neto
---

Imagine that you have a job offer, a new annual gross salary that sounds tempting, but what is the equivalent monthly net salary? What is the rise from your current job? Imagine that you can compare your current salary with the future one by simply dragging a slider, I bring you the solution:

:moneybag: [**Net Salary Calculator**](https://tusueldoneto.pallares.me){:target="\_blank"}

If you are like me, to calculate the net salary you used to pick the [first result of Google](https://cincodias.elpais.com/herramientas/calculadora-sueldo-neto/). Scrolling up and down all the time, bad UX, refreshing the page that by the way, it's not mobile friendly.

And if you wanted to go one step further, you created an Excel sheet with the typical sections table and you calculated it manually:

![Estatal IPRF sections](../images/tramos.jpg)

So...that's it? Well no ... to calculate well the net salary, there are many more details to consider.

One day I wanted to defeat that dragon and understand as much as possible how it's calculated. While I was investigating, I have been developing this [net salary calculator](https://tusueldoneto.pallares.me){:target="\_blank"} to validate what I was learning. Many cases are missing and the UX is abominable but I have prioritized the usability and ~~I suck doing UX~~. Brace yourselves.

## Basic knowledge First

There is a urban legend that says: "If your salary raises and changes to the next section, you can end up earning less." I have heard it several times and explains very well the little financial education there is in schools, I guess it's more important to learn that a person split the seas and multiplied the bread ... well, I stop before I lose focus.

NO.

**It is impossible that a raise of your salary ends up with you earning less net salary**. The sections are cumulative. Example, let's imagine that Paco earns 24,000 gross euros per year:

![Explanted sections](../images/tramosExplicados.png)

The first 12,450 € have 19% retention. What goes between € 12,450 and € 20,200, that is, the following 7,750 € have 24% retention. Finally, the difference between 24,000 € and 20,200 € => 3,800 € retains 30%.

Always the first part of the salary will have a lower retention and increase progressively in each section. I tried to show this through graphics in the [calculator](https://tusueldoneto.pallares.me){:target="\_blank"}, try it.

# State PIT and autonomic PIT

Online calculators normally only show you some sections of the IRPF (PIT). These sections are for the state and apply to all except Basques and Navarros. What we do not usually take into account is that each autonomy has its sections, and it's different for each one of them.

![Catalan sections](../images/dosTramos.png)

The typical state table only applies to non-resident Spaniards, if residing in Spanish territory, the table of your community and the state (with half the percentage in each section) is used. Following the example of Paco, if he lived in Barcelona, we would have the following PIT:

- State - 1,626.90 €
- Catalonia - 1,846.49 €
- Total - 3,473.39 €(14.47%)

If you are doing the calculations by your side and the numbers do not match it's normal, look at the next point.

## Deductions and expenses

First of all, there is a minimum of 2,000 € expenses, all calculations must be subtracted this value at first, in the case of Paquito 22,000 € is the figure we will use to calculate the PIT.

A number that may ring a bell is 5.550 €. It's the minimum deductible. The most common case: single person without children etc. has that deductible minimum. To deduce it, the sections are applied as well. That is, to know how much we can deduce if we live in Catalonia we have to apply the sections of the State and autonomy to the figure to be deduced. Example:

5,550 € is both in the first stretch of the state (up to 12,450 €) and Catalonia (up to 17,707.02 €), therefore the type of the first section is applied:

- State 9.5% - 527,25 €
- Catalonia 12% - 666.00 €

We substract the deducted amount from the taxes (both state and autonomy)

This is the standard case, deductions increase by each child, for each dependent ancestor, etc. I have collected some of these cases in the [net salary calculator](https://tusueldoneto.pallares.me){:target="\_blank"}, but I have several left to add.

Imagine that Paco has twins, 2 children under 3 years. The deductions increase:

- Status 4.66% - 1035.50 €
- Catalonia 5.2% - 1308.0 €

The monthly net salary with 12 resulting payments is 1679.4 €, which compared to the salary without children (1583.55 €) is almost 100 € more per month for having two children under 3 years, I do not know if it's enough for the diapers.

## Social Security

Once you have the PIT calculated, you may think it's over...not at all. There are also taxes for the Social Security and it's also removed from the gross salary. This should be easy, it's 6.35% but with a nuance, there is a [minimum and maximum](https://www.campmanyabogados.com/blog/bases-cotizacion). The maximum is reached with 48,841 € annual gross, all salaries from there pay the same. The minimum\* is 12,600 € annual gross.

Paco has a social security payment of 1,524.00 €

## The formula :tada:

The basic formula is as follows:

`Net Salary = Gross Salary - State PIT - Autonomic PIT - Social Security`

With the details already commented:

- Expenses and deductions modify the final IRPF/PIT.
- There is minimum and maximum social security.

I hope I have clarified a bit. I believe it's important to have this knowledge.

## Next steps

- Add the remaining deductions.
- Add tickets restaurant, kindergarden, etc.
- Improve UX.

#### Sources

- [Tablas de IRPF por comunidades autónomas](https://www.businessinsider.es/tablas-irpf-comunidades-autonomas-cuanto-pagas-renta-625415)
- [Como se cálcula el porcantaje de IRPF](https://ekuatio.com/como-se-calcula-el-porcentaje-de-irpf-en-la-nomina/)
- [Cálculo de rentenciones](https://www2.agenciatributaria.gob.es/wlpl/PRET-R170/index.zul)
- [Cuánto puedes desgravarte en la renta por tus hijos](https://www.finect.com/usuario/Josetrecet/articulos/hijos-declaracion-renta)
