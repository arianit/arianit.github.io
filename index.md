---
layout: default
title: Tracing my coding journey.
---

<h1>{{ page.title }}</h1>

{% for post in site.posts %}
<article>
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <div class="post-content">
    {{ post.excerpt }}
  </div>
</article>
{% endfor %}


