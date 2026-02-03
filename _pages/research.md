---
layout: archive
title: "Research"
permalink: /Research/
author_profile: true
---

<h2>Journal Articles</h2>
<hr />

{% assign articles = site.publications | where: "category", "articles" | sort: "year" | reverse %}
{% assign counter = 1 %}

{% for post in articles %}
<div style="margin-bottom: 1.5em;">
  [{{ counter }}] {{ post.authors }}. ({{ post.year }}). "{{ post.title }}." 
  <i>{{ post.venue }}</i>{% if post.volume %}, {{ post.volume }}{% endif %}{% if post.number %}({{ post.number }}){% endif %}{% if post.pages %}: {{ post.pages }}{% endif %}.
  {% if post.paperurl %} <a href="{{ post.paperurl }}">Paper</a>{% endif %}
</div>

{% assign counter = counter | plus: 1 %}
{% endfor %}
