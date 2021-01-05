---
layout: default
title: People - Barnard Bears
active_tab: people
---

<div class="container-fluid">

  <div class="row">
  <h2>Mentors</h2>


  {% for person in site.data.people %}
    {% if person.mentor %}
      <div class="col-lg-4 col-md-6 col-xs-12" style="margin-top: 25px; margin-bottom: 05px;"> 
        <ul class="list-unstyled">
          <li>
            {% if person.pic %}
              <img src="assets/img/people/{{ person.pic }}" class="img-circle" style="height: 100%; width: 100%; height: 150px; width: 150px">
            {% endif %}
          </li>
          {% if person.url %}
            <li><b><a href="{{ person.url }}">{{ person.name }}</a></b></li>
          {% else %}
            <li><b>{{ person.name }}</b></li>
          {% endif %}
          {% if person.research-area %}<li><em><b>Research Area:</b> {{ person.research-area }}</em></li>{% endif %}

          <!--{% if person.research %}<li><p>{{ person.research }}</p></li>{% endif %} -->
        </ul>
      </div>
      {% endif %}
    {% endfor %}
  </div>



  <div class="row">
  <h2>Organizers</h2>

  {% for person in site.data.people %}
    {% if person.organizer %}
      <div class="col-lg-4 col-md-6 col-xs-12" style="margin-top: 25px; margin-bottom: 20px; height: 350px;">
        <ul class="list-unstyled">
          <li>
            {% if person.pic %}
              <img src="assets/img/people/{{ person.pic }}" class="img-circle" style="height: 100%; width: 100%; height: 150px; width: 150px">
            {% endif %}
          </li>
          {% if person.url %}
            <li><b><a href="{{ person.url }}">{{ person.name }}</a></b></li>
          {% else %}
            <li><b>{{ person.name }}</b></li>
          {% endif %}
          {% if person.research-area %}<li><em><b>Research Area:</b> {{ person.research-area }}</em></li>{% endif %}
        </ul>
      </div>



    {% endif %}

  {% endfor %}

  </div>  
</div>

