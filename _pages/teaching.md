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
  {{ course.name }} ({{ course.level }}). {{ course.term }}.
</div>
{% endfor %}


<h2>Teaching Assistant</h2>
<hr />

{% assign sorted_ta = site.teaching | where: "role", "Teaching Assistant" | sort: "year" | reverse %}

{% for course in sorted_ta %}
<div style="margin-bottom: 1.2em;">
  <strong>{{ course.institution }}</strong><br />
  {{ course.name }} ({{ course.level }}). {{ course.term }}.
</div>
{% endfor %}
