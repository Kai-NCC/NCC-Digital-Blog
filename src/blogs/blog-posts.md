---
title: All blog Posts
layout: template.njk

pagination:
  data: collections.post
  size: 2
  alias: posts
---

<ol>
{% for post in posts %}
  <li><a href="{{ post.url | url }}">{{ post.data.title }}</a></li>
{% endfor %}
</ol>

<div>
  <ul>
    <li>{% if pagination.href.previous %}<a href="{{ pagination.href.previous | url }}">Prev</a>{% else %}Prev{% endif %}</li>
    {%- for pageEntry in pagination.pages -%}
      <li>{% if page.url != pagination.hrefs[loop.index0] %}<a href="{{ pagination.hrefs[loop.index0] | url }}">{{ loop.index }}</a>{% else %}{{ loop.index }}{% endif %}</li>
    {%- endfor -%}
    <li>{% if pagination.href.next %}<a href="{{ pagination.href.next | url }}">Next</a>{% else %}Next{% endif %}</li>
  </ul>
</div>
