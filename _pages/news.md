---
title: "Categories"
layout: default
permalink: "/issues"
---

<div class="container">
    <div class="row justify-content-center">
        <div class="col-md-8">

            {% for category in site.categories %}

            {% assign pages_list = category[1] %}

<div class="mb-5 d-flex ">
<div class="pr-3">
	<h2 class="mb-1 h4 font-weight-bold">
 
	</h2>
<h4 class="font-weight-bold spanborder text-capitalize" id="{{ category[0] | downcase }}"><span>{{
                    category[0] }}</span></h4>

    <small class="text-muted">
    	{{ post.author}}
    </small>

</div>
{% if post.image %}
	<div class="col-md-3 pr-0 text-right">
	<a href="{{site.baseurl}}{{post.url}}">
	<img class="w-100" src="{% if post.image contains "://" %}{{ post.image }}{% else %}{{ site.baseurl }}/{{ post.image }}{% endif %}" alt="{{ post.title }}">
	</a>
	</div>
{% endif %}
</div>

            {% assign pages_list = nil %}
            {% assign group = nil %}

            {% endfor %}

        </div>

        <div class="col-md-4">
            {% include sidebar-featured.html %}
        </div>

    </div>

</div>
