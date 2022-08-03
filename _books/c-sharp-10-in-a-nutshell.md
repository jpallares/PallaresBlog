---
title: C# 10 in a Nutshell
bookauthor: Joseph Albahari
date: 2022-06-12
header:
  teaser: /images/c-sharp-10-nutshell.jpeg
quotes:
  - date: 2022-06-12
    quote: The ??= operator (introduced in C&#35 8) is the null-coalescing assignment operator. It says, “If the operand to the left is null, assign the right operand to the left operand.”
  - date: 2022-06-01
    quote: decrementing the minimum possible int value results in the maximum possible int value&#58;
  - date: 2022-06-01
    quote: You can insert an underscore anywhere within a numeric literal to make it more readable&#58;
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
