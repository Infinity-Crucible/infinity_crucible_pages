---
layout: default
title: Updates
permalink: /updates/
---

<h1 class="section-title">Development Updates</h1>

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}" class="card" style="display: block; text-decoration: none;">
      <h2 class="card-title">{{ post.title }}</h2>
      <time class="card-date">{{ post.date | date: "%B %d, %Y" }}</time>
      <p class="card-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    </a>
  </li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
<p class="card" style="color: #a1a1a1;">No updates yet. Check back soon!</p>
{% endif %}
