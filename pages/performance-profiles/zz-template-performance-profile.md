---
title: ENTER OFFICE HERE - ENTER ROLE TITLE HERE 
# permalink: /join/performance-profiles/ENTER ROLE TITLE HERE/
# state: ENTER STATE HERE (open, closed, upcoming)
# job_post_type: ENTER TYPE HERE (tts or usajobs)
# parent_position_name: ENTER NAME OF OVERARCHING POSITION HERE
# parent_position_link: /join/ENTER POSITION LINK HERE
# related_performance_profiles:
#  - name: NAME OF PERFORMANCE PROFILE
#    link: /join/ENTER PERFORMANCE PROFILE PAGENAME HERE
#  - name: (repeat as necessary)
#    link: (repeat as necessary)
# apply_url: USAJOBS URL
# contact_name: TTS Talent Team
# contact_email: jointts@gsa.gov
# INSTRUCTIONS UPCOMING: These fields are required for upcoming
# role_name: ENTER THE NAME OF THE ROLE HERE (Without Org)
# gs_level: ENTER GS LEVEL (13, 14, 15, etc)
# org: 'ENTER ORG NAME HERE' (18F, Centers of Excellence, etc.)
---
{% if page.state == 'upcoming' %}
{{ page.org }} will soon be accepting applications for GS-{{ page.gs_level }} - {{ page.role_name }} roles. If you'd like to be
  notified when these positions are open, sign up to our [mailing list]({{ site.baseurl }}/newsletter). More details are available on [the main {{ page.parent_position_name }} posting]({{site.baseurl}}{{ page.parent_position_link }}).
{% endif %}

{% if page.state != 'upcoming' %}
{{ page.org }} is hiring for the role of GS-{{ page.gs_level }} {{ page.role_name }}. **There are several {{ page.org }} teams hiring for this role.** This page contains a summary of the {{ page.title }} role. [View descriptions of other {{ page.org }} {{ page.role_name }} positions.]({{site.baseurl}}{{ page.parent_position_link }})
{% endif %}

## Role summary

ENTER ROLE SUMMARY HERE

## Key objectives

### Objective #1: ENTER OBJECTIVE NAME
- X
- X
- X

### Objective #2: ENTER OBJECTIVE NAME
- X
- X
- X

## {{ page.related_performance_profiles | size | plus: 1 }} {{ page.org }} teams are hiring for this role

The links below provide descriptions specific to each {{ page.org }} team. When the role is posted and open for application on USAJobs, you can indicate which team(s) you’re interested in.
{% for profile in page.related_performance_profiles %}
  - [{{profile.name}}]{{site.baseurl}}({{profile.link}})
{% endfor %}

## Preparing to apply

This Join TTS site has information about [the application process](https://join.tts.gsa.gov/hiring-process/) and [how to prepare a government-style resume](https://join.tts.gsa.gov/resume/).