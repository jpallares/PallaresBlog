# Jekyll blog hosted in Vercel

Created from scratch using latest [Minimal Mistakes Theme](https://mmistakes.github.io/minimal-mistakes/) and then added all the old posts from previous blog ([outdated Jekyll and Minimal Mistakes theme](https://github.com/jpallares/minimal-mistakes))

Main reasons for the change:

- Now is easier to update since it's a ruby gem.
- Spain data provider (Movistar) was not providing access to Github.

## How to run in VS Code Dev Containers

Install and run `colima` or any other Docker CLI. [More details here](https://juan.pallares.me/visual-studio-code-dev-container/#i-dont-have-docker-desktop-whale).
- `colima start`
- Click `F1` Reopen in dev container
- If git not visible run `git status` and then `git config --global --add safe.directory /workspaces/PallaresBlog`

## How to run locally

You will need to have `ruby` and `jekyll` then:

- `gem install bundler`
- `bundle install`
- `bundle exec jekyll serve --future`

## Caveat

Since I have a very custom [multilanguage approach for Jekyll](https://juan.pallares.me/configure-jekyll-multi-language-without-plugin/). I have inside `_layouts` folder an override of the layouts inside the gem. If I update the gem I might have to update the layouts manually.
