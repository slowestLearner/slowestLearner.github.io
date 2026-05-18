---
layout: single
title: "Recent Discussions"
permalink: /recent-discussions/
author_profile: true
---

{% assign sorted_talks = site.talks | sort: 'date' | reverse %}

{% for post in sorted_talks %}
<div style="margin-bottom: 25px;">
  <p style="font-size: 0.95em; line-height: 1.6; margin: 0;">
    {{ post.date | date: "%Y" }}, {{ post.venue }}: 
    "<i>{{ post.title }}</i>" 
    {% if post.paperurl %}by {{ post.paperurl }}{% endif %}.
    [<a href="{{ post.slidesurl | relative_url }}" target="_blank">slides</a>]
  </p>
</div>
{% endfor %}