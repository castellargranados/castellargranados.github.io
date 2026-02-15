---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

<h2>Instructor of Record</h2>
<hr />

{% assign sorted_instructor = site.teaching | where: "role", "Instructor of Record" | sort: "year" | reverse %}

{% for course in sorted_instructor %}
<div style="margin-bottom: 1.2em;">
  <strong>{{ course.institution }}</strong><br />
  {{ course.title }} ({{ course.level }}). {{ course.term }}.
</div>
{% endfor %}
