---
layout: page
title: 摘经
permalink: /quotes/
---

{% assign quotes = site.quotes %}

{%- if quotes.size > 0 -%}

  <div>
    {%- for quote in quotes -%}
      <div>
        <a href="{{ quote.url | relative_url }}">{{ quote.title | escape }}</a>
        <div>{{ quote.content | markdownify }}</div>
      </div>
    {%- endfor -%}
  </div>

{%- endif -%}