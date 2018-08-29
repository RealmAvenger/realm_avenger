---
layout:   table

date: 		"2018-08-29 00:00:00"
title: 		"Wednesday 29 August 2018, 16:30 to 20:30 UTC"
subtitle: 	"Tournament 34 Day 6"

status:     "OPEN"
listing:    "Y"
loop_count: 2
type:       hour

category:   tournaments

---
<div class="table_header">
  <span class="table_title">{{ site.data.2018-08-29-four-hour-table.full_date }}, {{ site.data.2018-08-29-four-hour-table.window_start }} to {{ site.data.2018-08-29-four-hour-table.window_stop }} UTC</span><br>
  <span class="table_subtitle"><a href="">Tournament {{ site.data.2018-08-29-four-hour-table.tournament.week }}</a>, <a href="">Day {{ site.data.2018-08-29-four-hour-table.tournament.day_number }}</a></span>  
</div>

{% for i in (1..page.loop_count) %}
<span class="table_nextupdate">as at {{ site.data.2018-08-29-four-hour-table.update_at }}, next update {{ site.data.2018-08-29-four-hour-table.update_timestamp }} UTC</span> 
<table class="hour_table">
  <thead>
    <tr>
      <th>POS</th>
      <th class="AlignLeft">Name</th>
      <th class="AlignLeft">World</th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[0].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[0].start }} to {{ site.data.2018-08-29-four-hour-table.columns[0].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[1].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[1].start }} to {{ site.data.2018-08-29-four-hour-table.columns[1].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[2].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[2].start }} to {{ site.data.2018-08-29-four-hour-table.columns[2].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[3].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[3].start }} to {{ site.data.2018-08-29-four-hour-table.columns[3].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[4].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[4].start }} to {{ site.data.2018-08-29-four-hour-table.columns[4].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[5].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[5].start }} to {{ site.data.2018-08-29-four-hour-table.columns[5].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[6].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[6].start }} to {{ site.data.2018-08-29-four-hour-table.columns[6].stop }}</span></a></th>
      <th><a class="hideDisplay">{{ site.data.2018-08-29-four-hour-table.columns[7].label }}<span class="showDisplayOnHover">{{ site.data.2018-08-29-four-hour-table.columns[7].start }} to {{ site.data.2018-08-29-four-hour-table.columns[7].stop }}</span></a></th>
      <th>Total</th>
    </tr>
  </thead>
  {% assign offset = forloop.index0 | times: 20 %}
  <tbody>
    {% for entry in site.data.2018-08-29-four-hour-table.entries limit:20 offset:offset %}
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
        <td class="pl{{ entry.8p }}">{{ entry.8c }}<sup>{{ entry.8p }}</sup></td>
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
    {% for entry in site.data.2018-08-29-four-hour-table.commentary %}
    <li class="commentary_list">{{ entry.comment | escape }}</li>
    {% endfor %}
  </ul>
</div>







