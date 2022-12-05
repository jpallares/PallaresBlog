---
toc: true
toc_label: "Contents"
title: Net salary calculator
tags: [sueldo, salario, neto, bruto, salary, calculator, net]
excerpt: Personal income taxes in Spain explained
header:
  teaser: /images/tramos.jpg
lang: en
ref: sueldo-neto
---

**This is an update of the article published on 04/07/2021**

Imagine that you have a job offer, a new annual gross salary that sounds tempting, but what is the equivalent monthly net salary? What is the rise from your current job? Imagine that you can compare your current salary with the future one by simply dragging a slider, I bring you the solution:

:moneybag: [**Net Salary Calculator**](https://tecalculo.com/en/spanish-net-salary-calculator){:target="\_blank"}

If you are like me, to calculate the net salary you used to pick the [first result of Google](https://cincodias.elpais.com/herramientas/calculadora-sueldo-neto/). Scrolling up and down all the time, bad UX, refreshing the page that by the way, it's not mobile friendly.

And if you wanted to go one step further, you created an Excel sheet with the typical sections table and you calculated it manually:

![Estatal IPRF sections](/images/tramos.jpg)

So...that's it? Well no ... to calculate well the net salary, there are many more details to consider.

One day I wanted to defeat that dragon and understand as much as possible how it's calculated. While I was investigating, I have been developing this [net salary calculator](https://tecalculo.com/en/spanish-net-salary-calculator){:target="\_blank"} to validate what I was learning. Many cases are missing and the UX is abominable but I have prioritized the usability and ~~I suck doing UX~~. Brace yourselves.

## Basic knowledge First 🧑‍🏫

There is a urban legend that says: "If your salary raises and changes to the next section, you can end up earning less." I have heard it several times and explains very well the little financial education there is in schools, I guess it's more important to learn that a person split the seas and multiplied the bread ... well, I stop before I lose focus.

NO.

**It is impossible that a raise of your salary ends up with you earning less net salary**. The sections are cumulative. Example, let's imagine that Paco earns 30.000€ gross per year:

The first 12.450€ have 19% retention. What goes between 12.450€ and 20.200€, that is the following 7.750€ have 24% retention. Finally, the difference between 26.095€ and 20.200€ => 5.895€ retains 30%.

Always the first part of the salary will have a lower retention and increase progressively in each section. I tried to show this through graphics in the [calculator]https://tecalculo.com/calculadora-de-sueldo-neto

![Explanted sections](/images/tramosExplicados.png)

## Expenses 🚗

If you have been reading carefully, you will have noticed that the last subtraction did not use 30.000€ and used 26.095€. One of the reasons is the expenses.

There is a minimum expense of 2.000€. All calculations must be made by initially subtracting this value from the gross. In Paco's case, after restoring the expenses, we are left with 28.000€. But this figure is not yet 26.095€ what is missing? Social Security.

## Social Security 🏥

Apart from expenses, another concept to discount before calculating personal income tax is Social Security. This should be easy, it is 6.35% but with a nuance, [there is a minimum and a maximum](https://www.campmanyabogados.com/blog/bases-cotizacion). The maximum is reached with 48.841€ gross per year, all salaries from there pay the same. The minimum\* is 12.600€ gross per year.

Paco has a Social Security payment of 1.905€ left, which if we subtract it from 28.000€ we already have the figure he used in the previous calculation. Let's name everything.

## Tax base

`Tax base = Gross salary - Expenses - Social Security`
`26.095€ = 30.000€ - 2.000€ - 1.905€`

## State PIT and autonomic PIT

Now we can, once we have the tax base we can calulate the PIT.

Online calculators normally only show you some sections of the IRPF (PIT). These sections are for the state and apply to all except Basques and Navarros. What we do not usually take into account is that each autonomy has its sections, and it's different for each one of them. [Take a look at the different sections per community in the calculator tab](https://tecalculo.com/en/spanish-net-salary-calculator){:target="\_blank"}.

![PIT Sections per community](/images/tramosComunidades.png)

The typical state table only applies to non-resident Spaniards, if residing in Spanish territory, the table of your community and the state (with half the percentage in each section) is used. Check how the Spanish percents are now 9,5%, 12% and 15% instead of 19%, 24% and 30%

![Spain and Catalan sections](/images/dosTramos.png)

Following the example of Paco, if he lived in Barcelona, we would have the following PIT:

- State - 2.997€
- Catalonia - 3.163,35€
- Total - 6.160,35€ (20,53%) (State + Catalonia)

If you are doing the calculations by your side and the numbers do not match it's normal, look at the next point.

## Deductions

A number that may ring a bell is 5.550€. It's the minimum deductible. The most common case: single person without children etc. has that deductible minimum. To deduce it, the sections are applied as well. That is, to know how much we can deduce if we live in Catalonia we have to apply the sections of the State and autonomy to the figure to be deduced. Example:

5.550€ is both in the first stretch of the state (up to 12,450€) and Catalonia (up to 17.707,02€), therefore the type of the first section is applied:

- State 9,5% - 527,25 €
- Catalonia 10,5% - 582,75€

`PIT = PIT tax base (sections) - deductions (sections)`

We substract the deducted amount from the taxes (both state and autonomy).

This is the standard case, deductions increase by each child, for each dependent ancestor, etc. I have collected some of these cases in the [net salary calculator](https://tecalculo.com/en/spanish-net-salary-calculator){:target="\_blank"}, but I have several left to add.

Imagine that Paco has twins, 2 children under 3 years. The deductions increase:

- Status 4,66% - 1.035,5€
- Catalonia 5,2% - 1.144,5€

The monthly net salary with 12 resulting payments is 2.009,55€, which compared to the salary without children (1.920,39€) is 42,5€ more per month for having two children under 3 years, I do not know if it's enough for the diapers.

I added to the calculator this data

![Deduction benefit](/images/beneficioDeduccion.png)

*Note that I am assuming that Paco makes an individual PIT declaration, therefore the deduction is 50%. If you do it jointly (only married couples can), you get 100%.*

## The formula :tada:

The basic formula is as follows:

`Net Salary = Gross Salary - Expenses - Social Security - State PIT - Autonomic PIT`

With the details already commented:

- The PIT and his deductions are calculated from the tax base. Corresponding PIT sections are used.
- There is minimum and maximum social security.

I hope I have clarified a bit. I believe it's important to have this knowledge.

## Bonus tracks

From here I will talk about other very important concepts to take into account when we talk about salary.

## The Marginal Rate

Paco does an excellent job and they give him an extra bonus of 2.000€. How much will our friend receive in net? The temptation is to calculate with the rate of personal income tax paid out of the total salary (20.53%). But this is wrong, since everything works in sections, that extra income goes directly to the last section, the marginal section, which in this case is 30%. 15% state and 15% regional. Therefore the net of the bonus will be 1.400€. I've added the marginal type in the details:

![Marginal rate in Personal Income Tax tranches](/images/tramoMarginalGrafico.png)

![Marginal rate in the details](/images/tramoMarginalDetalles.png)

## Extra payments

When we have 14 payments instead of 12. The so-called "extra payments" are bigger because social security is not reduced. Social security is always paid in 12 payments.

![Example of net salary with 14 payments](/images/pagaExtra.png)

## Compare net salary between communities

In order to see the real difference between communities I have added a graph where you can see what the net salary would be in each community and the difference with the selected community. When your gross is 30.000€ it seems that Catalonia is almost the community with the highest tax burden. Madrid, on the contrary, where the net salary would be higher.

![Compare net salary between communities](/images/compararSueldoNetoComunidades.png)

## Next steps

- Add the remaining deductions.
- Add tickets restaurant, kindergarden, etc.
- Improve UX.

#### Sources

- [Tablas de IRPF por comunidades autónomas](https://www.businessinsider.es/tablas-irpf-comunidades-autonomas-cuanto-pagas-renta-625415)
- [Como se cálcula el porcantaje de IRPF](https://ekuatio.com/como-se-calcula-el-porcentaje-de-irpf-en-la-nomina/)
- [Cálculo de rentenciones](https://www2.agenciatributaria.gob.es/wlpl/PRET-R170/index.zul)
- [Cuánto puedes desgravarte en la renta por tus hijos](https://www.finect.com/usuario/Josetrecet/articulos/hijos-declaracion-renta)
