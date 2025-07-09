---
layout: page
title: Quantum Innovation Challenge
menu_title: Home
menu_icon: house-door
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

{:.secondary}
# sponsored by the Novo Nordisk Foundation, Danish Business Authority and Danish Centre for AI Innovation.

<div class="aside">
    <h2><i class="bi bi-calendar3"></i> Event timeline</h2>
    <dl>
        {% if registration_status == "soon" or registration_status == "open" or registration_status == "demo" %}
            <dt>{{ site.registration_opens_date }}</dt>
            <dd>
                Applications open for participants<br>
                {% if registration_status == 'open' %}
                    <a href="mailto:quantum_challenge@mqs.dk" class="btn">Register now</a>
                {% elsif registration_status == 'closed' %}
                    <a class="btn disabled">Registration has closed</a>
                {% elsif registration_status == 'soon' %}
                    <a class="btn disabled">Registration opens soon</a>
                {% endif %}
            </dd>
        {% endif %}

        <dt>{{ site.registration_closes_date }}</dt>
        <dd>Applications for Phase I closes. Evaluation within two weeks and top five projects will receive access to the Gefion Supercomputer for the Phase II project developments.</dd>

        <dt>{{ site.event_date }}</dt>
        <dd>Top five projects presentations at the <a href="https://qt.eu/events/eqtc2025">European Quantum Technologies Conference (EQTC)</a> in Copenhagen.</dd>
        
        <dd>Final winner presentation at leading quantum computing conference in spring 2026.</dd>
    </dl>
</div>

The [Novo Nordisk Foundation (NNF)](https://novonordiskfonden.dk/en/), [BioInnovation Institute (BII)](https://bii.dk/), [Danish Centre for AI Innovation (DCAI)](https://dcai.dk/), [Molecular Quantum Solutions (MQS)](https://mqs.dk), [Novo Holdings](https://novoholdings.dk/) and [QAI Ventures](https://qai-ventures.com/), together with [The Danish Business Authority](https://danishbusinessauthority.dk/), [Invest in Denmark](https://investindk.com/) and [Innovation Centre Denmark](https://icdk.dk/) and a number of collaborators and partners yet to be announced, have partnered up for organizing the Quantum Computing Innovation Challenge within the Life Sciences.

<div style="display: flex; align-items: left; justify-content: center;">
    <a href="https://novonordiskfonden.dk/">
        <img src="https://novonordiskfonden.dk//app/uploads/NNF-INT_logo_blue_RGB_solid.png" alt="Novo Nordisk Foundation" style="width:150px; margin-right:70px;">
    </a>
    <a href="https://bii.dk/">
        <img src="https://mva.org/wp-content/uploads/2019/03/BII_Logo_Petroleum_RGB.png" alt="BioInnovation Institute" style="width:150px;">
    </a>
</div>
<br>
<div style="display: flex; align-items: left; justify-content: center;">
    <a href="https://mqs.dk">
        <img src="https://mqs.dk/Images/Logo/MQS_Logo_Text_black.png" alt="Molecular Quantum Solutions (MQS)" style="width:200px; margin-right:20px;">
    </a>
    <a href="https://dcai.dk/">
        <img src="./assets/DCAI_Logo_horizontal_Black_RGB.png" alt="Danish Centre for AI Innovation" style="width:175px;">
    </a>
</div>
<br>
<div style="display: flex; align-items: left; justify-content: center;">
    <a href="https://qai-ventures.com">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT4yFd81seqGxOo0wpiPf_e27HXz6YQQHtZdw&s" alt="QAI Ventures" style="width:125px; margin-right:95px;">
    </a>
        <a href="https://investindk.com/">
        <img src="https://investinodense.dk/wp-content/uploads/2022/02/Invest-in-Denmark.png" alt="Invest in Denmark" style="width:200px;">
    </a>
</div>
<br>
<div style="display: flex; align-items: left; justify-content: center;">
    <a href="https://novoholdings.dk/">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/df/Novo_Holdings_logo.svg/1200px-Novo_Holdings_logo.svg.png" alt="Novo Holdings" style="width:150px; margin-right:70px;">
    </a>
    <a href="https://danishbusinessauthority.dk/">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBuppnIhRA_UeICVvPBL1nxTiL8KywgV71vg&s" alt="Danish Business Authority" style="width:175px;">
    </a>
</div>
<div style="display: flex; align-items: center; justify-content: center;">
    <a href="https://icdk.dk/">
        <img src="https://images.squarespace-cdn.com/content/v1/62d5863a24e5b67bc23dff1f/1661420026081-N55ZWI4RWDCUTJC9J5TE/WeChat-Image_20220221111631.png" alt="Innovation Centre Denmark" style="width:150px;">
    </a>
</div>
<br>
<br>
<br>
The 2025 challenge is supported by industry experts from Novo Nordisk A/S and Roche Holding AG:

<div style="display: flex; align-items: left; justify-content: center;">
    <a href="https://novonordisk.com/">
        <img src="https://upload.wikimedia.org/wikipedia/en/b/b1/Novo_Nordisk_-_Logo.svg" alt="Novo Nordisk A/S" style="height:75px; margin-right: 70px;">
    </a>
    <a href="https://roche.com/">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Hoffmann-La_Roche_logo.svg/1200px-Hoffmann-La_Roche_logo.svg.png" alt="Roche Holding AG" style="height:75px;">
    </a>
</div>


For further information see the list of experts on the [about page](_/../about.md).

With the emergence of near term intermediate quantum computers and quantum-inspired algorithms powered by GPUs, it is important to understand their strengths and weaknesses, reduce the barrier to use, and adapt them for (bio)pharmaceutical development.
The virtual quantum challenge is designed for researchers all over the world to work collaboratively in teams on projects.

Academic/industrial researchers, start-ups and students can propose projects with respect to this year's [challenge topic](_/../projects.md) applying quantum computing and quantum-inspired algorithms to existing benchmarks, developing new benchmarks involving quantum computing methods, creating sub-algorithms based on quantum computing methods, proposing quantum computing based sampling and optimization methods, and more.
After the challenge, results will be collated and secured under open-source and free license agreements (Apache/MIT) in the dedicated Quantum-Challenge-2025 repository.

[This opportunity](_/../registration.md) is open to researchers at all levels who are interested in quantum computing for better informed pharmaceutical development.
Prior programming experience is required and basic familiarity with git and GitHub.
Training and orientation resources are available on the [resources page](_/../resources.md).


## Logistics and Eligibility

[Element space](https://matrix.to/#/#mqs-community-space:mozilla.org) for ongoing comms, especially for the participants to find other team members (see also [https://element.io](https://element.io)).

A condition to be accepted for the submission of a project application is the clear documentation of an academic participant in form of a main team member of the project. More details about this on the [eligibility page](_/../eligibility.md).

Pre-registrations and questions via email can be sent to <a href="mailto:quantum_challenge@mqs.dk">quantum_challenge@mqs.dk</a> and will be collectively answered via the [FQA page](_/../faq.md).


## Why participate?

A total of five submissions will be selected for presentation during the [European Quantum Technologies Conference 2025 (EQTC)](_/../about.md) to be held in Copenhagen this year.
In addition, the top 5 teams will each receive a voucher giving them access to the Gefion AI Supercomputer to test and validate their proposals.
The winning solution will be announced in conjunction with another leading European quantum conference in the Spring of 2026.
Don't miss this opportunity to be part of a revolution that could change the world.

See also the [agenda](_/../agenda.md) to get a timeline overview.

The top-ranked projects will be highlighted here:

| Rank | Project #                                            | Team Name | Project Name |
| ---  | ---------------------------------------------------- | --------- | ------------ |
| 1st  | []()                                                 |           |              |
| 2nd  | []()                                                 |           |              |
| 3rd  | []()                                                 |           |              |
| 4th  | []()                                                 |           |              |
| 5th  | []()                                                 |           |              |

For a full list of the submitted challenge projects, we encourage you to take a look at the [challenge page](_/../projects.md).

<!--
## Partners

<div style="display: flex; align-items: center; justify-content: center;">
    <a href="https://novonordiskfonden.dk/">
        <img src="https://novonordiskfonden.dk//app/uploads/NNF-INT_logo_blue_RGB_solid.png" alt="Novo Nordisk Foundation" style="width:200px; margin-right: 70px;">
    </a>
    <a href="https://bii.dk/">
        <img src="https://mva.org/wp-content/uploads/2019/03/BII_Logo_Petroleum_RGB.png" alt="BioInnovation Institute" style="width:200px; margin-challenge5px;">
    </a>
    <br>
    <br>
    <a href="https://mqs.dk">
        <img src="https://mqs.dk/Images/Logo/MQS_Logo_Text_black.png" alt="Molecular Quantum Solutions (MQS)" style="width:300px; margin-left: 20px;">
    </a>
    <a href="https://dcai.dk/">
        <img src="./assets/DCAI_Logo_horizontal_Black_RGB.png" alt="Danish Centre for AI Innovation" style="width:300px; margin-left: 20px;">
    </a>
    <a href="https://qai-ventures.com">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT4yFd81seqGxOo0wpiPf_e27HXz6YQQHtZdw&s" alt="QAI Ventures" style="width:150px; margin-right: 20px;">
    </a>
    <br>
    <br>
    <a href="https://investindk.com/">
        <img src="https://investinodense.dk/wp-content/uploads/2022/02/Invest-in-Denmark.png" alt="Invest in Denmark" style="width:250px; margin-right: 20px;">
    </a>
    <a href="https://novoholdings.dk/">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/df/Novo_Holdings_logo.svg/1200px-Novo_Holdings_logo.svg.png" alt="Novo Holdings" style="width:200px; margin-right: 20px;">
    </a>
    <br>
    <br>
    <a href="https://danishbusinessauthority.dk/">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBuppnIhRA_UeICVvPBL1nxTiL8KywgV71vg&s" alt="Danish Business Authority" style="width:250px; margin-right: 20px;">
    </a>
    <a href="https://icdk.dk/">
        <img src="https://images.squarespace-cdn.com/content/v1/62d5863a24e5b67bc23dff1f/1661420026081-N55ZWI4RWDCUTJC9J5TE/WeChat-Image_20220221111631.png" alt="Innovation Centre Denmark" style="width:250px; margin-right: 20px;">
    </a>
</div>
-->

## Financial Sponsors

- [Novo Nordisk Foundation](https://novonordiskfonden.dk/)
- [Danish Business Authority](https://danishbusinessauthority.dk/)
- [Danish Centre for AI Innovation - Gefion](https://dcai.dk/)

[faq]: {{ site.baseurl }}{% link faq.md %}
