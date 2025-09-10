---
title: Meet the Jury
subtitle: Meet the jury members of the Quantum Innovation Challenge

menu_title: Jury
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


<div class="w-full max-w-6xl mx-auto">
    <table class="w-full border-collapse border border-electron/25 table-fixed">
        <tbody>
            {% for member in site.jury_members %}
            <tr class="{% unless forloop.last %}border-b border-electron/25  hover:bg-electron/10 {% endunless %}">
                <td class="py-6 pr-6 align-center p-5 w-1/6">
                <div class="w-full h-full flex items-center justify-center">
                    {% if member.image != "" %}
                        <img alt="{{ member.name }}"  
                             src="{{ member.image }}" 
                             class="w-20 h-20 md:w-24 md:h-24 rounded-full object-cover border border-quantum/25"> 
                    {% else %}
                        <div class="w-20 h-20 md:w-24 md:h-24 rounded-full bg-gray-100 border border-quantum/25 flex items-center justify-center">
                            <i class="bi bi-person text-gray-400 text-2xl"></i>
                        </div>
                    {% endif %}   
                </div>
                </td>
                <td class="py-6 align-top w-5/6">
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


</section>
