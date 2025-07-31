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
    <h2><i class="bi bi-calendar3"></i> Timeline</h2>
    <dl>
        {% if registration_status == "soon" or registration_status == "open" or registration_status == "demo" %}
            <dt>{{ site.registration_opens_date }}</dt>
            <dd>
                Applications open for participants<br>
                {% if registration_status == 'open' %}
                    <button class="btn" onclick="openRegistrationModal()">Register your team</button>
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
- After the announcement of the finalists at EQTC in November, the 5 finalists gain access to the GEFION Supercomputer to continue the development of their models. Submission deadline for the second phase is expected to be end of January 2026 with announcement of the final winner in Q1 2026.
- The winning solution will be announced in Spring 2026 during another leading European quantum event and a prize is offered for the final winning team in the form of extended free access to the Gefion AI supercomputer, sponsored by DCAI.
- Networking and access to a global community of experts from the academic and industrial life science community.
- Working on a relevant life science use case with feedback and mentoring from leading industry partners, investors, and experts.
- Direct access and support from Gefion, one of the fastest supercomputers globally, to run your challenge code (5 finalists).
- Global marketing and branding with free tickets to EQTC 2025, presentation opportunities and further fostering of relationships (5 finalists).
- Novo Holdings and QAI Ventures will help to facilitate access to their global investor network.
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

[faq]: {{ site.baseurl }}{% link faq.md %}

<!-- Registration Modal -->
<div id="registrationModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeRegistrationModal()">&times;</span>
    <h2>Register Your Team</h2>
    
    <form id="registrationForm" enctype="multipart/form-data">
      <div class="form-group">
        <label for="team_member_1_name">Team Member 1 Name *</label>
        <input type="text" id="team_member_1_name" name="team_member_1_name" required>
      </div>
      
      <div class="form-group">
        <label for="team_member_1_email">Team Member 1 Email *</label>
        <input type="email" id="team_member_1_email" name="team_member_1_email" required>
      </div>
      
      <div class="form-group">
        <label for="team_member_2_name">Team Member 2 Name *</label>
        <input type="text" id="team_member_2_name" name="team_member_2_name" required>
      </div>
      
      <div class="form-group">
        <label for="team_member_2_email">Team Member 2 Email *</label>
        <input type="email" id="team_member_2_email" name="team_member_2_email" required>
      </div>
      
      <div class="form-group">
        <label>Additional Team Members</label>
        <div id="additional-members-container">
          <!-- Additional members will be added here dynamically -->
        </div>
        <button type="button" class="btn btn-secondary" onclick="addTeamMember()" style="margin-top: 10px;">+ Add Team Member</button>
      </div>
      
      <div class="form-group">
        <label for="additional_notes">Additional Notes</label>
        <textarea id="additional_notes" name="additional_notes" placeholder="Our team is excited to participate in the quantum challenge!"></textarea>
      </div>
      
      <div class="form-group">
        <label for="pdf_document">Hosting Letter (pdf; optional), please send before submission of your project</label>
        <input type="file" id="pdf_document" name="pdf_document" accept=".pdf">
      </div>

      <div class="form-group" style="display: none;">
        <input type="text" id="email_honeypot" name="email_honeypot">
      </div>
      
      <div class="form-actions">
        <button type="submit" class="btn">Submit Registration</button>
        <button type="button" class="btn btn-secondary" onclick="closeRegistrationModal()">Cancel</button>
      </div>
    </form>
  </div>
</div>

<script>
function openRegistrationModal() {
  document.getElementById('registrationModal').style.display = 'block';
}

function closeRegistrationModal() {
  document.getElementById('registrationModal').style.display = 'none';
}

// Close modal when clicking outside of it
window.onclick = function(event) {
  const modal = document.getElementById('registrationModal');
  if (event.target == modal) {
    closeRegistrationModal();
  }
}

// Function to handle file upload and convert to base64
async function handleFileUpload(file) {
  return new Promise((resolve, reject) => {
    const reader = new FileReader();
    reader.onload = () => {
      // Convert to base64 (remove the data:application/pdf;base64, prefix)
      const base64Content = reader.result.split(',')[1];
      resolve({
        name: file.name,
        size: file.size,
        type: file.type,
        content: base64Content
      });
    };
    reader.onerror = reject;
    reader.readAsDataURL(file);
  });
}

document.getElementById('registrationForm').addEventListener('submit', async function(e) {
  e.preventDefault();
  
  try {
    // Prepare JSON payload with exact structure
    const payload = {
      team_member_1_name: document.getElementById('team_member_1_name').value,
      team_member_1_email: document.getElementById('team_member_1_email').value,
      team_member_2_name: document.getElementById('team_member_2_name').value,
      team_member_2_email: document.getElementById('team_member_2_email').value,
      email_honeypot: document.getElementById('email_honeypot').value
    };
    
    // Add optional fields
    const additionalMembers = getAdditionalTeamMembers();
    if (additionalMembers.length > 0) {
      payload.extra_team_members = additionalMembers;
    }
    
    const additionalNotes = document.getElementById('additional_notes').value;
    if (additionalNotes.trim()) {
      payload.additional_notes = additionalNotes;
    }
    
    // Handle file upload if selected
    const pdfFile = document.getElementById('pdf_document').files[0];
    if (pdfFile) {
      payload.pdf_document_base64 = await handleFileUpload(pdfFile);
    }
    
    // Debug: Log the JSON payload
    console.log('=== FORM SUBMISSION DEBUG ===');
    console.log('JSON payload:', payload);
    console.log('=== END DEBUG ===');
    
    // Submit to API with application/json
    const response = await fetch('https://api.contact.mqs.dk/quantumChallengeForm', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify(payload)
    });
    
    if (response.ok) {
      alert('Registration submitted successfully!');
      closeRegistrationModal();
      document.getElementById('registrationForm').reset();
    } else {
      throw new Error('Registration failed');
    }
  } catch (error) {
    console.error('Error:', error);
    alert('Registration failed. Please try again.');
  }
});

function addTeamMember() {
  const container = document.getElementById('additional-members-container');
  const memberCount = container.children.length;
  const memberNumber = memberCount + 3; // Start from 3 since we have 2 required members

  const memberDiv = document.createElement('div');
  memberDiv.className = 'additional-member';
  memberDiv.style.border = '1px solid #ddd';
  memberDiv.style.padding = '15px';
  memberDiv.style.marginBottom = '15px';
  memberDiv.style.borderRadius = '5px';
  memberDiv.style.backgroundColor = '#f9f9f9';
  memberDiv.innerHTML = `
    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px;">
      <h4 style="margin: 0;">Team Member ${memberNumber}</h4>
      <button type="button" class="btn btn-danger" onclick="removeTeamMember(this)" style="padding: 5px 10px; font-size: 12px;">Remove</button>
    </div>
    <div class="form-group" style="margin-bottom: 10px;">
      <label>Name *</label>
      <input type="text" name="team_member_${memberNumber}_name" required>
    </div>
    <div class="form-group" style="margin-bottom: 0;">
      <label>Email *</label>
      <input type="email" name="team_member_${memberNumber}_email" required>
    </div>
  `;
  container.appendChild(memberDiv);
}

function removeTeamMember(button) {
  button.closest('.additional-member').remove();
}

function getAdditionalTeamMembers() {
  const container = document.getElementById('additional-members-container');
  const members = [];
  const memberDivs = container.querySelectorAll('.additional-member');
  
  memberDivs.forEach((memberDiv, index) => {
    const nameInput = memberDiv.querySelector('input[type="text"]');
    const emailInput = memberDiv.querySelector('input[type="email"]');
    
    if (nameInput && emailInput && nameInput.value.trim() && emailInput.value.trim()) {
      members.push({
        name: nameInput.value.trim(),
        email: emailInput.value.trim()
      });
    }
  });
  
  return members;
}
</script>
