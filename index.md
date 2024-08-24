---
layout: home
title: Language Models in NLP
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


Coming Soon.

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


## Assignments

There will be three components to course grades, see more [details](details/assignments/).

* **[Homeworks](details/assignments/#homeworks-40) (40%).**
* **[Quizzes + Class Participation](details/assignments/#quizzes-15--class-participation-5-20-total) (20%).**
* **[Class Project](details/assignments/#class-project-40-total) (40%).**

Students are allowed a maximum of 6 [late days](details/assignments/#late-days) **total** for all assignments (_NO LATE DAYS ALLOWED FOR_ quizzes), with a maximum of 3 late days per deliverable.


**Note:** Please familiarize yourself with the [academic policies](details/policies/#policies) and read the [note about student well-being](details/policies/#student-well-being).


<!-- 
## Pre-Requisites

Students are required to have taken [CSCI-270 Introduction to Algorithms and Theory of Computing]() (4.0 units) as well as one of ([CSCI-360 Introduction to AI](), [CSCI-467 Introduction to Machine Learning]() or equivalent experience). Fluency with python programming is recommended. Please email the instructor for special circumstances or specific clarifications. -->


## Previous Iterations

- [Fall 2023](https://swabhs.com/fall23-csci499-lm4nlp/)
  - See [previous class projects here](https://swabhs.com/fall23-csci499-lm4nlp/details/class-projects/).