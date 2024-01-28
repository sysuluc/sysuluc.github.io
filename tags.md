---
title: Tags
layout: page
permalink: /tags
---

{% for tag in site.tags %}
  <h1>"{{ tag[0] | upcase }}" × {{ tag[1] | size }}</h1>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a>, published {{ post.date | date: "%Y-%m-%d" }}</li>
    {% endfor %}
  </ul>
{% endfor %}
