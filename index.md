---
layout: home
list_title: "佛典经籍："
---

{%- comment -%} 
<div>〖【繁体】普光佛、普明佛、普靜佛、多摩羅跋栴檀香佛、栴檀光佛、摩尼幢佛、歡喜藏摩尼寶積佛、一切世間樂見上大精進佛、摩尼幢燈光佛、慧炬照佛、海德明光佛、金剛牢疆普散金光佛、大彊精進勇猛佛、大悲光佛、慈力王佛、慈藏佛、栴檀窟莊嚴勝佛、賢善首佛、善意佛、廣莊嚴佛、金華光佛、寶蓋照空自在王佛、虛空寶華光佛、琉璃莊嚴王佛、普現色身光佛、不動智光佛、降伏諸魔王佛、才光明佛、智慧勝佛、彌勒仙光佛、世靜光佛、善寂月音妙尊智王佛、龍種上尊王佛、日月光佛、日月珠光佛、慧幡勝王佛、師子吼自在力王佛、妙音勝佛、常光幢佛、觀世燈佛、慧威燈王佛、法勝王佛、須彌光佛、須蔓那華光佛、優曇鉢羅華殊勝王佛、大慧力王佛、阿閦毘歡喜光佛、無量音聲王佛、才光佛、金海光佛、山海慧自在通王佛、大通光佛、一切法常滿王佛。</div>
{%- endcomment -%}

过去佛：
: - ...
    - **毘婆尸佛**
      - **尸棄佛**
        - **毘舍佉佛**
          - **拘留孫佛**
            - **拘那含牟尼佛**
              - **迦葉佛**
                - **釋迦牟尼佛**

{% if site.paginate %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{%- if posts.size > 0 -%}
  <div style="margin-bottom: 15px;">如《佛说海八德经》云：『<span style="font-style: italic;">（佛告沙门曰：）吾之经籍，义美甘露，仙圣所不闻、梵释所希睹；<strong>往古來今，无物不记，边中皆正</strong>，犹海通咸。亦以斯故，沙门<strong>乐</strong>之。夫见吾经者，<strong>意</strong>皆趣无为矣。</span>』</div>
  <hr>
  {%- if page.list_title -%}
  <h2 class="post-list-heading" style="margin-bottom: 5px;">{{ page.list_title }}</h2>
  <div style="margin-bottom: 15px; font-style: italic;">（本站经书皆用繁体本，以简体注释。原文由悟文重新断句标点。）</div>
  {%- endif -%}
  <ul class="post-list">
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    {%- for post in posts -%}
    <li>
      <span>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        <span class="post-meta post-tags">
          {%- if post.tags -%}
            {%- for tag in post.tags -%}
              <span>{{ tag }}</span>
            {%- endfor -%}
          {%- endif -%}
        </span>
        {%- comment -%}
        <span class="post-meta">
          <i>{{ post.date | date: date_format }}</i>
        </span>
        {%- endcomment -%}
      </span>
      {%- if site.show_excerpts -%}
        {{ post.excerpt }}
      {%- endif -%}
    </li>
    {%- endfor -%}
  </ul>

  {% if site.paginate %}
    <div class="pager">
      <ul class="pagination">
      {%- if paginator.previous_page %}
        <li><a href="{{ paginator.previous_page_path | relative_url }}" class="previous-page">{{ paginator.previous_page }}</a></li>
      {%- else %}
        <li><div class="pager-edge">•</div></li>
      {%- endif %}
        <li><div class="current-page">{{ paginator.page }}</div></li>
      {%- if paginator.next_page %}
        <li><a href="{{ paginator.next_page_path | relative_url }}" class="next-page">{{ paginator.next_page }}</a></li>
      {%- else %}
        <li><div class="pager-edge">•</div></li>
      {%- endif %}
      </ul>
    </div>
  {%- endif %}

{%- endif %}
