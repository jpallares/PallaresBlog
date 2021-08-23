---
title: FailSafe Investing
bookauthor: Harry Browne
date: 2021-03-10
header:
  teaser: https://covers.openlibrary.org/b/isbn/9780312263218-L.jpg
quotes:
  - date: 2021-03-06
    quote: The investment expert with the perfect record up to now will lose his touch as soon as you start acting on his advice.
  - date: 2021-03-06
    quote: Handle your business and investment affairs on a cash basis, and it's virtually impossible to lose everything — no matter what might happen in the world — especially if you follow the other rules in this book.
  - date: 2021-03-06
    quote: Every investment has its time in the sun — and its moment of shame. • Precious metals ruled the roost in the 1970s, while stocks and bonds were in disgrace. • Gold and silver became the losers of the 1980s, while stocks and bonds multiplied their value. • Real estate was a big winner in the 1970s, but lost its luster when the tax rules changed in 1986. No one investment is good for all times. Even U.S. Treasury bills can lose real value during times of inflation.
  - date: 2021-03-10
    quote: I call such a portfolio the Permanent Portfolio, because once you set it up, you never need to reconsider the investment mix — even if your outlook for the future changes. You leave it alone — to hold the same investments, in the same proportions, permanently. You don’t change the proportions as you, your friends, or investment gurus change their minds about the future.
  - date: 2021-03-10
    quote: Your portfolio needs to respond well only to those broad movements. And they fit into four general categories&#58; 1. Prosperity&#58; A period during which living standards are rising, the economy is growing, business is thriving, interest rates usually are falling, and unemployment is declining.2. Inflation&#58; A period when consumer prices generally are rising. They might be rising moderately (an inflation rate of 6% or so), rapidly (10% to 20% or so, as in the late 1970s), or at a runaway rate (25% or more). 3. Tight money or recession&#58; A period during which the growth of the supply of money in circulation slows down. This leaves people with less cash than they expected to have, which usually causes a recession — a period of poor economic conditions. 4. Deflation&#58; The opposite of inflation. Consumer prices decline and the purchasing power of money grows. In the past, deflation has usually triggered a depression — a prolonged period of very bad economic conditions, as in the 1930s.
  - date: 2021-03-10
    quote: The Permanent Portfolio is for the money that's precious to you — the capital you're counting on for retirement or to pass on to your heirs. I believe you should never take chances with that capital — never use a penny of it to bet on someone's forecast or to use market timing of any kind. But the Variable Portfolio (if you want to have one) is funded with money you've already decided you can afford to lose. Thus you can use it to try to build a big fortune or just to have fun — taking whatever chances you want, knowing that the worst possible loss won’t devastate you.
---
## *{{page.bookauthor}}*

<img width="200" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
