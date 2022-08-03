---
toc: true
toc_label: "Contents"
title: Convert O'Reilly highlights csv to Markdown. Then use them in your Jekyll blog as a collection
tags: [node, oreilly, books, highlights, Markdown, blog, jekyll]
excerpt: Do you know that all the interesting stuff that you highlight in your O'Reilly subscription books can be exported to a csv? With my tool you can parse this file to a more legible markdown format.
header:
  teaser: /images/highlight.jpg
  image: /images/highlight.jpg
lang: en
ref: oreilly-highlights
---

## 🏃 TL;DR

Find the script here [Highlights to Markdown](https://gitlab.com/jpallares/highlights-to-markdown), enjoy!

## Context

I'm lucky to have an [O'Reilly subscription](https://www.oreilly.com/online-learning/pricing.html) paid by my employer (thank you [Trainline](https://www.thetrainline.com/)!). When reading books from the tablet, I like highlighting interesting stuff all the time. It's my way of filtering the most important information and re-read it when needed. But how can I extract this data?

## 🕵️ Getting the csv file

Going to my O'Reilly profile, I realized all the highlights I made were stored there. There is a link to export them as a csv file:

![How to export O'Reilly highlights](/images/how_to_export_highlights.png)

## 💻 Reusing previous script

Recently, [I created an script to parse the highlights from Kindle](https://juan.pallares.me/parse-your-kindle-clippings-into-your-jekyll-blog/) so I decided to extend it to support O'Reilly too.

Converting the csv to an object was a different process than in kindle since the source is a txt file. But once I have an object I could reuse the logic that creates the Markdown file. Check out the resulting code in [Highlights to Markdown](https://gitlab.com/jpallares/highlights-to-markdown). In [the books section](https://juan.pallares.me/books) there are already some O'Reilly highlights added like [The Art of Unit Testing](https://juan.pallares.me/books/the-art-of-unit-testing-2nd-edition/).

## 🔑 Key differences

Pro:

- The csv includes the chapter were the highlight was made, giving more context than in the Kindle file

Con:

- For an unkown reason, the csv file does not include the author of the book, it has to be added manually.

## :writing_hand: Next steps

When reading from the Kindle app instead of a Kindle device, another kind of file can be generated. It's HTML instead of txt. It will be my next update to this script. I'll keep you posted!
