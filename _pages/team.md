---
layout: page
permalink: /about
title: About
description: Learn More About the Data Advocacy for All Project and the Team Behind It
nav: true
nav_rank: 8
---

# Mission

Data Advocacy for All is a CU Next Award project that aims to extend data humanities education throughout and beyond the University of Colorado system by offering an open-access modular approach to teaching data advocacy. Whether used by nonprofits to catalyze social action, think tanks to argue for policy change, or organizations to promote legislative equity, data advocacy is an increasingly important means of communication in the era of ubiquitous data. Yet while more and more undergraduate students are being exposed to the technical aspects of data science, too few students are being taught the complex array of data skills and communication literacies needed to use data responsibly and effectively advocate for social change. Data Advocacy for All aims to address this curricular gap by teaching students how to blend minimal computing and open-source tools with rhetorical literacies to ethically translate data into effective real-world action. 

This curriculum is grounded in the methodologies of data feminism and rhetorical data studies and guided by the following data justice perspective: 

_While coding and other technical skills are important for data literacy, students must also learn how to not only critically examine data issues in the context of existing power dynamics and social practices but also rhetorically use data to tell ethical, compelling data-driven stories and participate in ongoing conversations about pressing social matters._

Such critical-rhetorical labor takes place throughout all stages of data advocacy and demands a balanced curriculum in which all stages can be sufficiently learned. Data Advocacy for All thus offers a set of eight modules to train students in the full life cycle of the data advocacy process. 
<br><br>
# The CU Next Award

The [CU Next Award](https://www.cu.edu/oaa/academic-innovation-programs/cu-next-award) is an academic innovation program that supports pedagogical development within the University of Colorado system. The CU Next Award requires faculty from a minimum of two University of Colorado campuses to collaborate on a pedagogical project that innovates with technology in order to help “increase the efficacy and efficiency of student learning in courses and degree programs” as well as “reduce technology-related and other barriers for individual and small groups of faculty.” To fulfill this requirement, faculty from the University of Colorado Boulder and the University of Colorado Denver collaborated to design, implement, and assess the Data Advocacy for All modular curriculum over a three year span as well design this Open Access (OA) digital repository of curricular materials for instructors across the CU system and beyond. 

[You can learn more about the CU Next grant and the other awarded projects here.](https://www.cu.edu/oaa/academic-innovation-programs/cu-next-award)
<br><br>
<!--# Cite This Project-->

# The Data Advocacy for All Team
<br>
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
                        <a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
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
                        <small class="test-muted"><i class="fas fa-thumbtack"></i> {{ member.profile.address | replace: '<br />', ', ' }}</small> 
                    </p>
                </div>
            </div>
        </div>
    </div>
</p>

	{% endfor %}
<br>
{% endfor %}

