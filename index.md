---
layout: home
title: USC CSCI 544 Fall 2024 - Applied NLP
nav_exclude: true
toc: true
seo:
  type: Course
  name: Language Models in NLP
---

# {{ site.tagline }}
{: .no_toc .mb-2 }
<!-- {{ site.description }} -->
🍂 Fall 2024 &nbsp; &nbsp; ⏰  Tue / Thu 4:00 - 5:50p  &nbsp; &nbsp; 📍 [SAL](https://maps.usc.edu/?id=1928&reference=DMC#!m/552467?share) 101
{: .fs-6 .fw-300 }

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign cps = site.staffers | where: 'role', 'Grader' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% assign num_cps = cps | size %}

{% if num_teaching_assistants != 0 %}
{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

{% if num_cps != 0 %}

{% for staffer in cps %}
{{ staffer }}
{% endfor %}
{% endif %}


## Announcements

See [Brightspace](https://brightspace.usc.edu/d2l/lms/news/main.d2l?ou=114109).

<!-- {% assign announcements = site.announcements | reverse %}
{% for announcement in announcements %}
{{ announcement }}
{% endfor %} -->

## Summary

This course covers both fundamental and cutting-edge topics in Natural Language Processing (NLP) with a focus on Language Models. Natural language processing (NLP) has been revolutionized by the advancement of large-scale language models achieving state-of-the-art performance across a wide variety of tasks. This course will cover the fundamentals of language modeling and related topics in natural language processing, deep learning and machine learning. Students will gain familiarity with the capabilities of large language models as well as get hands-on experience with building and evaluating small-scale language models. The class will also explore the real-world consequences of deploying language models, such as the ethics and harms associated with them

## Calendar + Syllabus

<table>
  <thead>
  <tr>
    <th width="5%">Week</th>
    <th width="5%">Date</th>
    <th width="30%">Class Topics</th>
    <th width="40%">Readings</th>
    <th width="13%">Work Due</th>
  </tr>
  </thead>
  <tbody>
  {% for week in site.data.calendar %}
    {% for day in week.days %}
      <tr>
        {% if forloop.index == 1 %}
        <td rowspan="{{week.size}}">{{week.week}}</td>
        {% endif %}
        <td>{{day.date}}</td>
        <!-- <td>{{day.theme}}</td> -->
        <td class="cal-content">
        {% if day.slides %}
          <a href="{{day.slides}}">{{day. theme}}</a>
        {% else %}
          {{day.theme}}
        {% endif %}
        </td>
        <td class="cal-content">
          {% if day.readingslink %}
            <a href="{{day.readingslink}}">{{day.readings}}</a>
          {% else if day.readings %}
            {{day.readings}}
          {% endif %}
          {% if day.additional %}
            {% if day.additionallink %}
              <a href="{{day.additionallink}}"><b>Additional:</b> {{day.additional}}</a>
            {% else %}
              <b>Additional:</b> {{day.additional}}
            {% endif %}
          {% endif %}
        </td>
        <td class="cal-content">{{day.due}}</td>
      </tr>
    {% endfor %}
  {% endfor %}
  </tbody>
</table>


Calendar and [prespecified syllabus](https://web-app.usc.edu/soc/syllabus/20241/29980.pdf) are subject to change. More details, e.g. reading materials and additional [resources](details/resources/) will be added as the semester continues. All work (except the project final report) is due on the specified date by **11:59 PM PT**{: .label .label-red }.


## Assignments and Grading

There will be three components to course grades:

* **[Homeworks](./#homeworks-40) (40%).**
  * 10% X 4: Turn in Homeworks.
* **[Class Participation](./#quizzes-15--class-participation-5-20-total) (20%).**
  * 5%: Engage in Q/A during lectures.
  * 15%: Turn in quiz sheets.
* **[Class Project in groups of 2-3 students](./#class-project-40-total) (40%).**
  * 5%: [Pitch](./#project-pitches-5) your proposals.
  * 5%: Turn in a [project proposal](./#project-proposal-5).
  * 10%: Turn in a [progress report](./#project-progress-report-10).
  * 10%: [Present](./#project-final-presentation-10) your main findings.
  * 10%: Turn in a [final report](./#project-final-report-10).


## Homeworks (40%)


<!-- Students will be expected to present two research papers by leading class discussion on these papers.
Each paper presentation is responsible for 10% of the total grade.
The papers themselves will be selected by the instructor, but students can sign up their names 1-2 different papers; after the first two weeks the instructor will assign you to a paper which you might be presenting with another student.
The presentation format should ideally involve slide decks designed to help everyone in the class understand the papers --- think of yourself as the author of the paper presenting it at a conference venue.
The purpose of this presentation is not only to discuss the findings of the paper, but to connect the paper with other papers and lectures visited before.
The presenter is also encouraged to prepare 2-3 discussion questions to encourage discussion __after__ the presentation. -->

### Important Note about Academic Policy

For many of the assigned readings, the authors' own slides and even video are publicly available.
There are also tools like ChatGPT which are publicly available.
While students may watch these videos and explore the capabilities of public language models, **they must write their own homeworks and quizzes, and draw their own conclusions**, as this discussion is intended to be the students' own work.
<!-- If you *must* borrow a slide or two from elsewhere, attribute the source on each individual slide. -->
Non-adherence might amount to plagiarism, which amounts to a serious [academic misconduct](../policies/#academic-conduct).
If you find an assignment too difficult to follow, please use the available late days.
In extreme situations, please let the staff know and your case will be considered.


## Quizzes (15%) + Class participation (5%) (20% total)


Students are expected to participate in class discussions by not only asking questions, but also sharing their opinions on the topics under discussion.
Students are also expected to turn in written quiz sheets, which will be distributed in some, but not all of the classes.
Quizzes will be announced 2-3 days beforehand, and will cover 4-5 questions based on lecture materials and class discussions so far to be answered in 10-15 mins during class.
OSAS students can turn in a scanned copy of the filled out quiz sheet to the instructor by 11:59 PM PT on the day of the quiz.


## Class project (40% total)


Students must participate in teams of two or three (at maximum) complete a final research project on a topic related to the class. This project is expected to include work on language models.
<!-- either (1) building analytical tools for investigating large-scale datasets, or (2) replicating tools from prior research to apply on new datasets. Please come to office hours or email me if you have questions related to choosing a project direction. -->

### Project Pitches (5%)

Every student pitches a 3 minute project idea for which all the other students vote. This will help the students choose project teams. The pitch should outline what problem is being solved and why should we care about it. It should make a connection to language models as a path to addressing the problem. It should also provide an idea of the inputs and outputs, ideally with real world examples. It is important to name the project idea for ease of voting.

<!-- ****************************** IMP: Use this for ATRP. ***************************************-->

### Project proposal (5%).

Student teams should submit a ~1-page proposal (see format below*) for their project by Week 5. The proposal should:
  - state and motivate the problem by providing a problem or task definition (ideally with example inputs and expected outputs),
  - situate the problem within related work (this might help you find sources of data for training a model for your task),
  - state a hypothesis to be verified and how to verify it (evaluation framework), and
  - a brief description of the approach to be followed to verify the hypothesis (such as proposed models and baselines).

### Project progress report (10%).
Student teams should submit a ~3-page progress report (see format below*) for their project by the end of Week 8 (March 4). This report should:
- once again describe the project’s goals (it is okay if this has changed since the proposal),
- contain all details on the dataset (your dataset should mostly be collected by now),
- contain some initial results (think of this as a motivating result), and
- must outline a concrete plan of what will be done for the final report.

While the initial results might be inconclusive, you are expected to have made _non-trivial progress_ by this point. The project proposal may be repurposed for this report. Please take into consideration the earlier feedback you received, and address those inline (you may <span style="color:red">highlight these in a different text color</span> if you wish to draw the instructor's attention).

### Project final presentation (10%).
This will be a 30 minute presentation, followed by 5 minutes of Q/A during the last three weeks of class. Points will be deducted if 30+5 min time limit is exceeded, so please practice with timing your talk. Each student in the team must present an equal share of the work. Each project presentation should describe
- the research questions to be answered and the underlying motivation,
- the proposed methods, and
- their findings _so far_, as well as
- address audience questions.

You will be awarded points for asking questions / participating in a discussion during the talks given by other teams. Your talk must use slides.

### Project final report (10%).
Student teams should submit a ~6-8 page final report (see format below*) detailing all aspects of their project. The report should be structured like a conference paper, including an abstract, introduction, related work, and experiments; a tech report format is discouraged. Parts of the proposal and progress report may be reused for the final report. Negative results will not be penalized, but should be accompanied with detailed analysis of why the proposed method did not work as anticipated. You may include an appendix at the very end. References and the appendix di not count towards the main report page limit (i.e. can exceed 8 pages).
<!-- Negative results are okay, but they need to engage with that - not stop right there. -->

*All written assignments related to the final project should use the standard [*ACL paper submission template](https://github.com/acl-org/acl-style-files).


## Late Days

Students are allowed a maximum of 6 late days **total** for all assignments (but NOT the quiz sheets). You may use up to 3 late days per assignment. Using one late day for a project assignment involves each of the teammates using a late day each. Partial late days are not permitted. For every extra late day beyond the allowed late days, the student / team will lose 20% of the grade for the assignment.

**Note:** Please familiarize yourself with the [academic policies](details/policies/#policies) and read the [note about student well-being](details/policies/#student-well-being).


<!--
## Pre-Requisites

Students are required to have taken [CSCI-270 Introduction to Algorithms and Theory of Computing]() (4.0 units) as well as one of ([CSCI-360 Introduction to AI](), [CSCI-467 Introduction to Machine Learning]() or equivalent experience). Fluency with python programming is recommended. Please email the instructor for special circumstances or specific clarifications. -->


## Previous Iterations

- [Fall 2023](https://swabhs.com/fall23-csci499-lm4nlp/)
  - See [previous class projects here](https://swabhs.com/fall23-csci499-lm4nlp/details/class-projects/).