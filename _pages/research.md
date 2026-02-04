---
layout: archive
title: "Research"
permalink: /Research/
author_profile: true
---

<!-- JOURNAL ARTICLES -->

{% assign sorted_articles = site.publications | where: "category", "articles" | sort: "year" | reverse %}
{% assign counter = sorted_articles | size %}

<h2>Journal Articles</h2>
<hr />

{% for post in sorted_articles %}
<div style="margin-bottom: 1.5em;">
  [{{ counter }}] {{ post.authors }}. ({{ post.year }}). "{{ post.title }}."
  <i>{{ post.venue }}</i>{% if post.volume %}, {{ post.volume }}{% endif %}{% if post.number %}({{ post.number }}){% endif %}{% if post.pages %}: {{ post.pages }}{% endif %}.
</div>
{% assign counter = counter | minus: 1 %}
{% endfor %}


<!-- BOOKS -->

{% assign sorted_books = site.publications | where: "category", "books" | sort: "year" | reverse %}
{% assign counter = sorted_books | size %}

<h2>Authored Books</h2>
<hr />

{% for post in sorted_books %}
<div style="margin-bottom: 1.5em;">
  [{{ counter }}] {{ post.authors }}. ({{ post.year }}). <i>{{ post.title }}</i>.
  {{ post.venue }}.
</div>
{% assign counter = counter | minus: 1 %}
{% endfor %}


<!-- BOOK CHAPTERS -->

{% assign sorted_chapters = site.publications | where: "category", "chapters" | sort: "year" | reverse %}
{% assign counter = sorted_chapters | size %}

<h2>Book Chapters</h2>
<hr />

{% for post in sorted_chapters %}
<div style="margin-bottom: 1.5em;">
  [{{ counter }}] {{ post.authors }}. ({{ post.year }}). "{{ post.title }}."
  <i>{{ post.venue }}</i>{% if post.pages %}: {{ post.pages }}{% endif %}.
</div>
{% assign counter = counter | minus: 1 %}
{% endfor %}
