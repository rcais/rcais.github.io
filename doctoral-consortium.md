---
layout: splash
title: Doctoral Consortium
toc: true
---

<h1>Doctoral Consortium</h1>

The Doctoral Consortium on Responsible Computing, AI, and Society will be held on October 28th at the Global Learning Center on Georgia Tech campus.

The Doctoral Consortium will provide opportunities to receive mentorship on the crucial issues navigating research in responsible computing, AI, and policy.

<h1>Participants</h1>

{% assign participants = site.data.dc.participants | sort: 'name' %}

<table>
{% tablerow x in participants cols: 4 %}
<div id="{{ x.name }}" style="text-align:center;">
{% if x.image %}
<img src="{{ x.image }}" style="height:200px;width:auto;"><br>
{% endif %}
<a href="{{ x.website }}">{{ x.name }}</a><br>
{{ x.affiliation }}
</div>
{% endtablerow %}
</table>