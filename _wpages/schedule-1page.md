---
layout: other
title: Schedule
---

<style>
/* Style the tab */
.tab {
  overflow: hidden;
  /*border: 1px solid #ccc;
  background-color: #f1f1f1;*/
}

/* Style the buttons that are used to open the tab content */
.tab button {
  background-color: inherit;
  float: left;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 0px 16px;
  transition: 0.3s;
  background-color: #f1f1f1
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: #ddd;
}

/* Create an active/current tablink class */
.tab button.active {
  background-color: #ccc;
}

/* Style the tab content */
.tabcontent {
  display: block;
  padding: 6px 12px;
  /*border: 1px solid #ccc;*/
  /*border-top: none;*/
}

.tabcontent {
  animation: fadeEffect 1s; /* Fading effect takes 1 second */
}

/* Go from zero to full opacity */
@keyframes fadeEffect {
  from {opacity: 0;}
  to {opacity: 1;}
}


.conf-schedule td {
  border: solid 1px black;
  text-align: center;
}

.conf-schedule tr:nth-child(odd), .sc-bgcolor-odd {
  background-color: #D9E2F3;
}
.conf-schedule tr:nth-child(even), .sc-bgcolor-even {
  background-color: #6AA84F;
}

.text-em {
  font-style: italic;
}

.sc-bgcolor-1 {
  background-color: #B4C6E7;
}

.sc-color-1, .sc-color-1 h1 {
  color: #8D54A5;
}

.sc-color-2, .sc-color-2 h1 {
  color: #002060;
}

.sc-color-3, .sc-color-3 h1 {
  color: #333399;
}

.sc-header {
  padding-top: 0.5em;
  padding-bottom: 0.5em;
}

.conf-schedule h1{
  padding-top: .5em;
  padding-bottom: .5em;
}
.conf-schedule td {
  min-height: 2em;
  padding-top: .5em;
  padding-bottom: .5em;
}

.text-underline {
  text-decoration: underline;
}

.tabcontent{
  display: block;
}

</style>

<script>
  function openCity(evt, cityName) {
  // Declare all variables

  // Show the current tab, and add an "active" class to the button that opened the tab
  window.location.hash=cityName
}
</script>


<!-- Tab links -->
<div class="tab">
  <a href="{{ site.baseurl }}/schedule" class="btn btn-grey">Multi Page</a> <a href="{{ site.baseurl }}/technicalProgram" class="btn btn-grey">Technical Program</a>
</div>

<br><br>

<!-- Tab links -->
<div class="tab">
  <button class="tablinks" onclick="openCity(event, '20211021')">21-Oct-2021</button>
  <button class="tablinks" onclick="openCity(event, '20211022')">22-Oct-2021</button>
  <button class="tablinks" onclick="openCity(event, '20211023')">23-Oct-2021</button>
  <button class="tablinks" onclick="openCity(event, '20211024')">24-Oct-2021</button>
</div>

{% include sched_day1.html %}

{% include sched_day2.html %}

{% include sched_day3.html %}

{% include sched_day4.html %}


