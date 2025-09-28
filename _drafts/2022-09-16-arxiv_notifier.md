---
layout: post
title:  "How to set up a bot to notify you of relevant arXiv posts"
date:   2019-10-08 12:33:47 +0100
last_modified_at: 2019-10-08
categories: general
sidebar: true
text: true
---

The arXiv is a fantastic resource for keeping up-to-date on recent developments in science. As a data scientist, I am aware of how fast-moving the field of machine learning is, with big new developments coming on a weekly basis.

However, it can be difficult to be vigilant in reading every abstract on several sections of the arXiv every day. I have set up a bot that emails me and other people on my mailing list each Monday morning with relevant papers from the last week that feature the keywords that that person is interested in. The bot can also be told which sections each person wants to check, as well as any authors they want to check for. 

Here I show you how this is done in case you want to set up something similar. Note that I did not write the code for actually scraping the arXiv. That I attribute to [Morgane Goibert](https://mgoibert.github.io/ArXiv-Alert/).

### Step 1: Set up a gmail account.

I first created a new gmail account that will be used 

<figure>
<img src="/assets/images/posts/bayesian_entropy/pointing.jpg" />
</figure>

