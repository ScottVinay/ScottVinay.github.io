---
layout: post
title:  "Visual Hand Sign Recognition"
tags: computer-vision machine-learning deep-learning
sidebar: true
text: true
description: Captures images of hands from a webcam, recognises the number of fingers being held up, and localises the hand in a larger image. 
image: /assets/images/projects/handsign/local.png
---

<a href="https://github.com/ScottVinay/Visual_hand_sign_recognition/">View source on Github</a>


Here, I train a neural network on images that I recorded of my hand, to identify how many fingers I am holding up - resulting in an almost 100% accuracy. This is then used for a localisation script, which finds an image of my hand in a larger image. This can be generalised to multiple pictures of hands in one image.

<figure>
<img src="/assets/images/projects/handsign/ident.png" />
<figcaption>Perfect recignition.</figcaption>
</figure>
