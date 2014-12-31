## Jekyll Podcast Site & Feed

This is a super basic [Jekyll](http://jekyllrb.com) site to publish new podcast episodes and generate an RSS feed. It runs off GitHub Pages so all you need to do is make a new post in `_posts`, commit and push.

The RSS feed code is lifted from [Adam Wilcox](http://www.adamwilcox.org/2013/01/17/from-the-pub/).

People can subscribe to the RSS feed in most podcast apps except iTunes. All the required metadata for Apple should be in the feed if you want to submit the podcast to Apple too.

### Basic Setup

1. Install Jekyll with `sudo gem install jekyll`
2. Clone this repo. [GitHub for Mac](https://mac.github.com) make that easier.
3. Open `_config.yml` and add details of the podcast.
4. Replace cover-art.jpg with new cover art. Apparently iTunes requires a 1400px square.
5. `jekyll serve` will run a local server.
6. Push it up to GitHub and GitHub Pages will build your site. It'll be available at http://username.github.io/reponame/ but you can also use a [custom domain](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/).

### Publishing a New Episode

Open up `_posts` and make a new file following the pattern `YYYY-MM-DD-epN-title.md` (this makes the URL).

Put in YAML metadata and post content if you want any show notes or wot not (use Markdown).

```yaml
---
layout: post
date: 2014-12-28 20:25:00
title: "Ep 1: G'day, purple, yum yum."
duration: "02:47"
length: 2668168
link: https://dl.dropboxusercontent.com/u/21267/Podcasts/Ollie%20Talking%20Shit/Ollie%20Talking%20Shit%20Ep%201.mp3
---

Post content here.
```

The YAMLmetadata at the top of a post is mostly straight forward.

* Title and Duration are wrapped in `""` quotes because they contain `:` which confuses the YAML.
* Duration is HH:MM:SS or just MM:SS
* Length is the file size in bytes.
* Link is a direct link to the mp3. Mine are just in my Dropbox Public folder.
