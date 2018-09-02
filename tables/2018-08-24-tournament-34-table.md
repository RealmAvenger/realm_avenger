---
layout:   table

date: 		"2018-08-24 18:00:00"
title: 		"Tournament 34"
subtitle: 	"Fri 24 Aug 2018 18:00:00 UTC to Fri 31 Aug 2018 17:59:59 UTC"

status:     "status"
listing:    "listing"
loop_count: 4
type:       tournament

category:   tournaments

---
<div class="table_header">
  <span class="table_title">{{ site.data.2018-08-24-tournament-34-table.tournament.week_post_title }}</span><br>
  <span class="table_subtitle">{{ site.data.2018-08-24-tournament-34-table.tournament.week_post_subtitle }}</span>  
</div>

{% for i in (1..page.loop_count) %}
<br>
<table class="week_table">
  <thead>
    <tr>
      <th>POS</th>
      <th class="AlignLeft">Name</th>
      <th class="AlignLeft">World</th>
      <th><a class="hideDisplay">{{ site.data.2018-08-24-tournament-34-table.columns[0].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-24-tournament-34-table.columns[0].start }} to {{ site.data.2018-08-24-tournament-34-table.columns[0].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-24-tournament-34-table.columns[1].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-24-tournament-34-table.columns[1].start }} to {{ site.data.2018-08-24-tournament-34-table.columns[1].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-24-tournament-34-table.columns[2].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-24-tournament-34-table.columns[2].start }} to {{ site.data.2018-08-24-tournament-34-table.columns[2].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-24-tournament-34-table.columns[3].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-24-tournament-34-table.columns[3].start }} to {{ site.data.2018-08-24-tournament-34-table.columns[3].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-24-tournament-34-table.columns[4].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-24-tournament-34-table.columns[4].start }} to {{ site.data.2018-08-24-tournament-34-table.columns[4].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-24-tournament-34-table.columns[5].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-24-tournament-34-table.columns[5].start }} to {{ site.data.2018-08-24-tournament-34-table.columns[5].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-24-tournament-34-table.columns[6].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-24-tournament-34-table.columns[6].start }} to {{ site.data.2018-08-24-tournament-34-table.columns[6].stop }}</span></a></th>
      <th>Total</th>
    </tr>
  </thead>
  {% assign offset = forloop.index0 | times: 20 %}
  <tbody>
    {% for entry in site.data.2018-08-24-tournament-34-table.entries limit:20 offset:offset %}
      <tr>
        <td class="pl{{ entry.pos }}">{{ entry.pos }}</td>
        <td class="AlignLeft">{{ entry.name }}</td>
        <td class="AlignLeft">{{ entry.world }}</td>
        <td class="pl{{ entry.1p }}">{{ entry.1c }}<sup>{{ entry.1p }}</sup></td>
        <td class="pl{{ entry.2p }}">{{ entry.2c }}<sup>{{ entry.2p }}</sup></td>
        <td class="pl{{ entry.3p }}">{{ entry.3c }}<sup>{{ entry.3p }}</sup></td>
        <td class="pl{{ entry.4p }}">{{ entry.4c }}<sup>{{ entry.4p }}</sup></td>
        <td class="pl{{ entry.5p }}">{{ entry.5c }}<sup>{{ entry.5p }}</sup></td>
        <td class="pl{{ entry.6p }}">{{ entry.6c }}<sup>{{ entry.6p }}</sup></td>
        <td class="pl{{ entry.7p }}">{{ entry.7c }}<sup>{{ entry.7p }}</sup></td>
        <td>{{ entry.total }}</td>
      </tr>
    {% endfor %}  
  </tbody>
</table>
<div class="leaderboard"></div>
{% endfor %}

<div class="commentary">
  <span class="commentary_title">Commentary</span>
  <ul>
    {% for entry in site.data.2018-08-24-tournament-34-table.commentary %}
    <li class="commentary_list">{{ entry.comment | escape }}</li>
    {% endfor %}
  </ul>
</div>
