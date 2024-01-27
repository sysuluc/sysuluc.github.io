---
title: Tags
layout: page
permalink: /tags
---

{% for tag in site.tags %}
  <h1>{{ tag[1] | size }} articles tagged with "{{ tag[0] }}"</h1>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a>, published {{ post.date | date: "%Y-%m-%d" }}</li>
    {% endfor %}
  </ul>
{% endfor %}
