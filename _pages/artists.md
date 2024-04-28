---
layout: page
permalink: /testing/
title: Testing
description:
nav: true
nav_rank: 2
---

# Testing 3

{% assign members = site.members | sort: "title" %}

<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h5 class="card-title">{{ member.profile.name }}</h5>
                    {% if member.profile.position %}<h6 class="card-subtitle mb-2 text-muted">{{ member.profile.position }}</h6>{% endif %}
                    {% if member.profile.department %}<h6 class="card-subtitle mb-2 text-muted">{{ member.profile.department }}</h6>{% endif %}
                    {% if member.profile.organization %}<h6 class="card-subtitle mb-2 text-muted">{{ member.profile.organization }}</h6>{% endif %}
                    <p class="card-text">
                        {{ member.teaser }}
                    </p>
                    {% if member.inline == false %}</a>{% endif %}
                    {% if member.profile.website %}
                        <br><a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
                    {% endif %}
                    {% if member.profile.email %}
                        <a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a>
                    {% endif %}
                    {% if member.profile.phone %}
                        <a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a>
                    {% endif %}
                    {% if member.profile.orcid %}
                        <a href="https://orcid.org/{{ member.profile.orcid }}" class="card-link" target="_blank"><i class="fab fa-orcid"></i></a>
                    {% endif %}
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                    {% if member.profile.github %}
                        <a href="https://github.com/{{ member.profile.github }}" class="card-link" target="_blank"><i class="fab fa-github"></i></a>
                    {% endif %}
                    <p class="card-text">
                        <br><small class="test-muted"><i class="fas fa-thumbtack"></i> {{ member.profile.address | replace: '<br />', ', ' }}</small> 
                    </p>
                </div>
            </div>
        </div>
    </div>
</p>

	{% endfor %}
<br>
{% endfor %}


## Testing 2

{% assign members = site.members | sort: "title" %}

<div id="members-list" style="margin-top: 20px;">
    {% for member in members %}
        <div class="col-sm-4 col-md-3">
            <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
        </div>
        <div class="team col-sm-8 col-md-9">
            <div class="members {% if member.inline == false %}hoverable{% endif %}" style="margin-bottom: 20px;" data-domain="{{ member.domain }}" data-subdomain="{{ member.subdomain }}">
                <div class="row no-gutters">
                    <div class="team">
                        <div class="members-body">
                            {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                                <h5 class="members-title"><i class="{{ resource.icon | default: 'fas fa-file' }}"></i>&nbsp;&nbsp; {{ member.title }}</h5></a>
                            <p class="members-text"><small class="test-muted">
                                {% if member.profile.date %}<i class="fa-solid fa-calendar"></i>&nbsp; Date: {{ member.profile.date | replace: '<br />', ', ' }}{% endif %}
                                {% if member.profile.date and member.profile.author %}&nbsp;&nbsp;//&nbsp;&nbsp;{% endif %}
                                {% if member.profile.author %}<i class="fa-solid fa-user"></i>&nbsp; Author: {{ member.profile.author | replace: '<br />', ', ' }}{% endif %}
                            </small></p>
                            {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                            <p class="members-text">{{ member.teaser }}</p></a>
                            {% if member.profile.source or member.profile.license %}
                                <hr class="solid">
                            {% endif %}
                            <p class="members-text">
                                {% if member.profile.source %}<small class="test-muted"><i class="fas fa-link"></i> Source: <a href="{{ member.profile.source }}">{{ member.profile.source | replace: '<br />', ', ' }}</a></small>{% endif %}
                                {% if member.profile.source and member.profile.license %}<br>{% endif %}
                                {% if member.profile.license %}<small class="test-muted"><i class="fa-solid fa-quote-left"></i>&nbsp; License: {{ member.profile.license }}</small>{% endif %}
                            </p>
                            <hr class="solid">
                            <p class="members-text">
                                <small class="test-muted domain"><i class="fa-solid fa-square"></i>&nbsp; Domain: <a href="{{ site.url }}{{ site.baseurl }}{{ member.domain | downcase | replace: ' ', '-' }}">{{ member.domain }}</a> &nbsp;&nbsp;//&nbsp;&nbsp;</small>
                                <small class="test-muted subdomain"><i class="fa-solid fa-sitemap"></i>&nbsp; Subdomain: {{ member.subdomain }} &nbsp;&nbsp;//&nbsp;&nbsp;</small>
                                <small class="test-muted resource"><i class="fa-solid fa-file"></i>&nbsp; Type of Resource: {{ member.resource }}</small><br>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    {% endfor %}
</div>



## Testing 1

{% assign members = site.members | sort: "title" %}

<div id="members-list" style="margin-top: 20px;">
  {% for members in members %}
    {% assign resource = site.data.members.resources | where: "name", members.resource | first %}
    <div class="members {% if members.inline == false %}hoverable{% endif %}" style="margin-bottom: 20px;" data-domain="{{ members.domain }}" data-subdomain="{{ members.subdomain }}">
      <div class="row no-gutters">
        <div class="team">
          <div class="members-body">
            {% if members.inline == false %}<a href="{{ members.url | relative_url }}">{% endif %}
              <h5 class="members-title"><i class="{{ resource.icon | default: 'fas fa-file' }}"></i>&nbsp;&nbsp; {{ members.title }}</h5></a>
            <p class="members-text"><small class="test-muted">{% if members.profile.date %}<i class="fa-solid fa-calendar"></i>&nbsp; Date: {{ members.profile.date | replace: '<br />', ', ' }}{% endif %}
              {% if members.profile.date and members.profile.author %}&nbsp;&nbsp;//&nbsp;&nbsp;{% endif %}
              {% if members.profile.author %}<i class="fa-solid fa-user"></i>&nbsp; Author: {{ members.profile.author | replace: '<br />', ', ' }}{% endif %}</small></p>
            {% if members.inline == false %}<a href="{{ members.url | relative_url }}">{% endif %}
              <p class="members-text">{{ members.teaser }}</p></a>
            {% if members.profile.source or members.profile.license %}
              <hr class="solid">
            {% endif %}
            <p class="members-text">
              {% if members.profile.source %}<small class="test-muted"><i class="fas fa-link"></i> Source: <a href="{{ members.profile.source }}">{{ members.profile.source | replace: '<br />', ', ' }}</a></small>{% endif %}
              {% if members.profile.source and members.profile.license %}<br>{% endif %}
              {% if members.profile.license %}<small class="test-muted"><i class="fa-solid fa-quote-left"></i>&nbsp; License: {{ members.profile.license }}</small>{% endif %}
            </p>
              <hr class="solid">
            <p class="members-text">
              <small class="test-muted domain"><i class="fa-solid fa-square"></i>&nbsp; Domain: <a href="{{ site.url }}{{ site.baseurl }}{{ members.domain | downcase | replace: ' ', '-' }}">{{ members.domain }}</a> &nbsp;&nbsp;//&nbsp;&nbsp;</small>
              <small class="test-muted subdomain"><i class="fa-solid fa-sitemap"></i>&nbsp; Subdomain: {{ members.subdomain }} &nbsp;&nbsp;//&nbsp;&nbsp;</small>
              <small class="test-muted resource"><i class="fa-solid fa-file"></i>&nbsp; Type of Resource: {{ members.resource }}</small><br>
            </p>
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>
