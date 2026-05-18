---
title: "Recent Discussions"
permalink: /recent-discussions/
layout: archive
author_profile: true
---

{% for post in site.talks reversed %}
<div style="margin-bottom: 20px; font-size: 0.95em; line-height: 1.5;">
  {{ post.date | date: "%Y" }}, {{ post.venue }}: 
  "<i>{{ post.title }}</i>" 
  {% if post.paperurl %}by {{ post.paperurl }}{% endif %}.
  <a href="{{ post.slidesurl }}" target="_blank" style="text-decoration: underline;">slides</a>
</div>
{% endfor %}

<!-- {% include base_path %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %} -->