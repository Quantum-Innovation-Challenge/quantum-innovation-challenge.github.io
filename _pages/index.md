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

<section class="py-24 lg:pt-32 pb-24 flex max-w-screen-lg mx-auto text-center items-center justify-center px-5">
  <div class="flex-1 gap-4 flex flex-col">
    <h1 class="font-space-mono text-4xl font-bold">Quantum Innovation Challenge 2025</h1>
    <p class="tracking-[1px] font-space-mono text-xl">The Quantum Innovation Challenge 2025 invites researchers, start-ups, and students from around the world to explore how quantum computing and quantum-inspired algorithms can advance (bio)pharmaceutical innovation – offering selected teams exclusive access to the Gefion AI Supercomputer.</p>
  </div>
</section>

<section class="flex flex-col mx-auto text-center items-center justify-center mb-18 border-electron/25 py-10">
  <p class="text-electron/50 text-sm mb-5 uppercase tracking-[1px] text-lg font-space-mono px-5 ">
    A joint innovation challenge partnership between
  </p>
  
  <!-- Partner Grid -->
  <div class="border-y-1 w-full px-5 border-electron/25">
  <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-6 lg:grid-cols-5 xl:grid-cols-9 gap-8 md:gap-10 lg:gap-12 xl:gap-8 py-8 place-items-center w-full max-w-7xl mx-auto items-center justify-center ">
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/nnf.svg" | relative_url}}" alt="Novo Nordisk Foundation" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/bii.svg" | relative_url}}" alt="BII" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/nh.svg" | relative_url}}" alt="NH" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/mqs.svg" | relative_url}}" alt="MQS" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/dcai.svg" | relative_url}}" alt="DCAI" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/qai.svg" | relative_url}}" alt="QAI" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/dba.svg" | relative_url}}" alt="DBA" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/erhvervsstyrelsen.svg" | relative_url}}" alt="Erhvervsstyrelsen" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/icd.svg" | relative_url}}" alt="ICD" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
  </div>
  </div>
</section>



<section class="border-t-1 border-electron/25 ">
<div class="flex flex-col-reverse lg:flex-row">
<div class="flex-1 py-16 w-full lg:w-auto" id="left-content">
<div class="max-w-screen-lg! mx-auto prose-wrapped prose">

<h2> Accelerating Quantum Applications<br>in the Life Sciences</h2>

<p>The Quantum Innovation Challenge 2025 invites researchers, start-ups, and students from around the world to explore how quantum computing and quantum-inspired algorithms can advance (bio)pharmaceutical innovation – offering selected teams exclusive access to the Gefion AI Supercomputer.</p>

<p>With the emergence of near-term quantum computers and powerful GPU-based methods, there is a growing need to understand their strengths and limitations, reduce barriers to adoption, and apply them to real-world problems in drug development. This virtual challenge is designed to foster collaborative, open research that contributes to this mission.</p>

<h2> Your Role </h2>

<p>Academic/industrial researchers, start-ups and students can propose projects with respect to this year's <a href="https://quantum-innovation-challenge.github.io/projects/">challenge topic</a> applying quantum computing and quantum-inspired algorithms to:</p>

<ul>
<li>existing benchmarks or new benchmarks as further defined by the <a href="https://quantum-innovation-challenge.github.io/projects/">Quantum Challenge 2025 topic</a></li>
<li>creating sub-algorithms based on quantum computing methods</li>
<li>designing quantum-enhanced sampling and optimization techniques</li>
</ul>

<p>Following the challenge, results will be collated and secured under open-source and free license agreements (Apache/MIT) in the dedicated Quantum-Challenge-2025 repository.</p>

<h2> Who can participate? </h2>

<p>The challenge encourages cross-disciplinary and international collaboration. It is open to teams of academic and industrial researchers, start-ups, and students who are interested in using quantum computing and quantum-inspired methods to advance pharmaceutical development.</p>

<p>To be eligible for submission:</p>

<ul>
<li>Each team must include at least one clearly documented academic participant in a main role</li>
<li>Teams should have prior programming experience and basic familiarity with git and GitHub</li>
<li>Full eligibility details are available on the <a href="https://quantum-innovation-challenge.github.io/eligibility/">Eligibility page</a></li>
</ul>

<h2> Support and participation resources: </h2>

<ul>
<li>Participants are welcome to connect and form teams using our dedicated <a href="https://matrix.to/#/#mqs-community-space:mozilla.org">Element Space</a> (see also <a href="https://element.io">https://element.io</a>)</li>
<li>Orientation materials and technical guidance are available on the <a href="https://quantum-innovation-challenge.github.io/resources/">Resources page</a></li>
<li>Pre-registrations and questions can be sent to <a href="mailto:quantum_challenge@mqs.dk">quantum_challenge@mqs.dk</a>. All inquiries will be addressed collectively on the <a href="https://quantum-innovation-challenge.github.io/faq/">FAQ page</a></li>
</ul>

<h2> Why participate? </h2>

<div class="grid grid-cols-2 gap-4">
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/supercomputer.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Access to the Gefion AI supercomputer </p>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/globe.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Join QAI venture and Novo Holdings ecosystem (1:1 mentoring) </p>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/collaborate.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Sparring with life science, quantum computing and AI experts</p>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/exposure.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Exposure at high impact conferences</p>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/open-source.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Community driven open-source and free license efforts</p>
</div>

<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/network.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Supported and extended networking opportunities</p>
</div>
</div>

<ul>
<li>Five teams will be selected to present their work at the <a href="https://eqtc2025.ku.dk/">European Quantum Technologies Conference 2025 (EQTC)</a> in Copenhagen.</li>
<li>After the announcement of the finalists at EQTC in November, the 5 finalists gain access to the GEFION Supercomputer to continue the development of their models. Submission deadline for the second phase is expected to be end of January 2026 with announcement of the final winner in Q1 2026.</li>
<li>The winning solution will be announced in Spring 2026 during another leading European quantum event and a prize is offered for the final winning team in the form of extended free access to the Gefion AI supercomputer, sponsored by DCAI.</li>
<li>Networking and access to a global community of experts from the academic and industrial life science community.</li>
<li>Working on a relevant life science use case with feedback and mentoring from leading industry partners, investors, and experts.</li>
<li>Direct access and support from Gefion, one of the fastest supercomputers globally, to run your challenge code (5 finalists).</li>
<li>Global marketing and branding with free tickets to EQTC 2025, presentation opportunities and further fostering of relationships (5 finalists).</li>
<li>Novo Holdings and QAI Ventures will help to facilitate access to their global investor network.</li>
<li>Onboarding to the global QAI Ventures ecosystem with 1 year of exclusive 1:1 mentoring from investment and technology experts and a ticket to the QAI Ventures speed dating session to join upcoming venture building or accelerator programs (top 3 teams).</li>
</ul>

<p>Do not miss this opportunity to engage in quantum innovation at the frontier of life sciences.</p>

<p>📅 Visit the <a href="https://quantum-innovation-challenge.github.io/agenda/">Timeline page</a> to view the full agenda.</p>

<h2> Submitted Projects </h2>

<p>The top-ranked projects will be highlighted here:</p>

<div class="overflow-x-auto">
  <table class="w-full mx-auto border-collapse border border-electron/25">
    <thead>
      <tr class="bg-electron/5">
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Rank</th>
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Project #</th>
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Team Name</th>
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Project Name</th>
      </tr>
    </thead>
    <tbody>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">1st</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">2nd</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">3rd</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">4th</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">5th</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
    </tbody>
  </table>
</div>

<p>For a full list of the submitted challenge projects, we encourage you to take a look at the <a href="https://quantum-innovation-challenge.github.io/submission/">Submit a Project page</a>.</p>

<h2> Partners </h2>

<div class="grid grid-cols-4 gap-4">
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/partners/nnf.svg" | relative_url }}" alt="Novo Nordisk Foundation" class="svg w-12 h-12 text-electron">
</div>

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
</div>
</div>
</div>
<div class="w-full lg:min-w-[360px] lg:w-[360px] lg:max-w-[360px] py-16 border-l-0 lg:border-l-1 border-b-1  border-electron/25 px-8 w-full lg:w-[320px] lg:min-w-[320px] lg:max-w-[320px]  " id="right-sidebar">
<div class="flex gap-2 items-center">
    <img src="{{ "/assets/icons/timeline-calendar.svg" | relative_url }}" class="svg w-6 h-6 text-white">
    <h2 class="font-bold text-lg"> Timeline</h2>
</div>

<div class="flex gap-6 flex-col">
        {% if registration_status == "soon" or registration_status == "open" or registration_status == "demo" %}

            
            <div class="flex flex-col gap-2">
            <div class="text-electron">{{ site.registration_opens_date }}</div>
                <p class="text-white">Applications open for participants</p>
                {% if registration_status == 'open' %}
                    <button id="registerTeamButton"  class="plausible-event-name=Register+Team w-full lg:text-sm xl:text-base flex items-center text-white border-1 border-electron/25 bg-electron/5 py-3.5 px-5 h-16 cursor-pointer transition-all duration-300 ease-in-out hover:!text-quantum relative overflow-hidden group" onclick="openRegistrationModal()">
      <span class="relative z-10">

          <span>Register your team</span>
      </span>
      <div class="absolute inset-0 bg-electron transform -translate-x-full group-hover:translate-x-0 transition-transform duration-500 ease-in-out"></div>
    </button>

                    <p class="text-sm">Quick setup: Just share your team roster and hosting letter to join the quantum challenge.</p>

                    <p>Don't have have a team? Find team members via Element Space</p>
                                     <a target="_blank" id="findTeamMembersButton" class="plausible-event-name=Find+Team+Members+Click w-full lg:text-sm xl:text-base flex items-center text-white border-1 border-electron/25 bg-electron/5 py-3.5 px-5 h-16 cursor-pointer transition-all duration-300 ease-in-out hover:!text-quantum relative overflow-hidden group"  href="https://matrix.to/#/#mqs-community-space:mozilla.org ">
      <span class="relative z-10">

          <span>Find team members</span>
      </span>
      <div class="absolute inset-0 bg-electron transform -translate-x-full group-hover:translate-x-0 transition-transform duration-500 ease-in-out"></div>
    </a>

                {% elsif registration_status == 'closed' %}
                    <a class="btn disabled">Registration has closed</a>
                {% elsif registration_status == 'soon' %}
                    <a class="btn disabled">Registration opens soon</a>
                {% endif %}
            </div>
        {% endif %}


        <div class="flex flex-col gap-2">
        <div class="flex flex-col gap-1">
        <div class="flex gap-2 items-center">
            <img src="{{ "/assets/icons/timeline-item.svg" | relative_url }}" class="svg w-6 h-6 ">
            <h2 class="font-bold text-lg">Phase 1</h2>
        </div>
        <div class="text-electron ">{{ site.registration_closes_date }}</div>
</div>
        <p>Submission of the projects closes on the 30th of September at 10AM Central European Time (CET).</p>
        <p>Evaluation will be conducted from the 1st until the 15th of October.</p>
        </div>
        <div class="flex flex-col gap-2">
        <div class="flex flex-col gap-1">
        <div class="flex gap-2 items-center">
            <img src="{{ "/assets/icons/timeline-item.svg" | relative_url }}" class="svg w-6 h-6 ">
            <h2 class="font-bold text-lg">Phase II</h2>
        </div>
        <div class="text-electron ">{{ site.event_date }}</div>
        </div>
        <ul class="list-disc list-inside space-y-2">
        <li>The top five teams are invited to present at the <a href="https://eqtc2025.ku.dk/">European Quantum Technologies Conference 2025 (EQTC)</a> in Copenhagen (10-12 November).</li>
        <li>Travel costs and accomodation for all teams are sponsored and will be covered.</li>
        <li>Scheduled access to Gefion after EQTC until end of January 2026 (Phase III)</li>
        </ul>
        </div>
        <div class="flex flex-col gap-2">
        <div class="flex flex-col gap-1">
        <div class="flex gap-2 items-center">
            <img src="{{ "/assets/icons/timeline-item.svg" | relative_url }}" class="svg w-6 h-6 ">
            <h2 class="font-bold text-lg">Phase III</h2>
        </div>
        <div class="text-electron ">{{ site.event_date }}</div>
        </div>
        <ul class="list-disc list-inside space-y-2">
        <li>Finalization of the projects until the 31st of January 2026.</li>
        <li>The presentations and the winner announcement will be held at a leading quantum computing conference in spring 2026.</li>
            <li>A prize is offered for the final winning team in the form of extended free access to the Gefion AI supercomputer, sponsored by DCAI.</li>
        </ul>
        </div>
        
        

</div>
</div>
</div>

</section>

{% include registration.html %}
