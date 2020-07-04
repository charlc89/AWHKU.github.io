---
title: "News"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<div class="col-sm-10 clearfix">
<pubtit>{{ article.date }}</pubtit>
<p>
<em>{{ article.headline }}</em><br>
{{ article.description}}</p>
{{ article.images }}
<br />
</div>
{% endfor %}
