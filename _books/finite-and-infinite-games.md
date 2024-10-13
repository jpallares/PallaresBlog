---
title: Finite and Infinite Games
bookauthor: James Carse
date: 2024-08-11
header:
  teaser: 
quotes:
  - date: 2024-08-11
    chapter: 
    quote: In one respect, but only one, an infinite game is identical to a finite game&#58; Of infinite players we can also say that if they play they play freely; if they must play, they cannot play. Otherwise, infinite and finite play stand in the sharpest possible contrast.
  - date: 2024-08-11
    chapter: 
    quote: Finite games can be played within an infinite game, but
  - date: 2024-08-11
    chapter: 
    quote: Finite games can be played within an infinite game, but an infinite game cannot be played within a finite game. Infinite players regard their wins and losses in whatever finite games they play as but moments in continuing play.
  - date: 2024-08-11
    chapter: 
    quote: is on this point that we find the most critical distinction between finite and infinite play&#58; The rules of an infinite game must change in the course of play. The rules are changed when the players of an infinite game agree that the play is imperiled by a finite outcome—that is, by the victory of some players and the defeat of others. The rules of an infinite game are changed to prevent anyone from winning the game and to bring as many persons as possible into the play. If the rules of a finite game are the contractual terms by which the players can agree who has won, the rules of an infinite game are the contractual terms by which the players agree to continue playing. For this reason the rules of an infinite game have a different status from those of a finite game. They are like the grammar of a living language, where those of a finite game are like the rules of debate. In the former case we observe rules as a way of continuing discourse with each other; in the latter we observe rules as a way of bringing the speech of another person to an end.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
