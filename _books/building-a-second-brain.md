---
title: Building a Second Brain
bookauthor: Tiago Forte
date: 2023-03-08
header:
  teaser: https://covers.openlibrary.org/b/isbn/1982167386-L.jpg
quotes:
  - date: 2023-03-06
    chapter: 
    quote: This digital commonplace book is what I call a Second Brain. Think of it as the combination of a study notebook, a personal journal, and a sketchbook for new ideas. It is a multipurpose tool that can adapt to your changing needs over time. In school or courses you take, it can be used to take notes for studying. At work, it can help you organize your projects. At home, it can help you manage your household.
  - date: 2023-03-08
    chapter: 
    quote: “CODE”—Capture; Organize; Distill; Express.
  - date: 2023-03-08
    chapter: 
    quote: Adopting the habit of knowledge capture has immediate benefits for our mental health and peace of mind. We can let go of the fear that our memory will fail us at a crucial moment. Instead of jumping at every new headline and notification, we can choose to consume information that adds value to our lives and consciously let go of the rest.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
