---
title: Submit a Project
subtitle: Submit your project to the Quantum Challenge 2025
menu_title: Submission
menu_icon: cloud-arrow-up
---



{% include subpage_header.html %}
<section class="px-5 max-w-screen-lg mx-auto text-white py-10 gap-4 flex flex-col">
        <article class="prose prose-invert max-w-none w-full flex-1 block break-words mb-8">
            
            <h2>Project submission requirements</h2>
            
            <p>The projects must be submitted via a GitHub pull request where your code repository is licensed under the MIT (<a href="http://opensource.org/licenses/MIT">http://opensource.org/licenses/MIT</a>) or Apache Version 2.0 license (<a href="http://apache.org/licenses/LICENSE-2.0">http://apache.org/licenses/LICENSE-2.0</a>). If your submitted repository has no license affiliated with it, then your submission will be regarded as invalid and not taken into evaluation.</p>
            
            <h2>Language</h2>
            <p>Documentation regarding the challenge must be submitted in English.</p>
            
            <h2>Project initialization</h2>
            
            <p>As the three team leaders, to initialize your project<sup><a href="#faq" title="Can I participate in multiple projects?">(?)</a></sup>, please follow these steps:</p>
            
            <ol>
                <li>Use <a href="https://github.com/Quantum-Innovation-Challenge/">this link to open up an issue in the respective challenge repository</a>. For example, if your team name is "Bayes Bandits", the file should be named <code>project-bayes-bandits.md</code>. The team name can be whatever you want it to be as long it aligns with our code of conduct. Further, please also state the project name, your three team members names, GitHub usernames, and your company/institution affiliations.</li>
            </ol>
            
            <p>You do not already have to share a link to the repository you are working on for the challenge but feel free to also share the link with your public challenge repo if you feel comfortable doing it. But we recommend to fork the Quantum-Challenge-2025 repo because you later have to submit your project with a pull request.</p>
            
            <p>By experience we know that it can also be strategic to first share your repository to the public just before submission so that nobody can copy your ideas or build on top of them. But a challenge project like this over several months will probably not win just because you were hiding your development until just before the deadline. Check out the evaluation criteria to read up on how the scientific committee of this challenge will evaluate each project.</p>
            
            <img src="{{ site.baseurl }}/assets/project-submission.png" alt="project submission">
            
            <p>In summary:</p>
            
            <ol>
                <li>Fork the Quantum-Challenge-2025 repo</li>
                <li>Open up a github issue stating your team details and affiliations</li>
                <li>Submit a pull request to Quantum-Challenge-2025 repo with the title "Submit project &lt;team-name: project-name&gt;" and tag your team members in the pull request description using the <code>@</code> symbol followed by their real names and affiliations. It is very important that the scientific evaluation committee can see the affiliations of the team members due to the needed academic affiliation of one team member. Make also sure that you have sent us via email the confirmation of the academic background of that team member in form of a letter from your institution.</li>
                <li>Once the pull request is merged, your project will appear on <a href="_/../projects.md">the projects page</a> of this portal and will also be moved into the projects folder together with all other projects in the Quantum-Challenge-2025 repo.</li>
            </ol>
            
            <pre><code class="language-yaml">---
number: 1 # leave as-is, maintainers will adjust
title: Project 1 title
topic: &lt;topic-name&gt;
team_leads:
  - Project lead 1 (Institution 1) @gh-username1
  - Project lead 2 (Institution 2) @gh-username2

# Comment these lines by prepending the pound symbol (#) to each line to hide these elements

contributors:

- Contributor 1 (Institution 1) @gh-username3
- Contributor 2 (Institution 2) @gh-username4

# github: &lt;your-github-account&gt;/&lt;your-repo-name&gt;

# youtube_video: &lt;your-video-id&gt;

---

Project 1 description

References:
</code></pre>

            <p>Here is an example of a filled-in project file called <code>foobar.md</code> for the "Quantumpharma Lifesaver" team. Please replace any colons (<code>:</code>) with hyphens (<code>-</code>) in the title, if applicable, and ensure that the filename ends with the Markdown (<code>.md</code>) extension. Also, ensure that you include the first line with <code>---</code> (required for the webpage to build correctly). The references section is optional. Please include links in Markdown format where appropriate.</p>

            <pre><code class="language-yaml">---

number: 1 # leave as-is, maintainers will adjust
title: Quantum Graph Neural Networks for Biopharmaceutical Development
topic: general
team_leads:

- Jane Doe (University of Invention) @jdoe
- John Smith (Institute of Discovery) @john-smith

contributors:

- Larry Lab (University of Invention) @labamation
- David Data (University of Science) @data4everyone
- Rachel Research (Institute of Discovery) @researchlife

# github: &lt;your-github-account&gt;/&lt;your-repo-name&gt;

# youtube_video: &lt;your-video-id&gt;

---

This project will investigate the application of quantum graph neural networks to pharmaceutical drug development involving several sub-algorithms with quantum computing simulators and quantum-inspired methods. A benchmarking study has been established and is presented in this project report.

References:

1.

2.  </code></pre>
    <pre><code class="language-markdown">github: &lt;your-github-account&gt;/&lt;your-repo-name&gt;</code></pre>

                <p>will be replaced with:</p>

                <pre><code class="language-markdown">github: &lt;Quantum-Innovation-Challenge&gt;/&lt;Quantum-Challenge-2025&gt;</code></pre>

                <h2>Project showcase and evaluation</h2>

                <p>You can showcase your project in multiple ways and it is up to you how you would like to communicate your project in form of a video, a pdf report, a poster, or even a prototype software tool on-boarding documentation.</p>

                <p>It is very important that your submitted pull request with the repo content holds all the needed information and links to be able to judge your project fully.</p>

                <h2>End of Quantum Challenge</h2>

                <p>To ensure a dynamic and engaging submission process, we ask that all challenge teams announce their final projects through social media (e.g., BlueSky, LinkedIn, YouTube etc.) and then link to their project folder within the Quantum-Challenge-2025 repo.</p>

                <p>By sharing your work with a broader audience, you'll help to promote groundbreaking research within pharmaceutical development while inspiring others to contribute to the field.</p>

                <p>Here is a guideline for the optional presentation of your project:</p>

                <ol>
                    <li>Optional but recommended: Create a concise video presentation (3 minutes or less) summarizing your team's project, highlighting its application and novelty, and presenting your project outputs.</li>
                    <li>Upload your video to YouTube (unlisted is fine) and post about it on social media (e.g., BlueSky, LinkedIn, etc.)</li>
                    <li>With the pull request, update your project file with the YouTube video ID (e.g., <code>IVaWl2tL06c</code> for <code>https://youtu.be/IVaWl2tL06c</code>) and a sentence with a link to the social media post:</li>
                </ol>

                <pre><code class="language-markdown">github: Quantum-Challenge-2025/&lt;project-name&gt;

    youtube_video: &lt;your-video-id&gt;</code></pre>
    <p>For the social media post, you would add a sentence like <code>Check out our social media post on [LinkedIn](&lt;your link here&gt;)!</code> before the References section.</p>

                <p>This pull request will be considered your final submission for phase 1 of the challenge.</p>

                <h3>Assessment criteria</h3>

                <h4>1. Problem Understanding &amp; Approach (0-5 pts)</h4>

                <ul>
                    <li>Comparison to state of the art: Does the team clearly define the problem and put it into context?</li>
                    <li>Technical Feasibility: Is the approach reasonable given current or near term quantum computational/AI hardware capacities?</li>
                    <li>Innovativeness: Does the solution bring a novel perspective or improvement compared to existing approaches? Has the participant demonstrated (potential) advantage over classical methods (e.g. speedup, accuracy, resource efficiency)?</li>
                    <li>Scalability: Can the approach be extended or scaled up? For larger datasets can this solution adapted for another use case?</li>
                </ul>

                <h4>2. Computational Resource Estimation (0-5 pts)</h4>
                <ul>
                    <li>Hardware Requirements: Did the team estimate the needed computational resources (GPUs, CPUs)?</li>
                </ul>

                <h4>3. Technical Assessment (0-5 pts)</h4>
                <ul>
                    <li>Choice of Algorithms: Are the selected algorithms appropriate for the task?</li>
                    <li>Justification of Methods: Is there a solid reasoning behind using specific architectures or techniques?</li>
                    <li>Benchmark with existing solutions: Are existing solutions considered and benchmarked?</li>
                </ul>

                <h4>4. Structure of the Work Plan (0-5 pts)</h4>
                <ul>
                    <li>Step-by-Step Breakdown: Does the participant outline a clear roadmap how to approach the challenge?</li>
                    <li>Risk Assessment &amp; Mitigation: Are potential failure points identified with alternative solutions?</li>
                </ul>

                <h4>5. Team skills (0-5 pts)</h4>
                <ul>
                    <li>Skillset: Does the team cover the necessary experience in quantum/AI techniques?</li>
                </ul>

                <h4>6. Proof of Concept / Prototype (0-5 pts)</h4>
                <ul>
                    <li>Prototype Implementation: Has the team built a minimal working proof of concept?</li>
                    <li>Initial Results: Are preliminary results provided?</li>
                    <li>Demonstration of Key Concepts: Does the proof of concept validate core ideas effectively?</li>
                </ul>

                <h3>Notification of Results</h3>

                <p>All teams will be notified by email from <a href="mailto:quantum_challenge@mqs.dk">quantum_challenge@mqs.dk</a> once the assessment is complete, confirming whether or not they have been selected.</p>

                <p>Please note: The scientific committee will not provide detailed individual feedback to teams that are not selected among the top five. However, efforts will be made to provide each participating team with a feedback and scoring summary to support transparency and encourage further development of their project.</p>

            </article>
        </section>
