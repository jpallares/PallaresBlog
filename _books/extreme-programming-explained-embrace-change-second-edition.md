---
title: Extreme Programming Explained&#58; Embrace Change, Second Edition
bookauthor:
date: 2022-05-09
header:
  teaser: /images/extreme_programming_explained.jpg
quotes:
  - date: 2022-05-09
    chapter: The XP Series
    quote: 'One of the goals of XP is to bring accountability and transparency to software development, to run software development like any other business activity. Another goal is to achieve outstanding results—more effective and efficient development with far fewer defects than is currently expected. Finally, XP aims to achieve these goals by celebrating and serving the human needs of everyone touched by software development—sponsors, managers, testers, users, and programmers.'
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}

{{ quote.quote }}
{% endfor %}
