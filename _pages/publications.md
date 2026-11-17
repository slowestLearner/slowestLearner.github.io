---
layout: single
title: "Published Papers"
permalink: /publications/
author_profile: true
---

{% assign published = site.publications | where: "category", "published" | sort: "date" | reverse %}
{% for post in published %}
  {% include paper-item.html %}
{% endfor %}