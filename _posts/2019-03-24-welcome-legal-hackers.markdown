---
layout: post
title:  "Hello legal hackers!"
date:   2019-03-24 14:41:01 -0400
categories: data wrangling
---
This is a "Hello world" minimal site to guage interest in a 'hands on' approach to legal hacking.  It's also a place to put: 
*    how to guides 
*    cheat sheets
*    shared learnings

The first of these is on the [Intro page](/sh/Intro), it covers the installation of python and running `hello.py` from the terminal and IDLE.  

The rest of this page is a cheat sheet for setting up a website using Jekyll and GitHub pages.  **Please note** the baseurl in the screenshots below are out of date because I subsequently created `sh` as a personal/sandbox site and `lh` as a collaboration site.  The lh one will be right, I may get to correcting the sandbox ones, I may not :-).  The code snippets should be right though.

## Jekyll

These are the steps for setting up on a Mac.  Windows and Linux can be found on the main [Jekyll](https://jekyllrb.com/docs/installation/) site, see [subsequent post](https://halkypi.github.io/sh/2019/03/27/conformity-windows-pt-ii.html).  I'm also going to experiment with the documentation themes [just-the-docs](https://pmarsceill.github.io/just-the-docs/) and [documentation-theme-jekyll](https://github.com/tomjoht/documentation-theme-jekyll) locally.  I'd really like to delete some of the noise on this 'minimal' template but this should do for now.

### Useful resources

*    [video-walkthroughs](https://jekyllrb.com/tutorials/video-walkthroughs/) by Giraffe Academy
*    [Open government](https://github.com/github/government.github.com)
*    [GH examples](https://github.com/collections/github-pages-examples)
*    [jekyll](https://github.com/jekyll/jekyll)
*    [GH pages learning lab](https://lab.github.com/githubtraining/github-pages)

### Setting up GitHub Pages

There were a couple of gotchas here, for example don't add a README file to the initial repo.  Everything here was taken from the video walkthroughs, this is meant to be a cheat sheet/quick start guide.

#### Install Jekyll

*    Check Ruby and Gem installation - make sure it's local, if not [troubleshoot](https://jekyllrb.com/docs/troubleshooting/), then install gem and bundler
```
which ruby
/usr/local/bin/ruby
which gem
/usr/local/bin/gem
gem install jekyll bundler
```

#### Create local site
When creating for the first time use `bundle exec jekyll serve`, thereafter `jekyll serve` should work fine.

```
jekyll new sh
cd sh
```

*    add base url to `_confiq.yml`

![base-url](/sh/assets/images/base-url.png?raw=true)

*   launch site locally
```
bundle exec jekyll serve
```
*    server address: http://127.0.0.1:4000/sh
*    press ctrl-c to stop

#### Create new GitHub repository

*    **do not** Initialize repository with README
![](/sh/assets/images/new-repository.png?raw=true)

#### Initialize git repository

```
git init
git checkout -b gh-pages
git status
git add .
git commit -m "initial commit"
```
*    grab repository url
![](/sh/assets/images/initial-commit.png?raw=true)

```
git push -u origin gh-pages
```
#### Reload repository

![](/sh/assets/images/initial-commit-reload.png?raw=true)

![](/sh/assets/images/published-at.png?raw=true)

