---
title: Blog
layout: page
permalink: /blog/
pagination:
  enabled: true
---

<p class="blog-archive"><a href="{{ "/blog/archive" | relative_url }}">Archive</a></p>

{%- if paginator.posts.size > 0 -%}
    <ul class="post-list">
        {%- for post in paginator.posts -%}
            <li>{%- include post_excerpt.html post = post %}</li>
        {%- endfor -%}
    </ul>
    
    {% if paginator.total_pages > 1 %}
        {% include paginator.html %}
    {% endif %}
{%- endif -%}<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
