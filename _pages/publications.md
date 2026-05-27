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
    <a href="{{ post.paperurl }}" target="_blank" rel="noopener noreferrer" style="font-weight: bold; text-decoration: underline; font-size: 1.1em;">{{ post.title }}</a>
    {% if post.authors and post.authors != "" %} with {{ post.authors }}{% endif %}
  </p>
  
  {% if post.status and post.status != "Working Paper" %}
    <p style="margin: 5px 0; font-style: italic;">{{ post.status }}</p>
  {% endif %}

  {% if post.notes %}
  <div style="margin: 5px 0 10px 0; font-size: 0.95em; color: #333;">
    {{ post.notes | markdownify | replace: '<a href=', '<a target="_blank" rel="noopener noreferrer" href=' }}
  </div>
  {% endif %}

  <p style="margin: 5px 0;">
    <strong>Takeaway:</strong> <span style="color: #2c3e50; font-size: 0.9em; font-style: italic;">{{ post.takeaway }}</span>
  </p>
  
  {% if post.media_mentions %}
<p style="margin: 5px 0; font-size: 0.95em;">
  <strong>Media Coverage:</strong> 
  <span>
    {{ post.media_mentions | markdownify | replace: '<a href=', '<a target="_blank" rel="noopener noreferrer" href=' | remove: '<p>' | remove: '</p>' }}
  </span>
</p>
{% endif %}
</div>
{% endfor %}

---

## PUBLISHED PAPERS
{% assign published = site.publications | where: "category", "published" | sort: "date" | reverse %}
{% for post in published %}
<div style="margin-bottom: 30px;">
<p style="margin: 0;">
  <a href="{{ post.paperurl }}" target="_blank" rel="noopener noreferrer" style="font-weight: bold; text-decoration: underline; font-size: 1.1em;">{{ post.title }}</a>
  {% if post.authors and post.authors != "" %} with {{ post.authors }}{% endif %}
</p>
  <p style="margin: 5px 0;">{{ post.venue }}, {{ post.date | date: "%Y" }}</p>
  

  
  {% if post.publisher_url %}
  <p style="margin: 5px 0; font-size: 0.9em;">
    <a href="{{ post.publisher_url }}" target="_blank" rel="noopener noreferrer" style="text-decoration: underline;">Publisher Link</a>
  </p>
  {% endif %}

  {% if post.notes %}
  <div style="margin: 5px 0 10px 0; font-size: 0.95em; color: #333;">
    {{ post.notes | markdownify | replace: '<a href=', '<a target="_blank" rel="noopener noreferrer" href=' }}
  </div>
  {% endif %}

  <p style="margin: 5px 0;">
    <strong>Takeaway:</strong> <span style="color: #2c3e50; font-size: 0.9em; font-style: italic;">{{ post.takeaway }}</span>
  </p>

  {% if post.media_mentions %}
<p style="margin: 5px 0; font-size: 0.95em;">
  <strong>Media Coverage:</strong> 
  <span>
    {{ post.media_mentions | markdownify | replace: '<a href=', '<a target="_blank" rel="noopener noreferrer" href=' | remove: '<p>' | remove: '</p>' }}
  </span>
</p>
{% endif %}
</div>
{% endfor %}