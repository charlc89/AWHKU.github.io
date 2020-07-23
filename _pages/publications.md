---
title: "Alan Wong Lab @ HKUMed - Publications"
layout: gridlay
excerpt: "Alan Wong Lab @ HKUMed -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Selected articles

(For a full list see [below](#full-list))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-10 clearfix">
 <div class="well-lg">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/misc/{{ publi.image }}" class="img-responsive" height="15%" style="float: left" HSPACE="5" VSPACE="10" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>&nbsp;<em> {{ publi.year }} </em><br />
  <p>{{ publi.news1 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List

{% for publi in site.data.publist %}

  <pubtit>{{ publi.title }}</pubtit>
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br><em> {{ publi.year }} </em><br />
  <p>{{ publi.news1 }}</p><br />
{% endfor %}
