---
layout: other
title: Technical Program
---

{% for ses in site.data.technicalProgram %}

{% if forloop.index0 > 0 %}
<br>
{% endif %}

<a id="{{ ses[0] }}">

# {{ ses[1]["time"] }}

## {{ ses[0] }}: {{ ses[1]["session"] }}

<div markdown=1 class="bd-callout bd-callout-info">

<ul>
{% for paper in ses[1]["papers"] %}

<li><b><i>{{ paper }}</i></b></li>

{% endfor %}
</ul>

</div>


{% endfor %}
