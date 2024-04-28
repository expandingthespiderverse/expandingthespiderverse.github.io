---
layout: page
permalink: /testing/
title: Testing
description:
nav: true
nav_rank: 2
---

## Testing 4

<div style="background-color: #f2f2f2; padding: 10px;">
  <div id="filter-options" style="font-size: 0.8em;">
    
    <label for="resource-filter">Type of Resource:</label>
    <select id="resource-filter">
      <option value="all">All</option>
      {% for resource in site.data.cards.resources %}
      <option value="{{ resource }}">{{ resource }}</option>
      {% endfor %}
    </select>

    <br>

    <label for="domain-filter">Primary Domain:</label>
    <select id="domain-filter">
      <option value="all">All</option>
      {% for domain in site.data.cards.domains %}
      <option value="{{ domain }}">{{ domain }}</option>
      {% endfor %}
    </select>

    <br>

    <label for="subdomain-filter">Subdomain:</label>
    <select id="subdomain-filter">
      <option value="all">All</option>
      {% for subdomain in site.data.cards.subdomains %}
      <option value="{{ subdomain }}">{{ subdomain }}</option>
      {% endfor %}
    </select>

  </div>
</div>

{% assign cards = site.cards | sort: "title" %}

<div id="card-list" style="margin-top: 20px;">
  {% for card in cards %}
    {% assign resource = site.data.cards.resources | where: "name", card.resource | first %}
    <div class="card {% if card.inline == false %}hoverable{% endif %}" style="margin-bottom: 20px;" data-domain="{{ card.domain }}" data-subdomain="{{ card.subdomain }}">
      <div class="row no-gutters">
        <div class="team">
          <div class="card-body">
            {% if card.inline == false %}<a href="{{ card.url | relative_url }}">{% endif %}
              <h5 class="card-title"><i class="{{ resource.icon | default: 'fas fa-file' }}"></i>&nbsp;&nbsp; {{ card.title }}</h5></a>
            <p class="card-text"><small class="test-muted">{% if card.profile.date %}<i class="fa-solid fa-calendar"></i>&nbsp; Date: {{ card.profile.date | replace: '<br />', ', ' }}{% endif %}
              {% if card.profile.date and card.profile.author %}&nbsp;&nbsp;//&nbsp;&nbsp;{% endif %}
              {% if card.profile.author %}<i class="fa-solid fa-user"></i>&nbsp; Author: {{ card.profile.author | replace: '<br />', ', ' }}{% endif %}</small></p>
            {% if card.inline == false %}<a href="{{ card.url | relative_url }}">{% endif %}
              <p class="card-text">{{ card.teaser }}</p></a>
            {% if card.profile.source or card.profile.license %}
              <hr class="solid">
            {% endif %}
            <p class="card-text">
              {% if card.profile.source %}<small class="test-muted"><i class="fas fa-link"></i> Source: <a href="{{ card.profile.source }}">{{ card.profile.source | replace: '<br />', ', ' }}</a></small>{% endif %}
              {% if card.profile.source and card.profile.license %}<br>{% endif %}
              {% if card.profile.license %}<small class="test-muted"><i class="fa-solid fa-quote-left"></i>&nbsp; License: {{ card.profile.license }}</small>{% endif %}
            </p>
              <hr class="solid">
            <p class="card-text">
              <small class="test-muted domain"><i class="fa-solid fa-square"></i>&nbsp; Domain: <a href="{{ site.url }}{{ site.baseurl }}{{ card.domain | downcase | replace: ' ', '-' }}">{{ card.domain }}</a> &nbsp;&nbsp;//&nbsp;&nbsp;</small>
              <small class="test-muted subdomain"><i class="fa-solid fa-sitemap"></i>&nbsp; Subdomain: {{ card.subdomain }} &nbsp;&nbsp;//&nbsp;&nbsp;</small>
              <small class="test-muted resource"><i class="fa-solid fa-file"></i>&nbsp; Type of Resource: {{ card.resource }}</small><br>
            </p>
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const domainFilter = document.getElementById('domain-filter');
  const subdomainFilter = document.getElementById('subdomain-filter');
  const resourceFilter = document.getElementById('resource-filter');
  const cards = document.querySelectorAll('.card');

  function filterCards() {
    const selectedDomain = domainFilter.value;
    const selectedSubdomain = subdomainFilter.value;
    const selectedResource = resourceFilter.value;

    cards.forEach(card => {
      const domain = card.getAttribute('data-domain'); // Get domain from data attribute
      const subdomain = card.getAttribute('data-subdomain'); // Get subdomain from data attribute
      const resource = card.querySelector('.resource').textContent.trim().replace('Type of Resource: ', ''); 

      const domainMatch = selectedDomain === 'all' || domain === selectedDomain;
      const subdomainMatch = selectedSubdomain === 'all' || subdomain === selectedSubdomain;
      const resourceMatch = selectedResource === 'all' || resource === selectedResource;

      if (domainMatch && subdomainMatch && resourceMatch) {
        card.style.display = 'block';
      } else {
        card.style.display = 'none';
      }
    });
  }

  domainFilter.addEventListener('change', filterCards);
  subdomainFilter.addEventListener('change', filterCards);
  resourceFilter.addEventListener('change', filterCards);

  // Initial filtering when the page loads
  filterCards();
});
</script>


## Testing 3

{% assign members = site.members | sort: "title" %}

<div id="member-list" style="margin-top: 20px;">
  {% for member in members %}
    {% assign resource = site.data.members.resources | where: "name", member.resource | first %}
    <div class="member {% if member.inline == false %}hoverable{% endif %}" style="margin-bottom: 20px;" data-domain="{{ member.domain }}" data-subdomain="{{ member.subdomain }}">
      <div class="row no-gutters">
        <div class="team">
          <div class="member-body">
            {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
              <h5 class="member-title"><i class="{{ resource.icon | default: 'fas fa-file' }}"></i>&nbsp;&nbsp; {{ member.title }}</h5></a>
            <p class="member-text"><small class="test-muted">{% if member.profile.date %}<i class="fa-solid fa-calendar"></i>&nbsp; Date: {{ member.profile.date | replace: '<br />', ', ' }}{% endif %}
              {% if member.profile.date and member.profile.author %}&nbsp;&nbsp;//&nbsp;&nbsp;{% endif %}
              {% if member.profile.author %}<i class="fa-solid fa-user"></i>&nbsp; Author: {{ member.profile.author | replace: '<br />', ', ' }}{% endif %}</small></p>
            {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
              <p class="member-text">{{ member.teaser }}</p></a>
            {% if member.profile.source or member.profile.license %}
              <hr class="solid">
            {% endif %}
            <p class="member-text">
              {% if member.profile.source %}<small class="test-muted"><i class="fas fa-link"></i> Source: <a href="{{ member.profile.source }}">{{ member.profile.source | replace: '<br />', ', ' }}</a></small>{% endif %}
              {% if member.profile.source and member.profile.license %}<br>{% endif %}
              {% if member.profile.license %}<small class="test-muted"><i class="fa-solid fa-quote-left"></i>&nbsp; License: {{ member.profile.license }}</small>{% endif %}
            </p>
              <hr class="solid">
            <p class="member-text">
              <small class="test-muted domain"><i class="fa-solid fa-square"></i>&nbsp; Domain: <a href="{{ site.url }}{{ site.baseurl }}{{ member.domain | downcase | replace: ' ', '-' }}">{{ member.domain }}</a> &nbsp;&nbsp;//&nbsp;&nbsp;</small>
              <small class="test-muted subdomain"><i class="fa-solid fa-sitemap"></i>&nbsp; Subdomain: {{ member.subdomain }} &nbsp;&nbsp;//&nbsp;&nbsp;</small>
              <small class="test-muted resource"><i class="fa-solid fa-file"></i>&nbsp; Type of Resource: {{ member.resource }}</small><br>
            </p>
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

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
