---
title: "Tongji Flying Fish Research Lab - Team"
layout: gridlay
excerpt: "Team members"
sitemap: false
permalink: /team/
---

<style>

.button {
    background-color: #4CAF50; /* Green */
    border: none;
    color: white;
    padding: 10px 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 12px;
    margin: 4px 2px;
    -webkit-transition-duration: 0.4s; /* Safari */
    transition-duration: 0.4s;
    cursor: pointer;
}

.black {
    background-color: white;
    color: black;
    border: 2px solid #555555;
}

</style>

## Faculty
{% for member in site.data.team_members %}
{% if member.info contains "Professor" %}
<div class="row">
<div class="col-sm-12 clearfix">
  {% if member.photo contains 'http://' or member.photo contains 'https://' %}
  <img src="{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  {% else %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  {% endif %}
  
  <div style='margin-left:20%;'>
  <h4>{{ member.name }}</h4>
  <p><i>{{ member.info }}</i></p>
  
  {% if member.short_bio %}
  <p style="font-size:.8em">{{ member.short_bio }}</p>
  {% endif %}

  {% if member.topic %}
  <p style="font-size:.8em; margin-bottom: 5px;"><i class="fa fa-book" style="width: 15px; text-align: center;"></i> <strong>Research interests:</strong> {{ member.topic }}</p>
  {% endif %}

  {% include member_links.html member=member %}

  {% if member.education %}
{% for edu in member.education %}
<p style="font-size:.8em; margin-bottom: 5px;">{% if forloop.first %}<i class="fa fa-graduation-cap" style="width: 15px; text-align: center;"></i> {% else %}<span style="display:inline-block; width: 15px;"></span> {% endif %}{{ edu }}</p>
{% endfor %}
  {% endif %}
  </div>

  <p style="clear:both;"></p>
</div>
</div>
{% endif %}
{% endfor %}

## Ph.D. Students
{% for member in site.data.team_members %}
{% if member.info contains "Ph.D." %}
<div class="row">
<div class="col-sm-12 clearfix">
  {% if member.photo contains 'http://' or member.photo contains 'https://' %}
  <img src="{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  {% else %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  {% endif %}
  
  <div style='margin-left:20%;'>
  <h4>{{ member.name }}</h4>
  <p><i>{{ member.info }}</i></p>
  
  {% if member.short_bio %}
  <p style="font-size:.8em">{{ member.short_bio }}</p>
  {% endif %}

  {% if member.topic %}
  <p style="font-size:.8em; margin-bottom: 5px;"><i class="fa fa-book" style="width: 15px; text-align: center;"></i> <strong>Research interests:</strong> {{ member.topic }}</p>
  {% endif %}

  {% include member_links.html member=member %}

  {% if member.education %}
{% for edu in member.education %}
<p style="font-size:.8em; margin-bottom: 5px;">{% if forloop.first %}<i class="fa fa-graduation-cap" style="width: 15px; text-align: center;"></i> {% else %}<span style="display:inline-block; width: 15px;"></span> {% endif %}{{ edu }}</p>
{% endfor %}
  {% endif %}
  </div>

  <p style="clear:both;"></p>
</div>
</div>
{% endif %}
{% endfor %}

## Master's Students
{% for member in site.data.team_members %}
{% if member.info contains "M.Eng." or member.info contains "Master" %}
<div class="row">
<div class="col-sm-12 clearfix">
  {% if member.photo contains 'http://' or member.photo contains 'https://' %}
  <img src="{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  {% else %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  {% endif %}
  
  <div style='margin-left:20%;'>
  <h4>{{ member.name }}</h4>
  <p><i>{{ member.info }}</i></p>
  
  {% if member.short_bio %}
  <p style="font-size:.8em">{{ member.short_bio }}</p>
  {% endif %}

  {% if member.topic %}
  <p style="font-size:.8em; margin-bottom: 5px;"><i class="fa fa-book" style="width: 15px; text-align: center;"></i> <strong>Research interests:</strong> {{ member.topic }}</p>
  {% endif %}

  {% include member_links.html member=member %}

  {% if member.education %}
{% for edu in member.education %}
<p style="font-size:.8em; margin-bottom: 5px;">{% if forloop.first %}<i class="fa fa-graduation-cap" style="width: 15px; text-align: center;"></i> {% else %}<span style="display:inline-block; width: 15px;"></span> {% endif %}{{ edu }}</p>
{% endfor %}
  {% endif %}
  </div>

  <p style="clear:both;"></p>
</div>
</div>
{% endif %}
{% endfor %}


We welcome applications from prospective Ph.D. and master's students, and inquiries about postdoctoral research opportunities. [Learn more.]({{ site.url }}{{ site.baseurl }}/openings)
