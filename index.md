---
layout: page
title:
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

<div style="display: flex; align-items: left; justify-content: left;">
    <img src="./assets/Cover_Image.png" alt="Cover Image" style="widt:300px;">
</div>

<div class="aside">
    <h2><i class="bi bi-calendar3"></i>Timeline</h2>
    <dl>
        {% if registration_status == "soon" or registration_status == "open" or registration_status == "demo" %}
            <dt>{{ site.registration_opens_date }}</dt>
            <dd>
                Applications open for participants<br>
                {% if registration_status == 'open' %}
                    <a href="mailto:quantum_challenge@mqs.dk" class="btn">Register your team</a>
                    <br>
                    It is needed to register your team by sending us the names of your team members and the hosting letter.
                    <br>
                    <a href="https://quantum-innovation-challenge.github.io/projects/" class="btn">Read about the challenge</a>
                    <br>
                    <a href="https://matrix.to/#/#mqs-community-space:mozilla.org" class="btn">Find team members via Element Space</a>
                {% elsif registration_status == 'closed' %}
                    <a class="btn disabled">Registration has closed</a>
                {% elsif registration_status == 'soon' %}
                    <a class="btn disabled">Registration opens soon</a>
                {% endif %}
            </dd>
        {% endif %}

        <dt>{{ site.registration_closes_date }}</dt>
        <dd><b>Phase I</b>
        <br>
        - Submission of the projects closes on the 30th of September at 10AM Central European Time (CET).
        <br>
        - Evaluation will be conducted from the 1st until the 15th of October.
        <br>
        - The top five teams will receive GPU hours for the Gefion Supercomputer for Phase II.</dd>

        <dt>{{ site.event_date }}</dt>
        <dd><b>Phase II</b>
        <br>
        - The top five teams are invited to present at the <a href="https://eqtc2025.ku.dk/">European Quantum Technologies Conference 2025 (EQTC)</a> in Copenhagen (10-12 November).
        <br>
        - Travel costs and accomodation for all teams are sponsored and will be covered.
        <br>
        - Until the end of December 2025 the top 5 teams will have access to the Gefion Supercomputer.</dd>
        <br>
        <dd><b>Phase III (Q1/Q2 2026)</b>
        <br>
        - Finalization of the projects until the 31st of January 2026.
        <br>
        - The presentations and the winner announcement will be held at a leading quantum computing conference in spring 2026.</dd>
    </dl>
</div>


## Accelerating Quantum Applications<br>in the Life Sciences

The Quantum Innovation Challenge 2025 invites researchers, start-ups, and students from around the world to explore how quantum computing and quantum-inspired algorithms can advance (bio)pharmaceutical innovation – offering selected teams exclusive access to the Gefion AI Supercomputer.

With the emergence of near-term quantum computers and powerful GPU-based methods, there is a growing need to understand their strengths and limitations, reduce barriers to adoption, and apply them to real-world problems in drug development. This virtual challenge is designed to foster collaborative, open research that contributes to this mission.


## Your Role

Academic/industrial researchers, start-ups and students can propose projects with respect to this year's [challenge topic](_/../projects.md) applying quantum computing and quantum-inspired algorithms to:

- existing benchmarks or new benchmarks as further defined by the [Quantum Challenge 2025 topic](./../projects.md)
- creating sub-algorithms based on quantum computing methods
- designing quantum-enhanced sampling and optimization techniques

Following the challenge, results will be collated and secured under open-source and free license agreements (Apache/MIT) in the dedicated Quantum-Challenge-2025 repository.


## Who can participate?

The challenge encourages cross-disciplinary and international collaboration. It is open to teams of academic and industrial researchers, start-ups, and students who are interested in using quantum computing and quantum-inspired methods to advance pharmaceutical development.

To be eligible for submission:

- Each team must include at least one clearly documented academic participant in a main role
- Teams should have prior programming experience and basic familiarity with git and GitHub
- Full eligibility details are available on the [Eligibility page](_/../eligibility.md)

Support and participation resources:

- Participants are welcome to connect and form teams using our dedicated [Element Space](https://matrix.to/#/#mqs-community-space:mozilla.org) (see also [https://element.io](https://element.io))
- Orientation materials and technical guidance are available on the [Resources page](./../resources.md)
- Pre-registrations and questions can be sent to <a href="mailto:quantum_challenge@mqs.dk">quantum_challenge@mqs.dk</a>. All inquiries will be addressed collectively on the [FAQ page](./../faq.md)

    
## Why participate?

<div style="display: flex; align-items: left; justify-content: left;">
    <img src="./assets/Benefits.png" alt="Cover Image" style="widt:300px;">
</div>

- Five teams will be selected to present their work at the [European Quantum Technologies Conference 2025 (EQTC)](https://eqtc2025.ku.dk/) in Copenhagen.
- Each of the top 5 teams will receive a voucher for access to the Gefion AI Supercomputer to test and validate their solutions.
- The winning team ranking 1st place at the end of the challenge will receive 4136 GPU hours on Gefion sponsored by DCAI after the challenge.
- The winning solution will be announced in Spring 2026 during another leading European quantum event.
- Networking and access to a global community of experts from the academic and industrial life science community.
- Working on a relevant life science use case with feedback and mentoring from leading industry partners, investors, and experts.
- Direct access and support from Gefion, one of the fastest supercomputers globally, to run your challenge code (top 5 teams).
- Global marketing and branding with free tickets to EQTC 2025, presentation opportunities and further fostering of relationships (top 5 teams).
- Onboarding to the global QAI Ventures ecosystem with 1 year of exclusive 1:1 mentoring from investment and technology experts and a ticket to the QAI Ventures speed dating session to join upcoming venture building or accelerator programs (top 3 teams).

Do not miss this opportunity to engage in quantum innovation at the frontier of life sciences.

📅 Visit the [Agenda page](./../agenda.md) to view the full timeline.


## Submitted Projects

The top-ranked projects will be highlighted here:

| Rank | Project #                                            | Team Name | Project Name |
| ---  | ---------------------------------------------------- | --------- | ------------ |
| 1st  | []()                                                 |           |              |
| 2nd  | []()                                                 |           |              |
| 3rd  | []()                                                 |           |              |
| 4th  | []()                                                 |           |              |
| 5th  | []()                                                 |           |              |

For a full list of the submitted challenge projects, we encourage you to take a look at the [Challenge page](_/../projects.md).


## Partners

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
        <img src="./assets//MQS_Logo_Text_black.png" alt="Molecular Quantum Solutions (MQS)" style="width:175px; margin-right:70px">
    </a>
    <a href="https://dcai.dk/">
        <img src="./assets/DCAI_Logo_horizontal_Black_RGB.png" alt="Danish Centre for AI Innovation" style="width:175px;">
    </a>
</div>
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
<br>
<div style="display: flex; align-items: left; justify-content: center;">
    <a href="https://icdk.dk/">
        <img src="https://images.squarespace-cdn.com/content/v1/62d5863a24e5b67bc23dff1f/1661420026081-N55ZWI4RWDCUTJC9J5TE/WeChat-Image_20220221111631.png" alt="Innovation Centre Denmark" style="width:150px; margin-right:70px;">
    </a>
    <a href="https://fhnw.ch">
        <img src="https://www.fhnw.ch/logo/fhnw-logo-en.svg" alt="Fachhochschule Nordwestschweiz" style="width:150px;">
    </a>
</div>
<br>
<div style="display: flex; align-items: center; justify-content: center;">
    <a href="https://eqtc2025.ku.dk/">
        <img src="./assets/EQTC-2025.png" alt="European Quantum Technologies Conference 2025" style="width:300px;">
    </a>
</div>
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


## Financial Sponsors

- [Novo Nordisk Foundation](https://novonordiskfonden.dk/)
- [Danish Business Authority](https://danishbusinessauthority.dk/)
- [Danish Centre for AI Innovation - Gefion](https://dcai.dk/)

[faq]: {{ site.baseurl }}{% link faq.md %}
