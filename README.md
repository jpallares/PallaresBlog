# Jekyll blog hosted in Vercel

Created from scratch using latest [Minimal Mistakes Theme](https://mmistakes.github.io/minimal-mistakes/) and then added all the old posts from previous blog ([outdated Jekyll and Minimal Mistakes theme](https://github.com/jpallares/minimal-mistakes))

Main reasons for the change:
- Now is easier to update since it's a gem and
- Spain data provider (Movistar) was not providing access to Github.

## How to test locally

You will need to have `ruby` and `jekyll` then:

`bundle exec jekyll serve`

## Caveat

Since I have a very custom [multilanguage approach for Jekyll](https://juan.pallares.me/configure-jekyll-multi-language-without-plugin/). I have inside `_layouts` folder an override of the layouts inside the gem. If I update the gem I might have to update the layouts manually.