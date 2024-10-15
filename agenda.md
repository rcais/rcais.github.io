---
layout: splash
title: Agenda
toc: true
---

<font color="red"><em>The following schedule is tentative.</em></font>

<h1>Monday October 28th: Doctoral Consortium</h1>

| Time | Activity | 
|------|----------|
{% for x in site.data.agenda.monday -%}
{%- for y in x.slots -%}
| {{ y.time }} | {{ y.activity }} | 
{% endfor %}
{% endfor %} 

<h1>Tuesday October 29th: Main Summit</h1>

| Time | Activity | Room 1 | Room 2 | Room 3 |
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

| Time | Activity | Room 1 | Room 2 | Room 3 |
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


