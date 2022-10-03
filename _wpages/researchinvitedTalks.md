---
layout: other
title: Research Invited Speakers
---

{:.nt-header}
<!-- ## Invited Talks
 -->
 {:.text-center}
 ### {{ panel.time }}
{% assign speakers = site.data.researchinvitedTalk.invited %}

{% assign sm-modulo = speakers.size | modulo: 2 %}
{% assign md-modulo = speakers.size | modulo: 3 %}

{% for speaker in speakers %}
{% assign catId = forloop.index %}
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



<!-- {{ forloop.index }} -->
<a id="researchinvited_{{ forloop.index }}"></a>
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
        <h2>{{ detail['title'] }}</h2>
        {% if detail['abstract'] %}
        {% for d in detail['abstract'] %}
        <div class="text-justify">
            {% if forloop.first %}
            <b>Abstract:</b> <br/>
            {% else %}
                &nbsp;&nbsp;&nbsp;&nbsp;
            {% endif %}
            {{ d }}
        </div>
        <br/>
        {% endfor %}
        {% endif %}
        {% if site.data.bio[mem] %}
        {% for b in site.data.bio[mem] %}
        <div class="text-justify">
            {% if forloop.first %}
            <b>Bio:</b> <br/>
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
