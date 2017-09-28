---
layout: nil
title: archive
---

<a href="{{ site.baseurl }}">top</a>

{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.date | date_to_long_string }} : {{ post.title }}</a>
  </li>
{% endfor %}

{% for page in site.pages %}
  <li>
    <a href="{{ page.url }}">{{ page.date | date_to_long_string }} : {{ page.title }}</a>
  </li>
{% endfor %}
