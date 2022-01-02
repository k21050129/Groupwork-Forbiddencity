---
title: Divisions
layout: index
---

<ul>
{% assign divisions_alphabetical = site.data.divisions | sort: "division" %}
{% for division in divisions_alphabetical %}
 <li><a href = "{{ division.weburl }}">{{ division.division }}</a></li>
 {% endfor %}
 </ul>