---
title: "Recent Discussions"
permalink: /recent-discussions/
layout: archive
author_profile: true
---
<!-- ---
layout: archive
title: "Recent Discussions"
permalink: /recent-discussions/
author_profile: true
--- -->

{% include base_path %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}