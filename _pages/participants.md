---
layout: page
permalink: /participants/
title: Participants 
description: 
nav: true
nav_rank: 8
---

{% assign members = site.members | sort: "profile.name" %}

{% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}" id="{{ member.name }}">
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
				<small class="test-muted domain"><a href="{{ member.profile.youtubeurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fab fa-youtube"></i>&nbsp;&nbsp; <strong>YouTube:</strong> {{ member.profile.youtubeurl }}</a></small><br>
				{% endif %}
				{% if member.profile.bluesky %}
				<small class="test-muted domain"><a href="{{ member.profile.bluesky }}.bsky.social" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-cloud"></i>&nbsp;&nbsp; <strong>Bluesky:</strong> {{ member.profile.bluesky }}</a></small><br>
				{% endif %}
				{% if member.profile.kofi %}
				<small class="test-muted domain"><a href="{{ member.profile.kofiurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-mug-saucer"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.kofi }}</a></small><br>
				{% endif %}
				{% if member.profile.carrd %}
				<small class="test-muted domain"><a href="{{ member.profile.carrdurl }}" class="card-link" target="_blank" style="color: #7D858C;"><i class="fa-solid fa-address-card"></i>&nbsp;&nbsp; <strong>Carrd:</strong> {{ member.profile.carrd }}</a></small><br>
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
