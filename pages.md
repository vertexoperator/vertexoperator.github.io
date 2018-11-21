---
layout: nil
title: archive
---

<a href="{{ site.baseurl }}">top</a>

{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}" style="padding-top:5px;">{{ post.date | date_to_long_string }} : {{ post.title }}</a>
  </li>
{% endfor %}

