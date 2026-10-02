---
layout: page
title: 摘经
permalink: /highlights/
---

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