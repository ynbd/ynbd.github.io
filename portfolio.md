---
layout: page
title: portfolio
permalink: /portfolio/
---
<div class="album text-muted">
    <div class="container">
        <div class="row">
        {% for project in site.portfolio %}
        <div class="card col-sm" style="width: 20rem;">
                    <img class="card-img-top" src="{{ site.baseurl }}/assets/{{ project.img }}" alt="">
                    <div class="card-body">
                        <h4 class="card-title">{{ project.title }}</h4>
                        <p class="card-text">{{ project.description }}</p>
                        <a href="{{ site.baseurl }}{{ project.url }}" class="btn btn-primary">More..</a>
                    </div>
            </div>
        {% endfor %}
        </div>
    </div>
</div>

<!-- {% for project in site.portfolio %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %} -->
