---
title: Monolith to Microservices
bookauthor: Sam Newman
date: 2022-07-26
header:
  teaser: /images/monolith_to_microservices.jpeg
quotes:
  - date: 2022-07-26
    chapter: 1. Just Enough Microservices
    quote: 'To guarantee independent deployability, we need to ensure our services are loosely coupled—in other words, we need to be able to change one service without having to change anything else. This means we need explicit, well-defined, and stable contracts between services'
  - date: 2022-07-25
    chapter: 1. Just Enough Microservices
    quote: 'This is an architecture in which we have high cohesion of related technology, but low cohesion of business functionality. If we want to make it easier to make changes, instead we need to change how we group code—we choose cohesion of business functionality, rather than technology'
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}

{{ quote.quote }}
{% endfor %}
