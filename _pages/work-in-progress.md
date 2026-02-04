---
layout: archive
title: "Work in Progress"
permalink: /work-in-progress/
author_profile: true
---

<h2>Work in Progress</h2>
<hr />

{% assign sorted_wip = site.wip | sort: "year" | reverse %}
{% assign counter = sorted_wip | size %}

{% for post in sorted_wip %}
<div style="margin-bottom: 2em;">
  [{{ counter }}] <strong>{{ post.title }}</strong><br />
  {% if post.authors %}with {{ post.authors }}<br />{% endif %}
  {% if post.status %}{{ post.status }}.<br />{% endif %}
  {% if post.abstract %}<em>Abstract:</em> {{ post.abstract }}{% endif %}
</div>
{% assign counter = counter | minus: 1 %}
{% endfor %}
