---
layout: splash
title: Agenda
toc: true
---

<strong>Confirmed Speakers:</strong>

{% for x in site.data.organization.members %}
  <p>
    <img src="{{ x.image }}" width="100">
    <a href="{{ x.website }}">{{ x.name }}</a>, {{ x.rank }}, {{ x.title}}, {{ x.affiliation }}
{% endfor %}
