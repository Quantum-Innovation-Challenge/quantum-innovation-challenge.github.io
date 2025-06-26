---
title: About the Quantum Innovation Challenge
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

{% if event_status != "over" %}
The Quantum Innovation Challenge is a virtual competition and organised by the [Bio Innovation Institute (BII)](https://), [Molecular Quantum Solutions (MQS)](https://mqs.dk), [QAI Ventures](https://).
The competition is open to researchers and industrial participants at all levels who are interested in applying quantum computing and quantum-inspired algorithms to pharmaceutical development.
{% else %}
The Quantum Innovation Challenge was a hosted on {{ site.event_date }}, organised by the [Bio Innovation Institute (BII)](https://), [Molecular Quantum Solutions (MQS)](https://mqs.dk), [QAI Ventures](https://).
The event included researchers and industrial participants at all levels who are interested in applying quantum computing and quantum-inspired algorithms to pharmaceutical development.
{% endif %}

### The organizing team

To contact us about the quantum challenge, please contact us via mail (quantum_challenge@mqs.dk). Molecular Quantum Solutions (MQS) is the technical support of this challenge.

<table class="team-list">
    <tr>
        <td>
            <img alt="Mark Nicholas Jones" src="https://avatars.githubusercontent.com/u/61972059?v=4">
        </td>
        <td>
            <strong>Mark Nicholas Jones</strong>
            <span class="profile-links">
                <a title="Website" href="https://mqs.dk/"><i class="bi bi-globe2"></i></a> 
                <a title="GitHub" href="https://github.com/MQS-mark"><i class="bi bi-github"></i></a>
                <a title="LinkedIn" href="https://www.linkedin.com/in/mark-nicholas-jones-7730b1b4"><i class="bi bi-linkedin"></i></a>
            </span>
            <br>Molecular Quantum Solutions (MQS)
            <br>CEO/CTO
        </td>
    </tr>
       <tr>
        <td>
            <img alt="Nishta Raheesty Nem" src="https://bii.dk/media/pkqfmujr/nishta-raheesty-nem-00089-g.jpg?rxy=0.629281372476021,0.47382116554450443&width=366&height=355&v=1dba9eb1d9e1670&format=webp&quality=85">
        </td>
        <td>
            <strong>Nishta Raheesty Nem</strong>
            <span class="profile-links">
                <a title="Website" href="https://bii.dk"><i class="bi bi-globe2"></i></a> 
                <a title="LinkedIn" href="https://www.linkedin.com/in/raheestynem"><i class="bi bi-linkedin"></i></a>
            </span>
            <br>Bio Innovation Institute (BII)
            <br>Business Developer
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Francesco Russo" src="https://novonordiskfonden.dk//app/uploads/Francesco_Russo_FRU_NNF_TEMP-150x150.jpg">
        </td>
        <td>
            <strong>Francesco Russo</strong>
             <span class="profile-links">
                <a title="Website" href="https://novonordiskfonden.dk/"><i class="bi bi-globe2"></i></a>
                <a title="LinkedIn" href="https://www.linkedin.com/in/russof85"><i class="bi bi-linkedin"></i></a>
            </span>
            <br>Novo Nordisk Foundation
            <br>Scientific Manager
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Cathal Mahon" src="https://bii.dk/media/jdejbvl4/cathal-00648-g.jpg?rxy=0.6401117218224771,0.3826642854564162&width=366&height=355&v=1dba9ead369cf90&format=webp&quality=85">
        </td>
        <td>
            <strong>Cathal Mahon</strong>
            <span class="profile-links">
                <a title="Website" href="https://bii.dk/"><i class="bi bi-globe2"></i></a>
                <a title="LinkedIn" href="https://www.linkedin.com/in/cathalmahon"><i class="bi bi-linkedin"></i></a>
            </span>
            <br>Bio Innovation Institute (BII)
            <br>Chief Business Officer
        </td>
    </tr>
        <tr>
        <td>
            <img alt="Morten Bache" src="https://media.licdn.com/dms/image/v2/C4D03AQEaKrX4l2GVKQ/profile-displayphoto-shrink_200_200/profile-displayphoto-shrink_200_200/0/1535103225764?e=2147483647&v=beta&t=C4hMV2s6Y6P1_eUMOS-DOas00NqQY2F94ZJThQAQcdE">
        </td>
        <td>
            <strong>Morten Bache</strong>
             <span class="profile-links">
                <a title="Website" href="https://novonordiskfonden.dk/"><i class="bi bi-globe2"></i></a>
                <a title="LinkedIn" href="https://www.linkedin.com/in/mortenbache/"><i class="bi bi-linkedin"></i></a>
            </span>
            <br>Novo Nordisk Foundation
            <br>Scientific Director
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Ulrik Nicolai de Lichtenberg" src="https://cdn.sanity.io/images/knlngdbx/production/10ca7a817012ceef49820dac49a0540ccaf3da2a-6338x4225.jpg?w=1920&q=75&fit=clip&auto=format">
        </td>
        <td>
            <strong>Ulrik Nicolai de Lichtenberg</strong>
             <span class="profile-links">
                <a title="Website" href="https://dcai.dk"><i class="bi bi-globe2"></i></a>
                <a title="LinkedIn" href="https://www.linkedin.com/in/ulrik-nicolai-de-lichtenberg"><i class="bi bi-linkedin"></i></a>
            </span>
            <br>Danish Centre for AI Innovation (DCAI)
            <br>Director, Scientific Projects @ Gefion
        </td>
    </tr>
    <!--
    <tr>
        <td>
            <img alt="KJ Schmidt" src="../assets/kj.jpeg">
        </td>
        <td>
            <strong>KJ Schmidt</strong>
            <span class="profile-links">
                <a title="Website" href="http://kjschmidt.us/"><i class="bi bi-globe2"></i></a>
                <a title="GitHub" href="https://github.com/kjschmidt913"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/kj_schmidt"><i class="bi bi-twitter"></i></a>
            </span>
            <br>University of Chicago/Argonne National Lab
            <br>Research Scientist
        </td>
    </tr>
        <tr>
        <td>
            <img alt="Ari Scourtas" src="../assets/ari.JPG">
        </td>
        <td>
            <strong>Aristana Scourtas</strong>
            <span class="profile-links">
                <a title="GitHub" href="https://github.com/ascourtas"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/aristana_s"><i class="bi bi-twitter"></i></a>
            </span>
            <br>University of Chicago/Argonne National Lab
            <br>Research Scientist
        </td>
    </tr> -->
</table>

### Acknowledgements

We thank Sterling G. Baird, and the rest of the organizing team for the [Bayesian Optimization Hackathon for Chemistry and Materials](https://github.com/AC-BO-Hackathon/ac-bo-hackathon.github.io) which has built on top of the [LLMs in Materials and Chemistry '23 Hackathon](https://materials-data-facility.github.io/llm-hackathon/).
