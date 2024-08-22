---
layout: splash
title: Agenda
toc: true
---

<strong>Organizing Committee:</strong>

{% for x in site.data.organization.members %}
  <p>
    <img src="{{ x.image }}" width="100">
    <a href="{{ x.website }}">{{ x.name }}</a>, {{ x.rank }}, {{ x.affiliation }}
  </p>
{% endfor %}

