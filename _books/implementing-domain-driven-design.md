---
title: Implementing Domain-Driven Design
bookauthor: Vernon, Vaughn
date: 2017-09-24
header:
  teaser: 
quotes:
  - date: 2017-09-24
    quote: Applying Domain-Driven Design and Patterns&#58; With Examples in C# and .NET by Jimmy Nilsson
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
