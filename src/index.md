---
layout: template.njk
title: Home
---



<section class="section_stage_theme">
  <div class="container">
    <h1>Inclusive design in local government</h1>
    <p class="lead col-12 col-lg-8">Use this design system to make your service consistent with Norfolk.gov. Learn from the research and experience of other service teams and avoid repeating work that's already been done.</p>
  </div>
</section>

<section class="section_light_theme">
  <div class="container">
    <h2>This is a big header</h2>
    <p>Some random HTML</p>
    BLOG POSTS:
    <ul>
      {%- for post in collections.post -%}
        <li>
          Title: <a href="{{ post.data.link | url }}">{{ post.data.title }}</a><br>
          Description: {{ post.data.description }}<br>
          Date: {{ post.data.date }}<br>
          Author: {{ post.data.author }}<br>
          Tags: {{ post.data.tags }}
        </li>
      {%- endfor -%}
    </ul>
  </div>
</section>
