---
title: Cabin Architecture
permalink: cabin-architecture.html
layout: about
---
{% assign cabins = site.data[site.metadata] | map: "cabintype" | compact | uniq %}


# Cabin Architecture

*All cabins featured in Keeping Watch fall within one of these designs. Most cabins fall into one of three categories: D-Series, L-series, R-Series, and Aerometer Steel towers. 

{% for cabin in site.data.cabins %}

## {{cabin.title}} 

{% capture cabinimage%}{{cabin.img}}{% endcapture %}
{% include feature/image.html objectid=cabinimage %}

{{cabin.description}} 

{% if cabins contains cabin.title %}
#### Firetowers featuring this architecture

{% for item in site.data[site.metadata] %}{% if item.cabintype == cabin.title %}
- [{{item.title}}]({{ item.objectid | prepend: '/items/' | append: '.html' | relative_url }}){% endif %}{% endfor %}

{% endif %}
 
{% endfor %}




