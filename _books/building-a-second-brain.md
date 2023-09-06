---
title: Building a Second Brain
bookauthor: Tiago Forte
date: 2023-03-23
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
  - date: 2023-03-16
    chapter: 
    quote: Your notes will be useless if you can’t decipher them in the future, or if they’re so long that you don’t even try. Think of yourself not just as a taker of notes, but as a giver of notes—you are giving your future self the gift of knowledge that is easy to find and understand.
  - date: 2023-03-16
    chapter: 
    quote: Use your list of favorite problems to make decisions about what to capture&#58; anything potentially relevant to answering them.
  - date: 2023-03-23
    chapter: 
    quote: By saving ideas that may contradict each other and don’t necessarily support what we already believe, we can train ourselves to take in information from different sources instead of immediately jumping to conclusions. By playing with ideas—bending and stretching and remixing them—we become less attached to the way they were originally presented and can borrow certain aspects or
  - date: 2023-03-23
    chapter: 
    quote: By saving ideas that may contradict each other and don’t necessarily support what we already believe, we can train ourselves to take in information from different sources instead of immediately jumping to conclusions. By playing with ideas—bending and stretching and remixing them—we become less attached to the way they were originally presented and can borrow certain aspects or elements to use in our own work. If what you’re capturing doesn’t change your mind, then what’s the point?
  - date: 2023-03-23
    chapter: 
    quote: keep what resonates.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
