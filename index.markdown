---
title: Gallery index
layout: index
---
<div id = "gallery">
  {% assign sorted_exhibits = site.exhibits %}
  {% for exhibit in sorted_exhibits %}
    {% assign licence_url = site.data.licences | find: "licence", exhibit.licence %}
    {% assign division = site.data.divisions | find: "division", exhibit.division %}
    <div class = "">
      <a href = "{{ exhibit.url | relative_url }}"><img src="{{ exhibit.image-url }}" width = 250></a>
      <p class = ""><a href = "{{exhibit.url | relative_url}}">{{ exhibit.title }}</a> in <a href = "{{ division.weburl}}">{{ exhibit.division}}</a></p>
      <p><a href = "{{licence_url.url }}">{{ exhibit.licence }}</a></p>
      <p>{{ exhibit.tags }}</p>
    </div>
{% endfor %}
  <div id = "">
            <p>Creat by Chenkai, Zhuoqun, Mengxin, Ruowei</p>
  </div>
</div>

