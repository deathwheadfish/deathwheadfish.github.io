---
layout: default
title: list
permalink: /l/
---
{% for post in site.posts %}
  {% if post.categories contains 'postcategory' %}
    <h1>Do nothing</h1>
  {% else %}
    <h2>{{ post.title }}</h2>
  {% endif %}
{% endfor %}