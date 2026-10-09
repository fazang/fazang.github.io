---
layout: base
title: 摘经
permalink: /highlights/
---

<p class="breadcrumb">
  <span>位置：</span>
  <span>首页</span>
  <span>/</span>
  <span>{{ page.title }}</span>
</p>

{% assign highlights = site.highlights | sort: 'date' | reverse %}

{%- if highlights.size > 0 -%}

  <ul class="highlights-list">
    {%- for highlight in highlights -%}
      <li>
        <a href="{{ highlight.url | relative_url }}">{{ highlight.title | escape }}</a>
        {%- comment -%}<div>{{ highlight.content | markdownify }}</div>{%- endcomment -%}
      </li>
    {%- endfor -%}
  </ul>

{%- endif -%}