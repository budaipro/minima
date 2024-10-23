---
layout: home
list_title: "法藏经书："
---
<div>
  <h3 style="font-size: 18px;">过去五十三佛及过去七佛</h3>
  <p>〖【繁体】普光佛、普明佛、普靜佛、多摩羅跋栴檀香佛、栴檀光佛、摩尼幢佛、歡喜藏摩尼寶積佛、一切世間樂見上大精進佛、摩尼幢燈光佛、慧炬照佛、海德明光佛、金剛牢疆普散金光佛、大彊精進勇猛佛、大悲光佛、慈力王佛、慈藏佛、栴檀窟莊嚴勝佛、賢善首佛、善意佛、廣莊嚴佛、金華光佛、寶蓋照空自在王佛、虛空寶華光佛、琉璃莊嚴王佛、普現色身光佛、不動智光佛、降伏諸魔王佛、才光明佛、智慧勝佛、彌勒仙光佛、世靜光佛、善寂月音妙尊智王佛、龍種上尊王佛、日月光佛、日月珠光佛、慧幡勝王佛、師子吼自在力王佛、妙音勝佛、常光幢佛、觀世燈佛、慧威燈王佛、法勝王佛、須彌光佛、須蔓那華光佛、優曇鉢羅華殊勝王佛、大慧力王佛、阿閦毘歡喜光佛、無量音聲王佛、才光佛、金海光佛、山海慧自在通王佛、大通光佛、一切法常滿王佛。</p>
  <p>毘婆尸佛、尸棄佛、毘舍佉佛、拘留孫佛、拘那含牟尼佛、迦葉佛、釋迦牟尼佛。〗</p>
</div>

{% if site.paginate %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{%- if posts.size > 0 -%}
  {%- if page.list_title -%}
  <h2 class="post-list-heading">{{ page.list_title }}</h2>
  <div style="margin-bottom: 15px;">如《佛说海八德经》中云：『【繁体】（佛告沙門曰）<strong>吾之經籍，<em>義美</em>甘露，仙聖<em>所不聞</em>，梵釋<em>所希覩</em>，<em class="red">往古來今，無物不記</em>，邊中<em>皆正</em>，猶海通鹹。亦<em class="red">以斯故，沙門<i>樂之</i></em>。夫見吾經者，<span class="red"><em><i>意</i></em>皆趣無為</span>矣。</strong>』</div>
  <div style="margin-bottom: 15px;"><em>本站经书皆用繁体本，以简体注释。</em></div>
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
