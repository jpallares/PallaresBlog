---
title: Die with Zero
bookauthor: Bill Perkins
date: 2023-05-13
header:
  teaser: https://covers.openlibrary.org/b/isbn/9780358567097.jpg
quotes:
  - date: 2023-05-10
    chapter: 
    quote: So it makes no sense to let opportunities pass us by for fear of squandering our money. Squandering our lives should be a much greater worry.
  - date: 2023-05-10
    chapter: 
    quote: It was like the end of The Matrix, when Neo walks around seeing the world as it is. That’s how I was after reading the book&#58; I started going around calculating hours needed to buy stuff. I’d see a nice-looking shirt, do the mental math, and think, No, you cannot get me to work two hours just to buy that shirt!
  - date: 2023-05-13
    chapter: 
    quote: the cost in time of a long commute to the city, the cost of the kinds of clothes you need for this high-status job, and of course the extra hours you have to put into the job itself—
  - date: 2023-05-13
    chapter: 
    quote: I’m here to bridge the ant and the grasshopper, to help you find the right balance between the two. In fact, the stated moral of my favorite version of the fable is just this&#58; “There is a time for work and a time for play.”
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
