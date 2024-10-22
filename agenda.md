---
layout: splash
title: Agenda
toc: true
---

<h1>Agenda</h1>

The Summit takes place at the <a href="/location">Georgia Tech Global Learning Center</a> on the 2nd and 3rd floors.

<p><font color="red"><em>The following schedule is subject to change.</em></font></p>

<h1>Monday October 28th: Doctoral Consortium</h1>

The <a href="/doctoral-consortium">Doctoral Consortium</a> will be held in the Georgia Tech Hotel, Conference Room A. It is connected to the Global Learning Center on the 2nd floor.

| Time | Activity | 
|------|----------|
{% for x in site.data.agenda.monday -%}
{%- for y in x.slots -%}
| {{ y.time }} | {{ y.activity }} | 
{% endfor %}
{% endfor %} 

<h1>Tuesday October 29th: Main Summit</h1>

| Time | Activity | GLC Room 222 | GLC Room 330 | GLC Room 334 |
|------|----------|--------|--------|--------|
{% for x in site.data.agenda.tuesday -%}
{%- for y in x.slots -%}
{% if y.tracks == nil -%}
| {{ y.time }} | {{ y.activity }} | | | | 
{%- else -%}
| {{ y.time }} | {{ y.activity }} | {%- for z in y.tracks -%}<a href="/speakers/index.html#{{z.name}}">{{ z.name }}</a>|
{%- endfor -%}
{% endif %}
{% endfor %}
{% endfor %} 

<h1>Wednesday October 30th: Main Summit</h1>

| Time | Activity | GLC Room 222 | GLC Room 330 | GLC Room 334 |
|------|----------|--------|--------|--------|
{% for x in site.data.agenda.wednesday -%}
{% for y in x.slots -%}
{% if y.tracks == nil -%}
| {{ y.time }} | {{ y.activity }} | | | | 
{%- else -%}
| {{ y.time }} | {{ y.activity }} | {%- for z in y.tracks -%}<a href="/speakers/index.html#{{z.name}}">{{ z.name }}</a>|
{%- endfor -%}
{% endif %}
{% endfor %}
{%- endfor -%} 
