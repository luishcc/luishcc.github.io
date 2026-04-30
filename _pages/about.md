---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About

{% for member in site.data.pi %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h5><i>{{ member.info }}</i></h5>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-2x"></i></a> {% endif %}
  {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-2x"></i></a> {% endif %}
  {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-2x"></i></a> {% endif %}
    {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-2x"></i></a> {% endif %}

  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}

{% if site.data.grants %}

<div class="jumbotron">
  <h4>Grants</h4>
  <ul>
    {% for grant in site.data.grants %}
      <li>{{ grant.name }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

<div class="jumbotron">
  <h4>Research experience</h4>
  <ul>
    <li> 2026 (on-going), Kyushu University &ndash; MSCA funded secondments through ThermEnTrans research network </li>
    <li> 2023, Fedral University of Rio de Janeiro (UFRJ) &ndash; MSCA funded secondments through ThermaSMART research network for 2 months </li>
    <li> 2022, University College Dublin (UCD) &ndash; MSCA funded secondments through ThermaSMART research network for 5 months </li>
    <li> 2018, Rio de Janeiro State University (UERJ) &ndash; FAPERJ funded undergraduate research for 1 year </li>
  </ul>
</div>

{% if site.data.awards %}

<div class="jumbotron">
  <h4>Awards</h4>
  <ul>
    {% for award in site.data.awards %}
      <li>{{ award.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.people %}

<div class="jumbotron">
  <h4>Students and Mentoring</h4>
  <ul>
    {% for student in site.data.people %}
      <li>{{ student.name }}, {{ student.location }} ({{ student.degree }}, {{ student.year }})</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

<div class="jumbotron">
  <h4>Acknowledgements</h4>
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for funder in site.data.funders %}<a href="{{ funder.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}' style='max-height: 80px; margin: 2%'/></a>{% endfor %}
  </div>
</div>
