---
toc: true
toc_label: "Contents"
title: How to create a Github profile README
tags: [kindle, jekyll, clipping, reading, book, node, parser, markdown]
excerpt: Use this Node app to create a nice collection of all the clippings you have made in the books you read on Kindle
header:
  image: /images/bookCollection.png
  teaser: /images/bookCollection.png
lang: en
ref: kindle-clippings
---

Do you know every time you highlight something in your Kindle it's stored in a file called `MyClippings.txt`? The file itself it's ugly but it can be parsed to show something more eye-catching. [Check the books collection I have.](https://juan.pallares.me/books)

## Parse from txt to Markdown

I created a Nodejs app called [MyClippings to Markdown](https://gitlab.com/jpallares/myclippings-to-markdown) that parses this file and creates a Markdown file for each book, grouping the quotes. I know there are plenty of tools ([Clippings.io](https://www.clippings.io/)) and scripts ([1](https://github.com/kkincade/kindle-clippings-to-markdown),[2](https://github.com/baniol/kindle-my-clippings)) doing similar things, but none of them fit my requirements and well I was bored in a rainy quaratined weekend :sweat_smile:.

## Get and show the cover of the book

At the beginning, the way I showed the books was just a list of titles. Since now I have the [latest Minimal Mistakes version](https://juan.pallares.me/it-has-never-been-easier-to-have-a-blog/), I used the grid collection layout with reverse order functionality to order the list in a more attractive way. To show the book covers, I used the [openlibrary.org API](https://openlibrary.org/developers/api) to query for them. They are automatically queries in [MyClippings to Markdown](https://gitlab.com/jpallares/myclippings-to-markdown) parser but you can manually add the link to the image if the script does not find it.

## Use it with Jekyll

The markdown generated is intended to be used with a [Jekyll collection](https://jekyllrb.com/docs/collections/). I have created a book collection the following way:

1. Create a `_books` folder and move there all the generated files.
1. Add the collection to your `_config.yml`:

   ```yml
   include:
     - _books

   ...

   collections:
     books:
       output: true
       permalink: /:collection/:path/

   ...

   defaults:
     ...
     # _books
     - scope:
         path: ""
         type: books
       values:
         layout: single
         author_profile: true
         share: true
         comments: true

   ```

1. Add a navigation link in the top bar editing `navigation.yml` inside `_data` folder:

   ```yml
   main:
     - title: Tu sueldo neto
       url: https://tusueldoneto.pallares.me
     - title: CV
       url: /cv/
     - title: Books
       url: /books/
   ```

1. Finally create a page that will have the links to all the books. I created `books.md` and put it inside `_pages` folder:

   ```yml
   ---
   title: Books
   layout: collection
   permalink: /books/
   collection: books
   entries_layout: grid
   classes: wide
   sort_order: reverse
   ---
   ```

## See an example

Check [this blog repo](<(https://github.com/jpallares/PallaresBlog)>) to see the details on how to do it. Remember [you need to parse the `MyClippings.txt` file as a first step](https://gitlab.com/jpallares/myclippings-to-markdown).
