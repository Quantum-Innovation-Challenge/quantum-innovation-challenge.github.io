---
title: Timeline
subtitle: The anticipated schedule is as follows, with all times listed in Central European Time (CET).
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

{% include subpage_header.html %}

<section class="px-5 max-w-screen-lg mx-auto text-white py-10 gap-4 flex flex-col  ">
<article class="prose prose-invert max-w-none w-full flex-1 block break-words mb-8">
<h2 >Schedule</h2>
{% if event_status != "over" %}
<p>The anticipated schedule is as follows, with all times listed in Central European Time (CET).</p>    
{% else %}
<p>The schedule for the event was as follows, with all times listed in Central European Time (CET):</p>
{% endif %}

<p>The Quantum Innovation Challenge consists of multiple phases designed to guide you from team formation to final presentation and beyond.</p>
</article>  

  <!-- Challenge Timeline -->
  <div class="w-full">
    <div class="border border-electron/25 rounded-3xl overflow-hidden">
      <div class="relative">
        <!-- Timeline line -->
        <div class="absolute left-7 top-0 bottom-0 w-px bg-electron/25"></div>
        
        <!-- Phase I -->
        <div class="flex items-start p-6 border-b border-electron/25">
          <div class="flex-shrink-0 w-2 h-2 bg-electron rounded-full z-10 relative"></div>
          <div class="ml-6 flex-1">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-2">
              <h4 class="text-lg font-bold text-white">Phase I</h4>
              <span class="text-xs text-electron bg-electron/10 px-2 py-1 rounded self-start">July - Sept 30</span>
            </div>
            <h5 class=" font-medium text-electron mt-1">Team Formation & Proposal</h5>
            <div class="text-white  mt-2 space-y-2">
              <p>During the first weeks, we will compile an extensive FAQ summary with all your questions and fix outstanding issues for team setup.</p>
              <p>Submit your project via pull request to the <a class=" hover:text-blue-300 underline plausible-event-name=LSQI+Repo+Click" href="https://github.com/Quantum-Innovation-Challenge/LSQI-Challenge-2025">LSQI-Challenge-2025 repository</a>.</p>
              <div class="bg-electron/10 border border-electron/25 rounded-3xl p-3 mt-3">
                <p class="text-electron font-medium ">Deadline: September 30, 10am CET</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Phase II -->
        <div class="flex items-start p-6 border-b border-electron/25">
          <div class="flex-shrink-0 w-2 h-2 bg-electron rounded-full z-10 relative"></div>
          <div class="ml-6 flex-1">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-2">
              <h4 class="text-lg font-bold text-white">Phase II</h4>
              <span class="text-xs text-electron bg-electron/10 px-2 py-1 rounded self-start">Oct 15 - Nov 12</span>
            </div>
            <h5 class=" font-medium  text-electron mt-1">Evaluation & Presentation</h5>
            <div class="text-white  mt-2 space-y-2">
              <p>Evaluation period (October 1-14) and feedback notification on submitted projects (latest October 14).</p>
              <p><strong>Top 5 teams</strong> receive access to the Danish supercomputer Gefion throughout Q4 2025.</p>
              <p>Present at the European Quantum Technologies Conference 2025 in Copenhagen (November 10-12) to connect with the European quantum computing community.</p>
            </div>
          </div>
        </div>

        <!-- Phase III -->
        <div class="flex items-start p-6 border-b border-electron/25">
          <div class="flex-shrink-0 w-2 h-2 bg-electron rounded-full z-10 relative"></div>
          <div class="ml-6 flex-1">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-2">
              <h4 class="text-lg font-bold text-white">Phase III</h4>
              <span class="text-xs text-electron bg-electron/10 px-2 py-1 rounded self-start">Q4 2025 - Q1 2026</span>
            </div>
            <h5 class=" font-medium text-electron mt-1">Development & Finalization</h5>
            <div class="text-white  mt-2 space-y-2">
              <p>Final code repositories and reports expected to be pushed to the respective repository until <strong>January 31, 2026</strong>.</p>
              <p>Presentations and winner announcement will be held at a leading quantum computing conference in spring 2026.</p>
            </div>
          </div>
        </div>

        <!-- After Challenge -->
        <div class="flex items-start p-6">
          <div class="flex-shrink-0 w-2 h-2 bg-electron rounded-full z-10 relative"></div>
          <div class="ml-6 flex-1">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-2">
              <h4 class="text-lg font-bold text-white">After the challenge</h4>
              <span class="text-xs text-electron bg-electron/10 px-2 py-1 rounded self-start">Ongoing</span>
            </div>
            <h5 class=" font-medium text-electron mt-1">Open Source Resource</h5>
            <div class="text-white  mt-2 space-y-2">
              <p>The <a class="text-electron hover:text-purple-300 underline plausible-event-name=LSQI+Repo+Click" href="https://github.com/Quantum-Innovation-Challenge/LSQI-Challenge-2025">LSQI-Challenge-2025 repository</a> serves as documentation for all projects, becoming a valuable resource for academia and industry.</p>
              <p>All submitted projects screened to align with open-source and free license conditions (Apache/MIT).</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>

</section>