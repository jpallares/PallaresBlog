---
title: Working Effectively with Legacy Code
bookauthor: Michael C. Feathers
date: 2018-07-21
header:
  teaser: https://covers.openlibrary.org/b/olid/OL3315089M-L.jpg
quotes:
  - date: 2018-07-21
    quote: In fact, if you can’t present a compelling case to your coworkers, you might get beat up in the parking lot or, worse, ignored for the rest of your workdays, so let me help you make that case. The biggest obstacle
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }}
{{ quote.quote }}
{% endfor %}
