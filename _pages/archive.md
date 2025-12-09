---
layout: archive
title: "Archive"
permalink: /archive/
author_profile: true
---

{% include base_path %}

{% assign items = site.archive | sort: "date" %}
{% capture written_year %}'None'{% endcapture %}

{% for post in items %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
### {{ year }}
{% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
