---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

## Peer-Reviewed Publications
{% assign published_papers = site.publications | where: "status", "published" %}
{% for post in published_papers reversed %}
  {% include archive-single.html %}
{% endfor %}

## Under Review
{% assign review_papers = site.publications | where: "status", "review" %}
{% for post in review_papers reversed %}
  {% include archive-single.html %}
{% endfor %}


