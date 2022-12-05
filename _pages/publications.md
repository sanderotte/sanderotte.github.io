---
title: "OtteLab | Publications"
layout: gridlay
excerpt: "OtteLab | Publications"
sitemap: false
permalink: /publications/
---


## Publications
<br />
Skip to list of [all peer-reviewed publications](#allpubs). Below, you can also find our [popular scientific](#popsci) papers and [PhD theses](#theses).
<br />
<br />
 
### Highlights

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
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
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

<p id="allpubs"></p>

<!--
### Patents

-->


### All Publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <i>{{ publi.authors }}</i> <br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br />
  {{ publi.notes }}

{% endfor %}
<br />

#### Older Publications

{% for publi in site.data.oldpubs %}

  {{ publi.title }} <br />
  <i>{{ publi.authors }}</i> <br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br />
  {{ publi.notes }}

{% endfor %}
<br />

<p id="popsci"></p>

#### Popular Scientific

{% for publi in site.data.popsci %}

  {{ publi.title }} {{ publi.notes }} <br />
  <i>{{ publi.authors }}</i> <br />
  <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
<br />

<p id="theses"></p>

#### PhD Theses

{% for publi in site.data.phdtheses %}

<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive"  style="width: 100%; max-width: 160px" />
  {{ publi.title }} <br />
  <i>{{ publi.authors }}</i> <br />
  <a href="{{ publi.link.url }}">{{ publi.link.display }}</a> <br /><br />

{% endfor %}
<br />
