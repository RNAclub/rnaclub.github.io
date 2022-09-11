---
title: "Guangzhou RNA club - Home"
layout: homelay
excerpt: "Guangzhou RNA club at Bioland"
sitemap: false
permalink: /
---


<h4 class="small-title-b text-center mb-3">
	We are a group of scientists interested in all things RNA. We promote new research from within the South China area and beyond, for the advancement of RNA science and training. Guangzhou RNA club (Seminars+Symposiums), aiming to associate the RNA research society in South China with the global RNA SOCIETY. We are located at the International Bioland, Guangzhou.

	We are research groups at the [Guangzhou International Bioland](https://www.grmh-gdl.cn).
</h4>


{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p>{{ publi.authors }}</p>
  <p><em><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></em></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
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


## Funding

> We are grateful for funding from Guangzhou Laboratory ([Gzlab](www.gzlab.ac.cn)), [MOST]() and [NSFC]() .

<figure class="fourth">
  <img src="{{ site.url }}{{ site.baseurl }}/images/RNA-Puzzles_logo.jpg" style="width: 210px">
  <img src="{{ site.url }}{{ site.baseurl }}/images/homepic/NSFC_logo.png" style="width: 210px">
</figure>
