---
layout:   table

date: 		"2018-09-07 18:00:00"
title: 		"Tournament 36"
subtitle: 	"Fri  7 Sep 18:00:00 UTC 2018 to Fri 14 Sep 17:59:59 UTC 2018"

excerpt:    "Guild Wars 2 (GW2), World vs. World (WvW) Realm Avenger achivement Tournament. \"Every Kill Counts\""

status:     "OPEN"
listing:    "Y"
loop_count: 4
type:       tournament

category:   tournaments

---
<div class="table_header">
  <span class="table_title">{{ site.data.2018-09-07-tournament-36-table.tournament.week_post_title }}</span><br>
  <span class="table_subtitle">{{ site.data.2018-09-07-tournament-36-table.tournament.week_post_subtitle }}</span>  
</div>

{% for i in (1..page.loop_count) %}
<span class="table_nextupdate">as at {{ site.data.2018-09-07-tournament-36-table.update_at }}, next update {{ site.data.2018-09-07-tournament-36-table.update_weekly_timestamp }} UTC</span> 
<table class="week_table">
  <colgroup>
    <col style="width:18px">
    <col style="width:55px">
    <col style="width:55px">
    <col style="width:14px">
    <col style="width:14px">
    <col style="width:14px">
    <col style="width:14px">
    <col style="width:14px">
    <col style="width:14px">
    <col style="width:14px">
    <col style="width:18px">
  </colgroup>
  <thead>
    <tr>
      <th>POS</th>
      <th class="AlignLeft">Name</th>
      <th class="AlignLeft">World</th>
      <th><div class="label"><a href="{{ site.data.2018-09-07-tournament-36-table.columns[0].url }}">{{ site.data.2018-09-07-tournament-36-table.columns[0].label }}</a><p class="onhover">{{ site.data.2018-09-07-tournament-36-table.columns[0].start }} to {{ site.data.2018-09-07-tournament-36-table.columns[0].stop }}</p></div>​</th>
      <th><div class="label"><a href="{{ site.data.2018-09-07-tournament-36-table.columns[1].url }}">{{ site.data.2018-09-07-tournament-36-table.columns[1].label }}</a><p class="onhover">{{ site.data.2018-09-07-tournament-36-table.columns[1].start }} to {{ site.data.2018-09-07-tournament-36-table.columns[1].stop }}</p></div>​</th>
      <th><div class="label"><a href="{{ site.data.2018-09-07-tournament-36-table.columns[2].url }}">{{ site.data.2018-09-07-tournament-36-table.columns[2].label }}</a><p class="onhover">{{ site.data.2018-09-07-tournament-36-table.columns[2].start }} to {{ site.data.2018-09-07-tournament-36-table.columns[2].stop }}</p></div>​</th>
      <th><div class="label"><a href="{{ site.data.2018-09-07-tournament-36-table.columns[3].url }}">{{ site.data.2018-09-07-tournament-36-table.columns[3].label }}</a><p class="onhover">{{ site.data.2018-09-07-tournament-36-table.columns[3].start }} to {{ site.data.2018-09-07-tournament-36-table.columns[3].stop }}</p></div>​</th>
      <th><div class="label"><a href="{{ site.data.2018-09-07-tournament-36-table.columns[4].url }}">{{ site.data.2018-09-07-tournament-36-table.columns[4].label }}</a><p class="onhover">{{ site.data.2018-09-07-tournament-36-table.columns[4].start }} to {{ site.data.2018-09-07-tournament-36-table.columns[4].stop }}</p></div>​</th>
      <th><div class="label"><a href="{{ site.data.2018-09-07-tournament-36-table.columns[5].url }}">{{ site.data.2018-09-07-tournament-36-table.columns[5].label }}</a><p class="onhover">{{ site.data.2018-09-07-tournament-36-table.columns[5].start }} to {{ site.data.2018-09-07-tournament-36-table.columns[5].stop }}</p></div>​</th>
      <th><div class="label"><a href="{{ site.data.2018-09-07-tournament-36-table.columns[6].url }}">{{ site.data.2018-09-07-tournament-36-table.columns[6].label }}</a><p class="onhover">{{ site.data.2018-09-07-tournament-36-table.columns[6].start }} to {{ site.data.2018-09-07-tournament-36-table.columns[6].stop }}</p></div>​</th>
      <th>Total</th>
    </tr>
  </thead>
  {% assign offset = forloop.index0 | times: 20 %}
  <tbody>
    {% for entry in site.data.2018-09-07-tournament-36-table.entries limit:20 offset:offset %}
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
    {% for entry in site.data.2018-09-07-tournament-36-table.commentary %}
    <li class="commentary_list">{{ entry.comment | escape }}</li>
    {% endfor %}
  </ul>
</div>





