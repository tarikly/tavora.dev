---
layout: page
permalink: /blog/
---
blog posts

{%- if site.posts.size > 0 -%}

  <!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->
  <ul class="post-list">
    {%- for post in site.categories.blog -%}

    {%- include list-body.html -%}

    {%- endfor -%}

  </ul>
  {%- endif -%}