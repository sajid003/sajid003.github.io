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

## In Preparation
{% assign review_papers = site.publications | where: "status", "review" | sort: "weight" %}
{% for post in review_papers %}
  {% include archive-single.html %}
{% endfor %}

## Peer-Reviewed Publications
{% assign published_papers = site.publications | where: "status", "published" | sort: "weight" %}
{% for post in published_papers %}
  {% include archive-single.html %}
{% endfor %}
