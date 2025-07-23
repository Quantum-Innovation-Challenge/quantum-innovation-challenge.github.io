---
title: Quantum Challenge 2025 Timeline
menu_title: Timeline
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


The Quantum Innovation Challenge consists of two phases. During Phase 1, you will form your team, and you will submit your proposal. After the evaluation of the proposals, the best five proposals will enter a Phase 2, where the teams will have the opportunity to access the Gefion AI Supercomputer. The access to Gefion will be shared among the team members. The Danish Centre for AI Innovation (DCAI) runs and operates Gefion, a large-scale NVIDIA DGX SuperPOD. It comprises 191 NVIDIA DGX H100 systems for a total of 1,528 NVIDIA H100 Tensor Core GPUs.

### Phase I: July - 30th of September

During the first weeks of Phase 1 we will compile an extensive FQA summary with all your questions and try to fix all outstanding issues you might have to set up a team and work on a project. 

You will have time until the 30th of September to submit your project via a pull request to the <a href="https://github.com/Quantum-Innovation-Challenge/LSQI-Challenge-2025">LSQI-Challenge-2025 repository</a>.

The possibility to submit your project will close at 10am CET on the 30th of September, later pull requests will be disregarded.


### Phase II: 15th of October - 12th of November

Phase 2 of the challenge will include the evaluation (1st of October - 14th of October) and the feedback notification on the submitted projects (latest the 14th of October).
The top five teams will receive access to the Danish supercomputer Gefion throughout Q4 2025.
The top five teams will present their projects at the European Quantum Technologies Conference 2025 in Copenhagen (10-12 November 2025) giving the teams the opportunity to connect with the European quantum computing community and establish valuable relationships.


### Phase III: Q4 2025 - Q1 2026

The final code repositories and reports are expected to be pushed to the respective repository until the 31st of January 2026.
The presentations and the winner announcement will be held at a leading quantum computing conference in spring 2026.


### After the challenge

The <a href="https://github.com/Quantum-Innovation-Challenge/LSQI-Challenge-2025">LSQI-Challenge-2025 repository</a> will serve as the documentation for all projects and will become a valuable resource for academia and industry while the participating project teams have made valuable contacts to academia and industry to foster further venture building.
All submitted projects will have been screened to align with the open-source and free license (Apache/MIT) condition (see also Eligibility page).
