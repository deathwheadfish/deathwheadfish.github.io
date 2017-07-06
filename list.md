---
layout: default
permalink: /l/
---
<div class="big-list">
  {% for post in site.posts %}
    {% assign currentdate = post.date | date: "%Y" %}
    {% if currentdate != date %}
      {% unless forloop.first %}</ul>{% endunless %}
      <h3>{{ currentdate }}</h3>
      <ul>
      {% assign date = currentdate %}
    {% endif %}
      <li>
        <span class="hang-right">{{ post.date | date: "%-d %b" }}</span>
        <a href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
      </li>
    {% if forloop.last %}</ul>{% endif %}
    {% endfor %}
</div> <!-- /.big-list -->