---
layout: single
title: "Notes"
permalink: /notes/
author_profile: true
---

Welcome to my notes. Here you can find my latest posts and browse the full archive.

## Posts

You can find all posts on the dedicated posts page:

- [View all posts →](/posts/)

Below are the most recent posts:

{% assign recent_posts = site.posts | sort: "date" | reverse | slice: 0,5 %}
<ul>
{% for post in recent_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="page__meta"> — {{ post.date | date: "%b %-d, %Y" }}</span>
  </li>
{% endfor %}
</ul>

## Archive

If you prefer to browse posts by year, use the archive:

- [Browse the archive →](/archive/)
