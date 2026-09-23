---
layout: page
title: 摘经
---

{% assign quotes = site.quotes %}

{%- if quotes.size > 0 -%}

  <div>
    {%- for quote in quotes -%}
      <div>
        <a href="{{ quote.url | relative_url }}">{{ quote.title | escape }}</a>
        <p>{{ quote.content | markdownify }}</p>
      </div>
    {%- endfor -%}
  </div>

{%- endif -%}