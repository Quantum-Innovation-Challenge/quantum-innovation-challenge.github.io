---
layout: page
title: Home
menu_title: Home
menu_icon: house-door
permalink: /
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
<!-- 
<div style="display: flex; align-items: left; justify-content: left;">
    <img src="./assets/Cover_Image.png" alt="Cover Image" style="widt:300px;">
</div> -->



<section class="h-[500px] flex max-w-screen-lg mx-auto text-center items-center justify-center">
  <div class="flex-1 gap-4 flex flex-col">
    <h1 class="font-space-mono text-4xl font-bold">Quantum Innovation Challenge 2025</h1>
    <p class="tracking-[1px] font-space-mono text-lg">The Quantum Innovation Challenge 2025 invites researchers, start-ups, and students from around the world to explore how quantum computing and quantum-inspired algorithms can advance (bio)pharmaceutical innovation – offering selected teams exclusive access to the Gefion AI Supercomputer.</p>
  </div>
</section>

<section class="flex flex-col mx-auto text-center items-center justify-center mb-18 border-electron/25 border-y-1 py-10">
      <p class="text-electron/100  mb-5 tracking-[1px] text-lg font-space-mono">
        A joint innovation challenge partnership between
      </p>
      <div class=" max-w-screen-xl flex gap-10 justify-center items-center  text-white p-6">
        <img src="{{ site.asset_url }}/assets/partners/nnf.svg" alt="logo" class="svg h-full w-22 "
          >
        <img src="{{ site.asset_url }}/assets/partners/bii.svg" alt="logo" class="svg h-full w-32"
          >
        <img src="{{ site.asset_url }}/assets/partners/nh.svg" alt="logo" class="svg h-full w-18"
          >
        <img src="{{ site.asset_url }}/assets/partners/mqs.svg" alt="logo" class="svg h-full w-32"
          >
        <img src="{{ site.asset_url }}/assets/partners/dcai.svg" alt="logo" class="svg h-full w-20"
          >
        <img src="{{ site.asset_url }}/assets/partners/qai.svg" alt="logo" class="svg h-full w-34"
          >
        <img src="{{ site.asset_url }}/assets/partners/dba.svg" alt="logo" class="svg h-full w-34"
          >
        <img src="{{ site.asset_url }}/assets/partners/erhvervsstyrelsen.svg" alt="logo" class="svg h-full w-56"
          >
        <img src="{{ site.asset_url }}/assets/partners/icd.svg" alt="logo" class="svg h-full w-26"
          >

      </div>
    
</section>








<div class="aside">
    <h2><i class="bi bi-calendar3"></i> Timeline</h2>
    <dl>
        {% if registration_status == "soon" or registration_status == "open" or registration_status == "demo" %}
            <dt>{{ site.registration_opens_date }}</dt>
            <dd>
                Applications open for participants<br>
                {% if registration_status == 'open' %}
                    <button class="btn plausible-event-name=Register+Team" onclick="openRegistrationModal()">Register your team</button>
                    <br>
                    It is needed to register your team by sending us the names of your team members and the hosting letter.
                    <br>
                    <a href="https://quantum-innovation-challenge.github.io/projects/" class="btn">Read about the challenge</a>
                    <br>
                    <a href="https://matrix.to/#/#mqs-community-space:mozilla.org " class="btn plausible-event-name=Element+Space+Click">Find team members via Element Space</a>
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
        - Evaluation will be conducted from the 1st until the 15th of October.</dd>
        <br>
        <dt>{{ site.event_date }}</dt>
        <dd><b>Phase II</b>
        <br>
        - The top five teams are invited to present at the <a href="https://eqtc2025.ku.dk/">European Quantum Technologies Conference 2025 (EQTC)</a> in Copenhagen (10-12 November).
        <br>
        - Travel costs and accomodation for all teams are sponsored and will be covered.
        <br>
        - Scheduled access to Gefion after EQTC until end of January 2026 (Phase III).</dd>
        <br>
        <dd><b>13 November 2025 - 31 January 2026</b>
        <br>
        <b>Phase III</b>
        <br>
        - Finalization of the projects until the 31st of January 2026.
        <br>
        - The presentations and the winner announcement will be held at a leading quantum computing conference in spring 2026.
        <br>
        - A prize is offered for the final winning team in the form of extended free access to the Gefion AI supercomputer, sponsored by DCAI.
        </dd>
    </dl>
</div>


## Accelerating Quantum Applications<br>in the Life Sciences

The Quantum Innovation Challenge 2025 invites researchers, start-ups, and students from around the world to explore how quantum computing and quantum-inspired algorithms can advance (bio)pharmaceutical innovation – offering selected teams exclusive access to the Gefion AI Supercomputer.

With the emergence of near-term quantum computers and powerful GPU-based methods, there is a growing need to understand their strengths and limitations, reduce barriers to adoption, and apply them to real-world problems in drug development. This virtual challenge is designed to foster collaborative, open research that contributes to this mission.


## Your Role

Academic/industrial researchers, start-ups and students can propose projects with respect to this year's [challenge topic](https://quantum-innovation-challenge.github.io/projects/) applying quantum computing and quantum-inspired algorithms to:

- existing benchmarks or new benchmarks as further defined by the [Quantum Challenge 2025 topic](https://quantum-innovation-challenge.github.io/projects/)
- creating sub-algorithms based on quantum computing methods
- designing quantum-enhanced sampling and optimization techniques

Following the challenge, results will be collated and secured under open-source and free license agreements (Apache/MIT) in the dedicated Quantum-Challenge-2025 repository.


## Who can participate?

The challenge encourages cross-disciplinary and international collaboration. It is open to teams of academic and industrial researchers, start-ups, and students who are interested in using quantum computing and quantum-inspired methods to advance pharmaceutical development.

To be eligible for submission:

- Each team must include at least one clearly documented academic participant in a main role
- Teams should have prior programming experience and basic familiarity with git and GitHub
- Full eligibility details are available on the [Eligibility page](https://quantum-innovation-challenge.github.io/eligibility/)

Support and participation resources:

- Participants are welcome to connect and form teams using our dedicated [Element Space](https://matrix.to/#/#mqs-community-space:mozilla.org) (see also [https://element.io](https://element.io))
- Orientation materials and technical guidance are available on the [Resources page](https://quantum-innovation-challenge.github.io/resources/)
- Pre-registrations and questions can be sent to <a href="mailto:quantum_challenge@mqs.dk">quantum_challenge@mqs.dk</a>. All inquiries will be addressed collectively on the [FAQ page](https://quantum-innovation-challenge.github.io/faq/)

    
## Why participate?

<div style="display: flex; align-items: left; justify-content: left;">
    <img src="{{ site.asset_url }}/assets/Benefits.png" alt="Cover Image" style="widt:300px;">
</div>

- Five teams will be selected to present their work at the [European Quantum Technologies Conference 2025 (EQTC)](https://eqtc2025.ku.dk/) in Copenhagen.
- After the announcement of the finalists at EQTC in November, the 5 finalists gain access to the GEFION Supercomputer to continue the development of their models. Submission deadline for the second phase is expected to be end of January 2026 with announcement of the final winner in Q1 2026.
- The winning solution will be announced in Spring 2026 during another leading European quantum event and a prize is offered for the final winning team in the form of extended free access to the Gefion AI supercomputer, sponsored by DCAI.
- Networking and access to a global community of experts from the academic and industrial life science community.
- Working on a relevant life science use case with feedback and mentoring from leading industry partners, investors, and experts.
- Direct access and support from Gefion, one of the fastest supercomputers globally, to run your challenge code (5 finalists).
- Global marketing and branding with free tickets to EQTC 2025, presentation opportunities and further fostering of relationships (5 finalists).
- Novo Holdings and QAI Ventures will help to facilitate access to their global investor network.
- Onboarding to the global QAI Ventures ecosystem with 1 year of exclusive 1:1 mentoring from investment and technology experts and a ticket to the QAI Ventures speed dating session to join upcoming venture building or accelerator programs (top 3 teams).

Do not miss this opportunity to engage in quantum innovation at the frontier of life sciences.

📅 Visit the [Timeline page](https://quantum-innovation-challenge.github.io/agenda/) to view the full agenda.


## Submitted Projects

The top-ranked projects will be highlighted here:

| Rank | Project #                                            | Team Name | Project Name |
| ---  | ---------------------------------------------------- | --------- | ------------ |
| 1st  | []()                                                 |           |              |
| 2nd  | []()                                                 |           |              |
| 3rd  | []()                                                 |           |              |
| 4th  | []()                                                 |           |              |
| 5th  | []()                                                 |           |              |

For a full list of the submitted challenge projects, we encourage you to take a look at the [Submit a Project page](https://quantum-innovation-challenge.github.io/submission/).


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
        <img src="{{ site.asset_url }}/assets/MQS_Logo_Text_black.png" alt="Molecular Quantum Solutions (MQS)" style="width:175px; margin-right:70px">
    </a>
    <a href="https://dcai.dk/">
        <img src="{{ site.asset_url }}/assets/DCAI_Logo_horizontal_Black_RGB.png" alt="Danish Centre for AI Innovation" style="width:175px;">
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
     <a href="https://eqtc2025.ku.dk/">
        <img src="{{ site.asset_url }}/assets/EQTC-2025.png" alt="European Quantum Technologies Conference 2025" style="width:300px;">
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

[faq]: {{ site.baseurl }}{% link _pages/faq.md %}

{% include registration.html %}