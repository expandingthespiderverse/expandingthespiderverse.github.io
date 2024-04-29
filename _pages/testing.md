---
layout: page
permalink: /testing/
title: Testing
description: 
nav: True
nav_rank: 8
---

## Testing 6

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row">
            <!-- Left column for profile picture -->
            <div class="col-sm-4 col-md-3">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h3 class="card-title">{{ member.name }}</h3>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
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
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p>{{ member.profile.spidersona1description }}</p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p>{{ member.profile.spidersona2description }}</p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p>{{ member.profile.spidersona3description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}


## Testing 5

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3 position-relative">
                <!-- Main profile picture -->
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
                <!-- Second profile picture (Spider-Sona) -->
                <img src="{{ '/assets/img/' | append: member.profile.spidersonapic | relative_url }}" class="position-absolute bottom-0 end-0" style="width: 4rem; height: auto; z-index: 1;" alt="{{ member.profile.name }}" />
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h3 class="card-title">{{ member.name }}</h3>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">
                            {{ member.description }}
                        </p>
                    {% endif %}
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
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}


## Testing 4

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h3 class="card-title">{{ member.name }}</h3>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
			    <p class="card-text">
				    {{ member.description }}
			    </p>
			    {% endif %}
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
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

## Testing 3

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h3 class="card-title">{{ member.profile.name }}</h3>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
			    <p class="card-text">
				    {{ member.description }}
			    </p>
			    {% endif %}
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
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

## Testing 2

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
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

## Testing 1

{% comment %} 
{% assign groups = site.members | sort: "group_rank" | map: "group" | uniq %} 
{% endcomment %}

<!--this Liquid command looks in the Collection "members" that was created through a directory named members + adding it as a collection in _config.yml file. It sorts it by the variable you specify in teh frontmatter for each member markdown file - ex. group_rank, lastname, etc. The map command then puts them into a few buckets based on  "group" - defined in the frontmatter of each of the individual member pages - ex. "Principal Investigators". It goes through and only looks at unique values for all pages listed in here. We can change this and/or add different categories/designations - ex. "Faculty" "Researchers" etc. or a "school" category for "University of Colorado Denver" "CU Boulder" etc.  -->

{% assign groups = site.members | sort: "lastname" | map: "group" | uniq %}

{% for group in groups %}

## {{ group }}

	{% assign members = site.members | sort: "last_name" | where: "group", group %}
	{% for member in members %}


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

