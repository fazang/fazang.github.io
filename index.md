---
layout: base
---

<p class="breadcrumb">
  <span>经论</span>
</p>

{% if site.paginate %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{%- if posts.size > 0 -%}

  <ul>
    {%- assign date_format = site.minima.date_format -%}
    {%- for post in posts -%}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>&nbsp;{%- comment -%}<span>{{ post.date | date:
      date_format }}</span>{%- endcomment -%}
      </li>
    {%- endfor -%}
  </ul>

  {% if site.paginate %}
    <ul>
      {%- if paginator.previous_page %}
        <li>
          <a href="{{ paginator.previous_page_path | relative_url }}" title="Go to Page {{ paginator.previous_page }}">
            {{ paginator.previous_page }}
          </a>
        </li>
      {%- else %}
        <li>•</li>
      {%- endif %}

      <li>{{ paginator.page }}</li>

      {%- if paginator.next_page %}
        <li>
          <a href="{{ paginator.next_page_path | relative_url }}" title="Go to Page {{ paginator.next_page }}">
            {{ paginator.next_page }}
          </a>
        </li>
      {%- else %}
        <li>•</li>
      {%- endif %}
    </ul>
  {%- endif %}

{%- endif -%}