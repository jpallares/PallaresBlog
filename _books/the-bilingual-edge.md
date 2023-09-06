---
title: The Bilingual Edge
bookauthor: Kendall King, PhD
date: 2023-07-16
header:
  teaser: https://covers.openlibrary.org/b/isbn/0061246565-L.jpg
quotes:
  - date: 2023-06-25
    chapter: 
    quote: If someone is speaking her second language (and is not a highly proficient or nativelike speaker), then she may say simplified and sometimes ungrammatical sentences. However, these sorts of imperfections do not harm or impede children’s language learning.
  - date: 2023-06-25
    chapter: 
    quote: The truly critical factor is rich, dynamic, and meaningful interaction with speakers of those languages (and this can come in many different forms).
  - date: 2023-06-30
    chapter: 
    quote: it’s never too early or too late to start learning a new language. The best time to start is right now!
  - date: 2023-07-02
    chapter: 
    quote: New parents often complain of feeling a bit brain dead and in need of mental stimulation in those very time and labor intensive (and repetitive) first months—this approach provides a perfect way to make those everyday routines a bit more challenging and stimulating for mom, dad, or whoever is the caretaker. Parents might even find that they will brush up on their second language skills, too!
  - date: 2023-07-02
    chapter: 
    quote: with as little as 20 percent of total exposure in one language, children were still able to develop a productive vocabulary.
  - date: 2023-07-02
    chapter: 
    quote: strong skills in the first language help not hinder acquiring them in a second.
  - date: 2023-07-09
    chapter: 
    quote: Code-mixing describes how language learners combine two languages due to incomplete knowledge of one or both language(s). Code-switching, in contrast, is common among highly proficient adults and children, and a sign of mastery of two languages.
  - date: 2023-07-09
    chapter: 
    quote: children learn how to do things with a language (like how to tell stories, describe pictures, ask for specific foods, understand written texts, write letters to pen pals, etc.), by doing those things in that language. One major reason why there are so few true or balanced bilinguals is because most people do not do everything in both languages.
  - date: 2023-07-16
    chapter: 
    quote: children who speak Swiss German at home have little difficulty using standard German (which is actually quite different from Swiss German) when they start school. These children don’t experience more difficulties at school or problems with learning because of the switch in languages or dialects. So, if you are a native speaker of a so-called nonstandard variety of a language, you should not worry that your child will have difficulties when she enters school and begins using the standard variety. Research suggests this is simply not the case.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
