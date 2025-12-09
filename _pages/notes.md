---
layout: single
title: "Notes"
permalink: /notes/
author_profile: true
---

Welcome to my notes. Here I keep two different streams of writing:

- **Posts** – recent, mostly scientific or work-related notes.
- **Archive** – older essays and blog posts originally written on Blogger.

<div class="feature__wrapper">

  <div class="feature__item">
    <h2>Posts</h2>
    <p>
      Recent reflections, technical notes, and science-related writing.
    </p>
    <p>
      <a class="btn btn--primary" href="{{ '/posts/' | relative_url }}">
        View all posts →
      </a>
    </p>
  </div>

  <div class="feature__item">
    <h2>Archive</h2>
    <p>
      Migrated pieces from my old Blogger days, organised by year.
    </p>
    <p>
      <a class="btn btn--info" href="{{ '/archive/' | relative_url }}">
        Browse the archive →
      </a>
    </p>
  </div>

</div>

---

## Latest posts

{% assign recent_posts = site.posts | sort: "date" | reverse | slice: 0,5 %}

{% if recent_posts.size > 0 %}
<ul>
{% for post in recent_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="page__meta"> — {{ post.date | date: "%b %-d, %Y" }}</span>
  </li>
{% endfor %}
</ul>
{% else %}
<p>No posts yet. Stay tuned.</p>
{% endif %}
