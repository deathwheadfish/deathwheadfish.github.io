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