---
layout: base
title: 摘抄
---
<div class="breadcrumb">
  <a href="{{ site.baseurl }}/">主页</a>
  <span>/</span>
  <strong>摘抄</strong>
</div>

<ul>
{%- for excerpt in site.excerpts -%}
  <li><a href="{{ excerpt.url }}">{{ excerpt.title }}</a></li>
{%- endfor -%}
</ul>
