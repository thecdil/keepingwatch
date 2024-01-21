---
title: Excerpts
permalink: excerpts.html
layout: page-narrow
---
<style>p{font-size:1.1em}</style>

{:.mb-5 .display-4}
# Excerpts

{% for e in site.data.excerpts %}

{% if e.quote %}

{:.mt-5}
{{e.quote}}


{:.text-end .my-5 .small}
{% if e.person %}{{ e.person }}{% endif %}{% if e.affiliation %}, {{ e.affiliation }}{% endif %}<br>**{{e.date}}**{% if e.object_location %}<br><br><img src="{{e.object_location | relative_url }}" style="max-height:240px;"/>{% endif %}




{% else %}
{% include feature/video.html objectid=e.object_location %}
{% endif %}
<hr class="w-75 mx-auto text-center my-3">
{% endfor%}
