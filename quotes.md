---
layout: page
title: 摘经
permalink: /quotes/
---

{% assign quotes = site.quotes | sort: 'date' %}

{%- if quotes.size > 0 -%}

  <ul class="quote-list">
    {%- for quote in quotes -%}
      <li>
        <a href="{{ quote.url | relative_url }}">{{ quote.title | escape }}</a>
        {%- comment -%}<div>{{ quote.content | markdownify }}</div>{%- endcomment -%}
      </li>
    {%- endfor -%}
  </ul>

{%- endif -%}