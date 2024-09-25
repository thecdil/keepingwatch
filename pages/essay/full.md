---
title: Fire Lookouts and the Act of Remaining
permalink: essay/
layout: scrollabout
---
# Fire Lookouts and the Act of Remaining

{:.text-end}
### By Michael Decker


{% for s in site.data.essay-sections %}
<div class="row step" id="{{s.step}}">
{%- assign sec = s.section | append: ".md" | prepend: "essay/" -%}
{% capture section %}{% include {{sec}} %}{% endcapture %}
{{ section | markdownify }}
</div>
{% endfor %}
