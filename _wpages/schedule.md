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
  display: none;
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

.conf-schedule a::after {
  content: '\1F517';
}
</style>

<script>
  function openCity(evt, cityName) {
  // Declare all variables
  var i, tabcontent, tablinks;

  // Get all elements with class="tabcontent" and hide them
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }

  // Get all elements with class="tablinks" and remove the class "active"
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }

  // Show the current tab, and add an "active" class to the button that opened the tab
  document.getElementById(cityName).style.display = "block";
  evt.currentTarget.className += " active";
}
</script>

<!-- Tab links -->
<div class="tab">
  <a href="{{ site.baseurl }}/schedule-1page" class="btn btn-grey">Single Page</a> <a href="{{ site.baseurl }}/technicalProgram" class="btn btn-grey">Technical Program</a>
</div>

<br><br>

<!-- Tab links -->
<div class="tab">
  <button class="tablinks" onclick="openCity(event, '20211021')" id="defaultOpen">21-Oct-2021</button>
  <button class="tablinks" onclick="openCity(event, '20211022')">22-Oct-2021</button>
  <button class="tablinks" onclick="openCity(event, '20211023')">23-Oct-2021</button>
  <button class="tablinks" onclick="openCity(event, '20211024')">24-Oct-2021</button>
</div>

{% include sched_day1.html %}

{% include sched_day2.html %}

{% include sched_day3.html %}

{% include sched_day4.html %}


<script>
// Get the element with id="defaultOpen" and click on it
document.getElementById("defaultOpen").click();
</script>
