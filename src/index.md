---
layout: template.njk
title: Home
---

{% import "_pattern_macros/bloglist.njk" as bloglist %}

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
    {{ bloglist.bloglist(collections.post, 4) }}
  </div>
</section>

<a href="{{ 'blogs/blog-posts' | url }}">View all blog posts (pagination test)</a>
