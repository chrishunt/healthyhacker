---
layout: post
title:  "Welcome to Jekyll!"
date:   2014-07-17 17:45:54
thumb:  "example-1080p"
episode:  "4"
video: "xiVTGu92dw0"
categories: episodes
---

{% include video.html %}

<header class="post-header">
  <p class="meta">
    {{ page.date | date: "%b %-d, %Y" }} • <span>{{ page.title }}</span>
  </p>
</header>

You'll find this post in your `_posts` directory - edit this post and re-build
(or run with the `-w` switch) to see your changes!  To add new posts, simply
add a file in the `_posts` directory that follows the convention:
YYYY-MM-DD-name-of-post.ext.

