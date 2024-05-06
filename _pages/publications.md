---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<!--{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}-->

{% include base_path %}

{% assign current_year = "" %}
{% for post in site.publications reversed %}
  {% assign year = post.date | date: "%Y" %}
  {% if current_year != year %}
    {% assign current_year = year %}
    {% include archive-subheader.html %}
  {% endif %}
  {% include archive-single-publications.html %}
{% endfor %}
