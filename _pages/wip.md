---
layout: archive
title: "Work in Progress"
permalink: /wip/
author_profile: true
---

{% assign wips = site.wip | sort: "year" | reverse %}

{% for project in wips %}
<div style="margin-bottom: 1.5em;">
  <strong>{{ project.title }}</strong><br />
  with {{ project.authors }}<br />
  <em>{{ project.status }}</em><br />
  {% if project.abstract %}
  <span class="wip-abstract">Abstract:</span> {{ project.abstract }}
  {% endif %}
</div>
{% endfor %}
