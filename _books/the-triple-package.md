---
title: The Triple Package
bookauthor: Amy Chua
date: 2024-08-07
header:
  teaser: 
quotes:
  - date: 2024-08-05
    chapter: 
    quote: 1. A SUPERIORITY COMPLEX. This element of the Triple Package is the easiest to define&#58; a deeply internalized belief in your group’s specialness, exceptionality, or superiority.
  - date: 2024-08-05
    chapter: 
    quote: Yet insecurity runs deep in every one of America’s most successful groups, and these groups not only suffer from insecurity; they tend, consciously or unconsciously, to promote it.
  - date: 2024-08-05
    chapter: 
    quote: IMPULSE CONTROL. As we’ll use the term, impulse control refers to the ability to resist temptation, especially the temptation to give up in the face of hardship or quit instead of persevering at a difficult task.
  - date: 2024-08-06
    chapter: 
    quote: It’s remarkable how common this dynamic is among immigrant groups&#58; a minority, armed with enormous ethnocentric pride, suddenly finds itself disrespected and spurned in the United States. The result can border on resentment—and resentment, as Nietzsche taught, is one of the world’s great motivators. A particularly
  - date: 2024-08-07
    chapter: 
    quote: Clayton Christensen, author of The Innovator’s Dilemma (which Intel CEO Andy Grove said was the most important book he’d read in ten years),
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
