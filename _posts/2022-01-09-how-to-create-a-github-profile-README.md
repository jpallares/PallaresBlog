---
toc: true
toc_label: "Contents"
title: How to create a Github profile README
tags: [github, profile, code, development, coding, posts, blog, actions]
excerpt: Create a Github profile with cool graphics and latests blog posts
header:
  image: /images/jpallares_github_profile.png
  teaser: /images/jpallares_github_profile.png
lang: en
ref: github-profile
---

Github has a cool functionality, if you upload a repo with the same name as your profile, the README of that repo will be shown as profile. [Example with my Github profile](https://github.com/jpallares). [The repo](https://github.com/jpallares/jpallares). 

## The basic version

You can just set some text, a couple emojis and links. You will have a better profile than most of the people.

![Basic profile](/images/basic_profile.png)

## 📖 Show latest blog posts

If you have a blog, it won't hurt to show your latest posts. 

![Github blog posts](/images/github_blogposts.png)

But updating the README everytime you add a post? No! Are you crazy? Github Actions have you covered. It can check periodically for new posts and uptate your README accordingly. To create the Github action you need to create a file in the following path `.github/workflows/blog-post-workflow.yml`. [The contents](https://github.com/jpallares/jpallares/blob/main/.github/workflows/blog-post-workflow.yml) in my case are the following:

```yml
name: Blog Posts

on:
  # Run workflow automatically
  schedule:
    # Runs every hour, on the hour
    - cron: "0 * * * *"

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: gautamkrishnar/blog-post-workflow@master
        with:
          # comma-separated list of RSS feed urls
          feed_list: "https://juan.pallares.me/feed.xml"
```
First the schedule is configured. With this configuration the workflow will check every hour for new posts. 
Then we use an action that simply needs the blog feed to check. See how I use the public workflow from [gautamkrishnar](https://github.com/gautamkrishnar). His profile is worth checking. 

As a plus, I noticed that if the workflow does not detect changes in 60 days, it's disabled. Github emails you an alarm. Nice reminder to keep writing posts in the blog 😄.

![Github workflow emakil remainder](/images/github_workflow_reminder.png)

## 📈 Show Github stats

Finally, you can also add some cool stats about your Github usage. Since professionally I use a private Gitlab, [my stats are not impressive](https://github.com/jpallares#-my-github-stats).

![Github Stats](/images/github_stats.png)

In my case I just needed to add a couple lines directly in the README file

```markdown
[![My GitHub stats](https://github-readme-stats.vercel.app/api?username=jpallares&count_private=true&show_icons=true)))](https://github.com/anuraghazra/github-readme-stats)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=jpallares)](https://github.com/anuraghazra/github-readme-stats)
```

Notice how I set my github profile id (jpallares) as username. Check [anuraghazra github](https://github.com/anuraghazra/github-readme-stats) for more details.

Ready for showing off some cool stats?