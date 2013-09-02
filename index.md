---
layout: page
title: InTouch
tagline: Welcome to our Humble Abode
---
{% include JB/setup %}

{% for post in site.posts limit: 5 %}
    <header>
      <h2><a href="{{site.baseurl}}{{post.url}}">{{ post.title }}</a></h2>
    </header>
    <div class="entry">{{ post.excerpt }}</div>
  </article>
{% endfor %}
