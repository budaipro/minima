---
layout: base
title: 摘抄
---
<div class="breadcrumb">
  <a href="{{ site.baseurl }}/">主页</a>
  <span>/</span>
  <strong>摘抄</strong>
</div>

<h2 style="margin: 15px 0;">{{ page.title }}</h2>

<ul>
{%- for excerpt in site.excerpts -%}
  <li><a href="{{ excerpt.url }}">{{ excerpt.title }}</a><em class="darkgray">{{ excerpt.sutra }}</em></li>
{%- endfor -%}
</ul>
