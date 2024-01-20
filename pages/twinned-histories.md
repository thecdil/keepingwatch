---
title: Twinned Histories
permalink: twinned-histories.html
layout: page-full-width
---

{:.display-4 .text-center .my-5}
## Twinned Histories

<div class="px-md-5">
<table class="table table-hover table-borderless ">
  <thead>
    <tr class="text-center h2 sticky-top" style="background-color:white;z-index:101;">
      <th scope="col">Firetower</th>
      <th scope="col"></th>
      <th scope="col">Wilderness</th>
    </tr>
  </thead>
  <tbody>
{% for item in site.data.twinned-histories %}
    <tr >
        <td class="h4 py-5">{{item.firetower}}</td>
        <td class="align-middle h2 text-center">{{item.date}}</td>
        <td class="h4 py-5 text-right">{{item.wilderness}}</td>
    </tr>
{% endfor %}
</tbody>
</table>
</div>
