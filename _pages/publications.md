---
layout: single
title: "Research"
permalink: /publications/
author_profile: true
---

## WORKING PAPERS
{% assign working = site.publications | where: "category", "working" | sort: "date" | reverse %}
{% for post in working %}
<div style="margin-bottom: 30px;">
  <p style="margin: 0;">
    <a href="{{ post.paperurl }}" target="_blank" rel="noopener noreferrer" style="font-weight: bold; text-decoration: underline; font-size: 1.1em;">{{ post.title }}</a> with {{ post.authors }}
  </p>

  {% if post.status and post.status != "Working Paper" %}
    <p style="margin: 5px 0; font-style: italic;">{{ post.status }}</p>
  {% endif %}

  <p style="margin: 5px 0;">
    <strong>Takeaway:</strong> <span style="color: #2c3e50; font-size: 0.9em; font-style: italic;">{{ post.takeaway }}</span>
  </p>
</div>
{% endfor %}

---

## PUBLISHED PAPERS
{% assign published = site.publications | where: "category", "published" | sort: "date" | reverse %}
{% for post in published %}
<div style="margin-bottom: 30px;">
  <p style="margin: 0;">
    <a href="{{ post.paperurl }}" target="_blank" rel="noopener noreferrer" style="font-weight: bold; text-decoration: underline; font-size: 1.1em;">{{ post.title }}</a> with {{ post.authors }}
  </p>
  <p style="margin: 5px 0;">{{ post.venue }}, {{ post.date | date: "%Y" }}</p>
  
  {% if post.publisher_url %}
  <p style="margin: 5px 0; font-size: 0.9em;">
    <a href="{{ post.publisher_url }}" target="_blank" rel="noopener noreferrer" style="text-decoration: underline;">Publisher Link</a>
  </p>
  {% endif %}

  <p style="margin: 5px 0;">
    <strong>Takeaway:</strong> <span style="color: #2c3e50; font-size: 0.9em; font-style: italic;">{{ post.takeaway }}</span>
  </p>
</div>
{% endfor %}

