---
layout: page
title: 标签
header: Posts By Tag
permalink: /tags
comments: False
---
{% include JB/setup %}

<ul class="tag-box inline" style="margin-bottom: 20px;">
  {% assign tags_list = site.tags %}
  {% include JB/tags_list %}
</ul>

{% for tag in site.tags %} 
<h2 id="{{ tag[0] }}-ref">{{ tag[0] }}</h2>
<ul>
  {% assign pages_list = tag[1] %}
  {% include JB/pages_list %}
</ul>
{% endfor %}
