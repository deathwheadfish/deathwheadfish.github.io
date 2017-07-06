---
layout: default
permalink: /l/
---
{% if site.posts.size > 0 %}
  <ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">
        <h2>{{ post.title }}</h2>
      </a>
    </li>
  {% endfor %}
  </ul>
  {% else %}
  <p>There are no posts available right. Come back soon!</p>
{% endif %}