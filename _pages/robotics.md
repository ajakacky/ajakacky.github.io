---
layout: category
permalink: /categories/robotics/
taxonomy: Robotics
title: "Robotics Work"
author_profile: true
---

This page contains posts for all the robotics work that I have done over the years

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}