---
layout: page-fullwidth
title: "Programme"
permalink: "/programme/"
---

<p>The 2017 programme will appear!</p>



<h2>Here is the programme from 2016</h2>


{% assign schedule = site.schedule | sort: 'date' %}

<div class="row">
  <div class="large-6 columns">
      <h3>Monday 25th: workshops</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Monday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>

  <div class="large-6 columns">
      <h3>Tuesday 26th: workshops</h3>
      <p>No conference events taking place today. Events have been postponed due
      to student action at the University.</p>
  </div>
</div>

<div class="row">
  <div class="large-6 columns">
      <h3>Wednesday 27th: talks</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Wednesday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>

  <div class="large-6 columns">
      <h3>Thursday 28th: talks</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Thursday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
</div>

<div class="row">
  <div class="large-6 columns">
      <h3>Friday 29th: workshops</h3>
      <ul>
          {% for post in schedule %}
            {% if post.day == "Friday" %}
              <li>
                {% if {{post.date}} %}{{post.date | date: "%H:%M"}}: {% endif %}
                {% if {{post.speaker}} %}{{post.speaker}}: {% endif %} <a href="{{ post.url}}"><em>{{post.title}}</em></a>
                {% if {{post.location}} %} ({{post.location}}){% endif %}
              </li>
            {% endif %}
          {% endfor %}
      </ul>
  </div>
</div>


{% assign days = "Monday,Tuesday,Wednesday,Thursday,Friday" | split: "," %}
