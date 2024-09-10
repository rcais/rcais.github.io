---
layout: splash
title: Speakers
toc: true
---

<h2>Keynote</h2>

<ul>
{% for x in site.data.speakers.keynote %}
  <li>
    <a href="{{ x.website }}">{{ x.name }}</a>, {{ x.title}}, {{ x.affiliation }}
    <blockquote>{{ x.talk }}
    </blockquote>
   </li>
{% endfor %}
</ul>

<h2>Confirmed Speakers</h2>

<ul>
{% for x in site.data.speakers.invited %}
  <li>
    <a href="{{ x.website }}">{{ x.name }}</a>, {{ x.title}}, {{ x.affiliation }}
   </li>
{% endfor %}
</ul>