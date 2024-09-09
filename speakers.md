---
layout: splash
title: Speakers
toc: true
---

<strong>Confirmed Speakers:</strong>

<ul>
{% for x in site.data.speakers.invited %}
  <li>
    <a href="{{ x.website }}">{{ x.name }}</a>, {{ x.title}}, {{ x.affiliation }}
   </li>
{% endfor %}
</ul>