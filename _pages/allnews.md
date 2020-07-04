---
title: "News"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /allnews.html
---

# News
<div class="col-sm-10 clearfix">
{% for article in site.data.news %}
<pubtit>{{ article.date }}</pubtit>
<p>
<em>{{ article.headline }}</em><br>
{{ article.description}}</p>
{{ publi.images }}
<br />
</div>
{% endfor %}
