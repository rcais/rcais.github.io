---
layout: splash
title: Agenda
toc: true
---
<script type="text/javascript"> 
function toggleBibtex(obj) { 
	console.log(obj)
	var id = obj;
	element = document.getElementById(obj)
	console.log(element);
	if (element.style.display == "none") {
		element.style.display="block";
	}
	else {
		element.style.display="none";
	} 
}
</script>

<style type="text/css" src="bibs.css">
.bibbutton {
	font-size: small;
	background-color: black;
	color: white;
	border: 1px solid black;
	text-decoration: none;
	text-decoration-color: white;
	border-radius: 2px;
}
.bibtex {
	white-space: pre-wrap;
	background: #ffffff;
	color: red;
	border: 1px dotted red;
	width: 75%;
	position:absolute;
	overflow: hidden;
	z-index:2400;
	width: 250px;
}	
</style>

<h1>Agenda</h1>

The Summit takes place at the <a href="/location">Georgia Tech Global Learning Center</a> on the 2nd and 3rd floors.

<p><font color="red"><em>The following schedule is subject to change.</em></font></p>

<h1>Monday October 28th: Doctoral Consortium</h1>

The Doctoral Consortium will be held in the Georgia Tech Hotel, Conference Room A. It is connected to the Global Learning Center on the 2nd floor.

Please see the <a href="/doctoral-consortium">Doctoral Consortium</a> page for agenda.


<h1>Tuesday October 29th: Main Summit</h1>

{% assign allspeakers = site.data.speakers.invited | concat: site.data.speakers.gt | concat: site.data.speakers.keynote %}

<table width="100%" border=1 frame=void rules=rows>
	<tr><th>Time</th><th>Activity</th><th>Room 222</th><th>Room 330</th><th>Room 334</th></tr>
	{% for x in site.data.agenda.tuesday %}
		{% for y in x.slots %}
			<tr>
				<td>{{ y.time }}</td>
				<td>{{ y.activity }}</td>
				{% if y.tracks == nil %}
					<td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td>
				{% else %}
					{% for z in y.tracks %}
						{% assign foo = allspeakers | where:"name", z.name | first %}
						{% assign bar = foo.talk %}
						<td><a href="/speakers/index.html#{{z.name}}">{{ z.name }}</a>
						{% if bar != nil %}
							<a onclick="toggleBibtex('{{ z.name }}');"><span class="bibbutton">talk</span></a><div class="bibtex" id="{{ z.name }}" style="display: none;">{{ bar }}</div>
						{% endif %}
						</td>
					{% endfor %}
				{% endif %}
			</tr>
		{% endfor %}
	{% endfor %}
</table>



<h1>Wednesday October 30th: Main Summit</h1>

<table width="100%" border=1 frame=void rules=rows>
	<tr><th>Time</th><th>Activity</th><th>Room 222</th><th>Room 330</th></tr>
	{% for x in site.data.agenda.wednesday %}
		{% for y in x.slots %}
			<tr>
				<td>{{ y.time }}</td>
				<td>{{ y.activity }}</td>
				{% if y.tracks == nil %}
					<td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td>
				{% else %}
					{% for z in y.tracks %}
						{% assign foo = allspeakers | where:"name", z.name | first %}
						{% assign bar = foo.talk %}
						<td><a href="/speakers/index.html#{{z.name}}">{{ z.name }}</a>
						{% if bar != nil %}
							<a onclick="toggleBibtex('{{ z.name }}');"><span class="bibbutton">title</span></a><div class="bibtex" id="{{ z.name }}" style="display: none;">{{ bar }}</div>
						{% endif %}
						</td>
					{% endfor %}
				{% endif %}
			</tr>
		{% endfor %}
	{% endfor %}
</table>

