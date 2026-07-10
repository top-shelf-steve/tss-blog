---
layout: page
title: Archive
permalink: /archive/
---

{% assign prev_year = "" %}
{% for post in site.posts %}
{% assign year = post.date | date: "%Y" %}
{% if year != prev_year %}

## {{ year }}
{% assign prev_year = year %}
{% endif %}
- <time>{{ post.date | date: "%b %-d" }}</time> — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
