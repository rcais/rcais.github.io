---
layout: splash
title: Organization
toc: true
---

<h1>Organizing Committee:</h1>

{% for x in site.data.organization.members %}
  <p>
    <img src="{{ x.image }}" width="100">
    <a href="{{ x.website }}">{{ x.name }}</a>, {{ x.rank }}, {{ x.title}} {{ x.affiliation }}
  </p>
{% endfor %}

