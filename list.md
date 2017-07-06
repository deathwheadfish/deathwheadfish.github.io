---
layout: default
permalink: /l/
---
<ul>
	{% for post in site.posts %}
	<li>
		<a href="{{ post.url }}">
			<time>{{ post.date | date: "%-d %B %Y" }}</time>
			{{ post.title }}
		</a>
	</li>
	{% endfor %}
</ul>

{% for post in paginator.posts %}
  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
  <p class="author">
    <span class="date">{{ post.date }}</span>
  </p>
  <div class="content">
    {{ post.content }}
  </div>
{% endfor %}