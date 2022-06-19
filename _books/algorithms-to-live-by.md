---
title: Algorithms to Live By - The Computer Science of Human Decisions
bookauthor: Brian Christian
date: 2022-03-23
header:
  teaser: https://covers.openlibrary.org/b/olid/OL25935646M-L.jpg
quotes:
  - date: 2022-03-23
    quote: In your search for a secretary, there are two ways you can fail&#58; stopping early and stopping late. When you stop too early, you leave the best applicant undiscovered. When you stop too late, you hold out for a better applicant who doesn’t exist. The optimal strategy will clearly require finding the right balance between the two, walking the tightrope between looking too much and not enough.
  - date: 2022-03-23
    quote: the optimal solution takes the form of what we’ll call the Look-Then-Leap Rule&#58; You set a predetermined amount of time for “looking”—that is, exploring your options, gathering data—in which you categorically don’t choose anyone, no matter how impressive. After that point, you enter the “leap” phase, prepared to instantly commit to anyone who outshines the best applicant you saw in the look phase.
  - date: 2022-03-23
    quote: As the applicant pool grows, the exact place to draw the line between looking and leaping settles to 37% of the pool, yielding the 37% Rule&#58; look at the first 37% of the applicants,* choosing none, then be ready to leap for anyone better than all those you’ve seen so far.
  - date: 2022-03-23
    quote: Both Kepler and Trick—in opposite ways—experienced firsthand some of the ways that the secretary problem oversimplifies the search for love. In the classical secretary problem, applicants always accept the position, preventing the rejection experienced by Trick. And they cannot be “recalled” once passed over, contrary to the strategy followed by Kepler.
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
