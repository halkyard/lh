---
layout: post
title: Social conformity and Windows part II
date:   2019-03-27
---

##Social conformity##
Our team are preparing for a design sprint and someone shared this video which I thought was interesting: [Brain game - waiting room](https://youtu.be/o8BkzvP19v4).

##Running Jekyll on Windows part II##
I experimented with a few different approaches to getting Jekyll up and running on a Windows machine.  It is not very well supported unfortunately so I decided to try [Ubuntu linux running inside Windows 10](https://tutorials.ubuntu.com/tutorial/tutorial-ubuntu-on-windows#0) and it worked flawlessly.

The steps are listed here:  [https://jekyllrb.com/docs/installation/ubuntu/](https://jekyllrb.com/docs/installation/ubuntu/).  

```
sudo apt-get install ruby-full build-essential zlib1g-dev
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
gem install jekyll bundler
jekyll new lh
cd lh
bundle exec jekyll serve
```
