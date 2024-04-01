---
title: "January 2024 Issue: Gun Violence"
layout: default
image: assets/images/gunissue.png
permalink: "/current"
author: Chanah Yin, Melody Yu
---

<div class="container">
<div class="jumbotron jumbotron-fluid mb-3 pl-0 pt-0 pb-0 bg-white position-relative">
		<div class="h-100 tofront">
			<div class="row {% if page.image %} justify-content-between {% else %} justify-content-center {% endif %}">
				<div class="{% if page.image %} col-md-6 {% else %} col-md-8 {% endif %} pr-0 pr-md-4 pt-4 pb-4 align-self-center">
					<p class="text-uppercase font-weight-bold">
      		</p>
					<h2 class="display-4 mb-4 article-headline">{{ page.title }}</h2>
										<div class="d-flex align-items-center">
											<span class="text-muted d-block mt-1">Edited by {{ page.author }} </span>
										</div>
				</div>
                {% if page.image %}
				<div class="col-md-6 pr-0 align-self-center">
					<img class="rounded" src="{% if page.image contains "://" %}{{ page.image }}{% else %}{{ site.baseurl }}/{{ page.image }}{% endif %}" alt="{{ page.title }}">
				</div>
                {% endif %}
			</div>
		</div>
	</div>
</div>

<div class="container">
    <div class="row justify-content-center">
        {% assign pages_list = site.categories["Gun Violence"] %}
        {% for post in pages_list %}
        {% if post.title != null %}
          {% if group == null or group == post.group %}
            {% include main-loop-card.html %}
          {% endif %}
        {% endif %}
        {% endfor %}
        {% assign pages_list = nil %}
        {% assign group = nil %}
    </div>
</div>
