---
layout: archive
title: "Research"
permalink: /Research/
author_profile: true
---

{% assign articles = site.publications | where: "category", "articles" | sort: "year" | reverse %}
{% assign counter = articles | size %}

<h2>Journal Articles</h2><hr />

{% for post in articles %}
<div class="list__item">
{{ counter }}. {{ post.authors }}. ({{ post.year }}). "{{ post.title }}." <i>{{ post.venue }}</i>{% if post.volume %}, {{ post.volume }}{% endif %}{% if post.number %}({{ post.number }}){% endif %}{% if post.pages %}: {{ post.pages }}{% endif %}. 
{% if post.paperurl %}<a href="{{ post.paperurl }}">Paper</a>{% endif %}
</div>
{% assign counter = counter | minus: 1 %}
{% endfor %}
