---
layout: post
subtitle: ''
extlink: ''
index: true 
---
<h3 class="title" >Мои статьи</h3>

<ul class="articles-list">
  {% for post in paginator.posts %}
    {% capture that_year %}{{ this_year || '' }}{% endcapture %}
    {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% if this_year != that_year %}
      {% if !forloop.first %}
        <div class="articles-list__title" data-scroll-reveal="enter ease 0">{{ this_year }}</div>
      {% else %}
        </ul><ul class="articles-list__list">
          <div class="articles-list__title" data-scroll-reveal="enter ease 0">{{ this_year }}</div>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>
