---
title: "Alan Wong Lab @ HKUMed - Team"
layout: gridlay
excerpt: "Alan Wong Lab @ HKUMed -- Team members"
sitemap: false
permalink: /team/
---

<div class="container-text">
<img class="container-text__image"  src="/images/people/drwong.png" width="14%" VSPACE="50"/>
<div class="container-text__text">
<h3>Alan Wong</h3>
<p>
Dr. Alan Siu-lun Wong is an Assistant Professor of the School of Biomedical Sciences at the University of Hong Kong (HKU). <br>
Before he joined HKU, he obtained his B.Sc. and M.Phil. degrees in Biochemistry and Molecular Biotechnology from the Chinese University of Hong Kong in 2005 and 2007 respectively, and completed his Ph.D. in Biochemistry at the Hong Kong University of Science and Technology in 2011. He joined the Synthetic Biology Group at Massachusetts Institute of Technology from 2012-2016 for postdoctoral training. Dr. Wong was awarded with the Croucher Foundation Studentship (2008), the Butterfield-Croucher Award (2008), the Croucher Foundation Fellowship (2012), and the Hong Kong Institution of Science Young Scientist Award in life science (2011). 
</p>
</div>
___

</div>
<div class="col-sm-10 clearfix">
## Group Members
Jump to [staff](#staff), [students](#master-and-bachelor-students) and [alumni members](#alumni).

## Members
</div>
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-10 clearfix">
<div class="well-sm">  
{% if member.photo == null or  member.photo == "" %}
<br>
{% else %}
<img src="/images/people/{{ member.photo }}" class="img-responsive" width="15%" style="float: left;padding-right:12px" />
{% endif %}
<div class="textbox">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br> 
    {{ member.year }}<br> {{ member.email }} </i>
  <ul style="overflow: hidden">


  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
</div>  
</div>
</div>
{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<div class="col-sm-10 clearfix">
___  

## Students
  
</div>
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-10 clearfix">
<div class="well-sm"> 
{% if member.photo == null or  member.photo == "" %}
<br>
{% else %}
<img src="/images/people/{{ member.photo }}" class="img-responsive" width="15%" style="float: left;padding-right:12px" />
{% endif %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br> 
    {{ member.year }}<br> {{ member.email }} </i>
  <ul style="overflow: hidden">
 
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  </ul>

</div>
</div>
{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




<div class="col-sm-10 clearfix">
## Alumni
</div>
<div class="row">
<div class="col-sm-10 clearfix">
  
{% for member in site.data.alumni_members %}
<div class="well-sm"> 
<p>
{{ member.name }}&nbsp; -- &nbsp;{{ member.info }}&nbsp;({{ member.duration }})
<br>
</p>
</div>
{% endfor %}

</div>
</div>
