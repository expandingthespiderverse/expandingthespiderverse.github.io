---
layout: page
permalink: /testing/
title: Testing
description: 
nav: false
nav_rank: 8
---

## Testing 31

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="https://{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="https://{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="https://{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="https://{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="https://{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="https://{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>


## Testing 30

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
    {% assign image_count = 0 %}
    {% if member.profile.spidersona1 %}
        {% assign image_count = image_count | plus: 1 %}
    {% endif %}
    {% if member.profile.spidersona2 %}
        {% assign image_count = image_count | plus: 1 %}
    {% endif %}
    {% if member.profile.spidersona3 %}
        {% assign image_count = image_count | plus: 1 %}
    {% endif %}
    {% comment %}
    Calculate the column width based on the number of images present
    {% endcomment %}
    {% assign col_width = 12 %}
    {% if image_count != 0 %}
        {% assign col_width = 12 | divided_by: image_count %}
    {% endif %}
    <p>
        <div class="card {% if member.inline == false %}hoverable{% endif %}">
            <div class="row no-gutters">
                <!-- Left column for profile picture -->
                <div class="col-sm-5 col-md-5">
                    <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
                </div>
                <!-- Right column for member info -->
                <div class="col-sm-7 col-md-7">
                    <div class="card-body">
                        {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                        <h2 class="card-title mb-4">{{ member.name }}</h2>
                        {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                        {% if member.description %}
                            <p class="card-text">{{ member.description }}</p>
                        {% endif %}
                        {% if member.inline == false %}</a>{% endif %}
                        <p class="card-text">
                            {% if member.profile.website %}
                                <small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
                            {% endif %}
                            {% if member.profile.twitter %}
                                <small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
                            {% endif %}
                            <!-- Additional links -->
                        </p>
                        <hr class="solid">
                        <!-- Additional images and captions -->
                        <div class="row mt-3">
                            {% if member.profile.spidersona1 %}
                                <div class="col-md-{{ col_width }}">
                                    <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                                    <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                                </div>
                            {% endif %}
                            {% if member.profile.spidersona2 %}
                                <div class="col-md-{{ col_width }}">
                                    <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                                    <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                                </div>
                            {% endif %}
                            {% if member.profile.spidersona3 %}
                                <div class="col-md-{{ col_width }}">
                                    <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                                    <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                                </div>
                            {% endif %}
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </p>
{% endfor %}

<br><br>

## Testing 29

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
                    <p class="card-text">
                        {% if member.profile.website %}
                            <small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
                        {% endif %}
                        {% if member.profile.twitter %}
                            <small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
                        {% endif %}
                        <!-- Additional links -->
                    </p>
                    <hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        {% if member.profile.spidersona1 %}
                            <div class="col-md-4">
                                <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                                <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                            </div>
                        {% endif %}
                        {% if member.profile.spidersona2 %}
                            <div class="col-md-4">
                                <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                                <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                            </div>
                        {% endif %}
                        {% if member.profile.spidersona3 %}
                            <div class="col-md-4">
                                <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                                <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                            </div>
                        {% endif %}
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 28

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 27

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4" style="margin-right: 1px;">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4" style="margin-right: 1px;">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>


## Testing 26

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3 no-gutters">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 25

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4 mr-0.1">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4 mr-0.1">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 24

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4 mr-0.5">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4 mr-0.5">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 23

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4 mr-2">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4 mr-2">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 22

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 21

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i>&nbsp;&nbsp; <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i>&nbsp;&nbsp; <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i>&nbsp;&nbsp; <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i>&nbsp;&nbsp; <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i>&nbsp;&nbsp; <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-bluesky"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-linkedin"></i>&nbsp;&nbsp; <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i>&nbsp;&nbsp; <strong>Email:</strong> {{ member.profile.email }}</a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 20 

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i> <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i> <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.instagram %}
				<small class="test-muted domain"><a href="https://instagram.com/{{ member.profile.instagram }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-instagram"></i> <strong>Instagram:</strong> {{ member.profile.instagram }}</a></small><br>
				{% endif %}
				{% if member.profile.tiktok %}
				<small class="test-muted domain"><a href="https://tiktok.com/@{{ member.profile.tiktok }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tiktok"></i> <strong>TikTok:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.tumblr %}
				<small class="test-muted domain"><a href="https://{{ member.profile.tumblr }}.tumblr.com" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-tumblr"></i> <strong>Tumblr:</strong> {{ member.profile.tumblr }}</a></small><br>
				{% endif %}
				{% if member.profile.youtube %}
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i> <strong>YouTube:</strong> {{ member.profile.tiktok }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i> <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-mug-saucer"></i> <strong>Ko-fi:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-address-card"></i> <strong>Ko-fi:</strong> {{ member.profile.carrd }}</a></small><br>
				{% endif %}
				{% if member.profile.linkedin %}
				<small class="test-muted domain"><a href="{{ member.profile.linkedinurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-address-card"></i> <strong>LinkedIn:</strong> {{ member.name }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i></a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid mb-3" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>


## Testing 19

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-3">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fas fa-globe"></i> <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-twitter"></i> <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link" style="color: #7D858C;"><i class="fas fa-envelope"></i></a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <br><br><p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <br><br><p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <br><br><p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 18

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-3">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-3 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text" style="color: #7D858C;">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i> <strong>Website:</strong> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i> <strong>Twitter:</strong> {{ member.profile.twitter }}</a></small><br>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <br><p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <br><p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <br><p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>


## Testing 17

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-4">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i> <b>Website:</b> {{ member.profile.website }}</a></small><br>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i> <b>Twitter:</b> {{ member.profile.twitter }}</a></small>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 16

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title mb-2">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a> <b>Website:</b> <a href="{{ member.profile.website }}" class="card-link" target="_blank">{{ member.profile.website }}</a></small>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a></small>
				{% endif %}
				{% if member.profile.phone %}
				<small class="test-muted domain"><a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a></small>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted" style="line-height: 1;"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 15

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title pb-5">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted pb-5">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a></small>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a></small>
				{% endif %}
				{% if member.profile.phone %}
				<small class="test-muted domain"><a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a></small>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle text-muted"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

<br><br>

## Testing 14

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <!-- Add custom classes for name and subtitle -->
                    <h2 class="card-title custom-name">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted custom-subtitle">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
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

<!-- Inline CSS -->
<style>
.custom-name {
    margin-bottom: 10px; /* Adjust as needed */
}

.custom-subtitle {
    margin-bottom: 15px; /* Adjust as needed */
}
</style>

## Testing 13

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
			    {% endif %}
                    {% if member.inline == false %}</a>{% endif %}
			<p class="card-text">
				{% if member.profile.website %}
				<small class="test-muted domain"><a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a></small>
				{% endif %}
				{% if member.profile.email %}
				<small class="test-muted domain"><a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a></small>
				{% endif %}
				{% if member.profile.phone %}
				<small class="test-muted domain"><a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a></small>
				{% endif %}
				{% if member.profile.twitter %}
				<small class="test-muted domain"><a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a></small>
				{% endif %}
			</p>
			<hr class="solid">
                    <!-- Additional images and captions -->
                    <div class="row mt-3">
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona1 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle mb-2 text-muted"><small>{{ member.profile.spidersona1description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona2 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle mb-2 text-muted"><small>{{ member.profile.spidersona2description }}</small></p>
                        </div>
                        <div class="col-md-4">
                            <img src="{{ '/assets/img/' | append: member.profile.spidersona3 | relative_url }}" class="img-fluid" alt="{{ member.profile.name }}" />
                            <p class="card-subtitle mb-2 text-muted"><small>{{ member.profile.spidersona3description }}</small></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</p>
{% endfor %}

## Testing 12

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-5 col-md-5">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-7 col-md-7">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title">{{ member.name }}</h2>
                    {% if member.subtitle %}<h5 class="card-subtitle mb-2 text-muted">{{ member.subtitle }}</h5>{% endif %}
                    {% if member.description %}
                        <p class="card-text">{{ member.description }}</p>
                    {% endif %}
			    {% if member.profile.website or member.profile.twitter or member.profile.instagram or member.profile.tiktok or member.profile.tumblr or member.profile.youtube or member.profile.bluesky or member.profile.kofi or member.profile.caard or member.profile.linkedin or member.profile.email %}
			    <hr class="solid">
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

## Testing 11

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <!-- Left column for profile picture -->
            <div class="col-sm-6 col-md-6">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <!-- Right column for member info -->
            <div class="col-sm-6 col-md-6">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h2 class="card-title">{{ member.name }}</h2>
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

## Testing 10

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
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

## Testing 9

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row">
            <!-- Left column for profile picture -->
            <div class="col-sm-4 col-md-3 d-flex">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" style="max-width: 100%;" />
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

## Testing 8

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row">
            <!-- Left column for profile picture -->
            <div class="col-sm-4 col-md-3 d-flex justify-content-center align-items-center">
                <img src="{{ '/assets/img/' | append: member.profile.profilepic | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" style="max-width: 100%;" />
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


## Testing 7

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
                            <h7>{{ member.profile.spidersona1description }}</h7>
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

