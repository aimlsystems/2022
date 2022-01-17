---
layout: other
title: Industry Liaison
---

{% assign panel = site.data.indusLiason.panel %}

{:.nt-header}
## Panel Discussion

{:.text-center}
### {{ panel.time }}

{:.nt-panel-title}
##### Topic: _{{ panel.topic }}_

{:.nt-panel-title}
##### Moderator

<div class="row">
{% assign mem = panel.moderator %}
<div class="off-3 off-0-medium col-6 col-12-medium">
    <div class="row">
        <div class="col-3">
            <img class="img-fuild" style="max-width: 120px; max-height: auto;" src="{{ site.baseurl }}/images/peoples/{{ site.data.peoples[mem][3] | default: "avtar.png" }}?{{ site.time | date: "%s" }}">
        </div>
        <div class="col-9">
            <div class="nt-feature-pad">
                <h3><a href="{{ site.data.peoples[mem][2] | default: "#" }}" target="_blank">{{ site.data.peoples[mem][0] | default: mem }}</a></h3>
                <p>{{ site.data.peoples[mem][1] | default: ""}}</p>
            </div>
        </div>
    </div>
</div>
</div>

{% assign committee = panel.panelist %}

{% if committee.size > 0 %}

{:.nt-panel-title}
##### Panelists
<div class=row>
{% assign sm-modulo = committee.size | modulo: 2 %}
{% assign md-modulo = committee.size | modulo: 3 %}
{% for mem in committee %}
{% assign sm-offset = "0" %}
{% if forloop.last and sm-modulo==1 %}
{% assign sm-offset = "3" %}
{% endif %}
{% assign md-offset = "0" %}
{% if forloop.last and md-modulo==1 %}
{% assign md-offset = "4" %}
{% elsif forloop.rindex==2 and md-modulo==2 %}
{% assign md-offset = "2" %}
{% endif %}
<div class="col-6 col-12-medium">
    <div class="row">
        <div class="col-3">
            <img class="img-fuild" style="max-width: 120px; max-height: auto;" src="{{ site.baseurl }}/images/peoples/{{ site.data.peoples[mem][3] | default: "avtar.png" }}?{{ site.time | date: "%s" }}">
        </div>
        <div class="col-9">
            <div class="nt-feature-pad">
                <h3><a href="{{ site.data.peoples[mem][2] | default: "#" }}" target="_blank">{{ site.data.peoples[mem][0] | default: mem }}</a></h3>
                <p>{{ site.data.peoples[mem][1] | default: ""}}</p>
            </div>
        </div>
    </div>
</div>
{% endfor %}
</div>

{% endif %}



{:.nt-header}
## Invited Talks

{% assign speakers = site.data.indusLiason.invited %}

{% assign sm-modulo = speakers.size | modulo: 2 %}
{% assign md-modulo = speakers.size | modulo: 3 %}

{% for speaker in speakers %}

{% assign mem = speaker[0] %}
{% assign detail = speaker[1] %}

{% assign sm-offset = "0" %}
{% if forloop.last and sm-modulo==1 %}
{% assign sm-offset = "3" %}
{% endif %}

{% assign md-offset = "0" %}
{% if forloop.last and md-modulo==1 %}
{% assign md-offset = "4" %}
{% elsif forloop.rindex==2 and md-modulo==2 %}
{% assign md-offset = "2" %}
{% endif %}

{% if detail['title'] == nil %}
{% continue %}
{% endif %}

<a id="keynote_{{ forloop.index }}_{{ catId }}"></a>
<div class="row">
    <div class="col-3 col-12-medium">
        <div class="row text-center">
            <div class="col-12">
                <img class="img-fuild" style="max-width: 120px; max-height: auto;" src="{{ site.baseurl }}/images/peoples/{{ site.data.peoples[mem][3] | default: "avtar.png" }}?{{ site.time | date: "%s" }}">
            </div>
            <div class="col-12">
                <div class="nt-feature-pad">
                    <h3><a href="{{ site.data.peoples[mem][2] | default: "#" }}" target="_blank">{{ site.data.peoples[mem][0] | default: mem }}</a></h3>
                    <p>{{ site.data.peoples[mem][1] | default: ""}}</p>
                </div>
            </div>
        </div>
    </div>
    <div class="col-9 col-12-medium">
        <h4>{{ detail['title'] }}</h4>
        {% if detail['abstract'] %}

        {% for d in detail['abstract'] %}
        <div class="text-justify">
            {% if forloop.first %}
            <b>Abstract:</b> 
            {% else %}
                &nbsp;&nbsp;&nbsp;&nbsp;
            {% endif %}
            {{ d }}
        </div>
        {% endfor %}
        {% endif %}

        {% if site.data.bio[mem] %}
        {% for b in site.data.bio[mem] %}
        <div class="text-justify">
            {% if forloop.first %}
            <b>Bio:</b> 
            {% else %}
                &nbsp;&nbsp;&nbsp;&nbsp;
            {% endif %}
            {{ b }}
        </div>
        {% endfor %}
        {% endif %}
    </div>
</div>
<br>
<br>


{% endfor %}
