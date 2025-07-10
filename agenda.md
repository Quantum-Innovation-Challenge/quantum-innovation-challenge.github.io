---
title: Quantum Challenge Agenda 🗓️
menu_title: Agenda
menu_icon: clock
---
{% assign current_date = 'now' | date: "%Y-%m-%d" %}
{% assign event_start_date = site.event_start_date | date: "%Y-%m-%d" %}
{% assign event_close_date = site.event_close_date | date: "%Y-%m-%d" %}
{% assign registration_opens_date = site.registration_opens_date | date: "%Y-%m-%d" %}
{% assign registration_closes_date = site.registration_closes_date | date: "%Y-%m-%d" %}

{% if current_date < registration_opens_date %}
    {% assign registration_status = 'soon' %}
{% elsif current_date >= registration_opens_date and current_date <= registration_closes_date %}
    {% assign registration_status = 'open' %}
{% else %}
    {% assign registration_status = 'closed' %}
{% endif %}

{% if current_date < event_start_date %}
    {% assign event_status = 'soon' %}
{% elsif current_date >= event_start_date and current_date <= event_close_date %}
    {% assign event_status = 'now' %}
{% else %}
    {% assign event_status = 'over' %}
{% endif %}


## Schedule
{% if event_status != "over" %}
The anticipated schedule is as follows, with all times listed in Central European Time (CET).
{% else %}
The schedule for the event was as follows, with all times listed in Central European Time (CET):
{% endif %}


### Phase 1: Jul 01 - Aug 31

During the first weeks of Phase 1 we will compile an extensive Q&A summary with all your questions.
You will have time until the 15th of September to submit your project via a pull request to the Quantum-Challenge-2025 repository. 


### Phase 2: Sep 15 - European Quantum Technologies Conference 2025

Phase 2 of the challenge will include the evaluation and the feedback notification on their submitted project. The top five teams will receive access to the Danish supercomputer Gefion.


### Final presentations (10-12 November 2025)

The top five teams will present their projects at the European Quantum Technologies Conference 2025 in Copenhagen giving the teams the opportunity to connect with the European quantum computing community and establish valuable relationships.

A follow up participation of the top five teams for a conference in Spring 2026 is also in the planning.


### After the challenge

The Quantum-Challenge-2025 will be a documentation of all projects and a valuable resource for academia and industry.
All submitted projects have been screened to align with the necessary open-source and free license (Apache/MIT).
