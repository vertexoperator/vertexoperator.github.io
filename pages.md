---
layout: nil
title: archive
---

<a href="{{ site.baseurl }}">top</a>

{% for post in site.posts %}
  <li style="padding-top:5px;">
    <a href="{{ post.url }}">{{ post.date | date_to_long_string }} : {{ post.title }}</a>
  </li>
{% endfor %}

