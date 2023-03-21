---
layout: about
title: about
permalink: /
description: Robotics & Computer Vision enthusiast

profile:
  align: right
  image: img_profile.jpeg

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

Research Intern @MOONlab, IISER Bhopal  <br>
Third year Computer Engineering undergrad from VJTI, Mumbai (2024). 

My Research Interests are:
* Robotics & Automation
* Computer Vision
* SLAM
* Control Systems

You can reach me out on Matrix [@kunalagarwal18:matrix.org](https://matrix.to/#/kunalagarwal18:matrix.org) or email me at [kunalagarwal1072002@gmail.com](mailto:kunalagarwal1072002@gmail.com)

# Experience

{% for experience in site.data.experience %}
<div>
    {% if experience.title %}
    <h4 class="title font-weight-bold">{{experience.title}}</h4>
    {% endif %}
    {% if experience.role %}
    <h6 class="title font-weight-bold">{{experience.role}}</h6>
    {% endif %}
    {% if experience.year %}
    <span class="badge bg-dark font-weight-bold">
        {{ experience.year }}
    </span>
    {% endif %}
    <hr>
    {% if experience.description %}
        <ul class="items">
            {% for item in experience.description %}
                <li>
                    {% if item.contents %}
                        <span class="item-title">{{ item.title }}</span>
                        <ul class="subitems">
                        {% for subitem in item.contents %}
                            <li><span class="subitem">{{ subitem }}</span></li>
                        {% endfor %}
                        </ul>
                    {% else %}
                        <span class="item">{{ item }}</span>
                    {% endif %}
                </li>
            {% endfor %}
        </ul>
    {% endif %}
    {% if content.items %}
        <ul class="items">
            {% for item in content.items %}
                <li>
                    {% if item.contents %}
                        <span class="item-title">{{ item.title }}</span>
                        <ul class="subitems">
                        {% for subitem in item.contents %}
                            <li><span class="subitem">{{ subitem }}</span></li>
                        {% endfor %}
                        </ul>
                    {% else %}
                        <span class="item">{{ item }}</span>
                    {% endif %}
                </li>
            {% endfor %}
        </ul>
    {% endif %}
</div>
{% endfor %}