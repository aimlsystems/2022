---
layout: other
title: Volunteers
---

{% assign speakers = "Avaneesh, Tanmay Jain, Harsh Pandey, Utkalika Satapathy, Shivangi" | split: ", " %}
<div class="row">
{% for speaker in speakers %}
{% assign mem = speaker %}


<div class="col-6 col-12-medium">
    <div class="row">
        <div class="col-3">
            <img class="img-fuild" style="max-width: 120px; max-height: auto;" src="{{ site.baseurl }}/images/peoples/{{ site.data.peoples[mem][3] | default: "avtar.png" }}?{{ site.time | date: "%s" }}">
        </div>
        <div class="col-9">
            <div class="nt-feature-pad">
                <h3><a href="{{ site.data.peoples[mem][2] | default: "#" }}" target="_blank">{{ site.data.peoples[mem][0] | default: mem }}</a></h3>
                <div>{{ site.data.peoples[mem][1] | default: ""}}</div>
            </div>
        </div>
    </div>
</div>

<!-- <div class="col-12 offset-sm-{{ sm-offset }} col-sm-6 offset-md-{{ md-offset }} col-md-4 p-4">
    <div class="col-6 offset-3"><img src="{{ site.baseurl }}/images/peoples/{{ site.data.peoples[mem][3] | default: "avtar.png" }}?{{ site.time | date: "%s" }}" class="img-fluid" style="width: 100%;" ></div>
    <h5 class="text-center"><a href="{{ site.data.peoples[mem][2] | default: "#" }}" target="_blank">{{ site.data.peoples[mem][0] | default: mem }}</a></h5>
    <h5 class="text-center">{{ site.data.peoples[mem][1] | default: ""}}</h5>
    <h5 class="text-center">

    </h5>
</div> -->


{% endfor %}
</div>
