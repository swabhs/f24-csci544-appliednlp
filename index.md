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
          <a href="{{day.slides}}">{{day.theme}}</a>
        {% else %}
          {{day.theme}}
        {% endif %}
        {% if day.paper %}
          <span style="color:teal">{{day.paper}}</span>
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
        <td class="cal-content">
          {% if day.exam %}
            <span style="color:red">{{day.exam}}</span>
          {% endif %}
          {% if day.project %}
            <span style="color:blue">{{day.project}}; </span>
          {% endif %}
          {% if day.break %}
            <span style="color:green">{{day.break}}</span>
          {% endif %}
          {% if day.quiz %}
            <span style="color:fuchsia">{{day.quiz}}; </span>
          {% endif %}
          {% if day.due %}
              {{day.due}}
          {% endif %}
        </td>
      </tr>
    {% endfor %}
  {% endfor %}
  </tbody>
</table>


Calendar and [prespecified syllabus](https://web-app.usc.edu/soc/syllabus/20243/30249.pdf) are subject to change. More details, e.g. reading materials and additional resources will be added as the semester continues. All work (except the project final report) is due on the specified date by **11:59 PM PT**{: .label .label-red }.


## Assignments and Grading

There will be three components to course grades:

* **Homeworks (20%).**
  * 5% X 4: There will be four coding homework assignments based on the topics of the class.
* **Quizzes (10%).**
  * 2% X 5: Multiple-Choice Questions and Short Answers. Missed quizzes will receive a zero grade, and there will be no make-up quizzes.
* **Class Projects (40%).**
  * Each student will do a group class project based on the topics covered in the class.  Students will propose their own project, do the research and build a proof-of-concept, create a video demonstration of the proof-of-concept, and present the project in their report.
  * Proposal: 4%
  * Status Reports: 8%
  * Project Presentation: 10%
  * Final Write-up: 18%
* **Paper Presentations (5%).**
  * The project teams will present a scientific publication related to their project to the class.
  * All members of the team are expected to identify the central points of the research, and present that research to the class, as well as answer questions from the instructor, TAs and fellow students.
  * One member of team---randomly picked by the instructors a couple of hours before the presentation---will be the presenter, so please prepare accordingly!
  * The presenter is responsible for the entire team’s grade, so please ensure both you and your teammates are prepared!
  * The total time of each team's presentation is 5 minutes (3 min presentation + 2 min QA) - we will be very strict about this.
  * If you are NOT presenting, you could participate in Q/A - bonus points will be awarded to folks who ask insightful questions (announce your name before you ask a question).
  * Each team will prepare 3 slides (via Google slides) to be shared with their assigned TAs by 11:59 PM the day before the presentation. Failure to share will cause a loss of grade.
  * Content of the slides:
    * Slide 1: Main Research Question in the paper,
    * Slide 2: Main Results Summarized,
    * Slide 3: How this influences your project.
* **Exams (25%)**
  * Midterm (10%): The midterm exam will contain a mixture of multiple choice and long form questions, covering about the first half of the material covered in the class.
  * Final (15%): The final exam at the end of the semester covering all of the material covered in the class will contain a mixture of multiple choice and long form questions.

Grading inquiries and questions about the grading of the homeworks and the quizzes can be asked (to the TAs) within two weeks from the grading date (the date the grades are released). Grades will be available within 2-2.5 weeks after submission.

All written assignments related to the final project should use the standard [*ACL paper submission template](https://github.com/acl-org/acl-style-files).


## Late Days

Students are allowed a maximum of 6 late days total for all assignments (but NOT the quiz sheets). You may use up to 3 late days per assignment. Using one late day for a project assignment involves each of the teammates using a late day each. Partial late days are not permitted. For every extra late day beyond the allowed late days, the student / team will lose 20% of the grade for the assignment.

**Note:** Please familiarize yourself with the [academic policies](details/policies/#policies) and read the [note about student well-being](details/policies/#student-well-being).


<!--
## Pre-Requisites

Students are required to have taken [CSCI-270 Introduction to Algorithms and Theory of Computing]() (4.0 units) as well as one of ([CSCI-360 Introduction to AI](), [CSCI-467 Introduction to Machine Learning]() or equivalent experience). Fluency with python programming is recommended. Please email the instructor for special circumstances or specific clarifications. -->


## Similar Classes

- Undergraduate-level Special Topics: Language Models in NLP [Spring 2024](https://swabhs.com/sp24-csci499-lm4nlp/)
  <!-- - See [previous class projects here](https://swabhs.com/fall23-csci499-lm4nlp/details/class-projects/). -->
- Undergraduate-level Special Topics: Language Models in NLP [Fall 2023](https://swabhs.com/fall23-csci499-lm4nlp/)
  <!-- - See [previous class projects here](https://swabhs.com/fall23-csci499-lm4nlp/details/class-projects/). -->
