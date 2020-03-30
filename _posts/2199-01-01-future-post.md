---
title: 'Future Blog Post'
date: 2020-03-20
permalink: /posts/2012/08/blog-post-4/
tags:
  - cool posts
  - category1
  - category2
video: /video/liquid
layout: post
---

{% if page.image %}
  {% assign postImage = page.image %}
{% elsif post.image %}
  {% assign postImage = post.image %}
{% else %}
  {% if page.video %}
    {% assign postVideo = page.video %}
  {% elsif post.video %}
    {% assign postVideo = post.video %}
  {% else %}
    {% assign postImage = site.default_image %}
  {% endif %}
{% endif %}

<video class="background"
	loop
	muted
	autoplay
	preload="auto"
	poster="{{ postVideo }}.png">
<source src="{{ postVideo }}.mp4" type="video/mp4">
<source sr