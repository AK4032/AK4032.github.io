---
layout: default
title: Blog
---

# Blog

Pages that do not belong under Travel, Restaurants, or Festivals.

<div class="post-list">
{% for post in site.posts %}
<article class="post-entry">
    <header class="entry-header">
        <h2>{{ post.title }}</h2>
    </header>
    <div class="entry-content">
        <p>{{ post.excerpt | strip_html | strip | truncate: 220 }}</p>
    </div>
    <footer class="entry-footer">{{ post.date | date: "%B %d, %Y" }}</footer>
    <a class="entry-link" href="{{ post.url | relative_url }}" aria-label="{{ post.title }}"></a>
</article>
{% endfor %}
</div>
