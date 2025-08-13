---
title: About
subtitle: The Quantum Innovation Challenge is a virtual competition and organised by the Bio Innovation Institute (BII), Molecular Quantum Solutions (MQS), Danish Centre for AI Innovation Center (DCAI) and QAI Ventures

menu_title: About
menu_icon: globe2
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

{% include subpage_header.html %}

<section class="px-5 max-w-screen-lg mx-auto text-white py-10 gap-4 flex flex-col">
<article class="prose prose-invert max-w-none w-full flex-1 block break-words mb-8">

{% if event_status != "over" %}
<p>The Quantum Innovation Challenge is a virtual competition and organised by the <a href="https://bii.dk">Bio Innovation Institute (BII)</a>, <a href="https://mqs.dk">Molecular Quantum Solutions (MQS)</a>, <a href="https://dcai.dk">Danish Centre for AI Innovation Center (DCAI)</a> and <a href="https://qai-ventures.com">QAI Ventures</a>.</p>
<p>The competition is open to researchers and industrial participants at all levels who are interested in applying quantum computing and quantum-inspired algorithms to pharmaceutical development.</p>
{% else %}
<p>The Quantum Innovation Challenge was a hosted on {{ site.event_date }}, organised by the <a href="https://bii.dk">Bio Innovation Institute (BII)</a>, <a href="https://mqs.dk">Molecular Quantum Solutions (MQS)</a>, <a href="https://dcai.dk">Danish Centre for AI Innovation Center (DCAI)</a> and <a href="https://qai-ventures.com">QAI Ventures</a>.</p>
<p>The event included researchers and industrial participants at all levels who are interested in applying quantum computing and quantum-inspired algorithms to pharmaceutical development.</p>
{% endif %}

<h3>The organizing team</h3>

<p>To contact us about the quantum challenge, please contact us via mail quantum_challenge@mqs.dk. Molecular Quantum Solutions (MQS) is the technical support of this challenge.</p>

</article>

<div class="w-full max-w-6xl mx-auto">
    <table class="w-full border-collapse border border-electron/25">
        <tbody>
            {% for member in site.team_members %}
            <tr class="{% unless forloop.last %}border-b border-electron/25  hover:bg-electron/10 {% endunless %}">
                <td class="py-6 pr-6 align-center p-5 ">
                    {% if member.image != "" %}
                        <img alt="{{ member.name }}" 
                             src="{{ member.image }}"
                             class="w-20 h-20 md:w-24 md:h-24 rounded-full object-cover border border-quantum/25">
                    {% else %}
                        <div class="w-20 h-20 md:w-24 md:h-24 rounded-full bg-gray-100 border border-quantum/25 flex items-center justify-center">
                            <i class="bi bi-person text-gray-400 text-2xl"></i>
                        </div>
                    {% endif %}
                </td>
                <td class="py-6 align-top">
                    <div class="font-semibold text-lg text-white mb-2">{{ member.name }}</div>
                    <div class="flex gap-3 mb-3">
                        {% if member.website %}
                            <a title="Website" href="{{ member.website }}" class="text-white underline transition-colors">
                                Website
                            </a>
                        {% endif %}
                        {% if member.github %}
                            <a title="GitHub" href="{{ member.github }}" class="text-white underline transition-colors">
                                Github
                            </a>
                        {% endif %}
                        {% if member.linkedin %}
                            <a title="LinkedIn" href="{{ member.linkedin }}" class="text-white underline transition-colors">
                                LinkedIn
                            </a>
                        {% endif %}
                    </div>
                    <div class="text-electron font-medium">{{ member.organization }}</div>
                    <div class="text-electron">{{ member.role }}</div>
                </td>
            </tr>
            {% endfor %}
        </tbody>
    </table>
</div>

<article class="prose prose-invert max-w-none w-full flex-1 block break-words mb-8">
<h3>Acknowledgements</h3>
<p>
We thank Sterling G. Baird and the rest of the organizing team for the <a href="https://github.com/AC-BO-Hackathon/ac-bo-hackathon.github.io">Bayesian Optimization Hackathon for Chemistry and Materials</a> github repository (MIT license) which we have adapted for this quantum challenge initiative.
The AC-BO-Hackathon repository has built on top of the <a href="https://materials-data-facility.github.io/llm-hackathon/">LLMs in Materials and Chemistry '23 Hackathon</a> repository.
</p>
</article>
</section>
