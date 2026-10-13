---
layout: base
title: 摘要
permalink: /highlights/
---

<p class="breadcrumb">
  <span>{{ page.title }}</span>
</p>

{% assign highlights = site.highlights | sort: 'date' | reverse %}

{%- assign date_format = site.minima.date_format | default: "%Y/%d/b" -%}

{%- if highlights.size > 0 -%}

  <ul class="highlights-list">
    {%- for highlight in highlights -%}
      <li>
        <a href="{{ highlight.url | relative_url }}">{{ highlight.title | escape }}</a>
        <span>{{ highlight.date | date: date_format }}</span>
        {%- comment -%}<div>{{ highlight.content | markdownify }}</div>{%- endcomment -%}
      </li>
    {%- endfor -%}
  </ul>

{%- endif -%}