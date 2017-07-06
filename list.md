---
layout: default
permalink: /l/
---
  {% for post in site.posts %}
    <article class="hentry entry">
      <h1 class="entry-title">
        <a href="{{ post.url }}" rel="bookmark">{{ post.title }}</a>
      </h1>
      <p>Posted on <time class="published" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date }}</time></p>
    </article>
  {% endfor %}
