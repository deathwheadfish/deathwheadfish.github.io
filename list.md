---
layout: default
title: list
permalink: /l/
---
<link rel="stylesheet" href="../css/blog.css">
<section class="inner">
  <ul class="posts">
    {% for post in site.posts %}
	  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
	  {% if year != y %}
		{% assign year = y %}
		<span class="listing-seperator">{{ y }}</span>
	  {% endif %}
    <a class='post-link-in-posts' href="{{ site.url }}{{ post.url }}">
        <span class='date'>{{ post.date | date_to_string }}</span>
        <span class='article'>{{ post.title }}</span>
		<div class="tag-in-index-post">
        <i class="fa fa-tags"></i>
          <div class="tag">
		        {{ post.tags | first }}
          </div>
        </div>
    </a>
    {% endfor %}
  </ul>
</section>