---
title: Frequently Asked Questions
menu_title: FAQ
menu_icon: question-circle
---

### 1. What is quantum computing, and why is it important for the physical sciences?

Quantum computers allow to design algorithms within an extended state space (via qubits, qutrits, qudits for example) which classical compute hardware technologies are not able to provide with bit-based calcuation procedures when scaling the problem size.

The individual qubits/qutrits/qudits are in a superposition state and entanglement between them are defined based on the specific algorithm where the challenge is how to implement the quantum compute algorithm with respect to the mathematical problem one wants to tackle.

Important to acknowledge is that the results the quantum compute algorithm are read out from a quantum computer by destroying the superposition states. This implicates that the results are stochastic by nature and the algorithm has to be run many times on the quantum hardware to receive a probability distribution of the solution and hopefully with a clear answer what the solution is.


### 2. Am I eligible to participate in the hackathon?

Yes! The hackathon is open to everyone, regardless of background or experience. We encourage participants from all career stages, including students, researchers, and professionals, to join us. For code-based projects, we recommend at least beginner Python programming experience[<sup>(?)</sup>][faq]{:title="Do I need to use Python, or can I use other languages?"} and basic familiarity with git and GitHub. Prior to the hackathon, we also recommend that participants study the basic concepts behind Bayesian optimization. For those looking to learn or refresh their knowledge on these topics, please study the items provided in the [resources page](_/../resources.md).


### 3. Are there specific packages I should use?

This is a BYOP ("bring-your-own-package") event. We have some recommendations for newcomers, but we hope to see a diverse set of solutions applied to the benchmark tasks. Likewise, multiple teams using the same package is not a problem, since solutions can remain private during the course of the challenge until submission.


### 4. Do I need to use Python, or can I use other languages?

We recommend using Python, as it is the most common language for scientific computing and has a wide range of libraries with respect to quantum computing. However, you are welcome to use other languages if you prefer.


### 5. Does it have to be quantum computing or quantum-inspired computing, or are other algorithms allowed?

Yes, there needs to be some sub-algorithm or connected algorithm which makes use of a quantum computing based method or quantum-inspired method to enhance a model or calculation pipeline.


### 6. Do I need to have a team to participate?

Yes, it is a condition to form a team of a minimum of three members with one member having an academic affiliation.
This will allow you to share ideas and learn from others! It is up to you to identify and form a team, and you can do so at any time leading up to the phase 1 challenge submission.


### 7. Can I participate in multiple projects?

Yes, you may participate in multiple projects. For example, one may wish to apply a particular algorithm to a benchmark *and* create a concept-focused instructional tutorial to accompany it. Each of these would be considered a separate project with its own template. However, we encourage participants to be realistic about the limited time available during the challenge as well as communicate this to other team members if participating in multiple projects.


### 8. Does my GitHub repository need to be public?

During the course of the hackathon, your repository can remain private. However, to be considered for phase 2 and the final winners evaluation, your repository must be made public together with a pull request to the Quantum-Challenge-2025 repository.
This ensures that the work is accessible to the community and can be reviewed by the judges[<sup>(?)</sup>][faq]{:title="What is expected from me if I act as a judge?"} during the [judging and showcase section](_/../agenda.md). You are also welcome to make your repository public at any time leading up to or during the challenge.


### 9. How do I prepare for the project showcase?

You will receive further information when your team has been selected as one of the winner teams to present at the selected conference.


### 10. How many members can one participating group consist of?

At least 3 members have to form a team where at least 1 member has an academic affiliation. There is no upper limit to the team size but 3 team members have to selected as the official members of the projects which will be submitted.


### 11. Would it be possible that two start-up entities form one group?

There is no restriction with respect how many entities can collaborate. The only condition is that one of the three official members has an academic affiliation.


### 12. How many entities could possibly collaborate to participate in the challenge (e.g. 3 start-ups + academic research group; 2 start-ups + two academic research groups?)

Same answer as for question 2: There is no upper limit, only the condition that one official member has an academic affiliation.


### 13. To what degree is it allowed to mix commercial tools with a dedicated developed code base submitted to this challenge?

Commercial software tools can not be developed further during this challenge and submissions showcasing new capabilities of the commercial tool will be deemed not acceptable for this challenge.
Commercial software tools can be applied to generate data sets. These data sets have to be shared and made accessible in the project repository being submitted.


### 14. Is it allowed to apply our own commercial product in combination with an additional code base being submitted to this challenge?

The commercial tool should be seen as a data generator and all data generated with the commercial tool has to be shared in the repository when submitting a project.
The algorithm and/or method should also be well documented in form of a pre-review, reviewed paper or public accessible documentation.
Project submissions which solely rely on the commercial tool and no additional methods, algorithms or model has been developed during the challenge, will most likely get worse ratings than a project submission with extensive documented code which has been made accessible in the project repository.


### 15. In which format and form should the code base be submitted and which format should the report have? (Word doc, latex, markdown?)

There is no restriction to which programming language or text format files should be used. Important is that the code is well documented and executable.


### 16. Should we also present our contribution with a video? Would a video enhance our chances to get to the second round?

Video contributions are welcome but enhancing the chances to get accepted to the second round will be evaluated case by case. A video contribution will be helpful when it showcases well the scientific content of the submitted project.

 
### 17. We usually submit to hackathons/challenges a report, a video, a slide deck and a code repository. What is expected in this challenge?

The minimum requirement is a well documented code repository where the code is executable and the results presented in a report can be easily replicated.

 
### 18. Would publishing our report via arxiv give extra points?

No, publishing the report on the arxiv will not give extra points. It is recommended to deliver a well structured report in the repository in form of a pdf file.
 

### 19. We assume that the submitted code base would be released under the MIT license or are other licenses also allowed?

The Quantum Challenge enforces submissions under Creative Commons Attribution 4.0 International License, and the code itself under Apache License 2.0 and the submitting team agrees to license the Submission under the Creative Commons Attribution 4.0 International License, and all provided code under the Apache License, Version 2.0 or MIT license.

 

### 20. If we already have the infrastructure to make use of QPUs and GPUs (large cluster), how should we communicate the justification to further develop our submitted solution with Gefion? Could we also be selected as one of the pitch participants in the end if we do not need Gefion and show results with another HPC provider?

Yes. If you have your own GPU infrastructure with then you can indicate that you would like to participate in the final evaluation and do not need access to Gefion. Although we advice to carefully assess if you have a GPU infrastructure setup with the same capabilities as Gefion has.

[faq]: {{ site.baseurl }}{% link faq.md %}
